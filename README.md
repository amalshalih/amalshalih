<div align="center">
  <img src="https://raw.githubusercontent.com/amalshalih/amalshalih/main/assets/banner.svg" alt="Yayasan Amal Shalih Insan Bantul" width="100%">
</div>

<h1 align="center">Assalamu'alikum Warahmatullahi Wabarakatuh 🙏</h1>

<p align="center">
  <b>Yayasan Amal Shalih Insan Bantul (ASIB)</b> — 
  Menebar kebaikan, membangun peradaban melalui pendidikan, sosial, dan dakwah.
</p>

<p align="center">
  <a href="https://amalshalih.or.id">
    <img src="https://img.shields.io/badge/Website-amalshalih.or.id-2E7D32?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
  <a href="https://instagram.com/amalshalih">
    <img src="https://img.shields.io/badge/Instagram-@amalshalih-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram">
  </a>
  <a href="https://www.youtube.com/@amalshalih">
    <img src="https://img.shields.io/badge/YouTube-@amalshalih-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="YouTube">
  </a>
  <a href="mailto:timitasib@gmail.com">
    <img src="https://img.shields.io/badge/Email-timitasib@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
  </a>
</p>

---

## 🕌 Tentang Kami

**Yayasan Amal Shalih Insan Bantul (ASIB)** adalah lembaga nirlaba yang berfokus pada:

| 🌱 Pendidikan | 🤝 Sosial | 📖 Dakwah |
|---|---|---|
| TPA & Tahfidz Qur'an | Santunan anak yatim | Kajian pekanan |
| Beasiswa dhuafa | Jumat Bersedekah | Program keislaman |

> *"Sebaik-baik manusia adalah yang paling bermanfaat bagi manusia lain."* (HR. Ahmad)

---

## 🌐 Repo Tunggal Utama OpenKB — Yayasan ASIB

