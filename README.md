<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=24&pause=1000&color=9B59B6&center=true&vCenter=true&width=600&lines=VPS+Script;DevCulture+SSH+Tunnel+Setup;Nginx+%7C+SSL+%7C+SSH+over+443" alt="Typing SVG" />

<br/>

[![Part of DevCulture](https://img.shields.io/badge/ecosystem-DevCulture-9b59b6?style=for-the-badge&logo=githubactions&logoColor=white)](https://github.com/tuyulbodo99)
[![Shell](https://img.shields.io/badge/shell-bash-1a1a2e?style=for-the-badge&logo=gnubash&logoColor=white)](https://github.com/tuyulbodo99/vps-script)
[![Nginx](https://img.shields.io/badge/nginx-stream-6c3483?style=for-the-badge&logo=nginx&logoColor=white)](https://nginx.org)
[![SSL](https://img.shields.io/badge/SSL-certbot-5b2c6f?style=for-the-badge&logo=letsencrypt&logoColor=white)](https://certbot.eff.org)

</div>

---

## 🟣 Overview

**VPS-Script** adalah setup SSH Tunneling via Nginx dengan dukungan SSL penuh. Cocok untuk konfigurasi SSH over port 443 menggunakan Nginx stream module dan Certbot SSL.

> 🔗 **Bagian dari ekosistem DevCulture** — disinkronkan via `sync.sh`

---

## 🌐 Ekosistem DevCulture

| Repo | Fungsi |
|------|--------|
| [`devculture-vps`](https://github.com/tuyulbodo99/devculture-vps) | 🏠 Core installer & panel |
| [`hokagescript`](https://github.com/tuyulbodo99/hokagescript) | ⚙️ Menu & service scripts |
| [`vpnscript`](https://github.com/tuyulbodo99/vpnscript) | 🔒 VPN installer lengkap |
| **[`vps-script`](https://github.com/tuyulbodo99/vps-script)** | 🔧 **SSH tunnel setup** ← Anda di sini |
| [`ijin`](https://github.com/tuyulbodo99/ijin) | 🛡️ License system |

---

## ⚡ Instalasi

> ⚠️ **Edit variabel konfigurasi sebelum menjalankan!**

```bash
# 1. Download script
curl -fsSL https://raw.githubusercontent.com/tuyulbodo99/vps-script/main/install -o install.sh

# 2. Edit konfigurasi (domain, email)
nano install.sh

# 3. Jalankan
chmod +x install.sh && bash install.sh
```

---

## ⚙️ Konfigurasi

Edit bagian ini di awal file `install` sebelum menjalankan:

```bash
YOUR_DOMAIN="your.domain.com"   # Domain Anda yang sudah pointing ke VPS
SSH_USERNAME="admin"             # Username SSH yang ingin dibuat
SSH_PASSWORD=""                  # Kosongkan, gunakan SSH Key untuk keamanan
CERTBOT_EMAIL="your@email.com"  # Email untuk notifikasi SSL
SSH_TUNNEL_PORT=443              # Port tunnel (default 443)
SSH_INTERNAL_PORT=22             # Port SSH internal
```

---

## 🔄 Proses Instalasi

```
1. Uninstall Nginx & Certbot lama (clean slate)
2. Install OpenSSH Server
3. Install Nginx Full (dengan modul stream)
4. Install Certbot via snap
5. Konfigurasi Nginx stream → SSH tunnel
6. Dapatkan SSL certificate
7. Buat user SSH baru
8. Restart semua layanan
```

---

## 📋 Persyaratan

| Item | Detail |
|------|--------|
| OS | Debian 10/11/12 · Ubuntu 20/22 |
| Akses | Root |
| Domain | Sudah pointing ke IP VPS |
| Port 80 | Harus bebas (untuk verifikasi SSL) |
| Port 443 | Harus bebas sebelum install |

---

<div align="center">

[![Telegram](https://img.shields.io/badge/Telegram-@devculturebot-9b59b6?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/devculturebot)
[![GitHub](https://img.shields.io/badge/GitHub-tuyulbodo99-1a1a2e?style=for-the-badge&logo=github&logoColor=white)](https://github.com/tuyulbodo99)

<sub>© 2024 DevCulture VPS Store · Part of <a href="https://github.com/tuyulbodo99">tuyulbodo99</a> Ecosystem</sub>

</div>
