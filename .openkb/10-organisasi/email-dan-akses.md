# 📧 Email & Akses Digital

> Panduan lengkap setup dan pengelolaan email organisasi serta akses ke layanan digital

**Last Updated:** 7 Juni 2026  
**Status:** 🟢 Active  
**Source:** [.openkb/email-system.md](../../.openkb/email-system.md)

---

## 📋 Daftar Isi

1. [Email Structure](#email-structure)
2. [Setup Email untuk Tim](#setup-email-untuk-tim)
3. [Cara Pakai Email](#cara-pakai-email)
4. [Layanan Digital](#layanan-digital)
5. [Troubleshooting](#troubleshooting)

---

## 🏗️ Email Structure

### **Domain Strategy: Dual-Domain Protection**

Yayasan memiliki **2 domain** untuk strategi proteksi brand:

**1. Domain Aktif: `amalshalih.or.id`** ✅
- Domain utama untuk operasional sehari-hari
- Email organisasi: `@amalshalih.or.id`
- Website: `https://amalshalih.or.id`

**2. Domain Proteksi: `amalshalih.id`** 🔒
- Domain lama (legacy)
- **Status:** Redirect permanen ke `amalshalih.or.id`
- **Tujuan:** Mencegah penyalahgunaan oleh pihak yang tidak bertanggung jawab
- **Ownership:** Tetap atas nama Yayasan ASIB
- **Tidak ada email aktif** di domain ini (hanya redirect)

```
Strategi Brand Protection:
amalshalih.id (owned by yayasan)
       ↓ (301 Permanent Redirect)
amalshalih.or.id (active domain)
```

### **Email Routing Structure (amalshalih.or.id)**

Kita menggunakan **Cloudflare Email Routing** untuk meneruskan email dari domain `@amalshalih.or.id` ke Gmail pribadi masing-masing pengurus.

```
Pengirim → info@amalshalih.or.id
              ↓
      Cloudflare Email Routing
              ↓
      MX: route1/2/3.mx.cloudflare.net
              ↓
      timitasib@gmail.com (inbox)
```

### **Email Routing Table (amalshalih.or.id)**

| Email @amalshalih.or.id | Diteruskan Ke | Role | Status |
|-------------------------|---------------|------|--------|
| **info@** | timitasib@gmail.com | IT | ✅ Verified & Active |
| **donasi@** | amalshalih.insanbantul@gmail.com | Admin | ✅ Verified & Active |
| **admin@** | amalshalih.insanbantul@gmail.com | Admin | ✅ Verified & Active |
| **humas@** | amalshalih.insanbantul@gmail.com | Admin | ✅ Verified & Active |
| **Catch-all** | timitasib@gmail.com | IT | ✅ Verified & Active |

**All Emails Verified:** ✅ Semua email routing sudah diverifikasi dan aktif per 7 Juni 2026

### **Domain Protection: amalshalih.id**

| Setting | Value | Purpose |
|---------|-------|---------|
| **Status** | 301 Redirect | Redirect permanen ke amalshalih.or.id |
| **DNS** | Cloudflare | Managed oleh IT |
| **Email** | None | Tidak ada email aktif (hanya redirect) |
| **Website** | Redirect to amalshalih.or.id | Semua traffic dialihkan ke domain aktif |
| **Renewal** | Auto-renew | Pastikan domain tidak expired |

**Important:**
- ✅ Domain `amalshalih.id` harus tetap diperpanjang (auto-renew)
- ✅ Jangan pernah release domain ini ke pihak lain
- ✅ Redirect memastikan SEO value tetap terjaga
- ✅ Mencegah phishing/scam menggunakan nama yayasan

---

## 🛠️ Setup Email untuk Tim

### **Untuk Tim IT (timitasib@gmail.com)**

**Anda sudah setup:**
- ✅ Cloudflare Email Routing active
- ✅ Catch-all forwarding ke email Anda
- ✅ MX records configured

**Verify:**
1. Buka https://dash.cloudflare.com → pilih domain `amalshalih.or.id`
2. Kiri → **Email** → **Email Routing**
3. Pastikan status: **Active**
4. Cek rules: info@, catch-all → timitasib@gmail.com

### **Untuk Tim Admin (amalshalih.insanbantul@gmail.com)**

**Yang perlu dilakukan:**
1. **Verifikasi email** untuk forwarding donasi@ dan admin@
2. **Setup Gmail filters** untuk organize email
3. **Setup "Send mail as"** untuk balas dari alamat custom

**Step-by-step:**

#### **Step 1: Verifikasi Email**
1. Cek inbox `amalshalih.insanbantul@gmail.com`
2. Cari email verifikasi dari Cloudflare
3. Klik link verifikasi
4. Jika tidak ada, contact Tim IT untuk resend

#### **Step 2: Setup Gmail Filters**
1. Buka Gmail → ⚙️ Settings → **See all settings**
2. Tab **Filters and Blocked Addresses** → **Create a new filter**
3. Filter 1 (Donasi):
   - To: `donasi@amalshalih.or.id`
   - Create filter → Apply label: "Donasi" → Create
4. Filter 2 (Admin):
   - To: `admin@amalshalih.or.id`
   - Create filter → Apply label: "Admin" → Create

#### **Step 3: Setup "Send Mail As"**
1. Gmail → ⚙️ Settings → **See all settings**
2. Tab **Accounts and Import** → **Send mail as** → **Add another email address**
3. Isi:
   - Name: `Yayasan Amal Shalih Insan Bantul`
   - Email: `donasi@amalshalih.or.id`
   - Uncheck "Treat as an alias"
4. Next → SMTP Settings:
   - SMTP Server: `smtp.gmail.com`
   - Port: `587`
   - Username: `amalshalih.insanbantul@gmail.com`
   - Password: **App Password** (lihat cara di bawah)
   - Secured connection: TLS
5. Add Account → masukkan kode verifikasi
 6. Ulangi untuk `admin@amalshalih.or.id` dan `humas@amalshalih.or.id`

**App Password (jika 2FA aktif):**
1. https://myaccount.google.com/security
2. **2-Step Verification** → **App passwords**
3. Pilih app: **Mail**, device: **Other** → "Cloudflare Email"
4. Copy password 16 digit → gunakan di step 4

### **Untuk Tim Media (media.amalshalih@gmail.com)**

**Note:** humas@ saat ini dikelola oleh Admin untuk efisiensi administratif.
Media team fokus ke content creation & social media management.

**Jika Media perlu akses humas@ di masa depan:**
1. Koordinasi dengan Admin untuk setup filter shared
2. Setup "Send mail as" jika diperlukan
3. Contact Tim IT untuk bantuan setup

---

## 📧 Cara Pakai Email

### **Menerima Email**

Tidak perlu lakukan apa-apa. Email yang dikirim ke `info@`, `donasi@`, `admin@`, `humas@` akan otomatis masuk ke inbox masing-masing.

**Tips organisasi:**
- Pakai **Gmail labels** untuk pisahkan per alamat
- Setup **filters** untuk auto-labeling:
  - `to:info@amalshalih.or.id` → label "Info" (IT)
  - `to:donasi@amalshalih.or.id` → label "Donasi" (Admin)
  - `to:admin@amalshalih.or.id` → label "Admin" (Admin)
  - `to:humas@amalshalih.or.id` → label "Humas" (Admin)
- Cek spam folder jika email tidak masuk

### **Mengirim Email dari Alamat Custom**

Agar bisa **membalas** dari alamat yang sama:

**Saat compose email di Gmail:**
1. Klik **From** dropdown (di sebelah "To")
2. Pilih alamat yang sesuai:
   - Untuk donasi matters → `donasi@amalshalih.or.id`
   - Untuk admin matters → `admin@amalshalih.or.id`
   - Untuk humas matters → `humas@amalshalih.or.id`
3. Compose email seperti biasa
4. Send

**Signature per alamat:**
- Setup signature berbeda untuk setiap "Send mail as" address
- Settings → **See all settings** → **Signature**
- Create signature untuk:
  - `donasi@amalshalih.or.id` — fokus donasi
  - `admin@amalshalih.or.id` — formal administrative
  - `humas@amalshalih.or.id` — media relations

---

## 🌐 Layanan Digital

### **Daftar Lengkap Layanan**

| Layanan | URL | Owner | Access Request |
|---------|-----|-------|----------------|
| **Cloudflare** | dash.cloudflare.com | IT | Contact Tim IT |
| **Google Drive** | drive.google.com | Admin/Media | Contact owner |
| **Google Photos** | photos.google.com | Media | Contact Media |
| **Sanity CMS** | sanity.studio | Media | Invite via Sanity |
| **GitHub** | github.com/konxc/asib | IT | Contact Tim IT |
| **Sentry** | sentry.io | IT | Contact Tim IT |
| **Instagram** | instagram.com/amalshalihinsan | Media | Contact Media |
| **Facebook** | facebook.com/amalshalihinsanbantul | Media | Contact Media |

### **Cara Request Akses**

**Untuk layanan yang dikelola Tim IT:**
1. Email ke timitasib@gmail.com
2. Subjek: "Request Access: [Nama Layanan]"
3. Isi: nama lengkap, role, alasan butuh akses
4. Tim IT akan invite atau share credentials

**Untuk layanan yang dikelola Admin/Media:**
1. Contact langsung owner (lihat [Struktur & Role](struktur-dan-role.md))
2. Owner akan invite via email

---

## 🐛 Troubleshooting

### **Email tidak masuk**
- ✅ Cek spam folder
- ✅ Verify email sudah terverifikasi di Cloudflare
- ✅ Cek log di Cloudflare dashboard → Email → Email Routing → **View logs**
- ✅ Contact Tim IT jika masih bermasalah

### **Tidak bisa kirim dari alamat custom**
- ✅ Pastikan sudah setup "Send mail as" dengan benar
- ✅ Gunakan **App Password**, bukan password biasa
- ✅ Cek SMTP settings: `smtp.gmail.com:587` TLS
- ✅ Verify email sudah confirmed (cek inbox untuk kode verifikasi)

### **SPF/DKIM error**
- ✅ Jangan edit/delete MX records di Cloudflare
- ✅ DKIM di-manage otomatis oleh Cloudflare
- ✅ Jika error, contact Tim IT untuk check DNS records

### **Verifikasi email gagal**
- ✅ Request resend dari Cloudflare dashboard
- ✅ Cek spam folder untuk email verifikasi
- ✅ Pastikan email address benar

---

## 📞 Contact & Bantuan

| Masalah | Contact |
|---------|---------|
| Email routing error | Tim IT (timitasib@gmail.com) |
| Request akses layanan | Tim IT atau owner layanan |
| Setup "Send mail as" | Tim IT (bantuan teknis) |
| Gmail filter setup | Tim IT (bantuan teknis) |

---

## 📚 Referensi

- **Cloudflare Email Routing Docs:** https://developers.cloudflare.com/email-routing/
- **Tech Guide:** https://altersquare.medium.com/free-custom-domain-emails-with-gmail-and-cloudflare-a-beginners-guide-84d759b373f7
- **Internal Docs:** [.openkb/email-system.md](../../.openkb/email-system.md)

---

**Dokumen ini internal — jangan share ke pihak luar**  
**Last reviewed:** 7 Juni 2026  
**Next review:** 7 Desember 2026