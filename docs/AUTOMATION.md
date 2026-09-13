# ChatGPT Zamanlanmış Görev Tasarımı

## Önerilen sürüm: tek aşamalı

Her gün saat 05.00'te (Europe/Istanbul) tek görev çalışır:

1. Repodaki `AGENTS.md`, skill, politika ve şablonu okur.
2. Son 24–36 saati web üzerinden tarar.
3. Günlük raporu üretir.
4. `reports/YYYY/MM/YYYY-MM-DD.md` yoluna GitHub üzerinden kaydeder.
5. Sohbette kısa özet ve rapor bağlantısı verir.

Bu yapı, 04.00 Grok + 05.00 ChatGPT zincirinden daha az kimlik bilgisi, daha az entegrasyon ve daha az hata noktası gerektirir.

## Görev promptu

```text
eminwhocodes/daily-ai-podcast reposundaki AGENTS.md ve .codex/skills/daily-tech-podcast/SKILL.md talimatlarını tamamen oku. İlgili editoryal politika ile günlük şablonu uygula. Europe/Istanbul tarihine göre son 24–36 saatin teknoloji gündemini web'de güncel kaynaklardan araştır; önemli iddiaları birincil kaynaklarla doğrula. Türkçe, doğal podcast anlatımında, gündem yeterliyse 45–60 dakikalık rapor hazırla. Dosyayı reports/YYYY/MM/YYYY-MM-DD.md yolunda oluştur; aynı günün dosyası varsa önce okuyup yalnızca daha doğru/güncel sürümle güncelle. Başka dosyaları değiştirme. Sonuçta bana 60 saniyelik özeti, tahmini dinleme süresini ve GitHub rapor bağlantısını ver.
```

## Sesli dinleme

Zamanlanmış görev raporu ve sohbet özetini hazırlar; istemci tarafında kendiliğinden bir saatlik sesi başlatacağı varsayılmaz. Rapor, ChatGPT Voice içinde okutulmaya uygun bölüm kimlikleri taşır.

Örnek komutlar:

- “B01'den başlayarak podcast gibi anlat.”
- “B04'ü daha sade dille tekrar anlat.”
- “B07'deki ikinci güvenlik haberine geri dön.”
- “Burada dur; sonra B08'den devam edeceğiz.”

Bu yöntem etkileşimli tekrar ve kaldığın yerden devam etmeyi sağlar. Kalıcı MP3 gerekiyorsa ayrıca bir TTS üretim hattı tasarlanmalıdır.

## İki aşamalı Grok seçeneği

Daha sonra istenirse:

- 04.00: Ayrı bir servis/GitHub Actions, Grok API ile ham aday haberleri `intake/YYYY-MM-DD.json` dosyasına yazar.
- 05.00: ChatGPT ham adayları körlemesine kabul etmez; kaynakları tekrar açar, doğrular ve nihai raporu oluşturur.

Gerekli ek parçalar: Grok API anahtarı, GitHub secret, harcama limiti, hata/tekrar politikası, şema doğrulaması ve kaynak URL zorunluluğu. API anahtarı repoya yazılmaz. Bu seçenek ilk sürümün parçası değildir.

## İşletim notları

- Görev başarısızsa rapor varmış gibi bildirim yapılmaz.
- GitHub yazma yetkisi ve web erişimi görev çalışırken mevcut olmalıdır.
- Uzun çıktı sınırına takılırsa rapor dosyası önceliklidir; sohbet mesajı kısa kalabilir.
- Günlük rapor boyu haber yoğunluğuna bağlıdır; dolgu yapılmaz.
