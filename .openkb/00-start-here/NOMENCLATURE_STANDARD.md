# 📝 Nomenklatur & Naming Convention — Yayasan ASIB

> **Status:** ✅ **STANDARD** — Wajib diikuti untuk semua dokumen baru  
> **Last Updated:** 9 Juni 2026  
> **Audience:** Operator, IT Team, AI Agents  
> **Purpose:** Konsistensi penamaan file, folder, dan dokumentasi

---

## 🎯 Prinsip Dasar

### **1. Konsisten** 
Semua nama file harus mengikuti pola yang sama agar mudah:
- Dicari (searchable)
- Diurutkan (sortable)
- Dipahami (readable)
- Diakses oleh AI agents (parseable)

### **2. Deskriptif**
Nama file harus menjelaskan isi konten tanpa perlu membuka file

### **3. Bahasa**
- **Dokumen Teknis (IT):** English (kebab-case)
- **Dokumen Organisasi:** Bahasa Indonesia (kebab-case)
- **File Konfigurasi:** English (standard convention)

### **4. Case Style**
- **File Documents:** `kebab-case.md` (lowercase with hyphens)
- **Folder Names:** `kebab-case/` (lowercase with hyphens)
- **Constants/Config:** `SCREAMING_SNAKE_CASE` (uppercase with underscores)

---

## 📁 NAMING CONVENTION BY CATEGORY

### **1. Technical Documentation (40-it-teknis)**

**Pattern:** `<topic>-<subtopic>.md` (English, kebab-case)

**Examples:**
```
✅ cms-integration.md
✅ commit-strategy.md
✅ email-system.md
✅ deployment.md
✅ kegiatan-content-architecture.md

❌ CMS_Integration.md (not camelCase)
❌ cms_integration.md (not snake_case)
❌ CMS-Integration.md (not Pascal-Case)
```

**Special Cases:**
- **Audit Reports:** `<component>-audit.md`
  - ✅ `astro-config-audit.md`
  - ✅ `workerd-compatibility-audit.md`
- **Configuration Guides:** `<tool>-config.md`
  - ✅ `wrangler-config.md`
  - ✅ `sentry-config.md`
- **Error Troubleshooting:** `<tool>-error-<code>.md`
  - ✅ `wrangler-error-10015.md`

---

### **2. Organizational Documentation (10-organisasi, 20-sop)**

**Pattern:** `<topik>-<subtopik>.md` (Bahasa Indonesia, kebab-case)

**Examples:**
```
✅ email-dan-akses.md
✅ struktur-dan-role.md
✅ humas-decision-analysis.md (mixed OK for specific terms)
✅ workflow-kanban.md
✅ donasi-handling.md

❌ Email_Dan_Akses.md (not Pascal-Case)
❌ emailDanAkses.md (not camelCase)
❌ EMAIL_DAN_AKSES.md (not SCREAMING)
```

**Mixed Language (Allowed):**
- Istilah teknis yang lebih umum dalam English
- ✅ `humas-decision-analysis.md`
- ✅ `workspace-management.md`
- ✅ `content-calendar.md`

---

### **3. Templates (30-templates)**

**Pattern:** `<jenis>-template.md` atau `<kegunaan>.md`

**Examples:**
```
✅ template-notulen.md
✅ template-agenda.md
✅ kwitansi-donasi.md
✅ laporan-bulanan.md
✅ caption-templates.md (English OK for templates)
```

---

### **4. AI Agents (60-ai-agents)**

**Pattern:** `<function>-<type>.md` (English, kebab-case)

**Examples:**
```
✅ workflow-guides.md
✅ best-practices.md
✅ context-prompt.md
```

---

### **5. Legal Documents (50-legal)**

**Pattern:** `<document-type>.md` (English, kebab-case)

**Examples:**
```
✅ privacy-policy.md
✅ terms-of-service.md
✅ document-storage.md
```

---

### **6. Archive (90-archive)**

**Pattern:** `archive-<year>-<topic>.md` atau `<original-name>-archived.md`

**Examples:**
```
✅ archive-2025-structure.md
✅ old-sop-archived.md
```

---

## 🏗️ FOLDER NAMING

### **Pattern:** `<number>-<category>/`

**Directory Structure:**
```
.openkb/
├── 00-start-here/          # Getting started
├── 10-organisasi/          # Organization structure
├── 20-sop/                 # Standard Operating Procedures
├── 30-templates/           # Document templates
├── 40-it-teknis/           # IT technical docs
│   ├── website/           # Website-specific
│   ├── infrastructure/    # Infrastructure
│   └── security/          # Security policies
├── 50-legal/              # Legal documents
├── 60-ai-agents/          # AI agent guides
└── 90-archive/            # Archived docs
```

**Numbering System:**
- `00-` → Onboarding & getting started
- `10-` → Organization & structure
- `20-` → SOPs & workflows
- `30-` → Templates
- `40-` → IT technical
- `50-` → Legal & compliance
- `60-` → AI agents & automation
- `90-` → Archive

---

## 📝 FILE NAME RULES

### **DO (✅):**

1. **Use lowercase** (except SCREAMING constants)
   ```
   ✅ deployment.md
   ✅ email-system.md
   ```

2. **Use hyphens for spaces**
   ```
   ✅ commit-strategy.md
   ✅ kegiatan-content-architecture.md
   ```

