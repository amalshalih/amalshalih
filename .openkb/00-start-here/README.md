# 📚 Knowledge Base Yayasan ASIB

> Sentral dokumentasi, SOP, template, dan panduan kerja digital Yayasan Amal Shalih Insan Bantul

**Last Updated:** 7 Juni 2026  
**Status:** 🟢 Active  
**Maintained by:** Tim IT & Pengurus

---

## 🎯 Tujuan Knowledge Base

Knowledge Base ini dibuat untuk:

1. **Single Source of Truth** - Satu sumber referensi resmi untuk semua anggota
2. **Standardisasi Workflow** - SOP yang jelas untuk setiap proses kerja
3. **Onboarding Efisien** - Panduan lengkap untuk anggota & relawan baru
4. **Transparansi & Akuntabilitas** - Dokumentasi yang dapat diakses semua stakeholder
5. **Business Continuity** - Knowledge tetap ada meskipun ada pergantian anggota

---

## 📊 Progress Dokumentasi

### **Completed (15/25 dokumen):**

✅ **Phase 1: Foundation** (8 dokumen)
- [x] README (entry point)
- [x] Struktur & Role Organisasi
- [x] Email & Akses Management
- [x] SOP Rapat & Workflow
- [x] SOP Kegiatan & Event
- [x] Template Agenda Rapat
- [x] Template Notulen Rapat
- [x] Template Decision Log

✅ **Phase 2: Operational SOPs** (5 dokumen)
- [x] SOP Media Sosial & Content Workflow
- [x] SOP Donasi Handling & Keuangan
- [x] SOP Onboarding Relawan
- [x] SOP Rapat (Phase 1)
- [x] SOP Kegiatan (Phase 1)

✅ **Phase 3: IT Technical Docs** (4 dokumen)
- [x] IT Infrastructure & Technical Documentation
- [x] Security Guidelines & Procedures
- [x] Backup & Recovery Procedures
- [x] Credentials & Password Manager Setup

✅ **Phase 4: Templates** (2 dokumen)
- [x] Template Kwitansi Donasi
- [x] Template Laporan Bulanan

### **In Progress (0/25):**
- (none)

### **Planned (10/25):**
- [ ] Privacy Policy
- [ ] Terms of Service
- [ ] Document Storage & Retention Policy
- [ ] Content Calendar Template
- [ ] Analytics Report Template
- [ ] Caption Templates
- [ ] Email Response Templates
- [ ] Archive Structure
- [ ] RAB Template
- [ ] Laporan Keuangan Template

---

## 📂 Struktur Folder

```
docs/
├── 00-start-here/          # Entry point, README ini
│   └── README.md           # 📍 Start here!
│
├── 10-organisasi/          # Struktur organisasi & governance
│   ├── struktur-dan-role.md        # Org structure, roles, contacts
│   └── email-dan-akses.md          # Email routing, access matrix
│
├── 20-sop/                 # Standard Operating Procedures
│   ├── rapat-workflow.md           # SOP rapat & meeting
│   ├── kegiatan-workflow.md        # SOP kegiatan & event
│   ├── media-sosial.md             # SOP media sosial & content
│   ├── donasi-handling.md          # SOP donasi & keuangan
│   └── onboarding-relawan.md       # SOP relawan management
│
├── 30-templates/           # Template dokumen & formulir
│   ├── template-agenda.md          # Template agenda rapat
│   ├── template-notulen.md         # Template notulen rapat
│   ├── template-decision-log.md    # Template decision log
│   ├── kwitansi-donasi.md          # Template kwitansi donasi
│   └── laporan-bulanan.md          # Template laporan bulanan
│
├── 40-it-teknis/           # Dokumentasi teknis IT
│   ├── infrastructure.md           # IT infrastructure overview
│   ├── security.md                 # Security guidelines & procedures
│   ├── backup-recovery.md          # Backup & restore procedures
│   └── credentials.md              # Password manager & credentials
│
├── 50-legal/               # Dokumen legal & compliance
│   ├── (coming soon)
│
└── 90-archive/             # Dokumen historis & arsip
    └── (coming soon)
```
docs/
├── 00-start-here/
│   └── README.md                 # You are here!
│
├── 10-organisasi/
│   ├── visi-misi-digital.md      # Arah transformasi digital
│   ├── struktur-dan-role.md      # Siapa ngapain, contact, akses
│   ├── email-dan-akses.md        # Email routing & setup
│   └── contact-directory.md      # Contact person per role
│
├── 20-sop/
│   ├── rapat-workflow.md         # SOP rapat (pre/during/post)
│   ├── kegiatan-workflow.md      # SOP perencanaan & laporan kegiatan
│   ├── media-sosial.md           # SOP konten sosial media
│   ├── donasi-layanan.md         # SOP konfirmasi & laporan donasi
│   └── onboarding-relawan.md     # SOP onboarding relawan baru
│
├── 30-templates/
│   ├── template-agenda.md        # Template agenda rapat
│   ├── template-notulen.md       # Template notulen rapat
│   ├── template-decision-log.md  # Template decision log
│   ├── template-surat-resmi.md   # Template surat resmi
│   └── template-laporan.md       # Template laporan kegiatan
│
├── 40-it-teknis/
│   ├── infrastructure.md         # Daftar layanan digital
│   ├── security.md               # Security guidelines
│   ├── credentials.md            # API tokens (encrypted)
│   ├── backup-recovery.md        # Backup & disaster recovery
│   ├── sanity-cms-guide.md       # Sanity CMS technical guide
│   ├── cloudflare-email.md       # Cloudflare Email Routing
│   ├── google-drive-structure.md # Google Drive structure
│   └── website-deployment.md     # Website deployment guide
│
├── 50-legal/
│   ├── privacy-policy.md         # Privacy policy website
│   ├── terms-of-service.md       # Terms of service
│   └── dokumen-legal.md          # SK, NIB, NPWP (scan)
│
└── 90-archive/
    ├── rapat-2026/               # Notulen & decision log per tahun
    ├── kegiatan-arsip/           # Laporan kegiatan lama
    └── decision-history/         # Historical decisions
