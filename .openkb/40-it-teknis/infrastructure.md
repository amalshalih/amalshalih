# 🖥️ IT Infrastructure & Technical Documentation

> Dokumentasi lengkap infrastruktur digital, security, backup, dan credentials management Yayasan ASIB

**Last Updated:** 7 Juni 2026  
**Status:** 🟢 Active  
**Applies to:** Tim IT, Pengurus, Semua anggota dengan akses teknis

---

## 📋 Daftar Isi

1. [Infrastructure Overview](#infrastructure-overview)
2. [Domain & Hosting](#domain--hosting)
3. [Email System](#email-system)
4. [Website & Tech Stack](#website--tech-stack)
5. [Third-party Services](#third-party-services)
6. [Security Guidelines](#security-guidelines)
7. [Backup & Recovery](#backup--recovery)
8. [Credentials Management](#credentials-management)
9. [Monitoring & Maintenance](#monitoring--maintenance)

---

## 🏗️ Infrastructure Overview

### **Architecture Diagram:**

```
┌─────────────────────────────────────────────────────────────┐
│                    YAYASAN ASIB INFRASTRUCTURE               │
└─────────────────────────────────────────────────────────────┘

┌──────────────┐
│   DOMAIN     │
│ amalshalih   │
│ .or.id       │
└──────┬───────┘
       │
       │ DNS Management
       ▼
┌──────────────┐     ┌──────────────────┐
│  Cloudflare  │────▶│  Email Routing   │
│   DNS + CDN  │     │  (Free Plan)     │
└──────┬───────┘     └──────────────────┘
       │
       │ Proxy + SSL
       ▼
┌──────────────┐
│   Hosting    │
│ (Niagahoster)│
│ - Website    │
│ - cPanel     │
└──────────────┘

┌──────────────────────────────────────────────────────────────┐
│                    THIRD-PARTY SERVICES                       │
├──────────────────────────────────────────────────────────────┤
│  Google Workspace (Free Nonprofit)                           │
│  ├── Gmail (Custom Domain)                                   │
│  ├── Google Drive (15GB)                                     │
│  ├── Google Calendar                                         │
│  └── Google Meet                                             │
├──────────────────────────────────────────────────────────────┤
│  Trello (Free)                                               │
│  └── Workflow Management Boards                              │
├──────────────────────────────────────────────────────────────┤
│  Sanity.io (Free Tier)                                       │
│  └── CMS for Website Content                                 │
├──────────────────────────────────────────────────────────────┤
│  GitHub (Free)                                               │
│  └── Code Repository & Version Control                       │
├──────────────────────────────────────────────────────────────┤
│  Social Media                                                │
│  ├── Instagram (@amalshalihinsan)                            │
│  ├── Facebook (@amalshalihinsanbantul)                       │
│  ├── TikTok (@yayasan.amalshalihinsan)                       │
│  └── YouTube (@amalshalihinsanbantul9997)                    │
└──────────────────────────────────────────────────────────────┘
```

### **Service Ownership Matrix:**

| Service | Primary Owner | Recovery Access | Billing |
|---------|---------------|-----------------|---------|
| **Domain (.or.id)** | IT (timitasib@gmail.com) | Pengurus Ketua | Free (PANDI nonprofit) |
| **Cloudflare DNS** | IT | Pengurus Ketua | Free |
| **Hosting (Niagahoster)** | IT | Pengurus Ketua | Paid (annual) |
| **Google Workspace** | IT | Pengurus Ketua | Free (Nonprofit) |
| **Email Routing** | IT | Pengurus Ketua | Free |
| **Trello** | IT (Admin) | Pengurus | Free |
| **Sanity.io** | IT | - | Free Tier |
| **GitHub** | IT | - | Free |
| **Social Media** | Admin (Login) | IT (Recovery) | Free |

### **Access Levels:**

| Role | Domain | Hosting | Google | Trello | Social Media |
|------|--------|---------|--------|--------|--------------|
| **IT** | ✅ Full | ✅ Full | ✅ Full | ✅ Admin | ✅ Recovery |
| **Pengurus Ketua** | ✅ View | ✅ View | ✅ View | ✅ Admin | ❌ |
| **Admin** | ❌ | ❌ | ✅ Limited | ✅ Member | ✅ Full |
| **Koordinator Media** | ❌ | ❌ | ✅ Limited | ✅ Admin (Media) | ✅ Full |
| **Relawan** | ❌ | ❌ | ✅ Limited (folder) | ✅ Member (board) | ❌ |

---

## 🌐 Domain & Hosting

### **1. Domain: amalshalih.or.id**

**Registrar:** PANDI (Pengelola Nama Domain Internet Indonesia)  
**Type:** .or.id (Organisasi)  
**Status:** Active  
**Expiry:** [Check di PANDI dashboard]

**Registration Requirements (.or.id):**
- KTP Pengurus/Penanggung Jawab
- Akta Notaris Yayasan
- Surat Kuasa (jika dikuasakan)

**DNS Management:** Cloudflare (delegated from PANDI)

**Nameservers:**
```
ns1.cloudflare.com
ns2.cloudflare.com
```

**DNS Records (Cloudflare):**

```
Type    | Name                | Value                    | Proxy
--------|---------------------|--------------------------|-------
A       | @                   | [Hosting IP]             | ✅ Proxied
A       | www                 | [Hosting IP]             | ✅ Proxied
CNAME   | mail                | ghs.googlehosted.com     | ❌ DNS Only
MX      | @                   | ASPMX.L.GOOGLE.COM       | ❌ DNS Only
TXT     | @                   | google-site-verification | ❌ DNS Only
TXT     | @                   | v=spf1 include:_spf.google.com ~all | ❌
CNAME   | _dmarc              | v=DMARC1; p=none         | ❌
```

**Renewal Process:**
- Reminder: 30 hari sebelum expiry
- PIC: IT + Pengurus Ketua
- Cost: ~Rp 50.000/tahun (nonprofit discount)
- Documents: Same as registration

### **2. Hosting: Niagahoster**

**Plan:** [Check plan details]  
**Billing:** Annual  
**Next Billing:** [Date]

**Features:**
- cPanel access
- Unlimited bandwidth
- [X] GB SSD storage
- Free SSL (Let's Encrypt)
- Daily backup (optional)
- 1-click WordPress install

**cPanel Access:**
- URL: `https://amalshalih.or.id/cpanel`
- Username: [Username di password manager]
- Password: [Password di password manager]
- 2FA: ✅ Enabled (Google Auth)

**Main Websites:**
1. **Main Website:** `amalshalih.or.id` (Astro + Sanity)
2. **(Future) Landing Pages:** `campaign.amalshalih.or.id` (subdomain)

**File Structure (cPanel File Manager):**
```
/home/amalssal/public_html/
├── index.php (if WordPress exists)
├── wp-content/ (if WordPress)
├── astro/ (new Astro build)
├── wp-config.php (if WordPress)
└── .htaccess
```

**Database:**
- phpMyAdmin: `https://amalshalih.or.id/phpmyadmin`
- Database name: [Name di password manager]
- Username: [Username di password manager]
- Password: [Password di password manager]

**Backup Strategy:**
- **cPanel Backup:** Weekly (automatic, if enabled)
- **Manual Backup:** Before major changes
- **Off-site Backup:** Download backup ke Google Drive IT folder

**Monitoring:**
- Uptime: Manual check (or setup UptimeRobot free tier)
- Disk usage: Check monthly (cPanel → Metrics)
- Bandwidth: Check monthly (cPanel → Metrics)

---

## 📧 Email System

### **Current Setup:**

**Primary Email Provider:** Cloudflare Email Routing (Free) + Google Workspace (Free Nonprofit)

**Email Accounts:**

| Email | Purpose | Login | 2FA | Recovery | Status |
|-------|---------|-------|-----|----------|--------|
| **amalshalih.insanbantul@gmail.com** | Public-facing, social media login, admin, donasi, humas | ✅ Yes | ✅ Google Auth | timitasib@gmail.com | ✅ Verified |
| **timitasib@gmail.com** | IT, recovery, technical | ✅ Yes | ✅ Google Auth | - | ✅ Verified |
| **media.amalshalih@gmail.com** | Media coordinator | ✅ Yes | ✅ Google Auth | timitasib@gmail.com | ✅ Verified |
| **admin@amalshalih.or.id** | Admin (forwarding) | ❌ Forwarding | N/A | N/A | ✅ Verified |
| **humas@amalshalih.or.id** | Public inquiries (forwarding to Admin) | ❌ Forwarding | N/A | N/A | ✅ Verified |
| **donasi@amalshalih.or.id** | Donation inquiries (forwarding) | ❌ Forwarding | N/A | N/A | ✅ Verified |
| **it@amalshalih.or.id** | IT support (forwarding) | ❌ Forwarding | N/A | N/A | ✅ Verified |
| **info@amalshalih.or.id** | General info (forwarding) | ❌ Forwarding | N/A | N/A | ✅ Verified |

**Status Update 7 Juni 2026:** ✅ All email routing verified & active

### **Cloudflare Email Routing Setup:**

**Purpose:** Forward custom domain emails to Gmail accounts

**Configuration:**
```
Destination Address: amalshalih.insanbantul@gmail.com (verified)
                     timitasib@gmail.com (verified)
                     media.amalshalih@gmail.com (verified)

Routing Rules:
- admin@amalshalih.or.id       → amalshalih.insanbantul@gmail.com (Admin) ✅ Verified
- humas@amalshalih.or.id       → amalshalih.insanbantul@gmail.com (Admin) ✅ Verified
- donasi@amalshalih.or.id      → amalshalih.insanbantul@gmail.com (Admin) ✅ Verified
- it@amalshalih.or.id          → timitasib@gmail.com (IT) ✅ Verified
- info@amalshalih.or.id        → timitasib@gmail.com (IT) ✅ Verified
- Catch-all                    → timitasib@gmail.com (IT) ✅ Verified
```

**Status:** ✅ All routing rules verified & active per 7 Juni 2026

**Setup Guide:** [Lihat docs/10-organisasi/email-dan-akses.md](../10-organisasi/email-dan-akses.md)

### **Google Workspace (Nonprofit):**

**Status:** ⚠️ Currently using personal Gmail + forwarding  
**Recommendation:** Migrate to Google Workspace for Nonprofit (free) for professional email

**Benefits:**
- Custom domain email (nama@amalshalih.or.id)
- 30GB storage per user
- Google Meet premium
- Admin console
- Better security & control

**Migration Steps (Future):**
1. Apply Google for Nonprofit (requires akta yayasan)
2. Verify domain ownership
3. Setup Google Workspace users
4. Migrate emails (Google Takeout/transfer)
5. Update MX records

### **Email Security:**

**SPF Record:**
```
v=spf1 include:_spf.google.com ~all
```

**DKIM:** Enabled via Google Workspace (if migrated)

**DMARC:**
```
v=DMARC1; p=none; rua=mailto:timitasib@gmail.com
```

**2FA:** ✅ Mandatory for all email accounts  
**Recovery:** timitasib@gmail.com untuk semua akun

---

## 💻 Website & Tech Stack

### **Current Stack:**

**Framework:** Astro 5.x  
**CMS:** Sanity.io (Headless CMS)  
**Hosting:** Niagahoster (shared hosting)  
**Deployment:** Manual FTP / Git-based (future: Vercel/Netlify)

**File Structure:**
```
/home/dev/project/yayasan-amal-shalih-insan-bantul/
├── src/
│   ├── components/
│   ├── layouts/
│   ├── pages/
│   │   ├── index.astro
│   │   ├── tentang.astro
│   │   ├── program.astro
│   │   ├── blog/
│   │   └── kontak.astro
│   └── lib/
│       └── sanity/
│           └── client.ts
├── public/
│   ├── favicon.svg
│   └── images/
├── package.json
├── astro.config.mjs
├── tsconfig.json
└── docs/ (documentation)
```

**Dependencies:**
```json
{
  "astro": "^5.x",
  "@sanity/client": "^6.x",
  "@astrojs/sitemap": "^3.x",
  // ... other dependencies
}
```

### **Sanity.io CMS:**

**Project ID:** [Check sanity.jsonc atau .env]  
**Dataset:** production  
**API Version:** v2024-01-01

**Schema Types:**
- `post` — Blog posts
- `author` — Authors
- `page` — Static pages
- `siteSettings` — Site configuration

**Content Structure:**
```
Sanity Studio
├── Posts (blog)
│   ├── title
│   ├── slug
│   ├── excerpt
│   ├── body (Portable Text)
│   ├── author (reference)
│   ├── publishedAt
│   └── mainImage
├── Pages
│   ├── title
│   ├── slug
│   └── content
└── Site Settings
    ├── siteTitle
    ├── siteDescription
    └── socialLinks
```

**Frontend Integration:**
```typescript
// src/lib/sanity/client.ts
import Sanity from "@sanity/client";

export const client = Sanity({
  projectId: "your-project-id",
  dataset: "production",
  apiVersion: "2024-01-01",
  useCdn: true,
});

export async function getBlogPostList() {
  return client.fetch(`*[_type == "post"] | order(publishedAt desc)`);
}

export async function getBlogPost(slug: string) {
  return client.fetch(`*[_type == "post" && slug.current == $slug][0]`, { slug });
}
```

### **Deployment Process:**

**Current (Manual):**
1. Build: `npm run build`
2. Upload `dist/` folder via FTP (FileZilla)
3. Overwrite existing files
4. Clear cache (if any)

**Future (Automated):**
- GitHub Actions + FTP action
- Or migrate to Vercel/Netlify for Git-based deployment

### **Performance:**

**Target:**
- Lighthouse Score: 90+
- First Contentful Paint: <1.5s
- Time to Interactive: <3.5s

**Optimization:**
- Image optimization (Astro Image component)
- Lazy loading
- Minify CSS/JS
- CDN via Cloudflare

---

## 🔌 Third-party Services

### **1. Trello (Workflow Management)**

**URL:** `https://trello.com`  
**Plan:** Free  
**Admin:** timitasib@gmail.com

**Boards:**
- **Media & Publikasi** — Content workflow
- **IT & Teknis** — Technical tasks
- **Program & Kegiatan** — Event planning
- **Pengurus** — Strategic planning
- **Relawan** — Volunteer management

**Integration:**
- Email notifications → Gmail
- Calendar sync → Google Calendar
- Power-ups: Calendar, Custom Fields (free tier)

### **2. Google Drive (Storage & Collaboration)**

**Storage:** 15GB (shared across Gmail accounts)  
**Structure:**
```
My Drive/
├── Shared/
│   ├── Media & Publikasi/
│   ├── Program & Kegiatan/
│   ├── Keuangan/
│   ├── HR/
│   ├── IT & Teknis/
│   └── Templates/
├── Personal/ (per user)
└── Archive/
```

**Sharing Settings:**
- Internal: Comment access (default)
- External: View only (specific files)
- Sensitive: Restricted (IT, Keuangan, Pengurus)

### **3. GitHub (Code Repository)**

**Organization:** `amalshalih`  
**Repository:** `website-asib`  
**Access:** Private (invite-only)

**Branches:**
- `main` — Production-ready code
- `develop` — Development branch
- `feature/*` — Feature branches

**Workflow:**
1. Create feature branch
2. Commit changes
3. Push to GitHub
4. Create Pull Request
5. Review & merge

### **4. Social Media Platforms**

| Platform | Handle | Login Email | Management |
|----------|--------|-------------|------------|
| Instagram | @amalshalihinsan | amalshalih.insanbantul@gmail.com | Meta Business Suite |
| Facebook | @amalshalihinsanbantul | amalshalih.insanbantul@gmail.com | Meta Business Suite |
| TikTok | @yayasan.amalshalihinsan | amalshalih.insanbantul@gmail.com | TikTok app |
| YouTube | @amalshalihinsanbantul9997 | amalshalih.insanbantul@gmail.com | YouTube Studio |

### **5. Canva (Design)**

**Plan:** Free (consider Canva Pro for Nonprofit)  
**Team:** Yayasan ASIB  
**Members:** Koordinator Media + Relawan Media

**Brand Kit:**
- Colors: Primary (#166534), Gold (#fcd34d), Warm (#44403c)
- Fonts: Inter, Plus Jakarta Sans
- Logo: Uploaded

### **6. Google Analytics (Website Analytics)**

**Status:** ⚠️ To be setup  
**Recommendation:** Install GA4 for traffic insights

**Setup:**
1. Create GA4 property
2. Add tracking code to Astro (`<head>`)
3. Verify installation
4. Setup goals (donasi clicks, contact form submissions)

### **7. Google Search Console (SEO)**

**Status:** ⚠️ To be setup  
**Recommendation:** Submit sitemap for better indexing

**Setup:**
1. Verify domain ownership (DNS record)
2. Submit sitemap (`sitemap.xml`)
3. Monitor indexing status
4. Fix crawl errors

---

## 🔒 Security Guidelines

### **Password Policy:**

**Requirements:**
- Minimum 12 characters
- Mix of uppercase, lowercase, numbers, symbols
- No dictionary words
- Unique per service
- Use password manager (Bitwarden/1Password)

**Password Manager:**
- **Recommended:** Bitwarden (free, open-source)
- **Alternative:** 1Password, LastPass
- **Storage:** Encrypted vault, shared vault untuk tim

**Password Rotation:**
- Critical accounts (email, domain, hosting): Every 6 months
- Regular accounts: Every 12 months
- Immediately jika ada suspicion of breach

### **2FA (Two-Factor Authentication):**

**Mandatory for:**
- ✅ All email accounts
- ✅ Domain registrar
- ✅ Hosting (cPanel)
- ✅ Google Workspace
- ✅ Trello (admin)
- ✅ GitHub
- ✅ Social media accounts

**Method:** Google Authenticator / Authy  
**Backup:** Backup codes printed & stored in 3 locations:
1. IT (timitasib@gmail.com holder)
2. Pengurus Ketua
3. Bendahara

**2FA Setup Process:**
1. Install Google Auth / Authy
2. Scan QR code dari service
3. Save backup codes (print 3 copies)
4. Test 2FA login
5. Document di spreadsheet IT

### **Access Control:**

**Principle of Least Privilege:**
- Give minimum access necessary
- Review access quarterly
- Revoke immediately saat offboarding

**Access Request:**
1. Request via Trello card
2. Approve by IT + Koordinator
3. Setup by IT
4. Document di spreadsheet

### **Device Security:**

**Requirements:**
- Screen lock (PIN/password/biometric)
- Auto-lock: 5 minutes
- Encryption: Enabled (FileVault for Mac, BitLocker for Windows)
- Antivirus: Installed & updated

**Prohibited:**
- Sharing devices dengan unauthorized person
- Installing unapproved software
- Disabling security features

### **Phishing Prevention:**

**Red Flags:**
- Urgent request for credentials
- Suspicious links (check URL carefully)
- Attachments from unknown senders
- Requests to bypass 2FA

**Action:**
- Don't click suspicious links
- Verify sender via different channel
- Report to IT immediately
- Change password if compromised

### **Incident Response:**

**If Account Compromised:**
1. Change password immediately
2. Revoke all sessions
3. Check recent activity
4. Enable/re-setup 2FA
5. Notify IT & Pengurus
6. Document incident

**If Data Breach:**
1. Contain breach (revoke access, change passwords)
2. Assess damage (what data exposed)
3. Notify affected parties
4. Report to Pengurus
5. Review & improve security

---

## 💾 Backup & Recovery

### **Backup Strategy:**

**3-2-1 Rule:**
- 3 copies of data
- 2 different media types
- 1 off-site copy

### **What to Backup:**

| Data Type | Frequency | Method | Storage |
|-----------|-----------|--------|---------|
| **Website Code** | Every commit | Git (GitHub) | GitHub (cloud) |
| **Website Database** | Weekly | cPanel backup + manual export | Google Drive IT |
| **Google Drive Files** | Continuous | Google native backup | Google (cloud) |
| **Trello Boards** | Monthly | Export JSON | Google Drive IT |
| **Email** | Continuous | Google native | Google (cloud) |
| **Credentials** | When changed | Password manager backup | Encrypted file |
| **Financial Records** | Monthly | Download PDFs | Google Drive Keuangan |
| **Documentation** | When changed | Git + Google Drive | GitHub + Drive |

### **Backup Procedures:**

**1. Website (cPanel):**
```
1. Login cPanel
2. Backup → Download Backup
3. Download Full Backup / Home Directory / Database
4. Save to Google Drive: IT & Teknis/Backup/Website/YYYY-MM/
5. Verify backup can be restored
```

**2. Database (Manual):**
```
1. phpMyAdmin → Select database
2. Export → SQL format
3. Download .sql file
4. Save to Google Drive
```

**3. Trello Boards:**
```
1. Board → Menu → ... → Print & Export
2. Export to JSON
3. Save to Google Drive: IT & Teknis/Backup/Trello/YYYY-MM/
```

**4. Google Drive:**
- Native versioning (keep 30 days / 100 versions)
- Critical files: Download copy ke local + external drive

### **Recovery Procedures:**

**Website Down:**
1. Check hosting status (Niagahoster status page)
2. Contact support jika hosting issue
3. Restore from backup:
   - Upload backup via cPanel File Manager
   - Import database via phpMyAdmin
   - Update config jika perlu
4. Test website
5. Monitor for issues

**Data Loss:**
1. Identify what data lost
2. Check backup availability
3. Restore from latest backup
4. Verify data integrity
5. Document incident

**Account Recovery:**
1. Use recovery email (timitasib@gmail.com)
2. Follow provider recovery process
3. Reset password
4. Re-enable 2FA
5. Check for unauthorized activity

### **Disaster Recovery Plan:**

**Scenario: Complete Infrastructure Loss**

**Recovery Priority:**
1. **Email** (communication) — 24 hours
2. **Domain** (identity) — 48 hours
3. **Website** (presence) — 1 week
4. **Files** (operations) — 1 week
5. **Social Media** (engagement) — 2 weeks

**Recovery Steps:**
1. Assess damage
2. Contact providers (domain, hosting, Google)
3. Restore from backups
4. Reconfigure services
5. Test all systems
6. Notify stakeholders

**Contact List (Emergency):**
- IT: timitasib@gmail.com
- Pengurus Ketua: [Kontak]
- Hosting Support: [Phone/Chat]
- Domain Registrar: [Email/Phone]

---

## 🔑 Credentials Management

### **Password Manager Setup:**

**Recommended:** Bitwarden (free, open-source, self-hostable)

**Organization Structure:**
```
Bitwarden Vault
├── Personal (per user)
├── Shared (Yayasan ASIB Org)
│   ├── Email Accounts
│   ├── Domain & Hosting
│   ├── Social Media
│   ├── Financial (Bendahara only)
│   └── Third-party Services
└── Archive (old credentials)
```

### **Credential Categories:**

**Critical (Share dengan IT + Pengurus):**
- Domain registrar
- Hosting cPanel
- Primary email (amalshalih.insanbantul)
- Recovery email (timitasib)
- Financial accounts

**Important (Share dengan Koordinator):**
- Social media accounts
- Trello boards
- Canva team
- Google Drive shared folders

**Regular (Individual):**
- Personal login
- Non-critical services

### **Credential Storage:**

**DO:**
- ✅ Use password manager
- ✅ Enable 2FA for all critical accounts
- ✅ Share via password manager secure sharing
- ✅ Update immediately saat ada perubahan
- ✅ Audit quarterly

**DON'T:**
- ❌ Store in plain text files
- ❌ Share via WhatsApp/email
- ❌ Write on paper (kecuali backup codes)
- ❌ Reuse passwords across services
- ❌ Store browser passwords without master password

### **Credential Rotation:**

**Schedule:**
- Critical: Every 6 months (Jan, Jul)
- Important: Every 12 months
- Regular: When suspicious activity

**Process:**
1. Generate new strong password (password manager)
2. Update di service
3. Update di password manager
4. Notify authorized users
5. Test login dengan new password
6. Document rotation date

### **Emergency Access:**

**Emergency Contact:**
- Primary: Pengurus Ketua
- Secondary: Bendahara
- Technical: IT (timitasib)

**Emergency Access Process:**
1. Contact emergency contact
2. Verify identity (phone call + security question)
3. Grant temporary access via password manager emergency access feature
4. Monitor access
5. Revoke after emergency resolved

---

## 📈 Monitoring & Maintenance

### **Daily Checks (IT):**

- [ ] Email delivery (check spam folder, forwarding)
- [ ] Website uptime (manual visit or UptimeRobot)
- [ ] Social media notifications (comments, DMs)

### **Weekly Checks (IT):**

- [ ] Backup verification (check latest backup date)
- [ ] Disk usage (cPanel → Metrics)
- [ ] Error logs (cPanel → Error Logs)
- [ ] Trello board cleanup (archive completed cards)

### **Monthly Checks (IT + Pengurus):**

- [ ] Domain expiry date
- [ ] Hosting billing status
- [ ] SSL certificate expiry
- [ ] Access review (who has access to what)
- [ ] Security audit (2FA status, password age)
- [ ] Performance metrics (website speed, analytics)

### **Quarterly Tasks:**

- [ ] Password rotation (critical accounts)
- [ ] Full backup test (restore to staging)
- [ ] Access review & cleanup
- [ ] Documentation update
- [ ] Disaster recovery drill

### **Annual Tasks:**

- [ ] Domain renewal
- [ ] Hosting plan review (upgrade if needed)
- [ ] Security audit (external if possible)
- [ ] Backup strategy review
- [ ] Infrastructure planning for next year

---

## 📞 Support & Contact

| Issue | Contact | Escalation |
|-------|---------|------------|
| **Website Down** | IT: timitasib@gmail.com | Hosting Support |
| **Email Issue** | IT: timitasib@gmail.com | Google Support |
| **Domain Issue** | IT: timitasib@gmail.com | PANDI Support |
| **Access Request** | Trello: IT Board | Pengurus |
| **Security Incident** | IT + Pengurus | - |
| **Billing Question** | Bendahara | Pengurus |

---

**Dokumen ini internal & sensitif — jangan share ke pihak luar**  
**Last reviewed:** 7 Juni 2026  
**Next review:** 7 Desember 2026  
**Access Level:** IT, Pengurus, Koordinator (relevant sections only)