Repository ini merupakan **Single Source of Truth (Repo Tunggal Utama) Knowledge Base** Yayasan ASIB yang dibangun menggunakan kerangka **OpenKB** milik [`ainjiner/openkb`](https://github.com/ainjiner/openkb). 

Knowledge base ini dirancang secara terstruktur agar dapat digunakan dan dikolaborasikan secara dinamis oleh:
- 👥 **Operator (Manusia):** Pengurus, Admin, Media, IT, dan Relawan AMMA.
- 🤖 **AI / AI Agent:** Claude, Cursor, ChatGPT, dan asisten digital lainnya untuk mempermudah pengerjaan tugas sehari-hari.
- 🔐 **Consumer:** Publik, donatur, atau pihak eksternal (dengan sistem otorisasi khusus).

---

## 📁 Struktur Pengetahuan OpenKB (`.openkb/`)

Seluruh pengetahuan dan pedoman operasional yayasan disimpan di dalam folder [**.openkb/**](https://github.com/amalshalih/amalshalih/tree/main/.openkb):

```
.openkb/
├── README.md                           # Indeks utama OpenKB (dokumen ini)
├── 00-start-here/
│   └── README.md                       # Panduan onboarding anggota & relawan baru
├── 10-organisasi/
│   ├── struktur-dan-role.md            # Pengurus, kontak, direktori, matriks akses
│   ├── email-dan-akses.md              # Struktur perutean email yayasan
│   ├── workspace-management.md         # Manajemen workspace Google Drive & Trello
│   ├── yayasan-profile.md              # Profil legalitas resmi yayasan (NIB, NPWP, Bank)
│   └── humas-decision-analysis.md      # Analisis perutean humas@amalshalih.or.id
├── 20-sop/
│   ├── rapat-workflow.md               # SOP penyelenggaraan rapat (daring & luring)
│   ├── kegiatan-workflow.md            # SOP pelaksanaan acara/program (ide s.d laporan)
│   ├── media-sosial.md                 # SOP pengelolaan konten Instagram, FB, TikTok, YT
│   ├── donasi-handling.md              # SOP konfirmasi donasi & pencatatan keuangan
│   ├── onboarding-relawan.md           # SOP onboarding Relawan AMMA
│   └── workflow-kanban.md              # Pedoman kerja Kanban Trello (Gotong Royong Digital)
├── 30-templates/
│   ├── template-agenda.md / notulen.md / decision-log.md # Template rapat
│   ├── kwitansi-donasi.md / laporan-keuangan.md / rab-template.md # Template keuangan
│   ├── content-calendar.md / caption-templates.md # Template media sosial
│   └── email-templates.md / laporan-bulanan.md # Template korespondensi & publikasi
├── 40-it-teknis/
│   ├── infrastructure.md / security.md # IT infrastruktur & panduan keamanan 2FA
│   ├── credentials.md                  # Panduan password manager (restricted)
│   ├── ARCHITECTURE.md                 # Keputusan arsitektur website Astro v6 + Cloudflare
│   ├── cms-integration.md              # Integrasi Astro dengan Sanity CMS
│   ├── deployment.md / commit-strategy.md # Panduan deploy & aturan commit git
│   ├── email-system.md                 # Setup teknis perutean email di Cloudflare
│   └── [audit files & guides]          # Audit teknis & panduan troubleshooting error
├── 50-legal/
│   ├── privacy-policy.md               # Kebijakan privasi (UU PDP No. 27 Tahun 2022)
│   ├── terms-of-service.md             # Ketentuan layanan untuk website
│   └── document-storage.md             # Kebijakan retensi dan pengarsipan dokumen
├── 60-ai-agents/ (NEW!)
│   ├── context-prompt.md               # Prompt instruksi utama untuk asupan AI Agent
│   ├── workflow-guides.md              # Panduan kolaborasi manusia-AI (Human-in-the-Loop)
│   └── best-practices.md               # Praktik terbaik penggunaan AI & privasi data
└── 90-archive/
    └── archive-structure.md            # Struktur pengarsipan file bersejarah
```

---

## 🚀 Memulai Penggunaan (Quick Start)

### **Bagi Operator (Manusia)**
1. **Anggota/Relawan Baru:** Mulailah membaca [**`00-start-here/README.md`**](https://github.com/amalshalih/amalshalih/tree/main/.openkb/00-start-here/README.md).
2. **Menjalankan Tugas:** Ikuti SOP terkait di [**`20-sop/`**](https://github.com/amalshalih/amalshalih/tree/main/.openkb/20-sop) dan gunakan template yang sesuai di [**`30-templates/`**](https://github.com/amalshalih/amalshalih/tree/main/.openkb/30-templates).
3. **Koordinasi:** Gunakan Trello Board dan Google Drive Workspace sesuai pedoman di [**`10-organisasi/workspace-management.md`**](https://github.com/amalshalih/amalshalih/tree/main/.openkb/10-organisasi/workspace-management.md).

### **Bagi AI Agent (Claude/Cursor/GPT)**
1. **Asupan Konteks:** AI diinstruksikan untuk membaca seluruh folder `.openkb/` sebagai basis pengetahuan utama.
2. **System Prompt:** Gunakan panduan dan prompt di [**`60-ai-agents/context-prompt.md`**](https://github.com/amalshalih/amalshalih/tree/main/.openkb/60-ai-agents/context-prompt.md) untuk memastikan AI beroperasi dalam koridor keamanan yayasan.

---

## 🛠️ Hubungan dengan Project Lain

### **[amalshalih.github.io](https://github.com/amalshalih/amalshalih.github.io)**
> Codebase website resmi Yayasan ASIB (Astro v6 + Tailwind v4 + Cloudflare Workers + Sanity CMS). Website mem-fetch data berita/kegiatan secara dinamis menggunakan Sanity CMS.

---

## 📫 Kontak & Otorisasi Akses

| Media | Link |
|---|---|
| 🌐 Website Resmi | [amalshalih.or.id](https://amalshalih.or.id) |
| 📧 Email Utama (Admin) | [amalshalih.insanbantul@gmail.com](mailto:amalshalih.insanbantul@gmail.com) |
| 📧 Email IT & Support | [timitasib@gmail.com](mailto:timitasib@gmail.com) |
| 📧 Email Media | [media.amalshalih@gmail.com](mailto:media.amalshalih@gmail.com) |
| 📍 Lokasi Sekretariat | Bantul, Daerah Istimewa Yogyakarta, Indonesia |

---

<div align="center">
  <sub>© 2026 Yayasan Amal Shalih Insan Bantul — Terimakasih atas do'a dan dukungannya 🤲</sub>
</div>