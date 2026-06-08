# Manajemen Workspace & Operasional Digital — Yayasan Amal Shalih Insan Bantul

> **Status:** ✅ **FULLY OPERATIONAL** — Production System (7 Juni 2026)  
> **Penanggung Jawab:** timitasib@gmail.com (IT/Teknis)  
> **Tujuan:** Dokumen ini mendefinisikan struktur kerja, kepemilikan email, pengelolaan workspace digital, dan alur operasional — agar seluruh kegiatan yayasan terdokumentasi, teraudit, dan tidak bergantung pada individu tertentu.

---

## 🎯 Filosofi & Prinsip Dasar

### **Mengapa Dokumen Ini Ada**

Yayasan ASIB berkembang dari lembaga kecil berbasis relawan menjadi organisasi dengan 3 unit pendidikan, puluhan pengurus, dan jangkauan donasi nasional. Pertumbuhan ini menuntut sistem pengelolaan yang:

1. **Tidak single point of failure** — semua akses, password, dan keputusan terdokumentasi
2. **Sesuai kemampuan yayasan** — prioritas solusi gratis/terjangkau (Cloudflare, Gmail, Sanity free tier)
3. **Strategis** — bisa scale up ke Google Workspace for Nonprofit jika nanti disetujui
4. **Teraudit** — setiap aktivitas tracked di Trello, documented di Drive

### **Realita vs Ideal**

**PENTING:** Dokumen ini mendokumentasikan **REALITA OPERASIONAL** saat ini, bukan kondisi ideal yang belum terimplementasi.

**Realita Saat Ini:**
- ✅ Email existing pengurus tetap dipakai (tidak ada migrasi)
- ✅ Cloudflare Email Routing untuk custom domain
- ✅ Single owner per email kritis (trusted person)
- ✅ Relawan pakai Gmail pribadi (bukan email yayasan)
- ✅ Semua kinerja dipantau di Trello

**Ideal (Future, Optional):**
- ⏳ Google Workspace for Nonprofit (jika ACC)
- ⏳ Email `@amalshalih.or.id` direct (bukan forwarding)
- ⏳ Shared Drive terstruktur penuh

**Prinsip:** Start with reality, evolve gradually, don't break what works.

### **Prinsip Dasar**

| Prinsip | Makna |
|---------|-------|
| **Single Owner per Email** | Setiap email kritis dipegang 1 orang terpercaya (bukan "tim") |
| **Recovery Chain** | timitasib@gmail.com recovery untuk semua akun kritis |
| **Auditability First** | Setiap tindakan tracked di Trello, documented di Drive |
| **Progressive Enhancement** | Mulai dari yang gratis & cukup, upgrade bertahap |
| **Separation of Concerns** | Admin/IT/Media punya fokus jelas, tidak overlap |
| **Document Reality** | Dokumentasikan apa yang ada, bukan apa yang seharusnya |

---

## 👥 Struktur Operasional (Single Owner Model)

### **Email Kritis — Single Owner (Trusted Person)**

| Email | Owner | Role | Responsibility | Recovery |
|-------|-------|------|----------------|----------|
| **amalshalih.insanbantul@gmail.com** | 1 orang (Admin) | Email Utama | - Administratif & Akuntabilitas<br>- Login SOSMED (IG, FB, TikTok, YT, Linktree, Google Business)<br>- Public-facing (pengaduan, kerjasama)<br>- Folder `Kantor ASIB` di Drive | timitasib@gmail.com |
| **timitasib@gmail.com** | 1 orang (IT) | IT/Teknis | - Recovery SEMUA akun<br>- IT/Teknis kritis (domain, hosting, SEO)<br>- Folder `IT/Teknis` di Drive<br>- Approve relawan AMMA<br>- Inspeksi `Workspace ASIB` | - |
| **media.amalshalih@gmail.com** | 1 orang (Pengurus Media) | Media & Publikasi | - Pengelolaan konten<br>- Folder `Media & Publikasi` di Drive<br>- Supervisi relawan media<br>- Login Google Photos | timitasib@gmail.com |

**Catatan Penting:**
- ✅ **Bukan "Tim"** — setiap email dipegang **1 orang terpercaya**
- ✅ **timitasib@gmail.com** recovery untuk email utama & media
- ✅ **2FA mandatory** dengan QR di owner + IT backup
- ✅ **Relawan** pakai Gmail pribadi (bukan email yayasan)

