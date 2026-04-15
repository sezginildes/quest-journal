# 📜 Görev Günlüğü — Gamified Life RPG & Mentor Paneli

Hayatını bir RPG oyununa dönüştür. Görevleri tamamla, XP kazan, seviye atla ve bir "High-End Mentor" olarak günlük zihinsel ritüellerini kayıt altına al.

🔗 **Canlı Site:** [sezginildes.github.io/quest-journal](https://sezginildes.github.io/quest-journal)

---

## 🎮 Ne Yapar?

Sadece bir "yapılacaklar listesi" değil; Eisenhower matrisi ile görev önceliklendirmesi yapan, Pomodoro ile odaklanma sağlayan, RPG mekanikleriyle (XP, Seviye, Rastgele Ödüller) dopamin döngüsünü besleyen ve **Sabah/Akşam Ritüelleriyle** derinlemesine öz-farkındalık yaratan tam teşekküllü bir kişisel yönetim sistemidir.

---

## ✨ Özellikler

- **Bulut Senkronizasyonu** — Gmail (Google OAuth) ile giriş, her cihazda anında erişim.
- **Eisenhower Matrisi** — Görevleri Acil/Önemli durumuna göre 4 kadranda yönet, sürükle-bırak ile taşı.
- **6 Temel Kategori** — Beden, Zihin, Kariyer, İlişkiler, Anlam, Sistem.
- **XP & Seviye Sistemi** — Görev zorluğuna ve seçilen "Sınıf"a (Savaşçı, Alim, Bilge vb.) göre XP kazan.
- **Dopamin Ödül Çarkı** — Görev bitiminde %70 şansla sandık açılır (Common → Legendary ödüller).
- **Şefkatli Streak Takibi** — Günlük seri ateşi. (ADHD dostu "İrade Kalkanı" ile 1 gün atlasan bile serin bozulmaz).
- **Focus Modu (Pomodoro)** — Tek göreve odaklan, 25 dk geri sayım, zaman kumbarasında toplam odak süreni biriktir.
- **YENİ: Mentor Ritüelleri (Check-in)** — Excel tabanlı derin yansıma sistemi. Sabahları "Şafak Ritüeli" ile niyet belirle, akşamları "Alacakaranlık Ritüeli" ile 4 temel metriği (Performans, Enerji, Bağ, Büyüme) puanla.
- **YENİ: Gelişmiş Görev Yönetimi** — Görevleri düzenle, kopyala ve günlük/haftalık/aylık olarak **tekrarlanan (recurring)** görevler oluştur.
- **PWA Desteği** — Telefone yerel bir uygulama gibi yüklenebilir.

---

## 🛠️ Teknolojiler

| Araç | Kullanım |
|------|----------|
| **HTML/CSS/JS** | Frontend — tek dosya, harici framework yok (Vanilla JS). |
| **Supabase** | Backend — Auth (Google) + PostgreSQL Veritabanı + Realtime Sync. |
| **GitHub Pages** | Hosting (Ücretsiz ve hızlı yayına alma). |
| **Make.com & Claude** | Otomasyon pipeline ve haftalık rapor analizi. |
| **Telegram Bot** | Sabah 08:13 bildirimleri ve Pazar analiz raporları. |

---

## 📊 Veri Yapısı (Supabase)

Sistem 3 temel tablo üzerinde çalışır:

```text
Supabase
├── characters    → Kullanıcı karakter verisi, statlar, aktif görevler, envanter (JSONB)
├── quest_logs    → Tamamlanan görevlerin analitik logları (Tarih, Kategori, Kazanılan XP)
└── checkins      → YENİ: Sabah ve Akşam ritüellerinin detaylı raporları (JSONB)
```

---

## 🚀 Kurulum

Bu proje kişisel kullanım ve "High-End Coaching" süreçleri için tasarlanmıştır. Kendi versiyonunu kurmak için:

1. Bu repoyu fork'la.
2. [Supabase](https://supabase.com/)'de yeni bir proje oluştur.
3. SQL Editor üzerinden `characters`, `quest_logs` ve `checkins` tablolarını inşa et.
4. Supabase Auth ayarlarından Google sağlayıcısını (OAuth) aktif et.
5. `index.html` içindeki `SUPABASE_URL` ve `SUPABASE_KEY` sabitlerini kendi projeninkilerle değiştir.
6. GitHub Pages'i aktif ederek projeyi canlıya al.

---

## 🗺️ Yol Haritası

- [x] Görev düzenleme (Edit Modal eklendi)
- [x] Yinelenen görevler (Günlük/Haftalık/Aylık recur eklendi)
- [x] Detaylı Günlük Check-in Sistemi (Şafak ve Alacakaranlık Ritüelleri eklendi)
- [ ] Çok kullanıcılı — Koç/Mentor Paneli (Öğrenci verilerini tek ekrandan görme)
- [ ] Veli Telegram raporu otomasyonu
- [ ] Supabase RLS (Row Level Security) güvenlik politikalarının sıkılaştırılması
- [ ] Telegram bot üzerinden direkt uygulamaya görev ekleme (Webhook)

---

*Sıfır kod yazarak, sadece yapay zekaya doğru mimari soruları sorarak inşa edildi. (Güncellemeler dahil toplam süre: ~14 saat).*
