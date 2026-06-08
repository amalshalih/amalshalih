# 📁 Document Storage & Retention Policy

> Kebijakan penyimpanan, retensi, dan pemusnahan dokumen untuk Yayasan Amal Shalih Insan Bantul

**Last Updated:** 7 Juni 2026  
**Status:** 🟢 Active  
**Applies to:** Semua dokumen fisik & digital, semua anggota & relawan  
**Compliance:** UU PDP No. 27 Tahun 2022, Standar Akuntansi Keuangan

---

## 📋 Daftar Isi

1. [Tujuan & Scope](#tujuan--scope)
2. [Klasifikasi Dokumen](#klasifikasi-dokumen)
3. [Storage Structure](#storage-structure)
4. [Retention Periods](#retention-periods)
5. [Storage Guidelines](#storage-guidelines)
6. [Access Control](#access-control)
7. [Backup & Recovery](#backup--recovery)
8. [Document Disposal](#document-disposal)
9. [Compliance & Audit](#compliance--audit)

---

## 🎯 Tujuan & Scope

### **Tujuan Policy:**

1. **Compliance** - Memenuhi requirements regulasi (UU PDP, tax law, foundation law)
2. **Organization** - Struktur penyimpanan yang konsisten & mudah diakses
3. **Security** - Melindungi dokumen sensitif dari unauthorized access
4. **Efficiency** - Mudah find & retrieve dokumen yang dibutuhkan
5. **Risk Management** - Reduce risk dari loss, damage, atau breach
6. **Business Continuity** - Ensure critical documents available saat dibutuhkan

### **Scope:**

**Dokumen Fisik:**
```
✅ Legal documents (akta, SK, NIB, NPWP)
✅ Financial records (kwitansi, invoice, bank statements)
✅ Contracts & agreements
✅ Meeting minutes (printed)
✅ Correspondence (surat resmi)
✅ Photos (printed)
```

**Dokumen Digital:**
```
✅ Google Drive files (docs, sheets, slides)
✅ Email attachments
✅ Website content
✅ Social media assets
✅ Database records
✅ Backups
```

**Media:**
```
✅ Photos (digital & printed)
✅ Videos
✅ Audio recordings
```

---

## 📊 Klasifikasi Dokumen

### **Level 1: Public (Tidak Ada Restriction)**

**Examples:**
```
- Website content
- Social media posts
- Press releases
- Public reports (laporan bulanan/tahunan)
- Marketing materials
```

**Storage:**
```
- Website public folders
- Social media platforms
- Google Drive: Public folder (anyone with link can view)
```

**Access:**
```
- No restrictions
- Can be shared freely
- No NDA required
```

**Retention:**
```
- Permanent (for historical value)
- Or until outdated/irrelevant
```

### **Level 2: Internal (Restricted to Members)**

**Examples:**
```
- SOPs & procedures
- Meeting minutes (internal)
- Work plans
- Internal communications
- Training materials
- Process documentation
```

**Storage:**
```
- Google Drive: Shared/Internal folder
- Access: All members & relawan
- Permission: View/comment (not edit)
```

**Access:**
```
- Members & active relawan only
- NDA recommended
- Cannot share externally
```

**Retention:**
```
- Active + 3 years
- Then archive or delete
```

### **Level 3: Confidential (Need-to-Know)**

**Examples:**
```
- Donatur database (contact info, donation history)
- Financial records (detailed transactions)
- Relawan records (personal data)
- Performance reviews
- Strategic plans (belum publik)
- Vendor contracts
```

**Storage:**
```
- Google Drive: Confidential folder
- Access: Authorized personnel only
- Permission: View (no download/edit)
- Encryption: Recommended for sensitive data
```

**Access:**
```
- Need-to-know basis
- Role-based access
- Access log maintained
- NDA required
```

**Retention:**
```
- Sesuai retention schedule (lihat section 4)
- Typically 3-7 years
- Secure deletion after retention
```

### **Level 4: Highly Confidential (Critical)**

**Examples:**
```
- Credentials (passwords, API keys, tokens)
- 2FA backup codes
- Bank account details
- Legal documents (originals)
- Audit reports
- Investigation files
- Security incident reports
```

**Storage:**
```
- Password manager (Bitwarden) untuk credentials
- Encrypted storage untuk files
- Physical safe untuk originals
- Access: IT + Pengurus only
```

**Access:**
```
- Explicit authorization required
- Dual control (2 people for critical access)
- Access log mandatory
- NDA + background check
```

**Retention:**
```
- Until rotated/replaced
- Then secure destruction
- Archive historical credentials (encrypted)
```

---

## 🗂️ Storage Structure

### **Google Drive Structure:**

```
My Drive/
│
├── 📁 00-Public/                      # Public access
│   ├── Marketing Materials/
│   ├── Public Reports/
│   └── Press Releases/
│
├── 📁 10-Internal/                    # All members
│   ├── SOPs/
│   │   ├── 10-Organisasi/
│   │   ├── 20-SOP/
│   │   ├── 30-Templates/
│   │   └── 40-IT-Teknis/
│   ├── Meeting Minutes/
│   │   ├── 2026/
│   │   └── 2027/
│   ├── Training Materials/
│   └── Work Plans/
│
├── 📁 20-Confidential/                # Authorized only
│   ├── Keuangan/
│   │   ├── Donasi Masuk/
│   │   ├── Donasi Disalurkan/
│   │   ├── Bank Statements/
│   │   ├── Kwitansi/
│   │   ├── Laporan Bulanan/
│   │   └── Audit/
│   ├── HR/
│   │   ├── Database Relawan/
│   │   ├── Performance Reviews/
│   │   └── Onboarding/
│   ├── Donatur/
│   │   ├── Database Donatur/
│   │   ├── Communication Logs/
│   │   └── Major Donors/
│   └── Legal/
│       ├── Contracts/
│       ├── Compliance/
│       └── Intellectual Property/
│
├── 📁 30-IT-Teknis/                   # IT team only
│   ├── Infrastructure/
│   ├── Security/
│   ├── Backups/
│   ├── Credentials (encrypted)/
│   └── Documentation/
│
├── 📁 40-Media-Publikasi/             # Media team
│   ├── Photos/
│   │   ├── 2026/
│   │   │   ├── 01-Januari/
│   │   │   └── ...
│   │   └── 2027/
│   ├── Videos/
│   ├── Graphics/
│   ├── Social Media/
│   └── Brand Assets/
│
├── 📁 50-Archive/                     # Historical documents
│   ├── 2024/
│   ├── 2025/
│   └── 2026/
│
└── 📁 99-Templates/                   # Reusable templates
    ├── Documents/
    ├── Spreadsheets/
    ├── Presentations/
    └── Forms/
```

### **Folder Naming Convention:**

```
Format: [Category]-[Subcategory]/

Examples:
✅ 10-Organisasi/
✅ 20-SOP/
✅ 30-Templates/
✅ Keuangan-Donasi-Masuk/
✅ HR-Relawan-Database/
❌ keuangan/ (lowercase, no structure)
❌ Donasi Masuk 2026 Baru/ (inconsistent)
```

### **File Naming Convention:**

```
Format: YYYY-MM-DD_Description_Version.ext

Examples:
✅ 2026-06-07_Laporan-Bulanan-Juni_v1.0.pdf
✅ 2026-06-07_Notulen-Rapat-Pengurus_v2.0.docx
✅ 2026-06-07_Kwitansi-DON-20260607-001.pdf
❌ laporan.pdf (no date, vague)
❌ final_final_revised.pdf (unprofessional)
```

### **Version Control:**

```
Format: v[major].[minor]

Examples:
- v1.0 = Initial version
- v1.1 = Minor revision
- v2.0 = Major revision

Old versions:
- Keep last 3 versions
- Archive or delete older versions
- Change log in document properties
```

---

## 📅 Retention Periods

### **Legal & Corporate Documents:**

| Document Type | Retention Period | Storage | Disposal Method |
|---------------|------------------|---------|-----------------|
| **Akta Notaris (Original)** | Permanent | Physical safe + scanned digital | Never dispose |
| **SK Kemenkumham** | Permanent | Physical safe + scanned | Never dispose |
| **NIB** | Permanent | Physical safe + scanned | Never dispose |
| **NPWP** | Permanent | Physical safe + scanned | Never dispose |
| **Perubahan AD/ART** | Permanent | Physical + digital | Never dispose |
| **Surat Izin Usaha** | Active + 2 years after expiry | Physical + digital | Shred + secure delete |

### **Financial Documents:**

| Document Type | Retention Period | Storage | Disposal Method |
|---------------|------------------|---------|-----------------|
| **Laporan Keuangan Tahunan** | 10 years | Digital (encrypted) + physical | Secure delete + shred |
| **Laporan Keuangan Bulanan** | 7 years | Digital + physical | Secure delete + shred |
| **Kwitansi Donasi** | 7 years | Digital (scanned) + physical | Secure delete + shred |
| **Bank Statements** | 7 years | Digital (PDF) | Secure delete |
| **Bukti Transfer** | 7 years | Digital (scanned) | Secure delete |
| **Invoice & Billing** | 7 years | Digital | Secure delete |
| **Tax Returns (SPT)** | 10 years | Digital + physical | Secure delete + shred |
| **Audit Reports** | 10 years | Digital + physical | Secure delete + shred |
| **Budget Plans** | 3 years after fiscal year end | Digital | Secure delete |

### **Donatur Records:**

| Document Type | Retention Period | Storage | Disposal Method |
|---------------|------------------|---------|-----------------|
| **Database Donatur (Active)** | Active + 3 years inactive | Digital (encrypted) | Anonymize or secure delete |
| **Donation History** | 7 years | Digital (encrypted) | Anonymize or secure delete |
| **Donatur Correspondence** | 3 years | Digital | Secure delete |
| **Major Donor Agreements** | 7 years after agreement end | Digital + physical | Secure delete + shred |
| **Pledge Records** | Until fulfilled + 7 years | Digital | Secure delete |

### **Relawan Records:**

| Document Type | Retention Period | Storage | Disposal Method |
|---------------|------------------|---------|-----------------|
| **Application Forms** | Active + 3 years | Digital | Secure delete |
| **KTP Copy** | Active + 1 year | Digital (encrypted) | Secure delete |
| **Performance Reviews** | Active + 3 years | Digital | Secure delete |
| **Training Records** | Active + 5 years | Digital | Secure delete |
| **Offboarding Documents** | 3 years | Digital | Secure delete |
| **NDA Signed** | Active + 3 years | Digital + physical | Secure delete + shred |

### **Program & Kegiatan:**

| Document Type | Retention Period | Storage | Disposal Method |
|---------------|------------------|---------|-----------------|
| **Proposal Kegiatan** | 3 years after completion | Digital | Secure delete |
| **Laporan Kegiatan** | 5 years | Digital + photos | Secure delete |
| **Beneficiary Data** | 5 years | Digital (encrypted) | Anonymize or secure delete |
| **Event Photos/Videos** | Permanent (for historical value) | Digital (Google Photos) | Archive (don't delete) |
| **Testimonials** | 5 years | Digital | Secure delete |
| **Impact Reports** | Permanent | Digital | Archive |

### **Legal & Contracts:**

| Document Type | Retention Period | Storage | Disposal Method |
|---------------|------------------|---------|-----------------|
| **Vendor Contracts** | Life of contract + 7 years | Digital + physical | Secure delete + shred |
| **Partnership Agreements** | Life of agreement + 7 years | Digital + physical | Secure delete + shred |
| **Service Agreements** | Life of agreement + 3 years | Digital | Secure delete |
| **Lease Agreements** | Life of lease + 7 years | Digital + physical | Secure delete + shred |
| **Insurance Policies** | Active + 7 years | Digital + physical | Secure delete + shred |

### **Communications:**

| Document Type | Retention Period | Storage | Disposal Method |
|---------------|------------------|---------|-----------------|
| **Email (General)** | 3 years | Google Mail | Delete from server |
| **Email (Legal/Financial)** | 7 years | Google Mail + archive | Archive then delete |
| **WhatsApp Messages** | Until conversation ends | WhatsApp (encrypted) | Delete when no longer needed |
| **Meeting Minutes** | 5 years | Digital | Secure delete |
| **Decision Logs** | Permanent | Digital | Archive |

### **IT & Security:**

| Document Type | Retention Period | Storage | Disposal Method |
|---------------|------------------|---------|-----------------|
| **Credentials (Active)** | Until rotated | Bitwarden (encrypted) | Auto-delete when replaced |
| **Credentials (Historical)** | 7 years | Encrypted archive | Secure delete |
| **2FA Backup Codes (Used)** | After use | Physical (shredded) | Shred immediately |
| **Access Logs** | 1 year | Digital (encrypted) | Secure delete |
| **Security Incident Reports** | 7 years | Digital (encrypted) | Secure delete |
| **Backup Files** | 3 generations (weekly/monthly/yearly) | External HDD + cloud | Overwrite oldest |
| **System Configurations** | Current + 1 previous | Digital | Secure delete |

### **Marketing & Media:**

| Document Type | Retention Period | Storage | Disposal Method |
|---------------|------------------|---------|-----------------|
| **Social Media Posts** | Permanent (unless outdated) | Platform + Google Drive | Archive (don't delete) |
| **Marketing Materials** | 3 years after campaign end | Digital | Secure delete |
| **Brand Assets** | Permanent | Digital | Archive |
| **Press Releases** | Permanent | Digital + website | Archive |
| **Media Coverage** | Permanent | Digital (scanned) | Archive |

---

## 💾 Storage Guidelines

### **Digital Storage Best Practices:**

**File Formats:**
```
✅ Documents: PDF/A (archival), DOCX (editable)
✅ Spreadsheets: XLSX, CSV (for data export)
✅ Presentations: PDF (view), PPTX (editable)
✅ Images: PNG (graphics), JPEG (photos), WebP (web)
✅ Videos: MP4 (H.264 codec)
✅ Audio: MP3, WAV
```

**File Size Limits:**
```
- Google Drive: Max 5 TB per file (practical: <1 GB)
- Email attachments: Max 25 MB (use Drive link for larger)
- Website uploads: Max 5 MB per file
```

**Organization:**
```
✅ Consistent folder structure
✅ Clear file names (YYYY-MM-DD_Description)
✅ Version control (v1.0, v1.1, v2.0)
✅ Regular cleanup (quarterly)
❌ Deep nesting (max 5 levels)
❌ Duplicate files (use shortcuts/links)
❌ "Misc" or "Temporary" folders (temporary becomes permanent)
```

### **Physical Storage Best Practices:**

**Storage Location:**
```
✅ Dedicated filing cabinet (locked)
✅ Climate-controlled room (no humidity, direct sunlight)
✅ Fire-resistant safe for critical documents
✅ Off the floor (flood protection)
✅ Pest control measures
```

**Organization:**
```
✅ Labeled folders (color-coded by category)
✅ Index system (digital or card catalog)
✅ Chronological order within folders
✅ Cross-reference for related documents
```

**Security:**
```
✅ Locked cabinet (key controlled)
✅ Access log (who accessed what)
✅ CCTV for storage area (optional)
✅ Regular inventory checks
```

### **Hybrid Storage (Physical + Digital):**

**When to Keep Both:**
```
✅ Legal documents (originals + scanned copies)
✅ Financial records (originals for audit, digital for daily use)
✅ Contracts (signed originals + digital copies)
✅ Photos (printed for display, digital for backup)
```

**Sync Process:**
```
1. Scan physical document (300 DPI minimum)
2. Save as PDF/A (archival format)
3. Name file per convention (YYYY-MM-DD_Description)
4. Upload to appropriate Google Drive folder
5. Mark physical file with "Scanned: [Date]"
6. Store physical in designated location
```

---

## 🔐 Access Control

### **Access Levels:**

| Level | Description | Who | Examples |
|-------|-------------|-----|----------|
| **Level 1: Public** | Anyone can access | Everyone | Website content, public reports |
| **Level 2: Internal** | Members & relawan only | All members | SOPs, meeting minutes, templates |
| **Level 3: Confidential** | Need-to-know basis | Authorized roles | Financial data, donatur database |
| **Level 4: Restricted** | Explicit authorization only | IT, Pengurus | Credentials, legal documents |

### **Access Request Process:**

```
1. Request via Trello card or email
2.Approval by coordinator/manager
3. IT grants access (within 24 hours)
4. User confirms access working
5. Access logged in spreadsheet
6. Quarterly review
```

### **Access Review:**

**Frequency:** Quarterly (every 3 months)

**Checklist:**
```
[ ] Review all Level 3 & 4 access
[ ] Verify users still need access
[ ] Remove access for inactive users
[ ] Update access matrix
[ ] Document review results
[ ] Report to Pengurus
```

---

## 💾 Backup & Recovery

### **Backup Strategy:**

**3-2-1 Rule:**
```
3 copies of data
2 different media types
1 off-site copy
```

**Backup Schedule:**
```
Daily:   Google Drive (automatic sync)
Weekly:  cPanel backup (website)
Monthly: Google Takeout + external HDD
Quarterly: Full backup test (restore verification)
Annually: Disaster recovery drill
```

**Backup Locations:**
```
Primary:   Google Drive (cloud)
Secondary: External HDD (local)
Tertiary:  Encrypted cloud backup (off-site)
```

### **Recovery Procedures:**

**Priority Order:**
```
1. Credentials (Bitwarden backup)
2. Email (Google recovery)
3. Financial data (Drive backup)
4. Website (cPanel backup)
5. Documentation (Drive backup)
6. Archive (HDD backup)
```

**Testing:**
```
- Monthly: Random file restore test
- Quarterly: Full system restore test
- Annually: Disaster recovery drill
```

---

## 🗑️ Document Disposal

### **Digital Disposal:**

**Secure Delete Process:**
```
1. Identify documents past retention period
2. Verify no legal hold or ongoing need
3. Move to "To Delete" folder
4. Review by IT + Pengurus
5. Use secure delete tool (not just trash)
6. Empty trash/recycle bin
7. Document deletion in log
```

**Tools:**
```
- Windows: File Shredder, Eraser
- Mac: Permanent Eraser, Shred
- Linux: shred command
- Google Drive: Remove + empty trash
```

### **Physical Disposal:**

**Shredding Process:**
```
1. Identify documents past retention
2. Verify no legal hold
3. Place in secure shredding bin
4. Shred (cross-cut recommended)
5. Dispose of shredded material securely
6. Document in disposal log
```

**Shredder Types:**
```
✅ Cross-cut (recommended) - 3x10mm particles
✅ Micro-cut (best) - 2x3mm particles
❌ Strip-cut (not secure) - long strips
```

**Professional Shredding Service:**
```
- For large volumes
- Certificate of destruction provided
- NAID certified recommended
- Cost: Rp 500-1000 per kg
```

### **Disposal Log:**

```markdown
| Date | Document Type | Period Covered | Quantity | Method | Approved By | Witness |
|------|---------------|----------------|----------|--------|-------------|---------|
| 2026-07-15 | Kwitansi Donasi | 2019 | 5 boxes | Shred | [Name] | [Name] |
| 2026-07-15 | Email Archive | 2019-2020 | 2 GB | Secure Delete | [Name] | [Name] |
```

---

## ✅ Compliance & Audit

### **Internal Audit:**

**Frequency:** Annual

**Scope:**
```
[ ] Retention compliance (are we deleting on time?)
[ ] Access control (who has access to what?)
[ ] Backup verification (can we restore?)
[ ] Security measures (encryption, 2FA, etc)
[ ] Physical security (locks, safes, CCTV)
[ ] Documentation (is policy up to date?)
```

**Process:**
```
1. IT prepares audit report
2. Pengurus reviews
3. Identify gaps/issues
4. Create action plan
5. Implement improvements
6. Follow-up audit (next year)
```

### **External Audit:**

**When Required:**
```
- Annual financial audit (mandatory for foundations)
- Regulatory inspection (Kemenkumham, Kemenag)
- Donor audit (for major grants)
- Security incident (forensic audit)
```

**Preparation:**
```
- Maintain organized records
- Keep audit trail (who accessed what when)
- Document all disposals
- Have retention policy readily available
- Train staff on compliance
```

### **Non-Compliance Consequences:**

**Internal:**
```
- Warning (first offense)
- Access suspension (repeated offense)
- Termination (serious violation)
- Legal action (if criminal)
```

**External (Regulatory):**
```
- Fines (UU PDP violations: up to 2% annual revenue or Rp 2M)
- Suspension of activities
- Criminal liability (for serious data breaches)
- Reputation damage
```

---

## 📞 Contact & Support

| Issue | Contact |
|-------|---------|
| **Access Request** | IT: timitasib@gmail.com |
| **Storage Questions** | IT: timitasib@gmail.com |
| **Disposal Authorization** | Pengurus: [Email Pengurus] |
| **Legal/Compliance** | legal@amalshalih.or.id |
| **Security Incident** | security@amalshalih.or.id |

---

**Policy ini ditinjau dan diupdate secara berkala.**

**Last reviewed:** 7 Juni 2026  
**Next review:** 7 Juni 2027  
**Approved by:** Pengurus Yayasan Amal Shalih Insan Bantul

---

*Proper document management is a form of amanah. Protect what needs protection, share what should be shared, and dispose what has served its purpose.*