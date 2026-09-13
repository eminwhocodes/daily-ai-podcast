# AGENTS.md

## Görev

Bu repo, Emin için her gün Türkçe teknoloji gündemi ve podcast anlatı metni üretir. Çıktı; kod yazarken arkada dinlenebilecek, açıklayıcı, samimi ve teknik doğruluğu yüksek olmalıdır.

## Her çalışmada zorunlu akış

1. Bugünün tarihini ve `Europe/Istanbul` saat dilimini belirle.
2. `.codex/skills/daily-tech-podcast/SKILL.md` dosyasını tamamen oku ve uygula.
3. Varsa `intake/YYYY/MM/YYYY-MM-DD.json` Grokbot taramasını oku. Adayları ipucu olarak kullan; hiçbir iddiayı otomatik doğru kabul etme.
4. Son 24–36 saati ayrıca tara. Büyük ve hâlâ gelişen bir olayda daha eski bağlam kullanılabilir; eski haberi yeniymiş gibi sunma.
5. Türkiye teknoloji, girişim, savunma ve havacılık takip hatlarını ayrı ayrı kontrol et.
6. Önce birincil kaynakları incele; önemli iddiaları mümkünse ikinci güvenilir kaynakla doğrula.
7. Aynı olayın kopya haberlerini tek başlıkta birleştir.
8. `templates/DAILY_REPORT.md` yapısına uygun rapor oluştur.
9. Dosyayı `reports/YYYY/MM/YYYY-MM-DD.md` yoluna yaz.
10. Kaydedilen dosyayı yeniden okuyup tarih, bağlantı, sayı, şirket/ürün adı ve çelişkileri kontrol et.
11. Kullanıcıya kısa bir özet ve rapor bağlantısı ver; Voice ile bölüm bölüm dinlenebileceğini söyle.

## Dil ve anlatım

- Türkçe, doğal, samimi ve podcast ritminde yaz.
- Kullanıcıya “kanka” diye hitap edilebilir; argo ölçülü olsun.
- Bir kavram ilk geçtiğinde kısa ve sade tanım ver, sonra teknik ayrıntıya geç.
- Haberleri dizmek yerine bağ kur: “Bu senin Coolify/Laravel/ajans işleri için ne demek?”
- Kesin bilgi, resmî açıklama, üçüncü taraf iddiası ve editoryal çıkarımı ayır.
- Hype, clickbait, propaganda, reklam dili ve dolgu kullanma.
- Kod bloklarını anlatı gövdesine koyma.
- Telaffuzu zor adlarda ilk kullanımda Türkçe okunuş ipucu ver.

### Sesli anlatım ritmi

- Açılış her zaman: `{gün} {ay} {haftanın günü}. Günaydın. Günün podcast'ına hoş geldin.` (ör. `13 Eylül Pazar. Günaydın. Günün podcast'ına hoş geldin.`)
- Konuşma hızı sakin ve rahat olsun; radyo spikeri gibi acele etme, robotik de olma.
- Ana başlığı önce kısa ve net söyle, ardından ne olduğunu ve neden önemli olduğunu tane tane açıkla.
- Başlıklar arasında doğal bir kısa boşluk/nefes hissi bırak; bunu metin içinde meta cümleyle anlatma.
- “Burada duruyorum”, “nefes alıyorum”, “sonraki başlığa geçiyorum”, “devam edeyim mi?” gibi anlatım sürecini tarif eden cümleler kullanma.
- Kullanıcıdan bölüm bölüm devam onayı isteme. Akış kendi kendine sürsün.
- Her paragrafı aşırı kısa kesme; aynı konuyu 2–4 doğal paragrafta bağlamıyla anlat.
- Haber başlığını okuyup hemen jargon yığma. Önce sade anlamını ver, sonra teknik detaya gir.
- Uzun bölümde ton monotonlaşmasın: önemli noktada vurgu yap, küçük gelişmede kısa kal.

## Kullanıcı tercihleri

- Emin podcastin kapsamı, tonu, ritmi, kaynak önceliği veya bölüm yapısı hakkında kalıcı bir tercih verdiğinde bu repo kurallarını da tercihe göre güncelle.
- Tercihi en uygun yere işle: genel davranış için `AGENTS.md`, Grokbot çıktısı için `docs/GROKBOT_PROMPT.md`, üretim ayrıntısı için `SKILL.md`, rapor yapısı için `templates/DAILY_REPORT.md`.
- Aynı tercihi farklı dosyalarda gereksiz tekrar etme; ancak ajan davranışını güvenceye almak için gereken kısa çapraz kural eklenebilir.

### Intake ve ses çıktısı (kalıcı)

