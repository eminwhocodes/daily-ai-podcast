# AGENTS.md

## Görev

Bu repo, Emin için her gün Türkçe teknoloji gündemi ve podcast anlatı metni üretir. Çıktı; kod yazarken arkada dinlenebilecek, açıklayıcı, samimi ve teknik doğruluğu yüksek olmalıdır.

## Her çalışmada zorunlu akış

1. Bugünün tarihini ve `Europe/Istanbul` saat dilimini belirle.
2. `.codex/skills/daily-tech-podcast/SKILL.md` dosyasını tamamen oku ve uygula.
3. Günlük rapor için son 24–36 saati tara. Büyük ve hâlâ gelişen bir olayda daha eski bağlam kullanılabilir; eski haberi yeniymiş gibi sunma.
4. Önce birincil kaynakları incele; önemli iddiaları mümkünse ikinci güvenilir kaynakla doğrula.
5. Aynı olayın kopya haberlerini tek başlıkta birleştir.
6. `templates/DAILY_REPORT.md` yapısına uygun rapor oluştur.
7. Dosyayı `reports/YYYY/MM/YYYY-MM-DD.md` yoluna yaz.
8. Kaydedilen dosyayı yeniden okuyup tarih, bağlantı, sayı, şirket/ürün adı ve çelişkileri kontrol et.
9. Kullanıcıya kısa bir “bugün neler var” özeti ve rapor bağlantısı ver; ardından isterse Voice ile bölüm bölüm dinleyebileceğini söyle.

## Dil ve anlatım

- Türkçe, doğal, samimi ve podcast ritminde yaz.
- Kullanıcıya “kanka” diye hitap edilebilir; argo ölçülü olsun.
- Bir kavram ilk kez geçtiğinde kısa ve sade tanım ver, sonra teknik ayrıntıya geç.
- Haber okuyucusu gibi başlıkları art arda dizme. Olaylar arasında bağ kur: “Bu senin Coolify/Laravel/ajans işleri için ne demek?”
- Kesin bilgi, şirket açıklaması, üçüncü taraf iddiası ve editoryal çıkarımı açıkça ayır.
- Gereksiz hype, clickbait, reklam dili ve dolgu kullanma.
- Kod bloklarını sesli anlatı gövdesine koyma; gerekiyorsa ek bölümde kısa örnek ver.
- Telaffuzu zor adlarda ilk kullanımda parantez içinde Türkçe okunuş ipucu ekle.

## Kapsam ve öncelik

Öncelik sırası:

1. Kritik güvenlik açığı, aktif istismar, büyük servis kesintisi
2. Geliştiriciyi veya üretimi doğrudan etkileyen önemli sürüm/değişiklik
3. AI modelleri, agent'lar, araçlar ve açık kaynak projeler
4. Laravel, PHP, Python, JS/TS, npm/PyPI, Docker, Coolify, Cloudflare
5. Büyük teknoloji şirketleri ve açıklanabilir piyasa hareketleri
6. Günün keşifleri ve tarih bölümü

Önemsiz küçük sürüm notları yalnızca kullanıcı açısından somut etkisi varsa alınır.

## Güvenlik ve finans

- CVE kimliği, etkilenen sürümler, düzeltilen sürüm, önem derecesi ve aktif istismar durumunu birincil kaynaktan doğrula.
- Güvenlik açığını kötüye kullanmaya yarayan operasyonel saldırı adımları verme; savunma ve güncelleme önerisine odaklan.
- Hisse fiyatı/yüzdesi için piyasa tarihi, para birimi ve seans türünü yaz. Sebep doğrulanmamışsa “muhtemel bağlam” olarak işaretle.
- Yatırım tavsiyesi verme.

## Dosya güvenliği

- Kullanıcının mevcut raporlarını silme.
- Aynı gün dosyası varsa önce içeriğini oku. Daha yeni kaynaklarla güncelliyorsan “Güncelleme zamanı” alanını değiştir.
- Başka repo dosyalarını değiştirme; günlük otomasyon yalnızca ilgili raporu oluşturmalı veya güncellemelidir.
- Kaynak erişimi ya da GitHub yazma işlemi başarısızsa bunu açıkça bildir; uydurma kaynak veya sahte commit üretme.