3. **Be descriptive**
   ```
   ✅ sanity-cms-integration-guide.md
   ✅ cloudflare-workers-deployment.md
   ```

4. **Include version if needed**
   ```
   ✅ astro-v6-migration-guide.md
   ✅ tailwind-v4-upgrade.md
   ```

5. **Use standard extensions**
   ```
   ✅ file.md (documentation)
   ✅ file.mdx (documentation with JSX)
   ✅ file.json (data/config)
   ```

---

### **DON'T (❌):**

1. **Don't use spaces**
   ```
   ❌ deployment guide.md
   ✅ deployment-guide.md
   ```

2. **Don't use underscores (except SCREAMING)**
   ```
   ❌ deployment_guide.md
   ✅ deployment-guide.md
   ```

3. **Don't use camelCase**
   ```
   ❌ deploymentGuide.md
   ✅ deployment-guide.md
   ```

4. **Don't use special characters**
   ```
   ❌ deployment&config.md
   ✅ deployment-and-config.md
   ```

5. **Don't use dates in filenames (unless archive)**
   ```
   ❌ 2026-06-09-deployment.md
   ✅ deployment.md (date in git history)
   ```

---

## 🔤 ACRONYM RULES

### **Well-Known Acronyms (UPPERCASE):**
```
✅ API (Application Programming Interface)
✅ CMS (Content Management System)
✅ KV (Key-Value storage)
✅ SQL (Structured Query Language)
✅ URL (Uniform Resource Locator)
✅ HTTP/HTTPS (Hypertext Transfer Protocol)
✅ JSON (JavaScript Object Notation)
```

### **Project-Specific Acronyms (Define first):**
```
✅ ASIB (Amal Shalih Insan Bantul) — define on first use
✅ YASIB (Yayasan Amal Shalih Insan Bantul) — define on first use
```

### **In Filenames:**
```
✅ astro-cms-integration.md (spell out)
✅ api-endpoints.md (well-known acronym OK)
✅ kv-storage-guide.md (well-known in context)
```

---

## 📊 NAMING DECISION TREE

```
Is it a technical document?
├─ YES → Use English, kebab-case
│  └─ Example: cms-integration.md
│
└─ NO → Is it organizational?
   ├─ YES → Use Bahasa Indonesia, kebab-case
   │  └─ Example: email-dan-akses.md
   │
   └─ NO → Is it a template?
      ├─ YES → Use template-<jenis>.md
      │  └─ Example: template-notulen.md
      │
      └─ NO → Is it a config/constant?
         ├─ YES → Use SCREAMING_SNAKE_CASE
         │  └─ Example: DATABASE_URL
         │
         └─ NO → Follow category convention
```

---

## 🎯 MIGRATION GUIDE

### **For Existing Files:**

**Don't rename everything at once!** Rename gradually:

1. **New files:** Follow this convention immediately
2. **Updated files:** Rename when making significant changes
3. **Old files:** Rename in batches during maintenance

**Example Migration:**
```
Old: ASTRO_V6_CLOUDFLARE_CONFIG_AUDIT.md
New: astro-v6-cloudflare-config-audit.md

Old: CLEAN_CONFIGURATION_SUMMARY.md
New: clean-configuration-summary.md

Old: WORKERD_COMPATIBILITY_AUDIT.md
New: workerd-compatibility-audit.md
```

**Keep redirects:** When renaming, add redirect in git or update all links

---

## 📋 CHECKLIST

Before committing documentation:

- [ ] Filename uses kebab-case (lowercase with hyphens)
- [ ] Filename is descriptive (< 5 words)
- [ ] Language matches category (EN for IT, ID for org)
- [ ] No special characters or spaces
- [ ] File extension is `.md` (or appropriate)
- [ ] Folder follows numbering convention
- [ ] Acronyms are well-known or defined
- [ ] Name is consistent with existing files

---

## 🔍 EXAMPLES BY CATEGORY

### **Technical (40-it-teknis):**
```
✅ astro-config-audit.md
✅ cloudflare-workers-deployment.md
✅ sanity-cms-integration.md
✅ sentry-error-tracking.md
✅ firebase-admin-setup.md
✅ google-drive-api-integration.md
✅ kv-cache-implementation.md
```

### **Organizational (10-organisasi):**
```
✅ struktur-organisasi.md
✅ email-dan-akses.md
✅ role-dan-responsibility.md
✅ workflow-approval.md
```

### **SOP (20-sop):**
```
✅ donasi-handling.md
✅ kegiatan-workflow.md
✅ media-sosial-management.md
✅ onboarding-relawan.md
```

### **Templates (30-templates):**
```
✅ template-notulen-rapat.md
✅ template-laporan-bulanan.md
✅ template-kwitansi-donasi.md
✅ template-content-calendar.md
```

---

## 📖 REFERENCES

- [Google Developer Documentation Style Guide](https://developers.google.com/style)
- [Microsoft Writing Style Guide](https://learn.microsoft.com/en-us/style-guide/)
- [Keep a Changelog](https://keepachangelog.com/)
- [Semantic Versioning](https://semver.org/)

---

**Maintained by:** IT Team & Documentation Working Group  
**Review Schedule:** Quarterly  
**Next Review:** September 2026  
**Version:** 1.0 (Initial Standard)

---

*This nomenclature standard ensures consistency across all Yayasan ASIB documentation, making it easier for humans and AI agents to find, understand, and maintain documentation.*