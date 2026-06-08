# AI-Assisted Workflows Guide — Yayasan ASIB

> **Status:** ✅ **ACTIVE** — Operational Playbook for AI & Operators  
> **Audience:** Operators + AI Agents  
> **Last Updated:** 7 Juni 2026

---

## 🤖 Kolaborasi Manusia + AI (Human-in-the-Loop)

Di Yayasan Amal Shalih Insan Bantul, kita mengadopsi model **Human-in-the-Loop**. AI agent (seperti Claude, ChatGPT, atau Cursor) bertindak sebagai **co-pilot** yang sangat pintar, sedangkan keputusan akhir, persetujuan legal, dan tindakan fisik tetap dipegang penuh oleh **Operator (Manusia)**.

```
+--------------------+      💡 Ide & Konteks      +-------------------+
|  Operator Manusia  | -------------------------> |     AI Agent      |
|  (Pengurus/Relawan)| <------------------------- | (Co-pilot/Writer) |
+--------------------+    Naskah, Draft, Coding   +-------------------+
          |                                                 |
          |  1. Review & Approve                            |
          |  2. Upload/Execute                              |
          v                                                 v
+--------------------+                            +-------------------+
| Trello & Drive     |                            | Sentry / SBM logs |
+--------------------+                            +-------------------+
```

---

## 📋 Alur Kerja 1: Pembuatan Konten Media Sosial (Instagram/FB/TikTok)

**Target Pembuat:** Pengurus Media (`media.amalshalih@gmail.com`) / Relawan Media  
**Asisten AI:** Claude/ChatGPT

### **Langkah-langkah:**

1. **Operator membuat ide konten di Trello:**
   - Masukkan kartu baru di Board **Website & Konten** -> Kolom `💡 Ide Konten`
2. **AI mengumpulkan referensi:**
   - Operator memberikan outline/tema ke AI: *"Buat naskah postingan tentang program Jumat Bersedekah pekan ini."*
   - AI membaca SOP Media Sosial (`.openkb/20-sop/media-sosial.md`) dan Caption Templates (`.openkb/30-templates/caption-templates.md`).
3. **AI menulis draft konten:**
   - AI menghasilkan copy caption, rekomendasi visual (Carousel/Video), hashtag, dan Trello Checklist.
4. **Review & Visual:**
   - Operator menyalin naskah ke Google Drive `Workspace ASIB/Media & Publikasi/Draft Konten/`.
   - Mas Aziz (Kepala Media) mengulas naskah dan membuat desain visual di Canva.
5. **Siap Upload:**
   - Pindahkan kartu Trello ke `🚀 Siap Upload` dan jadwalkan di Meta Business Suite.

---

## 📋 Alur Kerja 2: Penanganan Konfirmasi Donasi

**Target Pembuat:** Admin (`amalshalih.insanbantul@gmail.com`)  
**Asisten AI:** WhatsApp Bot / GPT Custom

### **Langkah-langkah:**

1. **Donatur mengirim konfirmasi:**
   - Donatur mengirim bukti transfer ke WhatsApp utama (`0821-3800-7102`) atau email `donasi@amalshalih.or.id`.
2. **AI membantu penulisan respon:**
   - Admin meminta AI menulis pesan balasan: *"Tolong buatkan pesan balasan resmi untuk Pak [Nama] yang baru saja menyumbang Rp [Jumlah] untuk program Rumah Tahfidz."*
   - AI merujuk ke SOP Donasi Handling (`.openkb/20-sop/donasi-handling.md`) dan email-templates (`.openkb/30-templates/email-templates.md`).
3. **Penerbitan Kwitansi:**
   - AI mengisi template kwitansi (`.openkb/30-templates/kwitansi-donasi.md`).
   - Admin mengecek mutasi bank, memberikan nomor kwitansi, dan membubuhkan stempel digital.
4. **Pencatatan Keuangan:**
   - Catat transaksi di Google Sheet Laporan Keuangan (`Workspace ASIB/Kantor ASIB/Keuangan/`).
   - Pindahkan kartu Trello di Board **Administrasi & Keuangan** ke kolom `📁 Tersimpan`.

---

## 📋 Alur Kerja 3: Troubleshooting IT & Website

**Target Pembuat:** IT (`timitasib@gmail.com`) / Relawan IT  
**Asisten AI:** Claude Code / Cursor / Sentry AI

### **Langkah-langkah:**

1. **Menerima alert error:**
   - Sentry mendeteksi error di website `amalshalih.or.id` dan mengirim notifikasi ke email `info@amalshalih.or.id` / Discord IT.
2. **AI menganalisis error:**
   - IT engineer memberikan trace error ke AI: *"Ada crash di halaman detail kegiatan. Ini logs dari Sentry."*
   - AI membaca Technical Docs (`.openkb/40-it-teknis/`) dan CMS Integration (`.openkb/40-it-teknis/cms-integration.md`).
3. **AI menyarankan perbaikan:**
   - AI menulis kode perbaikan, memverifikasi kompatibilitas Cloudflare Workers (`.openkb/40-it-teknis/WORKERD_COMPATIBILITY_AUDIT.md`), dan memastikan type-safety.
4. **Developer melakukan deploy:**
   - IT engineer menguji perbaikan di staging, membuat commit sesuai aturan (`.openkb/40-it-teknis/commit-strategy.md`), dan mendeploy ke Cloudflare Workers (`.openkb/40-it-teknis/deployment.md`).

---

## 📋 Alur Kerja 4: Onboarding Relawan AMMA Baru

**Target Pembuat:** IT (`timitasib@gmail.com`) + Koordinator Unit  
**Asisten AI:** Onboarding Assistant

### **Langkah-langkah:**

1. **Relawan mendaftar:**
   - Calon relawan mengisi form pendaftaran.
2. **AI menyusun checklist onboarding:**
   - AI membaca SOP Onboarding Relawan (`.openkb/20-sop/onboarding-relawan.md`) dan membuat Trello Card personal untuk relawan tersebut.
3. **Setup Akses:**
   - IT (timitasib@gmail.com) mengonfirmasi kecocokan dan memberikan akses Google Drive Workspace, Trello, Sentry, dll.
4. **Pemberian Tugas Pertama:**
   - Koordinator memberikan tugas pertama yang terdokumentasi di Trello.

---

**Last Updated:** 7 Juni 2026  
**Maintained by:** timitasib@gmail.com (IT/Teknis)  
**Next Review:** 7 Desember 2026

---

*"AI mempercepat pengerjaan tugas administratif, memberi ruang bagi manusia untuk fokus pada sentuhan kemanusiaan dan empati dakwah."*