### **Email Routing (@amalshalih.or.id)**

| Email @amalshalih.or.id | Routing To | Owner | Purpose | Status |
|-------------------------|------------|-------|---------|--------|
| **info@** | timitasib@gmail.com | IT | Informasi umum, technical | ✅ Verified |
| **donasi@** | amalshalih.insanbantul@gmail.com | Admin | Konfirmasi donasi | ✅ Verified |
| **admin@** | amalshalih.insanbantul@gmail.com | Admin | Administrasi, surat | ✅ Verified |
| **humas@** | amalshalih.insanbantul@gmail.com | Admin | Public inquiries | ✅ Verified |
| **Catch-all** | timitasib@gmail.com | IT | Email tidak terdaftar | ✅ Verified |

**Key Decision (7 Juni 2026):**
- ✅ **humas@ → Admin** (bukan Media) untuk efisiensi administratif
- ✅ Media fokus ke content creation, tidak handle correspondence
- ✅ See: `docs/10-organisasi/humas-decision-analysis.md` untuk detail

---

## 🗂️ Google Drive Structure

### **Workspace ASIB (Root Folder)**

```
Workspace ASIB/ (Root - diinspeksi berkala oleh timitasib@gmail.com)
│
├── Kantor ASIB/ (Shortcut/Pintasan dari amalshalih.insanbantul@gmail.com)
│   ├── Administratif/
│   ├── Keuangan/
│   ├── Legal/
│   └── [Admin-managed folders]
│
├── Media & Publikasi/ (Dikelola media.amalshalih@gmail.com)
│   ├── Draft Konten/ (Google Docs)
│   ├── Dokumentasi/ (Foto & Video)
│   ├── Social Media/ (Content calendar, analytics)
│   └── [Media-managed folders]
│
├── IT/Teknis/ (Dikelola timitasib@gmail.com)
│   ├── Handover Teknis/
│   ├── SOP & Panduan/
│   ├── Informasi Sensitif/ (encrypted)
│   ├── Backup & Recovery/
│   └── [IT-managed folders]
│
└── [Folder lain sesuai kebutuhan]
```

**Security & Access:**
- **Workspace ASIB:** timitasib@gmail.com inspeksi berkala
- **Kantor ASIB:** Dikelola Admin, shortcut ke Workspace ASIB
- **Media & Publikasi:** Dikelola Media, relawan dapat view/comment access
- **IT/Teknis:** Dikelola IT, restricted access

### **Folder Organization Principles**

1. **Naming Convention:**
   ```
   Format: [Category]-[Subcategory]/
   Contoh: 10-Organisasi/, 20-SOP/, 30-Templates/, 40-IT-Teknis/
   ```

2. **File Naming:**
   ```
   Format: YYYY-MM-DD_Description_v[Version].ext
   Contoh: 2026-06-07_Notulen-Rapat_v1.0.pdf
   ```

3. **Access Levels:**
   - **Owner:** Full control (add, edit, delete, share)
   - **Editor:** Can edit & add (cannot delete folder or share)
   - **Commenter:** Can view & comment (cannot edit)
   - **Viewer:** Can view only

---

## 🔒 Security & Access Control

### **2FA Policy (Mandatory)**

| Akun | 2FA Required | QR Code Stored In | Recovery |
|------|--------------|-------------------|----------|
| amalshalih.insanbantul@gmail.com | ✅ Yes | - Owner's Google Auth<br>- Copy di timitasib@gmail.com's Auth | timitasib@gmail.com |
| timitasib@gmail.com | ✅ Yes | timitasib@gmail.com's Auth | - |
| media.amalshalih@gmail.com | ✅ Yes | - Owner's Google Auth<br>- Copy di timitasib@gmail.com's Auth | timitasib@gmail.com |
| All social media (IG, FB, TikTok, YT) | ✅ Yes | Same as email utama | timitasib@gmail.com |
| All critical services | ✅ Yes | respective owner + IT copy | timitasib@gmail.com |

**Policy:**
- QR code HARUS ada di 2 tempat: owner + IT backup
- Backup codes print 3 copies: IT, Pengurus, Bendahara
- Review 2FA status quarterly

