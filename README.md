# 💰 FinansPanel — Gelir & Gider Takip Paneli

Modern, animasyonlu ve tamamen tarayıcıda çalışan kişisel finans paneli.
Kurulum, veritabanı veya sunucu gerekmez — tek dosya HTML.

## ✨ Özellikler

| Alan | Detay |
|---|---|
| **KPI Kartları** | Toplam gelir, toplam gider, net bakiye, tasarruf oranı — sayaç animasyonlu |
| **Nakit Akışı Grafiği** | SVG ile çizilen gelir/gider alan grafiği, çizgi çizim animasyonu, hover tooltip, 6/12 ay geçişi |
| **Gider Dağılımı** | Animasyonlu donut grafik + yüzdelik kategori listesi |
| **İşlem Geçmişi** | Arama, gelir/gider filtresi, satır hover aksiyonları, silme |
| **Bütçe Hedefleri** | Kategori limitleri, renk kodlu ilerleme çubukları (düşük/uyarı) |
| **Son Hareketler** | Zaman akışı görünümü |
| **İşlem Ekleme** | Modal form: tür, açıklama, tutar, tarih, kategori |
| **CSV Dışa Aktarım** | Filtrelenmiş listeyi Excel uyumlu CSV olarak indirir |
| **Tema** | Karanlık / aydınlık mod, tercih hatırlanır |
| **Duyarlı** | Masaüstü, tablet ve mobil (açılır menü) |

## 🚀 Çalıştırma

```bash
npm run dev
# → http://localhost:3000
```

Ya da doğrudan `index.html` dosyasını tarayıcıda açın.

## 💾 Veri

Tüm kayıtlar `localStorage` içinde (`finans-panel-v1`) saklanır.
İlk açılışta 12 aylık gerçekçi örnek veri otomatik üretilir; kendi kayıtlarını ekleyip silebilirsin.

## 🎨 Teknik

- Bağımlılık yok: saf HTML + CSS + JavaScript (ES2020+)
- Grafikler el yazımı SVG (harici chart kütüphanesi kullanılmadı)
- Animasyonlar CSS `@keyframes` + `cubic-bezier` easing + `requestAnimationFrame` sayaçları
- `crypto.randomUUID()` ile kayıt kimlikleri
- Erişilebilir kontrast, klavye ile modal kapatma (ESC)

## 📁 Yapı

```
gelir-gider-takip/
├── index.html   # panelin tamamı (arayüz + stil + mantık)
├── server.js    # basit statik sunucu (npm run dev)
└── package.json
```
