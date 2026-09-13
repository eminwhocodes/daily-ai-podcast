---
name: daily-tech-podcast
description: Research and write the dated Turkish daily technology podcast report for this repository. Use for the daily AI/software/open-source/security/market briefing or when updating an existing daily report.
metadata:
  short-description: Günlük teknoloji podcast raporu
---

# Daily Tech Podcast

Günün doğrulanmış teknoloji gündemini Emin'in kod yazarken dinleyebileceği, doğal Türkçe bir podcast metnine dönüştür.

## Başlamadan önce

- Repo kökündeki `AGENTS.md` kurallarını uygula.
- Kaynak seçimi, güvenlik ve piyasa iddiaları için [editoryal politika](../../../references/EDITORIAL_POLICY.md) dosyasını oku.
- Çıktı düzeni için [günlük rapor şablonunu](../../../templates/DAILY_REPORT.md) oku.
- Mevcut gün raporu varsa önce onu oku ve yinelenen içerikleri birleştir.

## Araştırma penceresi

Ana pencere son 24–36 saattir. Yayın/olay tarihini ayrı ayrı kontrol et. Daha eski bir olay yalnızca bugün yeni bir sürüm, düzeltme, resmi açıklama veya anlamlı devam gelişmesi aldıysa ana gündeme girer.

Arama sorgularını konu kümelerine böl:

- AI modelleri, OpenAI/ChatGPT, agent ve geliştirici araçları
- GitHub releases/trending, açık kaynak, Coolify/Docker
- Laravel/PHP, Python/PyPI, JavaScript/TypeScript/npm
- CISA KEV, NVD/CVE, GitHub Security Advisories ve üretici bültenleri
- Cloudflare, Microsoft, GitHub ve büyük servis durum sayfaları
- Büyük teknoloji şirketlerinin resmi yatırımcı ilişkileri ve doğrulanmış piyasa verisi
- Bugünün/yarının önemli tarihleri

## Seçim ölçütü

Her aday için şu soruları sor:

1. Yeni mi ve tarih doğrulandı mı?
2. Emin'in yazılım, sunucu, ajans veya AI işlerine somut etkisi var mı?
3. Birincil ya da güçlü bir kaynak var mı?
4. Önemi bir paragrafta açıklanabiliyor mu?
5. Aynı konunun daha değerli bir gelişmesini dışarıda bırakıyor mu?

Zayıf maddeleri çıkar. Gündem zayıfsa 60 dakikayı doldurmak için içerik uydurma veya tekrar yapma.

## Zorunlu bölümler

- Açılış ve bugünün haritası
- Kritik gelişmeler
- AI ve agent dünyası
- Yazılım ve açık kaynak
- Laravel/PHP, Python ve web ekosistemi
- Coolify, Docker, Cloudflare ve altyapı
- Siber güvenlik ve güncelleme kontrol listesi
- Büyük teknoloji şirketleri, kesintiler ve piyasalar
- Günün keşifleri: tam olarak 1 skill, 1 agent, 1 AI tool, 1 AI firması
- Bugünün anlam ve önemi; yarın/arife notu varsa ekle
- Emin için “bugün ne yapmalı?” özeti
- Kapanış
- Kaynakça

Bir kategoride doğrulanmış önemli gelişme yoksa bunu tek cümleyle söyle; sahte dolgu ekleme.

## Podcast yazımı

Hedef 45–60 dakika ve yaklaşık 6.500–8.500 Türkçe kelimedir; haber yoğunluğu yetersizse daha kısa olabilir. Her ana bölüme benzersiz bir kimlik ver: `[B01]`, `[B02]`… Böylece kullanıcı Voice içinde “B04'ü tekrar anlat” diyebilir.

Her önemli maddede doğal akışla şunları açıkla:

- Ne oldu?
- Neden şimdi konuşuyoruz?
- Teknik olarak ne değişti?
- Emin'in işleri açısından etkisi ne?
- Bugün yapılacak bir işlem var mı?
- Neyi henüz bilmiyoruz?

Metni sesli okunacak şekilde yaz. Uzun URL'leri gövdede okuma; kaynakçaya koy. Tabloyu yalnızca hızlı başvuru özetinde kullan, anlatı gövdesini paragraflarla yaz.

## Çıktı

`reports/YYYY/MM/YYYY-MM-DD.md` dosyasını oluştur veya dikkatle güncelle. Bütün esas iddialarda yakın Markdown bağlantısı bulunmalı; kaynakçada yinelenen bağlantıları temizle.

Son kontrolde:

- Tarih ve saat dilimi doğru mu?
- Her haber gerçekten araştırma penceresinde mi?
- Kaynak bağlantıları iddiayı destekliyor mu?
- CVE ve sürüm numaraları doğru mu?
- Piyasa verisinin tarihi/seansı belirtilmiş mi?
- Gerçek ile çıkarım ayrılmış mı?
- Dört günlük keşif kategorisi birbirinden farklı mı?
- Bölüm kimlikleri sıralı mı?
- Dosya yolu doğru mu?
