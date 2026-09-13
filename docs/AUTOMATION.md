# Multi-bot + iki aşamalı yayın

## 04.00 — Fan-out

Daily Podcast, Europe/Istanbul 04.00'te uzman DP botlarına derin tarama dağıtır (AI, Yazılım, Açık Kaynak, Altyapı, Siber, Büyük Tech, Piyasa, TR Tech, TR Savunma, Havacılık, Keşif, Tarih, **TR Yatırım / `tr_invest`**).

Botlar podcast yazmaz; kaynaklı uzun araştırma paketi üretir ve orkestratöre döner.

## 04.45 — Merge + Fish + WhatsApp

Daily Podcast staging/gelen paketleri birleştirir ve şunları yazar:

- `intake/YYYY/MM/YYYY-MM-DD.json` — pretty-print UTF-8 (minify yok; alan kısaltması yok); track’ler arasında `tr_invest` vardır
- `intake/YYYY/MM/YYYY-MM-DD.elevenlabs.txt` — açılış: `{gün} {ay} {haftanın günü}. Günaydın. Günün podcast'ına hoş geldin.`

Ardından KNT-MONSTER17 üzerinde:

```bat
fish-podcast.bat "https://raw.githubusercontent.com/eminwhocodes/daily-ai-podcast/main/intake/YYYY/MM/YYYY-MM-DD.elevenlabs.txt"
```

MP3 oluşunca WA Gönderici / Evolution MeteAI (`whatsapp.codron.cloud`) ile `905335666101` numarasına ses olarak gönderilir. Box TLS bozuksa PC üzerinden REST.

## 05.00 — ChatGPT doğrulaması ve podcast

ChatGPT:

1. Repo kurallarını ve bugünün intake dosyasını okur.
2. Aday kaynaklarını yeniden açar.
3. Eksik alanlarda ek araştırma yapar.
4. Yanlış/yinelenen/önemsiz maddeleri eler.
5. Nihai raporu `reports/YYYY/MM/YYYY-MM-DD.md` yoluna yazar (Türkiye yatırımlar/fırsatlar bölümü dahil; tavsiye değil).
6. Kısa özet + rapor bağlantısı verir.

## Cron (Europe/Istanbul)

```cron
0 4 * * *
45 4 * * *
```

## Hata davranışı

- Eksik uzman paketi `failed_tracks` ile işaretlenir; merge mümkünse devam eder.
- Fish veya WA başarısızsa “gönderildi” denmez; hata + local MP3 yolu bildirilir.
- Kaynak URL’siz aday nihai rapora otomatik alınmaz.
