# Editoryal Politika

## Kaynak hiyerarşisi

Önce birincil kaynak:

- Resmî ürün blogu, dokümantasyon, sürüm notu ve status sayfası
- Projenin resmî GitHub release/advisory sayfası
- CISA KEV, NVD, CVE kaydı ve üretici güvenlik bülteni
- Şirket SEC bildirimi/yatırımcı ilişkileri açıklaması
- Paket kayıtlarının resmî npm/PyPI sayfası

Sonra doğrulayıcı kaynak:

- Reuters, AP ve güvenilir teknik yayınlar
- Güvenlik araştırmacısının özgün teknik raporu
- Bakımı aktif projenin issue/PR tartışması

Sosyal medya, forum ve topluluk gönderileri keşif için kullanılabilir; tek başına önemli bir iddianın kanıtı değildir. Arama sonucu özetini kaynak sayma; sayfayı açıp içeriği kontrol et.

## Tarih ve tekrar

- “Yayınlandı” tarihi ile olayın gerçekleştiği tarihi ayır.
- Saat dilimini mümkünse belirt.
- Önceki gün raporundaki olayı yalnızca yeni bilgi varsa tekrar ele al ve “devam gelişmesi” olarak işaretle.
- Birden fazla sitenin aynı basın bültenini kopyalaması bağımsız doğrulama değildir.

## Güvenlik

Her önemli açıkta mümkün olduğunda şunları kaydet:

- CVE/GHSA kimliği
- Ürün/paket ve etkilenen sürümler
- Düzeltilen sürüm veya azaltma adımı
- CVSS/önem derecesi ve bunu veren kuruluş
- Aktif istismar ya da PoC durumu
- Kullanıcının yığınına olası etkisi

Aktif istismar iddiasını CISA KEV, üretici veya güvenilir araştırmacı olmadan kesinleştirme. Exploit kodunu, saldırı zincirini veya zararlı operasyon adımlarını çoğaltma.

## Açık kaynak ve paketler

Yeni proje keşfinde yıldız sayısına tek başına güvenme. Son commit/release, bakımcı etkinliği, lisans, kurulum yolu, Docker/self-host desteği, issue sağlığı ve gerçek kullanım örneklerini kontrol et. Paket adı benzerliği ve typosquatting riskine dikkat et.

Sürüm notunda yalnızca kullanıcıyı etkileyen değişiklikleri anlat: breaking change, güvenlik düzeltmesi, performans, yeni API veya önemli deprecation.

## Şirketler, kesintiler ve piyasa

- Servis kesintisinde resmî status sayfasını ve olay zamanını kullan.
- Fiyat değişiminde sembol, borsa, para birimi, veri tarihi, kapanış/seans içi ayrımını yaz.
- Hareketi anlamlı değilse sırf sayı vermek için bölüme alma.
- Şirket açıklaması, analist yorumu ve kendi çıkarımını birbirine karıştırma.
- Nedensellik kanıtlanmadıysa “hareket şu gelişmeyle aynı döneme denk geldi” de.
- Bu bölüm yatırım tavsiyesi değildir.

## Günün dört keşfi

Her gün birbirinden farklı dört öğe seç:

- Skill: ajan/modelin belirli işi daha iyi yapmasını sağlayan tekrar kullanılabilir talimat veya yetenek paketi
- Agent: hedefe dönük, araç kullanan otonom/yarı otonom sistem veya açık kaynak agent framework/projesi
- AI tool: son kullanıcının belirli bir işi yapmasını sağlayan ürün
- AI firması: ayrı bir şirket veya doğrulanabilir girişim

Her biri için: ne işe yarar, kimin için, neden bugün seçildi, lisans/fiyat/self-host durumu biliniyorsa ve doğrudan bağlantı. Aynı ürünü iki kategoriye koyma.

## Belirsizlik dili

- Doğrulandı: birincil kaynak açıkça destekliyor.
- Bildirildi: güvenilir ikincil kaynak söylüyor, birincil teyit yok.
- İddia: taraflı veya henüz bağımsız doğrulanmamış açıklama.
- Çıkarım: kaynaklardan yapılan, açıkça etiketlenmiş editoryal değerlendirme.

Sayısal veri ve doğrudan alıntılarda kaynağa özellikle yakın bağlantı ver. Uzun alıntı kullanma; özetle.
