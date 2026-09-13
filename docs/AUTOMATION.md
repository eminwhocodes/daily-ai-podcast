# İki Aşamalı Zamanlanmış Görev Tasarımı

## 04.00 — Grokbot taraması

Grokbot her gün Europe/Istanbul 04.00'te [GROKBOT_PROMPT.md](GROKBOT_PROMPT.md) içindeki promptla çalışır. Dünya ve Türkiye gündemini geniş tarar, podcast yazmaz ve sonuçları şu iki dosyaya kaydeder:

- `intake/YYYY/MM/YYYY-MM-DD.json` — pretty-print UTF-8 JSON (asla tek satır minify değil; alan kısaltması yok)
- `intake/YYYY/MM/YYYY-MM-DD.elevenlabs.txt` — ElevenLabs’a yapıştırılacak Türkçe ses metni

Grokbot'un görevi yüksek geri çağırmalı aday keşfidir. Haber atlamamaya çalışır ancak iddiaları “doğrulandı/bildirildi/iddia” seviyesinde işaretler. GitHub'a yazamıyorsa her iki dosyanın içeriğini tam çıktı olarak verir ve başarısızlığı bildirir.

## 05.00 — ChatGPT doğrulaması ve podcast

ChatGPT:

1. Repo kurallarını ve bugünün intake dosyasını okur.
2. Grok adaylarının kaynaklarını yeniden açar.
3. Eksik alanlarda kendi güncel araştırmasını yapar.
4. Yanlış, yinelenen veya önemsiz maddeleri eler.
5. Nihai raporu `reports/YYYY/MM/YYYY-MM-DD.md` yoluna yazar.
6. Sohbette kısa özet, süre ve rapor bağlantısını verir.

ChatGPT zamanlanmış görev promptu:

```text
eminwhocodes/daily-ai-podcast reposundaki AGENTS.md ve .codex/skills/daily-tech-podcast/SKILL.md talimatlarını tamamen oku. Bugünün intake/YYYY/MM/YYYY-MM-DD.json Grokbot taraması varsa onu aday havuzu olarak kullan fakat bütün önemli iddiaları kaynaklarını açarak yeniden doğrula; intake yoksa çalışmayı durdurma ve kendi taramanla devam et. Türkiye teknoloji/startup/TEKNOFEST, Türk savunma sanayii ve dünyadaki kritik askeri-sivil uçak/havacılık gelişmelerini özellikle kontrol et. Europe/Istanbul tarihine göre son 24–36 saatin teknoloji gündemini araştır. Türkçe, doğal podcast anlatımında, gündem yeterliyse 45–60 dakikalık rapor hazırla. Dosyayı reports/YYYY/MM/YYYY-MM-DD.md yolunda oluştur; aynı günün dosyası varsa önce okuyup yalnızca daha doğru veya güncel sürümle güncelle. Başka dosyaları değiştirme. Sonuçta 60 saniyelik özeti, tahmini dinleme süresini ve GitHub rapor bağlantısını ver.
```

## Sesli dinleme

04.00 çıktısının ElevenLabs metni `intake/...elevenlabs.txt` dosyasındadır; Emin bunu TTS’e yapıştırır. Açılış her zaman `{gün} {ay} {haftanın günü}. Günaydın. Günün podcast'ına hoş geldin.` kalıbındadır (ör. `13 Eylül Pazar. Günaydın. Günün podcast'ına hoş geldin.`). Nihai rapor için görev otomatik ses çalmayı garanti etmez; rapor Voice içinde bölüm kimlikleriyle kontrol edilir:

- “B01'den başlayarak podcast gibi anlat.”
- “B09'daki KAAN bölümünü daha teknik tekrar anlat.”
- “B10'daki ikinci uçak gelişmesine geri dön.”
- “Burada dur; sonra B11'den devam et.”

Kalıcı MP3 istenirse ayrı bir TTS hattı gerekir.

## Kurulum gereksinimleri

- Grok API/uygulama erişimi
- GitHub'da yalnızca bu repoya gerekli minimum yazma yetkisi
- `XAI_API_KEY` ve GitHub token'ının secret olarak tutulması
- Harcama/token limiti, timeout ve en fazla bir kontrollü retry
- Aynı tarih dosyasında idempotent çalışma
- API anahtarlarının loga veya repoya yazılmaması

## Hata davranışı

- Grok başarısız olsa da 05.00 ChatGPT kendi araştırmasıyla devam eder.
- Intake bozuksa ChatGPT onu kullanmaz ve raporda belirtir.
- Kaynak URL'siz aday nihai rapora otomatik alınmaz.
- Görev rapor/intake varmış gibi sahte başarı bildirmez.