- `intake/**/*.json` dosyaları **asla tek satır / minify edilmez**. Her zaman okunabilir UTF-8 pretty-print (2 boşluk girinti, satır sonları, sonda tek newline) yaz.
- Alanları `…` veya benzeri kısaltmayla kesme; MCP/payload sınırı varsa dosyayı parçalı yaz veya geçici dosyadan commit et — içerik tam kalsın.
- Her intake JSON ile birlikte ElevenLabs’a yapıştırılabilir Türkçe ses metni üret: `intake/YYYY/MM/YYYY-MM-DD.elevenlabs.txt`
- Ses metni: markdown/JSON/URL yığını yok; doğal konuşma; özet + öncelikli adaylar; TTS’e uygun kısa paragraflar.
- Ses ve rapor açılışında ilk üç cümle ZORUNLU ve birebir şu kalıptır: `{gün} {ay} {haftanın günü}. Günaydın. Günün podcast'ına hoş geldin.` Örnek: `13 Eylül Pazar. Günaydın. Günün podcast'ına hoş geldin.` Yıl, saat dilimi veya alternatif selamlama ekleme.


### Multi-bot orkestrasyon (kalıcı)

- 04.00: Daily Podcast uzman DP botlarına fan-out (AI, Yazılım, Açık Kaynak, Altyapı, Siber, Büyük Tech, Piyasa, TR Tech, TR Savunma, Havacılık, Keşif, Tarih, TR Yatırım).
- 04.45: paketleri birleştir → pretty JSON + `elevenlabs.txt` → Fish Audio MP3 (`fish-podcast.bat`) → WA Gönderici / MeteAI ile `905335666101`.
- Uzman botlar yalnızca derin araştırma paketi üretir; repo yazımı ve WA orkestratördedir.

### Fish Audio + WhatsApp

- TTS: `C:\workspace\podcast\fish-audio\fish-podcast.bat` + raw `elevenlabs.txt` URL (KNT-MONSTER17, `FISH_API_KEY`).
- WA hedef: `905335666101` (Evolution `whatsapp.codron.cloud` / `MeteAI`).

## Kapsam ve öncelik

1. Kritik güvenlik açığı, aktif istismar ve büyük servis kesintisi
2. Türkiye'yi etkileyen kritik teknoloji, savunma veya havacılık gelişmesi
3. Dünyadaki büyük askeri/sivil uçak, motor, İHA/SİHA, helikopter, avionik, test ve teslimat gelişmeleri
4. Geliştiriciyi/üretimi doğrudan etkileyen sürüm ve değişiklikler
5. AI modelleri, agent'lar, araçlar ve açık kaynak projeler
6. Laravel/PHP, Python, JS/TS, npm/PyPI, Docker, Coolify ve Cloudflare
7. Türkiye'deki startup, teknopark, TÜBİTAK ve TEKNOFEST gelişmeleri
8. Türkiye yatırımlar ve fırsatlar (`tr_invest`: VC/PE, teşvik/grant, exit/M&A, yabancı yatırımcı hamleleri, açık çağrılar — bilgilendirme, tavsiye değil)
9. Büyük teknoloji şirketleri ve açıklanabilir piyasa hareketleri
10. Günün keşifleri ve tarih bölümü

Savunma ve uçak takibi geniş olmalıdır ancak önemsiz sosyal medya söylentileri podcasti doldurmamalıdır.

## Türkiye, savunma ve havacılık

- SSB, MSB, ASELSAN, TUSAŞ, Baykar, ROKETSAN, HAVELSAN, TEI, STM ve ilgili resmî/kurumsal kaynakları kontrol et.
- KAAN, HÜRJET, HÜRKUŞ, KIZILELMA, ANKA, AKSUNGUR, TB2/TB3, AKINCI, GÖKBEY ve ATAK gibi programları örnek izleme listesi say; listeyle sınırlı kalma.
- Küresel ölçekte yeni uçak programı, ilk uçuş, kritik test, motor/avionik gelişmesi, büyük sipariş/teslimat, kaza, yere indirme, yaptırım veya ihracat kararını yakala.
- Sivil havacılıkta Airbus, Boeing, COMAC, Embraer ve önemli motor üreticilerinin emniyet, sertifikasyon, üretim ve teslimat gelişmelerini izle.
- Yalnızca kamuya açık bilgiyi kullan. Gizli bilgi iddiası, hassas üs/konum, operasyonel zafiyet veya saldırıyı kolaylaştıran teknik ayrıntı verme.
- Resmî açıklamayı bağımsız başarı doğrulaması gibi sunma; test, prototip, seri üretim ve operasyonel hizmet kavramlarını ayır.

## Güvenlik ve finans

- CVE, etkilenen/düzeltilen sürüm, önem ve aktif istismar durumunu birincil kaynaktan doğrula.
- Kötüye kullanıma yarayan saldırı adımları verme; savunmaya odaklan.
- Hisse verisinde tarih, para birimi ve seans türünü yaz. Doğrulanmamış nedeni “muhtemel bağlam” diye işaretle.
- Yatırım tavsiyesi verme.

## Dosya güvenliği

- Mevcut raporları veya intake dosyalarını silme.
- Aynı gün raporu varsa önce oku; güncellemede “Güncelleme zamanı” alanını değiştir.
- Nihai rapor ajanı yalnızca ilgili raporu oluşturmalı/güncellemelidir.
- Kaynak veya GitHub yazma işlemi başarısızsa açıkça bildir; uydurma kaynak ya da sahte commit üretme.
