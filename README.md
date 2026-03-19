# 📜 Görev Günlüğü — Gamified Life RPG

Hayatını bir RPG oyununa dönüştür. Görevleri tamamla, XP kazan, seviye atla.

🔗 **Canlı Site:** [sezginildes.github.io/quest-journal](https://sezginildes.github.io/quest-journal)

---

## 🎮 Ne Yapar?

Günlük görevlerini RPG mekanikleriyle takip eder. Her tamamlanan görev XP kazandırır, streak oluşturur ve rastgele dopamin ödülleri verir.

---

## ✨ Özellikler

- **Gmail ile giriş** — veriler buluta kaydedilir, cihaz bağımsız
- **Eisenhower Matrisi** — görevleri önceliğine göre grupla, sürükle bırak ile taşı
- **6 Kategori** — Beden, Zihin, Kariyer, İlişkiler, Anlam, Sistem
- **XP & Seviye Sistemi** — görev zorluğuna göre XP kazan, seviye atla
- **Dopamin Ödül Sistemi** — %70 şansla rastgele ödül (Common → Legendary)
- **Streak Takibi** — günlük seri, ateş animasyonu
- **Focus Modu** — tek görev, 25 dakika geri sayım timer, tam ekran
- **Haftalık Rapor** — her Pazar Telegram'a otomatik analiz
- **Günlük Hatırlatma** — her sabah 08:13'te Telegram bildirimi
- **PWA** — telefona uygulama olarak yüklenebilir

---

## 🛠️ Teknolojiler

| Araç | Kullanım |
|------|----------|
| HTML/CSS/JS | Frontend — tek dosya, framework yok |
| Supabase | Auth (Google OAuth) + Veritabanı |
| GitHub Pages | Hosting (ücretsiz) |
| Make.com | Otomasyon pipeline |
| Claude API | Haftalık rapor analizi |
| Telegram Bot | Bildirimler ve raporlar |

---

## 📊 Veri Yapısı

```
Supabase
├── characters    → Kullanıcı karakter verisi (JSON)
└── quest_logs    → Tamamlanan görev logları
```

---

## 🚀 Kurulum

Bu proje kişisel kullanım için tasarlanmıştır. Kendi versiyonunu kurmak için:

1. Repoyu fork'la
2. Supabase projesi oluştur, `characters` ve `quest_logs` tablolarını kur
3. Google Cloud Console'da OAuth app oluştur
4. `index.html` içindeki `SUPABASE_URL` ve `SUPABASE_KEY` değerlerini güncelle
5. GitHub Pages'i aktif et

---

## 📱 Ekran Görüntüleri

| Ana Ekran | Görev Matrisi | Focus Modu |
|-----------|---------------|------------|
| Karakter barı, XP, streak | Eisenhower 4 kutu | 25 dk timer, tam ekran |

---

## 🗺️ Yol Haritası

- [ ] Görev düzenleme
- [ ] Yinelenen görevler (günlük/haftalık)
- [ ] Çok kullanıcılı — koç paneli
- [ ] Veli Telegram raporu
- [ ] Supabase RLS güvenlik
- [ ] Telegram bot komutları

---

*Sıfır kod yazarak, sadece doğru soruları sorarak inşa edildi. Toplam süre: ~12 saat.*
