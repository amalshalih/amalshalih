# 🏛️ Struktur Organisasi & Role Digital

> **Single Source of Truth** untuk struktur organisasi, role, responsibility, dan contact person

**Last Updated:** 7 Juni 2026  
**Status:** 🟢 Active  
**Maintained by:** Tim IT

---

## 📋 Daftar Isi

1. [Struktur Organisasi](#struktur-organisasi)
2. [Role & Responsibility](#role--responsibility)
3. [Contact Directory](#contact-directory)
4. [Access Matrix](#access-matrix)
5. [Recovery Chain](#recovery-chain)

---

## 🏢 Struktur Organisasi

### **Pengurus Yayasan (Strategic Level)**
```
┌─────────────────────────────────────┐
│        DEWAN PEMBINA / PENGURUS     │
│  - Ketua Pembina: Haryadi           │
│  - Ketua Pengawas: Fury Artanto     │
│  - Ketua Umum: Fat-han Kurnia Mubina│
│  - Bendahara: M. Ilham Syaifudin    │
└─────────────────────────────────────┘
                  │
                  ▼
┌─────────────────────────────────────┐
│        TIM PELAKSANA (Operational)  │
│  - Tim IT & Teknis                  │
│  - Tim Admin & Keuangan             │
│  - Tim Media & Publikasi            │
└─────────────────────────────────────┘
```

---

## 👥 Role & Responsibility

### **1. Tim IT & Teknis**

**Pemegang:** 1 orang (dipercaya)  
**Email:** `timitasib@gmail.com`  
**Backup:** - (hanya 1 orang)

**Responsibilities:**
- 🔐 **Security & Access Control** — manage akses ke semua layanan digital
- 💾 **Backup & Recovery** — backup berkala, disaster recovery planning
- 🖥️ **Infrastructure** — website, DNS, email routing, monitoring
- 📧 **Email Management** — Cloudflare Email Routing setup & maintenance
- 🔑 **Credentials** — API tokens, passwords management (encrypted)
- 📊 **Monitoring** — uptime, error tracking (Sentry), performance
- 📚 **Knowledge Base** — maintenance dokumentasi teknis

**Layanan yang Dikelola:**
| Layanan | Access Level | Criticality |
|---------|--------------|-------------|
| Cloudflare (DNS & Email) | Admin | 🔴 Critical |
| GitHub (Code Repository) | Admin | 🔴 Critical |
| Sanity CMS (Developer) | Developer | 🟡 High |
| Sentry (Monitoring) | Admin | 🟡 High |
| Google Workspace | Super Admin | 🔴 Critical |
| Website Deployment | Deploy access | 🟡 High |

**Contact:** timitasib@gmail.com

---

### **2. Tim Admin & Keuangan**

**Pemegang:** 1 orang (dipercaya)  
**Email:** `amalshalih.insanbantul@gmail.com`  
**Backup:** timitasib@gmail.com (recovery only)

**Responsibilities:**
- 📧 **Administrasi Umum** — surat-menyurat, agenda, notulen rapat
- 💰 **Keuangan & Akuntabilitas** — laporan keuangan, donasi tracking
- 📊 **Laporan Donasi** — konfirmasi donasi, laporan ke donatur
- 📋 **Legal & Compliance** — dokumen legal (SK, NIB, NPWP), privacy policy
- 📅 **Agenda & Jadwal** — calendar yayasan, jadwal rapat, jadwal kegiatan
- 🗂️ **Arsip Digital** — Google Drive `Kantor ASIB` (administratif)

**Layanan yang Dikelola:**
| Layanan | Access Level | Criticality |
|---------|--------------|-------------|
| Google Drive (Kantor ASIB) | Owner | 🔴 Critical |
| Email (admin@, donasi@) | Editor | 🟡 High |
| Rekening Bank | Signatory | 🔴 Critical |
| Template Surat & Laporan | Editor | 🟡 High |

**Contact:** amalshalih.insanbantul@gmail.com

---

### **3. Tim Media & Publikasi**

**Pemegang:** 1 orang (dipercaya)  
**Email:** `media.amalshalih@gmail.com`  
**Backup:** timitasib@gmail.com (recovery only)

**Responsibilities:**
- 📱 **Social Media Management** — Instagram, Facebook, TikTok, YouTube
- 🌐 **Website Content** — update konten via Sanity CMS
- 📷 **Dokumentasi** — foto & video kegiatan, galeri website
- 📰 **Content Creation** — artikel blog, press release, newsletter
- 🎨 **Branding & Design** — visual identity, template, assets
- 📸 **Google Photos** — organize & manage photo library

**Layanan yang Dikelola:**
| Layanan | Access Level | Criticality |
|---------|--------------|-------------|
| Sanity CMS | Editor | 🟡 High |
| Google Drive (Media & Publikasi) | Editor | 🟡 High |
| Google Photos | Owner | 🟡 High |
| Instagram | Admin | 🟢 Medium |
| Facebook | Admin | 🟢 Medium |
| TikTok | Admin | 🟢 Medium |
| YouTube | Admin | 🟢 Medium |

**Contact:** media.amalshalih@gmail.com

---

## 📞 Contact Directory

### **Email Internal (Priority Order)**

| Priority | Email | Role | Use Case |
|----------|-------|------|----------|
| **1** | timitasib@gmail.com | IT/Teknis | Technical issues, access request, security |
| **2** | amalshalih.insanbantul@gmail.com | Admin | Administrasi, keuangan, legal, agenda |
| **3** | media.amalshalih@gmail.com | Media | Konten, sosial media, dokumentasi, pers |

### **Email Publik (@amalshalih.or.id)**

**Status:** ✅ All Verified & Active (7 Juni 2026)

| Email | Diteruskan Ke | Use Case | Status |
|-------|---------------|----------|--------|
| info@amalshalih.or.id | timitasib@gmail.com | Informasi umum, pertanyaan publik | ✅ Verified |
| donasi@amalshalih.or.id | amalshalih.insanbantul@gmail.com | Konfirmasi donasi, laporan donasi | ✅ Verified |
| admin@amalshalih.or.id | amalshalih.insanbantul@gmail.com | Administrasi, surat-menyurat | ✅ Verified |
| humas@amalshalih.or.id | amalshalih.insanbantul@gmail.com | Public inquiries, media relations | ✅ Verified |
| **Catch-all** | timitasib@gmail.com | Email ke alamat lain yang tidak terdaftar | ✅ Verified |

**🔒 Domain Protection Strategy:**
- **Domain Aktif:** `amalshalih.or.id` — untuk semua operasional & email (✅ Verified)
- **Domain Legacy:** `amalshalih.id` — redirect 301 ke `amalshalih.or.id` (brand protection)
- **Purpose:** Mencegah penyalahgunaan nama yayasan oleh pihak tidak bertanggung jawab
- **Ownership:** Kedua domain tetap atas nama Yayasan ASIB
- **Email:** Hanya menggunakan `@amalshalih.or.id` (domain aktif)

### **Contact Person per Area**

| Area | Primary Contact | Backup | WhatsApp |
|------|-----------------|--------|----------|
| **IT & Teknis** | timitasib@gmail.com | - | 0821-3800-7102 |
| **Admin & Keuangan** | amalshalih.insanbantul@gmail.com | timitasib@gmail.com | 0897-2182-648 |
| **Media & Publikasi** | media.amalshalih@gmail.com | timitasib@gmail.com | TBD |
| **Pengurus (Ketua)** | Haryadi | - | TBD |
| **Pengurus (Sekretaris)** | Fat-han Kurnia Mubina | - | TBD |
| **Pengurus (Bendahara)** | M. Ilham Syaifudin | - | TBD |

---

## 🔐 Access Matrix

### **Layanan Digital — Siapa Akses Apa**

| Layanan | IT | Admin | Media | Pengurus |
|---------|----|-------|-------|----------|
| **Cloudflare (DNS)** | ✅ Admin | ❌ | ❌ | ❌ |
| **Cloudflare (Email)** | ✅ Admin | ⚠️ Read-only | ❌ | ❌ |
| **GitHub** | ✅ Admin | ❌ | ❌ | ❌ |
| **Sanity CMS** | ✅ Developer | ⚠️ Viewer | ✅ Editor | ⚠️ Viewer |
| **Google Drive (Kantor)** | ⚠️ Viewer | ✅ Owner | ❌ | ⚠️ Viewer |
| **Google Drive (Media)** | ⚠️ Viewer | ❌ | ✅ Editor | ❌ |
| **Google Photos** | ❌ | ❌ | ✅ Owner | ❌ |
| **Instagram** | ❌ | ❌ | ✅ Admin | ❌ |
| **Facebook** | ❌ | ❌ | ✅ Admin | ❌ |
| **Sentry** | ✅ Admin | ❌ | ❌ | ❌ |
| **Email (info@)** | ✅ Forward | ❌ | ❌ | ❌ |
| **Email (donasi@)** | ✅ Forward | ✅ Receive | ❌ | ❌ |
| **Email (admin@)** | ✅ Forward | ✅ Receive | ❌ | ❌ |
| **Email (humas@)** | ✅ Forward | ❌ | ✅ Receive | ❌ |
| **Rekening Bank** | ❌ | ✅ Signatory | ❌ | ✅ Signatory |
| **Website Deploy** | ✅ Deploy | ❌ | ❌ | ❌ |

**Legend:**
- ✅ Full Access (Owner/Admin)
- ⚠️ Limited Access (Viewer/Read-only)
- ❌ No Access

---

## 🔄 Recovery Chain

### **Prinsip:**
1. **Setiap critical access punya backup person**
2. **Recovery chain harus jelas dan teruji**
3. **Tidak ada single point of failure (kecuali IT)**

### **Recovery Matrix:**

| Primary | Backup | Recovery Scenario |
|---------|--------|-------------------|
| **timitasib@gmail.com** (IT) | - | ⚠️ **Single point of failure** — tidak ada backup. Jika berhalangan, semua critical access terkunci. |
| **amalshalih.insanbantul@gmail.com** (Admin) | timitasib@gmail.com | IT dapat recovery via Google Workspace Super Admin |
| **media.amalshalih@gmail.com** (Media) | timitasib@gmail.com | IT dapat recovery via Google Workspace Super Admin |
| **Sanity CMS (Editor)** | timitasib@gmail.com (Developer) | Developer dapat takeover content management |
| **Rekening Bank** | Pengurus (Ketua/Bendahara) | Dual signatory — jika 1 berhalangan, yang lain bisa akses |

### **Emergency Recovery Procedure:**

**Jika Admin berhalangan:**
1. Contact Tim IT (timitasib@gmail.com)
2. IT recovery via Google Workspace Super Admin
3. Reset password & transfer temporary access
4. Document recovery in decision log

**Jika Media berhalangan:**
1. Contact Tim IT (timitasib@gmail.com)
2. IT recovery via Google account recovery
3. Temporary access ke pengurus yang ditunjuk
4. Document recovery in decision log

**Jika IT berhalangan (CRITICAL):**
1. Contact Pengurus (Ketua atau Sekretaris)
2. Pengurus contact Google Support dengan dokumen legal
3. Recovery via organization ownership proof
4. **Mitigation:** Pertimbangkan untuk tambah 1 orang IT backup

---

## 📋 Next Steps

### **Untuk Anggota Baru:**
1. ✅ Baca dokumen ini
2. ✅ Simpan contact person di phone/email
3. ✅ Pahami role & responsibility Anda
4. ✅ Tahu siapa contact untuk area Anda

### **Untuk Pengurus:**
1. Review access matrix — apakah sudah sesuai?
2. Pertimbangkan untuk tambah IT backup person
3. Setup emergency recovery procedure
4. Document dalam decision log

---

**Dokumen ini bersifat internal — jangan share ke pihak luar**  
**Last reviewed:** 7 Juni 2026  
**Next review:** 7 Desember 2026 (6 bulan)