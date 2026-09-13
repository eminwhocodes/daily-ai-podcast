# Daily AI Podcast

Her sabah güncel teknoloji gündemini tarayan, kaynakları doğrulayan ve Türkçe, uzun biçimli bir podcast metni üreten kişisel yayın akışı.

## Amaç

Günün önemli gelişmelerini yalnızca sıralamak değil; ne olduğunu, neden önemli olduğunu, geliştirici ve ürün sahibi açısından etkisini ve takip edilmesi gereken noktaları sohbet eder gibi açıklamak.

Ana konular:

- Yapay zekâ, agent ekosistemi ve geliştirici araçları
- Yazılım, web geliştirme, Laravel, PHP, Python, JavaScript/TypeScript
- Açık kaynak projeler, GitHub sürümleri, Coolify, Docker ve bulut altyapısı
- npm, PyPI ve ilgili paket ekosistemleri
- Siber güvenlik, CVE'ler, aktif istismar ve tedarik zinciri riskleri
- OpenAI/ChatGPT, Cloudflare, Microsoft, GitHub ve diğer büyük teknoloji şirketleri
- Önemli servis kesintileri, güvenlik açıklamaları ve anlamlı piyasa hareketleri
- Her gün: 1 AI skill, 1 agent, 1 AI aracı ve 1 AI şirketi
- Günün anlam ve önemi; özellikle yaklaşan önemli günler

## Günlük çıktı

Raporlar şu yola yazılır:

`reports/YYYY/MM/YYYY-MM-DD.md`

Her rapor hem okunabilir araştırma dosyası hem de sesli anlatı metnidir. Hedef süre 45–60 dakikadır; gündem zayıfsa tekrar veya dolgu yapılmaz.

## Repo yapısı

- [AGENTS.md](AGENTS.md): Bu repoda çalışan ajanların ana kuralları
- [.codex/skills/daily-tech-podcast/SKILL.md](.codex/skills/daily-tech-podcast/SKILL.md): Günlük podcast üretme skill'i
- [docs/AUTOMATION.md](docs/AUTOMATION.md): ChatGPT zamanlanmış görev kurulumu ve sınırlar
- [templates/DAILY_REPORT.md](templates/DAILY_REPORT.md): Günlük rapor şablonu
- [references/EDITORIAL_POLICY.md](references/EDITORIAL_POLICY.md): Kaynak, doğrulama ve editoryal kalite kuralları

## Kullanım

Bir ajan günlük rapor hazırlarken önce `AGENTS.md`, ardından skill ve gerekli referansları okur. Rapor oluşturulduktan sonra aynı tarihli dosya varsa körlemesine üzerine yazılmaz; içerik karşılaştırılır ve yalnızca daha güncel/doğru sürüm kaydedilir.

> Bu repo yatırım tavsiyesi, güvenlik garantisi veya otomatik ses dosyası üretmez. Piyasa bölümü bilgilendirme amaçlıdır; güvenlik iddiaları birincil kaynaklarla doğrulanır.
