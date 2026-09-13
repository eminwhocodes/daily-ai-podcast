# Daily AI Podcast

Her sabah güncel teknoloji gündemini tarayan, kaynakları doğrulayan ve Türkçe, uzun biçimli bir podcast metni üreten kişisel yayın akışı.

## Çalışma düzeni

- **04.00 — Fan-out:** 13 uzman DP botuna derin tarama dağıtılır (AI, yazılım, güvenlik, TR tech/savunma/havacılık, **TR yatırım/fırsat**, keşif, tarih…).
- **04.45 — Merge:** Daily Podcast paketleri birleştirir → pretty `intake/...json` + `...elevenlabs.txt` → Fish Audio MP3 → WhatsApp `905335666101`.
- **05.00 — ChatGPT:** Ham adayları yeniden doğrular ve nihai podcast raporunu yazar.
- **Dinleme:** Sabah MP3 WA ile gelir; txt ayrıca ElevenLabs’a da yapıştırılabilir.

## Kapsam

- Yapay zekâ, agent ekosistemi ve geliştirici araçları
- Yazılım, Laravel/PHP, Python, JavaScript/TypeScript, npm ve PyPI
- Açık kaynak, GitHub sürümleri, Coolify, Docker, Cloudflare ve bulut altyapısı
- Siber güvenlik, CVE'ler, aktif istismar ve tedarik zinciri riskleri
- Büyük teknoloji şirketleri, servis kesintileri ve anlamlı piyasa hareketleri
- Türkiye teknoloji gündemi, TEKNOFEST, TÜBİTAK, teknoparklar, yerli girişimler
- Türkiye yatırımlar ve fırsatlar (VC/PE, teşvik, exit, açık çağrılar — tavsiye değil)
- Türk savunma sanayii: SSB, MSB, ASELSAN, TUSAŞ, Baykar, ROKETSAN, HAVELSAN, TEI, STM ve ilgili ekosistem
- Türkiye ve dünyada kritik askeri/sivil uçak, motor, İHA/SİHA, helikopter, avionik, test, teslimat ve ihracat gelişmeleri
- Her gün 1 AI skill, 1 agent, 1 AI aracı, 1 AI şirketi
- Bugünün ve gerekiyorsa yaklaşan günün anlam ve önemi

## Dosyalar

- Grokbot ham taraması: `intake/YYYY/MM/YYYY-MM-DD.json` (pretty-print JSON; minify yok)
- Grokbot ElevenLabs ses metni: `intake/YYYY/MM/YYYY-MM-DD.elevenlabs.txt`
- Nihai podcast: `reports/YYYY/MM/YYYY-MM-DD.md`

Hedef podcast süresi 45–60 dakikadır. Gündem zayıfsa tekrar veya dolgu yapılmaz.

## Repo yapısı

- [AGENTS.md](AGENTS.md): Ana çalışma kuralları
- [.codex/skills/daily-tech-podcast/SKILL.md](.codex/skills/daily-tech-podcast/SKILL.md): Nihai rapor skill'i
- [docs/GROKBOT_PROMPT.md](docs/GROKBOT_PROMPT.md): 04.00 Grokbot üretim promptu
- [docs/AUTOMATION.md](docs/AUTOMATION.md): İki aşamalı otomasyon tasarımı
- [templates/DAILY_REPORT.md](templates/DAILY_REPORT.md): Nihai rapor şablonu
- [references/EDITORIAL_POLICY.md](references/EDITORIAL_POLICY.md): Kaynak ve doğrulama kuralları

> Bu repo yatırım tavsiyesi, güvenlik garantisi veya otomatik ses dosyası üretmez. Savunma ve havacılık bölümü yalnızca kamuya açık, güvenli kaynaklardan hazırlanır.
