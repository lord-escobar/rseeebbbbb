# 🏨 Retrosen Başlangıç Rehberi: Kendi Retro Otelini Kur!

Retro oyun dünyasına adım atmak mı istiyorsun? Bu rehber, sıfırdan kendi retro otelini kurmanı sağlayacak. Hazırsan başlayalım!

## 🚀 Giriş

Retro otel, Habbo tarzında çalışan, oyuncuların sohbet edebileceği, odalar oluşturabileceği bir sosyal platformdur. Kendi otelini kurarak bu dünyaya liderlik edebilirsin!

---

## 📦 Gerekli Dosyalar

Otel kurmak için bazı temel dosyalara ihtiyacın olacak:

- ✅ Otel CMS'i (örneğin: RevCMS, PlusEMU uyumlu bir CMS)
- ✅ Emulator (örneğin: PlusEMU veya ArcturusEMU)
- ✅ Veritabanı (MySQL)
- ✅ Xampp ya da Laragon gibi bir sunucu ortamı

---

## 🛠️ Kurulum Adımları

### 1. Sunucu Ortamını Kur
- [XAMPP](https://www.apachefriends.org/tr/index.html) veya [Laragon](https://laragon.org/) indir.
- Apache ve MySQL'i çalıştır.

### 2. Veritabanını Hazırla
- `localhost/phpmyadmin` adresine git.
- Yeni bir veritabanı oluştur (örnek: `retro_db`).
- CMS'in içinden `.sql` dosyasını içeri aktar.

### 3. Emulator Kurulumu
- Emulator dosyalarını indir.
- `config.ini` dosyasını düzenleyerek veritabanı ve bağlantı ayarlarını yap.
- `PlusEMU.exe` dosyasını çalıştır.

### 4. CMS Kurulumu
- CMS dosyalarını `htdocs` klasörüne at.
- `app/config.php` gibi yapılandırma dosyalarını düzenle.
- Tarayıcıdan otel sitesine girerek kurulumu tamamla.

---

## 🔐 Yönetici Hesabı Oluşturma

Veritabanına gidip `users` tablosunu aç. Mevcut hesabına `rank` değerini `7` yaparak kendini otelin sahibi yapabilirsin.

---

## 💡 İpuçları

- Tarayıcıda hata alıyorsan `error_log` dosyasını kontrol et.
- Otelini başkalarıyla paylaşmak için bir sunucuya taşıman gerekir.
- Güvenlik için veritabanı ve CMS şifrelerini güçlü yap!

---

## 🤝 Yardım & Destek

Sorun mu yaşıyorsun? [Retrosen Discord](https://discord.gg/seninlinkin) sunucumuza gel ve destek al!

---

**Hazırlayan:** Retrosen Ekibi  
**Tarih:** Haziran 2025  