### **Relawan AMMA (Approved Individual)**

**Model:**
- Relawan **TIDAK** dapat email yayasan
- Relawan pakai **Gmail pribadi**
- Approval ketat oleh **timitasib@gmail.com** (validasi)
- Supervision oleh **coordinator masing-masing** (kerja harian)
- Access granted per layanan (Sentry, Trello, Google Docs, dll)
- Status: "Relawan AMMA" setelah valid & approved

**Approval Process:**
1. Relawan submit request (form/WA)
2. IT validasi (background check, motivation)
3. If approved → IT setup access (Sentry, Trello, etc)
4. Coordinator supervise daily work
5. IT monitor & audit access

**Access Examples:**
- Relawan Media: Trello (Media board), Google Docs (draft), Canva
- Relawan IT: Sentry (view), GitHub (contributor), Trello (IT board)
- Relawan Admin: Google Docs (template), Trello (Admin board)

---

## 📋 Trello Integration (Primary Workflow Tracker)

### **Trello sebagai Single Source of Truth**

**All performance monitored di Trello:**
- Kantor ASIB (administratif tasks)
- IT/Teknis (infrastructure, security, development)
- Media & Publikasi (content, social media, documentation)
- Relawan AMMA (task assignment, progress tracking)

**Board Structure:**
```
Trello Boards:
├── Media & Publikasi (Admin: media.amalshalih@gmail.com)
│   ├── 📥 Ide Konten
│   ├── 📝 Dalam Pengerjaan
│   ├── 👀 Menunggu Review
│   ├── ✅ Approved - Siap Schedule
│   ├── 📅 Scheduled
│   └── 📢 Live
├── IT & Teknis (Admin: timitasib@gmail.com)
│   ├── 📥 Requests
│   ├── 📝 In Progress
│   ├── 👀 Review
│   ├── ✅ Done
│   └── 📚 Documentation
├── Program & Kegiatan (Admin: [Pengurus])
│   ├── 📥 Ide Program
│   ├── 📝 Planning
│   ├── 📢 Active
│   ├── ✅ Completed
│   └── 📊 Reports
└── Pengurus (Admin: [Ketua])
    ├── 📋 Strategic Plans
    ├── 📊 Monitoring
    └── ✅ Decisions
```

**SOP Compatibility:**
- ✅ Semua SOP compatible dengan Trello workflow
- ✅ Dynamic workflow (bisa jalan tanpa Trello, tapi prioritize Trello)
- ✅ Chronological & structured tracking
- ✅ All performance auditable via Trello history

---

## 🔄 Operational Workflows

### **Email Management Workflow**

```
1. Email masuk ke @amalshalih.or.id
   ↓
2. Cloudflare forward ke Gmail owner
   ↓
3. Gmail filter auto-label per alamat
   ↓
4. Owner process email
   ↓
5. Reply via "Send Mail As" (SMTP Gmail)
   ↓
6. Track di Trello (jika task)
```

**SLA (Service Level Agreement):**
- info@: 24 hours (IT)
- donasi@: 24 hours (Admin)
- admin@: 24 hours (Admin)
- humas@: 24 hours (Admin)

### **Content Creation Workflow (Media)**

```
1. Ide → Trello card (📥 Ide Konten)
   ↓
2. Draft → Google Docs (Media & Publikasi folder)
   ↓
3. Move card to 📝 Dalam Pengerjaan
   ↓
4. Koordinator review → 👀 Menunggu Review
   ↓
5. Approve → ✅ Approved - Siap Schedule
   ↓
6. Schedule → 📅 Scheduled (Meta Business Suite)
   ↓
7. Publish → 📢 Live
   ↓
8. Track analytics → Update card
```

### **Relawan Onboarding Workflow**

```
1. Submit application (form/WA)
   ↓
2. IT validasi (background, motivation)
   ↓
3. If approved → IT setup access (Sentry, Trello, etc)
   ↓
4. Coordinator assign mentor
   ↓
5. Training & onboarding
   ↓
6. First task assignment (Trello)
   ↓
7. Review & feedback
   ↓
8. Status: "Relawan AMMA" (active)
```

---

## 📊 Current Reality (Honest Assessment)

### **What Works Well ✅**

