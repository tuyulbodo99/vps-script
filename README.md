<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=24&pause=1000&color=9B59B6&center=true&vCenter=true&width=600&lines=VPS+Script;DevCulture+SSH+Tunnel+Setup;Nginx+%7C+SSL+%7C+SSH+over+443" alt="Typing SVG" />

<br/>

[![Part of DevCulture](https://img.shields.io/badge/ecosystem-DevCulture-9b59b6?style=for-the-badge&logo=githubactions&logoColor=white)](https://github.com/tuyulbodo99)
[![Shell](https://img.shields.io/badge/shell-bash-1a1a2e?style=for-the-badge&logo=gnubash&logoColor=white)](https://github.com/tuyulbodo99/vps-script)
[![Nginx](https://img.shields.io/badge/nginx-stream-6c3483?style=for-the-badge&logo=nginx&logoColor=white)](https://nginx.org)
[![SSL](https://img.shields.io/badge/SSL-Let%27s%20Encrypt-5b2c6f?style=for-the-badge&logo=letsencrypt&logoColor=white)](https://certbot.eff.org)

</div>

---

## ⚡ Install — Satu Perintah, Langsung Jalan

> ⚠️ **Edit variabel konfigurasi di dalam script sebelum menjalankan!**
> Domain, username, dan email harus diisi terlebih dahulu.

**Langkah 1 — Download & edit konfigurasi:**
```bash
curl -fsSL https://raw.githubusercontent.com/tuyulbodo99/vps-script/main/install -o install.sh && nano install.sh
```

**Langkah 2 — Jalankan:**
```bash
bash install.sh
```

**Atau download, edit, dan langsung jalankan dalam satu blok:**
```bash
curl -fsSL https://raw.githubusercontent.com/tuyulbodo99/vps-script/main/install -o install.sh \
  && sed -i "s/your.domain.com/DOMAIN_ANDA/g; s/your@email.com/EMAIL_ANDA/g" install.sh \
  && bash install.sh
```

### 🔄 Sync Semua Komponen DevCulture

```bash
bash <(curl -fsSL https://raw.githubusercontent.com/tuyulbodo99/devculture-vps/main/sync.sh)
```

---

## 🟣 Overview

**VPS-Script** adalah setup SSH Tunneling via Nginx dengan dukungan SSL penuh. Cocok untuk konfigurasi SSH over port 443 menggunakan Nginx stream module dan Certbot SSL.

> 🔗 **Bagian dari ekosistem DevCulture** — disinkronkan via `sync.sh`

---

## 🌐 Ekosistem DevCulture

| Repo | Fungsi | One-Click Install |
|------|--------|-------------------|
| [`devculture-vps`](https://github.com/tuyulbodo99/devculture-vps) | 🏠 Core installer | `bash <(curl -fsSL https://raw.githubusercontent.com/tuyulbodo99/devculture-vps/main/install.sh)` |
| [`hokagescript`](https://github.com/tuyulbodo99/hokagescript) | ⚙️ Menu scripts | `bash <(curl -fsSL https://raw.githubusercontent.com/tuyulbodo99/hokagescript/main/setup.sh)` |
| [`vpnscript`](https://github.com/tuyulbodo99/vpnscript) | 🔒 VPN installer | `bash <(curl -fsSL https://raw.githubusercontent.com/tuyulbodo99/vpnscript/main/premi.sh)` |
| **[`vps-script`](https://github.com/tuyulbodo99/vps-script)** | 🔧 **SSH tunnel** ← ini | lihat langkah di atas |
| [`ijin`](https://github.com/tuyulbodo99/ijin) | 🛡️ License DB | `bash <(curl -fsSL https://raw.githubusercontent.com/tuyulbodo99/ijin/main/check-ijin.sh)` |

---

## ⚙️ Konfigurasi

Edit bagian ini di awal file `install` sebelum menjalankan:

```bash
YOUR_DOMAIN="your.domain.com"   # Domain yang sudah pointing ke VPS
SSH_USERNAME="admin"             # Username SSH baru
SSH_PASSWORD=""                  # Kosongkan → gunakan SSH Key
CERTBOT_EMAIL="your@email.com"  # Email untuk notifikasi SSL
SSH_TUNNEL_PORT=443              # Port tunnel (default 443)
SSH_INTERNAL_PORT=22             # Port SSH internal
```

---

## 🔄 Proses Instalasi Otomatis

```
1. Uninstall Nginx & Certbot lama
2. Install OpenSSH Server
3. Install Nginx Full (dengan modul stream)
4. Install Certbot via snap
5. Konfigurasi Nginx stream → SSH tunnel
6. Dapatkan SSL certificate (Let's Encrypt)
7. Buat user SSH baru
8. Restart semua layanan
```

---

## 📋 Requirements

| Item | Detail |
|------|--------|
| OS | Debian 10/11/12 · Ubuntu 20/22 |
| Akses | **Root** |
| Domain | Sudah pointing ke IP VPS |
| Port 80 | Harus bebas (verifikasi SSL) |
| Port 443 | Harus bebas sebelum install |

---

<div align="center">

[![Telegram](https://img.shields.io/badge/Order%20%26%20Support-@devculturebot-9b59b6?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/devculturebot)
[![GitHub](https://img.shields.io/badge/GitHub-tuyulbodo99-1a1a2e?style=for-the-badge&logo=github&logoColor=white)](https://github.com/tuyulbodo99)

<sub>© 2024 DevCulture VPS Store · Part of <a href="https://github.com/tuyulbodo99">tuyulbodo99</a> Ecosystem</sub>

</div>
