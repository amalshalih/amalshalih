# OpenKB — Yayasan Amal Shalih Insan Bantul

> **Single Source of Truth** untuk semua operasional Yayasan ASIB  
> **Audience:** Operator (manusia) + AI Agent + Consumer (dengan authorization)  
> **Framework:** Based on [ainjiner/openkb](https://github.com/ainjiner/openkb)  
> **Status:** ✅ **ACTIVE** — Production Ready  
> **Last Updated:** 7 Juni 2026

---

## 🔐 Access Control

**Repository:** `github.com/amalshalih/amalshalih` (Private)  
**Branch:** `main` (production)  
**Access Level:**
- **Operator** (Pengurus, Admin, Media, IT): Full access via GitHub team
- **AI Agent**: Access via token/PAT (Personal Access Token)
- **Consumer**: Read-only access via public API (future, with token)

**Security:**
- ✅ Private repo (invite-only)
- ✅ 2FA required for all members
- ✅ Token-based access for AI agents
- ✅ Audit trail via git history

---

## 📁 OpenKB Structure

```
.openkb/
├── README.md (this file — OpenKB index)
├── 00-start-here/
│   └── README.md (getting started guide)
├── 10-organisasi/
│   ├── struktur-dan-role.md
│   ├── email-dan-akses.md
│   └── humas-decision-analysis.md
├── 20-sop/
│   ├── rapat-workflow.md
│   ├── kegiatan-workflow.md
│   ├── media-sosial.md
│   ├── donasi-handling.md
│   └── onboarding-relawan.md
├── 30-templates/
│   ├── template-agenda.md
│   ├── template-notulen.md
│   ├── template-decision-log.md
│   ├── kwitansi-donasi.md
│   ├── laporan-bulanan.md
│   ├── content-calendar.md
│   ├── analytics-report.md
│   ├── caption-templates.md
│   ├── email-templates.md
│   ├── rab-template.md
│   └── laporan-keuangan.md
├── 40-it-teknis/
│   ├── infrastructure.md
│   ├── security.md
│   ├── credentials.md
│   ├── ARCHITECTURE.md
│   ├── ASTRO_V6_CLOUDFLARE_CONFIG_AUDIT.md
│   ├── CLEAN_CONFIGURATION_SUMMARY.md
│   ├── DATA_SOURCES.md
│   ├── ROOT_LEVEL_WRANGLER_CONFIG.md
│   ├── WORKERD_COMPATIBILITY_AUDIT.md
│   └── WRANGLER_PREVIEW_ERROR_10015.md
├── 50-legal/
│   ├── privacy-policy.md
│   ├── terms-of-service.md
│   └── document-storage.md
├── 60-ai-agents/ (NEW!)
│   ├── context-prompt.md (AI context & instructions)
│   ├── workflow-guides.md (AI-assisted workflows)
│   └── best-practices.md (AI usage guidelines)
├── 90-archive/
│   └── archive-structure.md
├── PROJECT_STATUS.md
├── GALERI_GOOGLE_DRIVE.md
├── KONVENSI_NAMA_FOLDER.md
└── PANDUAN_UPLOAD_FOTO_TIM_MEDIA.md
```

---

## 🎯 Purpose & Use Cases

### **For Operators (Manusia)**

**Who:** Pengurus, Admin, Media, IT, Relawan AMMA

**Use Cases:**
1. **Onboarding** → Start at `00-start-here/README.md`
2. **Daily Operations** → Follow SOPs in `20-sop/`
3. **Templates** → Use ready-made templates from `30-templates/`
4. **Decision Making** → Reference organizational docs in `10-organisasi/`
5. **Troubleshooting** → Check technical guides in `40-it-teknis/`

**Workflow:**
```
1. Buka OpenKB (via GitHub atau AI agent)
2. Cari SOP/template yang dibutuhkan
3. Ikuti workflow yang terdokumentasi
4. Update status di Trello
5. Dokumentasikan hasil di Google Drive
```

### **For AI Agents**

**Who:** Claude, Cursor, GitHub Copilot, custom AI agents

**Use Cases:**
1. **Context Understanding** → Read entire `.openkb/` for Yayasan context
2. **Task Execution** → Follow SOPs to guide operators
3. **Decision Support** → Provide recommendations based on organizational rules
4. **Documentation** → Help update OpenKB with new knowledge
5. **Workflow Automation** → Automate repetitive tasks following documented procedures

**AI Context Prompt:**
```markdown
You are an AI assistant for Yayasan Amal Shalih Insan Bantul.
Context: `.openkb/` folder contains all organizational knowledge.
Rules:
1. Always reference OpenKB docs when giving advice
2. Follow SOPs strictly for operational tasks
3. Respect access control (don't expose sensitive info)
4. Help operators work more efficiently
5. Document new learnings back to OpenKB
```

### **For Consumers (Public with Authorization)**

**Who:** Donatur, mitra, publik yang butuh info

**Use Cases:**
1. **Transparency** → Access public docs (privacy policy, terms)
2. **Donation Info** → Check donation handling SOP
3. **Program Info** → Learn about yayasan programs
4. **Contact** → Find right contact person

**Access Method:**
- Token-based API access (future)
- Public website (amalshalih.or.id) synced with public OpenKB docs
- Controlled disclosure (sensitive info remains private)

---

## 📊 Knowledge Categories

| Category | Folder | Files | For Who |
|----------|--------|-------|---------|
| **Getting Started** | `00-start-here/` | 1 | All |
| **Organization** | `10-organisasi/` | 3 | All |
| **SOPs** | `20-sop/` | 5 | Operators |
| **Templates** | `30-templates/` | 12 | Operators |
| **Technical** | `40-it-teknis/` | 10 | IT + AI |
| **Legal** | `50-legal/` | 3 | All |
| **AI Agents** | `60-ai-agents/` | 3 | AI + Operators |
| **Archive** | `90-archive/` | 1 | Admin |
| **Operational Guides** | Root `.openkb/` | 3 | Media |
| **Status Tracking** | `PROJECT_STATUS.md` | 1 | Pengurus |
| **TOTAL** | | **42 files** | |

---

## 🔄 Workflow Integration

### **OpenKB → Trello → Google Drive**

```
OpenKB (Knowledge)
   ↓
Trello (Workflow Tracking)
   ↓
Google Drive (Execution & Assets)
```

**Example: Media Content Workflow**
1. **OpenKB:** Read `20-sop/media-sosial.md` + `30-templates/content-calendar.md`
2. **Trello:** Create card in "Media & Publikasi" board
3. **Google Drive:** Create content in `Media & Publikasi/` folder
4. **OpenKB:** Update analytics in `30-templates/analytics-report.md`

### **OpenKB → AI Agent → Operator**

```
Operator asks AI: "How to handle donation?"
   ↓
AI reads: `20-sop/donasi-handling.md`
   ↓
AI guides operator step-by-step
   ↓
Operator executes, documents in Drive
   ↓
AI updates OpenKB if there's new learning
```

---

## 🛠️ How to Use OpenKB

### **For New Members**

1. **Read:** `00-start-here/README.md`
2. **Understand:** `10-organisasi/struktur-dan-role.md` (your role)
3. **Follow:** Relevant SOP in `20-sop/`
4. **Use:** Templates from `30-templates/`
5. **Ask:** AI agent or IT if confused

### **For AI Agents**

1. **Ingest:** Read entire `.openkb/` folder
2. **Index:** Build knowledge graph
3. **Reference:** Always cite OpenKB docs when advising
4. **Update:** Suggest improvements to outdated docs
5. **Respect:** Access control & sensitivity levels

### **For Maintainers**

1. **Review:** Check for outdated docs monthly
2. **Update:** Keep SOPs aligned with reality
3. **Organize:** Maintain folder structure
4. **Onboard:** Help new members access OpenKB
5. **Secure:** Manage access control & tokens

---

## 🔒 Access Control & Security

### **Access Levels**

| Level | Who | Access | Method |
|-------|-----|--------|--------|
| **Full** | IT, Pengurus | Read + Write | GitHub team member |
| **Operator** | Admin, Media, Relawan | Read + Write (specific folders) | GitHub team member |
| **AI Agent** | Claude, Cursor, etc. | Read-only | Token/PAT |
| **Consumer** | Public | Read-only (public docs only) | Token-based API (future) |

### **Security Measures**

- ✅ Private GitHub repository
- ✅ 2FA mandatory for all members
- ✅ Token-based access for AI agents
- ✅ Audit trail via git commit history
- ✅ Regular access review (quarterly)
- ✅ Sensitive docs encrypted (passwords, credentials)

### **Sensitive Documents**

These docs are **RESTRICTED** (IT/Pengurus only):
- `40-it-teknis/credentials.md`
- `40-it-teknis/security.md` (partial)
- `50-legal/` (some legal docs)

---

## 📈 Metrics & Monitoring

### **Usage Metrics** (Track Monthly)

| Metric | Target | Actual |
|--------|--------|--------|
| **Active Operators** | 10+ | TBD |
| **AI Agent Queries** | 100+/month | TBD |
| **SOP Updates** | 2+/month | TBD |
| **New Templates** | 1+/month | TBD |
| **Access Reviews** | Quarterly | TBD |

### **Health Checks**

- [ ] All SOPs up-to-date (review quarterly)
- [ ] Templates usable (test monthly)
- [ ] AI agent has latest context (sync weekly)
- [ ] Access control working (audit quarterly)
- [ ] No orphaned docs (cleanup monthly)

---

## 🚀 Future Enhancements

### **Phase 1: Foundation (CURRENT ✅)**
- [x] Consolidate all knowledge in `.openkb/`
- [x] Structure by user journey
- [x] AI agent integration ready
- [ ] Deploy to `amalshalih/amalshalih` repo

### **Phase 2: AI Integration (NEXT)**
- [ ] Create `60-ai-agents/` section
- [ ] Build AI context prompts
- [ ] Integrate with Claude/Cursor
- [ ] AI-assisted documentation updates

### **Phase 3: Public Access (FUTURE)**
- [ ] Token-based API for consumers
- [ ] Sync public docs to website
- [ ] Controlled disclosure system
- [ ] Analytics dashboard

### **Phase 4: Scalability (LONG-TERM)**
- [ ] Multi-tenant support (other yayasan)
- [ ] OpenKB framework improvements
- [ ] Community contributions
- [ ] Integration with other tools

---

## 📚 Related Resources

- **Framework:** [ainjiner/openkb](https://github.com/ainjiner/openkb)
- **Website:** `github.com/amalshalih/amalshalih.github.io`
- **Trello:** Yayasan ASIB boards (4 boards)
- **Google Drive:** Workspace ASIB structure
- **Email:** Cloudflare Email Routing

---

## 📞 Contact & Support

| Role | Contact | For |
|------|---------|-----|
| **OpenKB Maintainer** | timitasib@gmail.com | Access requests, technical issues |
| **IT Support** | timitasib@gmail.com | AI agent setup, token management |
| **Pengurus** | [Pengurus contact] | Policy decisions, access approval |

---

**Last Updated:** 7 Juni 2026  
**Maintained by:** timitasib@gmail.com (IT/Teknis)  
**Next Review:** 7 Desember 2026

---

*"OpenKB adalah jantung kolaborasi Yayasan ASIB. Semua pengetahuan dalam satu tempat, dapat diakses oleh manusia dan AI, untuk kerja yang lebih efektif dan transparan."*