```

---

## 🔐 Akses & Security

### **Prinsip:**
1. **Need-to-know basis** — akses diberikan sesuai role
2. **Separation of concerns** — setiap area ada 1 penanggung jawab
3. **Recovery chain** — setiap critical access punya backup person

### **Email Structure:**
| Email | Pemegang | Role | Recovery |
|-------|----------|------|----------|
| `timitasib@gmail.com` | 1 orang | IT/Teknis | - |
| `amalshalih.insanbantul@gmail.com` | 1 orang | Admin | timitasib@gmail.com |
| `media.amalshalih@gmail.com` | 1 orang | Media | timitasib@gmail.com |

**Detail lengkap:** [Email & Akses](../10-organisasi/email-dan-akses.md)

---

## 📊 Layanan Digital

| Layanan | URL | Access | Owner |
|---------|-----|--------|-------|
| **Website** | amalshalih.or.id | Public | Tim Media |
| **Legacy Domain** | amalshalih.id (redirect) | Protection | Tim IT |
| **Sanity CMS** | sanity.studio | Editor | Tim Media |
| **Google Drive** | drive.google.com | Workspace ASIB | Tim Media |
| **Google Photos** | photos.google.com | Media | Tim Media |
| **Cloudflare** | dash.cloudflare.com | DNS & Email | Tim IT |
| **GitHub** | github.com/konxc/asib | Code repo | Tim IT |
| **Sentry** | sentry.io | Error monitoring | Tim IT |

**Daftar lengkap:** [Infrastructure](../40-it-teknis/infrastructure.md)

---

## 📞 Contact Person

| Area | Contact | Email |
|------|---------|-------|
| **IT & Teknis** | Tim IT | timitasib@gmail.com |
| **Admin & Keuangan** | Tim Admin | amalshalih.insanbantul@gmail.com |
| **Media & Publikasi** | Tim Media | media.amalshalih@gmail.com |
| **Umum** | info@ | info@amalshalih.or.id |
| **Donasi** | donasi@ | donasi@amalshalih.or.id |

**Directory lengkap:** [Contact Directory](../10-organisasi/contact-directory.md)

---

## 🚀 Quick Links

### **Untuk Semua Anggota:**
- 📖 [Visi Misi Digital](../10-organisasi/visi-misi-digital.md)
- 📧 [Setup Email](../10-organisasi/email-dan-akses.md)
- 👥 [Struktur & Role](../10-organisasi/struktur-dan-role.md)

### **Untuk Rapat:**
- 📋 [SOP Rapat](../20-sop/rapat-workflow.md)
- 📄 [Template Agenda](../30-templates/template-agenda.md)
- ✍️ [Template Notulen](../30-templates/template-notulen.md)

### **Untuk Kegiatan:**
- 📅 [SOP Kegiatan](../20-sop/kegiatan-workflow.md)
- 📊 [Template Laporan](../30-templates/template-laporan.md)
- 📸 [Upload Foto](../../PANDUAN_UPLOAD_FOTO_TIM_MEDIA.md)

### **Untuk Media:**
- 📱 [SOP Sosmed](../20-sop/media-sosial.md)
- 🌐 [Update Website](../40-it-teknis/sanity-cms-guide.md)
- 📷 [Galeri Foto](../../PANDUAN_UPLOAD_FOTO_TIM_MEDIA.md)

### **Untuk IT:**
- 🖥️ [Infrastructure](../40-it-teknis/infrastructure.md)
- 🔐 [Security](../40-it-teknis/security.md)
- 💾 [Backup & Recovery](../40-it-teknis/backup-recovery.md)

---

## 📝 Maintenance

**Knowledge Base ini:**
- ✅ Diupdate setiap ada perubahan SOP atau structure
- ✅ Direview berkala (minimal 6 bulan sekali)
- ✅ Version controlled via GitHub
- ✅ Maintained oleh Tim IT

**Cara contribute:**
1. Edit file markdown di folder `docs/`
2. Commit dengan pesan jelas: `docs: update SOP rapat section 3.2`
3. Push ke GitHub
4. Informasikan ke anggota lain via email/WhatsApp

---

## 🎓 Onboarding Checklist

**Untuk anggota baru, pastikan sudah:**

- [ ] Baca dokumen ini (README.md)
- [ ] Baca [Visi Misi Digital](../10-organisasi/visi-misi-digital.md)
- [ ] Baca [Struktur & Role](../10-organisasi/struktur-dan-role.md)
- [ ] Setup email sesuai [panduan](../10-organisasi/email-dan-akses.md)
- [ ] Dapatkan akses ke layanan yang diperlukan
- [ ] Ikuti sesi onboarding dengan coordinator
- [ ] Simpan contact person di phone/email

---

**📢 Penting:** Knowledge Base ini adalah **living document**. Jika ada yang kurang jelas, outdated, atau perlu ditambah, segera informasikan ke Tim IT atau update langsung via pull request.

---

**Dibuat:** 7 Juni 2026  
**Oleh:** Tim IT Yayasan ASIB  
**License:** Internal Use Only — Yayasan Amal Shalih Insan Bantul