- ✅ Email routing stable & verified
- ✅ Single owner model clear accountability
- ✅ Recovery chain established
- ✅ Trello tracking all activities
- ✅ Drive structure organized
- ✅ 2FA mandatory & implemented

### **Current Challenges ⚠️**

| Challenge | Impact | Owner | Status |
|-----------|--------|-------|--------|
| **Email utama overload** | Single point of failure, burnout risk | Admin | 🔴 Critical |
| **IT role confusion** | Technical vs Content blur, nothing done well | IT | 🔴 Critical |
| **No content specialist** | Content strategy non-existent | Media | 🔴 Critical |
| **Role separation not socialized** | Public confusion, wrong expectations | Pengurus | 🟡 High |
| **Relawan capability gap** | Cannot handle structured content | Media + IT | 🟡 High |
| **All sosmed on one email** | Security risk (but stable for now) | Admin + IT | 🟡 Medium |

### **Role Separation Status**

**Current Public Perception:**
- "Email ASIB = amalshalih.insanbantul@gmail.com" (CORRECT)
- "timitasib@gmail.com = IT, dokumentasi, media, website, SEO, domain, hosting" (WRONG - terlalu banyak!)
- Role separation **BELUM** tersosialisasikan ke yayasan
- Orang yayasan **TIDAK TAHU** ada pemisahan Admin/IT/Media

**Target State:**
- Admin = Administratif & Akuntabilitas
- IT = Critical infrastructure only (domain, hosting, recovery, security)
- Media = Content strategy, creation, distribution

**Gap:** Perlu sosialisasi & change management

---

## 🛣️ Strategic Roadmap

### **Phase 1: Stabilization (COMPLETED ✅)**

- [x] Setup Cloudflare Email Routing
- [x] Verify all email addresses
- [x] Setup 2FA for all critical accounts
- [x] Create Workspace ASIB structure
- [x] Setup Trello boards
- [x] Document SOPs

### **Phase 2: Optimization (CURRENT 🔄)**

- [ ] Sosialisasi role separation ke yayasan
- [ ] Train content specialist (Media)
- [ ] Refine relawan onboarding process
- [ ] Implement Trello Power-ups
- [ ] Create AI-Trello integration (OpenKB)
- [ ] Document "current reality" honestly

### **Phase 3: Scale Up (OPTIONAL ⏳)**

- [ ] Apply Google for Nonprofit (if beneficial)
- [ ] Migrate to `@amalshalih.or.id` direct emails (if ACC)
- [ ] Implement Google Shared Drive
- [ ] Advanced Trello automation
- [ ] External audit (annual)

**Note:** Phase 3 is OPTIONAL. Current system (Cloudflare + Gmail) sudah efektif & bisa digunakan long-term.

---

## 📚 Related Documentation

| Document | Purpose | Location |
|----------|---------|----------|
| **Email System** | Email routing setup & management | `.openkb/email-system.md` |
| **Struktur & Role** | Org structure, contacts, access matrix | `docs/10-organisasi/struktur-dan-role.md` |
| **humas@ Decision** | Trade-off analysis for humas@ routing | `docs/10-organisasi/humas-decision-analysis.md` |
| **Security Guidelines** | 2FA, passwords, access control | `docs/40-it-teknis/security.md` |
| **Credentials** | Password manager, sharing | `docs/40-it-teknis/credentials.md` |
| **SOPs** | Operational procedures | `docs/20-sop/` |
| **Templates** | Reusable templates | `docs/30-templates/` |

---

## 📞 Contact & Escalation

| Issue | Contact | Escalation |
|-------|---------|------------|
| **Email Routing** | timitasib@gmail.com | Pengurus |
| **Access Request** | timitasib@gmail.com | Koordinator |
| **Security Issue** | timitasib@gmail.com | Pengurus |
| **Content Approval** | media.amalshalih@gmail.com | Pengurus |
| **Administratif** | amalshalih.insanbantul@gmail.com | Pengurus |

---

**Last Updated:** 7 Juni 2026  
**Status:** ✅ Fully Operational  
**Maintained by:** timitasib@gmail.com (IT/Teknis)  
**Next Review:** 7 Desember 2026

---

*"Sistem yang baik bukan yang sempurna, tapi yang bisa berjalan stabil, terdokumentasi, dan tidak bergantung pada satu orang."*