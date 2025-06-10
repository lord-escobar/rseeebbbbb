> 💡 Ana Sayfaya dönmek istiyorsan [Ana Sayfaya git →](./baslangic-rehberi.md)

# 🌐 IIS (Internet Information Services) Kurulumu Rehberi

Bu döküman, Windows kullanıcıları için IIS'nin nasıl kurulacağını ve retro otel projelerinde nasıl kullanılacağını adım adım açıklar.

---

## 🧩 IIS Nedir?

**IIS**, Windows tarafından geliştirilen bir web sunucu yazılımıdır. XAMPP gibi Apache tabanlı çözümlere alternatif olarak kullanılır. Retro otel projelerinde özellikle CMS (örneğin AtomCMS) yayınlamak için tercih edilebilir.
> 💡 Bizde Xampp yerine IIS kurmanızı tevsiye ederiz.

---

## 🖥️ Gereksinimler

- ✅ Windows 10 / 11 Pro veya Enterprise (Home sürümleri kısıtlı olabilir)
- ✅ İnternet bağlantısı
- ✅ Yönetici yetkileri

---

## 🛠️ IIS Nasıl Kurulur?

### 1. Denetim Masasını Aç
- Başlat'a **“Denetim Masası”** yaz ve aç.

### 2. "Programlar ve Özellikler"e Git
- Sol menüden "**Windows özelliklerini aç veya kapat**" seçeneğine tıkla.

### 3. IIS Seç
Açılan pencerede aşağıdaki kutuları işaretle:

- **Internet Information Services**
- Altındaki şu bileşenleri de seç:
  - **Web Management Tools**
  - **World Wide Web Services**
  - **Application Development Features** > `ASP.NET`, `.NET Extensibility`, `CGI`, `ISAPI Extensions`, `ISAPI Filters`
  - **Common HTTP Features** > `Default Document`, `Static Content`, `HTTP Errors`

📝 İpucu: CMS sistemleri genellikle `ASP.NET` veya `PHP` kullanmaz, ama bazı sistemlerde gerekli olabilir.

### 4. Kurulumu Tamamla
- Seçim yaptıktan sonra **Tamam** butonuna bas.
- Windows bileşenleri yükleyecek (birkaç dakika sürebilir).

---

## ✅ Kurulum Kontrolü

Tarayıcıya girip şu adresi yaz:
http://localhost


Eğer “**IIS Welcome Page**” (hoş geldin sayfası) açılıyorsa, IIS başarıyla kurulmuştur.

---

## 🗂️ Web Sitesi Yayınlama (Örnek)

1. **Web Dosyalarını Hazırla:**
   - Otel CMS dosyalarını bir klasöre koy (örneğin `C:\inetpub\wwwroot\atomcms`)

2. **IIS Üzerinden Yayınla:**
   - `Internet Information Services (IIS) Manager` uygulamasını aç.
   - Sol menüden "Sites" > Sağ tıkla > "Add Website"
   - Site adını gir (örnek: `RetroOtel`)
   - Fiziksel yol olarak dosyalarının olduğu klasörü seç (örnek: `C:\inetpub\retro`)
   - Portu 80 bırakabilirsin. Domainin yoksa `localhost` olarak çalışır.

3. **Hosts Dosyasına Giriş Ekle (İsteğe Bağlı):**

127.0.0.1 retrootel.local

Ardından `http://retrootel.local` yazarak giriş yapabilirsin.

---

## 🧪 Ekstra Ayarlar

- **PHP ile Kullanmak için:** [PHP for IIS indir](https://windows.php.net/download) ve FastCGI ile entegre et.
- **Veritabanı için:** MySQL veya MariaDB kurulu olmalı.

---

## 💬 Yardım ve Destek

Kurulumda takıldığın yerler için bize ulaşabilirsin:  
👉 [Retrosen Discord Destek Sunucusu](https://discord.gg/seninlinkin)

---

## 📌 Not

Bu döküman retro otel sistemlerinde kullanımı hedeflenmiştir. Gelişmiş yapılandırma için IIS belgelerine göz atabilirsin:  
🔗 https://learn.microsoft.com/en-us/iis/

---

**Hazırlayan:** Lord
**Tarih:** Haziran 2025  
