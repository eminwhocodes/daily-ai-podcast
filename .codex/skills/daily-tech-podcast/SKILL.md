---
name: daily-tech-podcast
description: Research and write the dated Turkish daily technology podcast report for this repository, including global and Turkish technology, startups, defense, aviation, software, security, AI, open-source, infrastructure, and market developments.
metadata:
  short-description: Günlük teknoloji podcast raporu
---

# Daily Tech Podcast

Günün doğrulanmış teknoloji gündemini Emin'in kod yazarken dinleyebileceği doğal Türkçe bir podcast metnine dönüştür.

## Başlamadan önce

- Repo kökündeki `AGENTS.md` kurallarını uygula.
- [Editoryal politikayı](../../../references/EDITORIAL_POLICY.md) ve [günlük rapor şablonunu](../../../templates/DAILY_REPORT.md) oku.
- Varsa bugünün `intake/YYYY/MM/YYYY-MM-DD.json` Grokbot dosyasını oku. Bunu aday havuzu say; kaynakları yeniden açıp doğrula.
- Mevcut gün raporu varsa önce onu oku ve yinelenen içerikleri birleştir.

## Araştırma penceresi ve hatları

Ana pencere son 24–36 saattir. Yayın ve olay tarihini ayrı kontrol et. Daha eski olay ancak bugün yeni test, sürüm, düzeltme, resmî açıklama veya devam gelişmesi aldıysa ana gündeme girer.

Şu hatları ayrı sorgularla tara:

- AI modelleri, OpenAI/ChatGPT, agent ve geliştirici araçları
- GitHub releases/trending, açık kaynak, Coolify/Docker
- Laravel/PHP, Python/PyPI, JavaScript/TypeScript/npm
- CISA KEV, NVD/CVE, GitHub Security Advisories ve üretici bültenleri
- Cloudflare, Microsoft, GitHub ve büyük servis status sayfaları
- Büyük teknoloji şirketlerinin yatırımcı ilişkileri ve doğrulanmış piyasa verisi
- Türkiye teknoloji gündemi, yerli startup/yatırım, teknopark, TÜBİTAK ve TEKNOFEST
- Türkiye savunma sanayii kurumları, şirketleri ve programları
- Küresel askeri/sivil havacılık, uçak, motor, avionik, İHA/SİHA, test, sertifikasyon, sipariş ve teslimatlar
- Bugünün ve yarının önemli tarihleri

## Seçim ölçütü

Her adayda yenilik, tarih, kaynak gücü, Emin'e etkisi ve gerçek önem aranır. Savunma/havacılıkta ilk uçuş, kritik test, kaza, yere indirme, büyük sözleşme, seri üretim, teslimat, ihracat ve doktrin/tedarik değişikliği yüksek önceliklidir. Küçük PR paylaşımlarını, doğrulanmamış söylentileri ve tekrarları çıkar.

Gündem zayıfsa 60 dakikayı doldurmak için içerik uydurma.

## Zorunlu bölümler

- Açılış ve bugünün haritası
- Kritik gelişmeler
- AI ve agent dünyası
- Yazılım ve açık kaynak
- Laravel/PHP, Python ve web ekosistemi
- Coolify, Docker, Cloudflare ve altyapı
- Siber güvenlik ve güncelleme kontrol listesi
- Türkiye teknoloji, girişimler ve TEKNOFEST
- Türk savunma sanayii
- Dünya savunma ve havacılık
- Büyük teknoloji şirketleri, kesintiler ve piyasalar
- Tam olarak 1 skill, 1 agent, 1 AI tool, 1 AI firması
- Bugünün anlam ve önemi; gerekiyorsa yarın/arife
- Emin için bugün ne yapmalı?
- Kapanış ve kaynakça

Bir kategoride doğrulanmış gelişme yoksa tek cümleyle söyle; sahte dolgu ekleme.

## Podcast yazımı

Hedef 45–60 dakika ve yaklaşık 6.500–8.500 Türkçe kelimedir; haber yoğunluğu yetersizse daha kısa olabilir. Her ana bölüme sıralı kimlik ver: `[B01]`, `[B02]`… Böylece Voice içinde “B10'u tekrar anlat” denebilir.

Her önemli maddede ne oldu, neden önemli, teknik/stratejik değişiklik, Emin'e etkisi, yapılacak işlem ve bilinmeyenleri doğal akışta açıkla. Savunma haberinde prototip, test, seri üretim, teslimat ve operasyonel hizmet seviyelerini karıştırma. Kamuya açık bilgiyle sınırlı kal; hassas operasyonel ayrıntı verme.

Uzun URL'leri gövdede okuma; kaynakçaya koy. Tabloları yalnızca hızlı başvuru için kullan.

## Çıktı ve kontrol

`reports/YYYY/MM/YYYY-MM-DD.md` dosyasını oluştur veya dikkatle güncelle. Esas iddialara yakın Markdown bağlantısı ver.

Son kontrolde tarih/pencere, kaynakların iddiayı desteklemesi, CVE/sürüm numarası, piyasa tarihi/seansı, savunma program aşaması, uçak/model adı, gerçek-iddia-çıkarım ayrımı, dört keşfin farklılığı, bölüm sırası ve dosya yolunu denetle.
