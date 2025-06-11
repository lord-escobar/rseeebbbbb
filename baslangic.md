# 💡Başlangıç Rehberi

Kendi retro otelini kurmak istiyorsan, sadece CMS ve emulator yetmez. Bu projeyi **internet üzerinden yayınlamak** için aşağıdaki temel gereksinimlere ihtiyacın olacak.

---

## 🖥️ 1. VDS (Sanal Sunucu)

Otelini 7/24 açık tutmak için kişisel bilgisayar yerine bir **VDS (Virtual Dedicated Server)** kullanmalısın. VDS, sana ait özel bir sanal makinedir.

### Önerilen VDS Özellikleri

| Kullanım Türü | Minimum Özellikler | Not |
|---------------|--------------------|-----|
| Test Oteli (az kişi) | 1vCPU, 2 GB RAM, 20 GB SSD | Ucuzdur ama yavaş olabilir |
| Orta Seviye Otel | 2vCPU, 4 GB RAM, 40+ GB SSD | Tavsiye edilen minimum |
| Büyük Otel (aktif oyunculu) | 4vCPU+, 8 GB RAM+, NVMe disk | Cloudflare + güvenlik şart |

### VDS Firması Önerileri
> ⚠️ Türkiye'den alınan VDS’lerde ping düşüktür, Avrupa lokasyonlarında ise bağlantı daha dengelidir.

- [**Etkinhost** (TR)](https://www.etkinhost.com.tr)
- [**Natro** (TR)](https://www.natro.com)
- [**Vultr** (EU/US)](https://www.vultr.com/)
- [**Hetzner** (DE)](https://www.hetzner.com/)
- [**Contabo** (DE)](https://contabo.com/)

---

## 🌐 2. Domain (Alan Adı)

Oyuncuların oteline kolayca ulaşabilmesi için bir alan adına ihtiyacın var. IP ile giriş amatörce görünür.

### Önerilen Domain Uzantıları

- `.com` → Profesyonel görünüm, önerilir  
- `.fun`, `.xyz` → Ucuz ama geçici olabilir  
- `.net`, `.org` → Alternatifler  

### Domain Firması Önerileri

- [**Namecheap**](https://www.namecheap.com/)
- [**Porkbun**](https://porkbun.com/)
- [**Turhost** (TR)](https://www.turhost.com/)
- [**İsimtescil** (TR)](https://www.isimtescil.net/)

> 🔐 Domain alırken WHOIS koruması sunan firmaları tercih et.

---

## ☁️ 3. Cloudflare

Cloudflare, otelinin **güvenliği**, **DDoS koruması** ve **hız optimizasyonu** için olmazsa olmazdır.

### Cloudflare Ne Yapar?

- 🛡️ DDoS saldırılarına karşı koruma sağlar  
- ⚡ Siteyi daha hızlı açar (cache)  
- 🔒 SSL (https) desteği sunar  
- 🌍 Gerçek IP’yi gizleyerek güvenlik sağlar  

Cloudflare'e domainini bağlamak için [Cloudflare Başlangıç Rehberi](./cloudflare-rehberi.md) sayfamıza göz atabilirsin.

---

## 🎯 Neler Öğrendik?

Otelini kurmadan önce:

- Bir VDS kiralamalısın  
- Bir domain alarak giriş adresi belirlemelisin  
- Cloudflare kullanarak güvenlik ve hız avantajı sağlamalısın  

Bunlar tamamlandıktan sonra **CMS, emulator ve veritabanı** kurulumuna geçebilirsin.

---

## 💬 Yardım mı Lazım?

Her adımı detaylıca anlatıyoruz. Takıldığında topluluğumuza katıl:

👉 [Retrosen Discord Destek Sunucusu](https://discord.gg/seninlinkin)  
🌐 [Web Sitemiz](https://www.retrosen.com)

---

**Hazırlayan:** Retrosen Ekibi  
**Tarih:** Haziran 2025
