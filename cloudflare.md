# ☁️ Cloudflare Rehberi (Retro Oteller İçin)

Bu döküman, domain'ini Cloudflare'e nasıl bağlayacağını ve retro otelinin güvenliğini nasıl artıracağını adım adım açıklar.

---

## ❓ Cloudflare Nedir?

**Cloudflare**, siteni hızlandıran ve aynı zamanda saldırılara karşı koruyan ücretsiz bir servistir.  
Retro otellerde en çok kullanılan güvenlik çözümlerinden biridir.

**Avantajları:**

- 🛡️ DDoS koruması sağlar  
- 🔒 Ücretsiz SSL (https) sunar  
- ⚡ Siteyi daha hızlı açar (cache sistemi)  
- 🌐 Gerçek IP’yi gizleyerek sunucunu korur  

---

## 🧾 Gerekli Olanlar

- ✅ Bir adet domain (örnek: otelim.com)
- ✅ Domain yönetim paneline erişim (Yöncü, Hostinger, vs.)
- ✅ Cloudflare hesabı ([https://dash.cloudflare.com](https://dash.cloudflare.com))

---

## 🚀 Adım Adım Cloudflare Kurulumu

### 1. Hesap Oluştur

1. [https://cloudflare.com](https://cloudflare.com) adresine git.  
2. Sağ üstten **Sign Up** diyerek kayıt ol.

---

### 2. Domain Ekle

1. Giriş yaptıktan sonra **Add a Site** butonuna tıkla.  
2. Domain adını yaz (örnek: `otelim.com`) ve devam et.  
3. Ücretsiz planı seç (Free Plan) > Continue

---

### 3. Nameserver (NS) Değiştirme

Cloudflare sana iki adet NS (nameserver) verecek.

Bu nameserver’ları, domaini aldığın firmanın yönetim panelinden değiştirmelisin.

**Örnek:**  
- `jessica.ns.cloudflare.com`  
- `max.ns.cloudflare.com`

> ⚠️ DNS değişikliklerinin aktif olması 5 dakikadan 24 saate kadar sürebilir.

---

### 4. DNS Kayıtlarını Kontrol Et

Cloudflare domain’ini tarayıp mevcut DNS kayıtlarını gösterir.

Retro otel kurulumunda eklemen gereken tipik kayıt:

| Tip   | Ad        | Değer               | Proxy |
|--------|-----------|---------------------|--------|
| A     | `@`       | `VDS IP adresin`     | Auto ☁️ |
| A     | `ws`      | `VDS IP adresin`     | Auto ☁️ |

> 🎯 Cloudflare proxy'si **auto** olmalı!

Devam > Save

---

### 5. SSL ve Güvenlik Ayarları

Cloudflare panelinden:

- **SSL/TLS** > Full seç  
- **Page Rules** ile `www` yönlendirmesi ayarla _(isteğe bağlı)_
- **Firewall** bölümünden basit DDoS filtreleri ekleyebilirsin _(isteğe bağlı)_

---

### 6. Websocket SSL Off
Kullanıcının emülatör üzerinden otele bağlanabilmesi için WebSocket bağlantısının SSL olmadan (`ws://`) çalışması gerekmektedir. Bu nedenle Cloudflare üzerinde aşağıdaki şekilde bir **Page Rule** oluşturulmalıdır:

1. Cloudflare panelinden **Rules > Page Rules** bölümüne girin.  
2. **Create Page Rule** butonuna tıklayın.  
3. **URL (required)** kısmına şu ifadeyi yazın: `ws.otelin.com:2096/`
4. **Pick a Setting** alanında `SSL` seçeneğini seçin.  
5. **Select SSL/TLS encryption mode** kısmında `Off` seçin.  
6. Kaydedin.

> ⚠️ Bu ayar, sadece **emülatör bağlantısında SSL zorunluluğu olmayan WebSocket** erişimini sağlamak içindir.

---

## 💬 Destek ve Topluluk

Yardım mı gerekiyor? Fikrin mi var? Geliştiricilerle ve diğer kullanıcılarla iletişim kurmak için destek sunucumuza katılabilirsin:

👉 [Discord Sunucumuz](https://discord.gg/YgeZNjc2ef)  
🌐 [Web Sitemiz](https://www.retrosen.biz)
