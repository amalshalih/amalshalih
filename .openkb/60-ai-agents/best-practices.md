# AI Agent Best Practices — Yayasan ASIB

> **Status:** ✅ **ACTIVE** — Guidelines for AI Usage  
> **Audience:** Operators + AI Engineers  
> **Last Updated:** 7 Juni 2026

---

## 💡 Prinsip Penggunaan AI di Yayasan ASIB

Penggunaan AI (Artificial Intelligence) di lingkungan Yayasan Amal Shalih Insan Bantul harus berlandaskan pada prinsip-prinsip berikut:

1. **Amanah & Kejujuran (Integrity):** AI digunakan untuk meningkatkan efisiensi, bukan untuk memanipulasi data, laporan, atau informasi publik.
2. **Kemanusiaan (Humanity):** AI tidak menggantikan empati dan kepedulian manusia. Tugas sosial, dakwah, dan konseling tetap membutuhkan kehadiran dan hati manusia.
3. **Keamanan & Privasi (Security & Privacy):** Data sensitif donatur, laporan keuangan internal, dan data pribadi anak asuh/siswa tidak boleh diekspos ke public AI model training.
4. **Verifikasi Manusia (Double Check):** Semua keluaran AI (kode, naskah, hitungan keuangan) **wajib diverifikasi** oleh manusia sebelum dieksekusi atau dipublikasikan.

---

## 🔒 Privasi Data & UU PDP No. 27 Tahun 2022

Sesuai dengan kebijakan privasi yayasan (`.openkb/50-legal/privacy-policy.md`), kita harus mematuhi UU Pelindungan Data Pribadi (PDP):

### **Aturan untuk Operator:**
- ❌ **JANGAN PERNAH** mengunggah file spreadsheet berisi nama donatur + nomor HP + jumlah donasi ke ChatGPT/Claude gratisan.
- ❌ **JANGAN PERNAH** mengunggah foto anak asuh tanpa izin tertulis dari wali/orang tua untuk keperluan deskripsi konten AI.
- ✅ **SELALU** lakukan anonimisasi data sebelum meminta AI menganalisis data (misal: ganti nama donatur menjadi "Donatur A", "Donatur B", dst).

---

## 🛠️ Praktik Terbaik Interaksi dengan AI Agent

### **1. Berikan Konteks Lengkap (Context-Rich Prompting)**
AI bekerja dengan sangat baik jika diberikan konteks yang kaya. Gunakan template prompt seperti ini:

```markdown
Konteks: Saya adalah pengurus bidang Pendidikan di Yayasan ASIB.
Tugas: Buat proposal singkat untuk pengadaan buku pelajaran baru di PAUD Bina Tunas Mulia.
Batasan: Target pembaca adalah donatur lokal. Bahasa sopan, hangat, dan profesional.
Referensi: Gunakan data di [.openkb/10-organisasi/struktur-dan-role.md](https://github.com/amalshalih/amalshalih/tree/main/.openkb/10-organisasi/struktur-dan-role.md) untuk verifikasi unit PAUD.
```

### **2. Gunakan System Prompts Secara Konsisten**
Jika Anda menggunakan custom tool seperti Cursor atau Claude Projects, pastikan Anda memuat file `.openkb/60-ai-agents/context-prompt.md` sebagai **system instruction** utama agar AI tidak membuat keputusan di luar kebijakan yayasan.

### **3. Penulisan Kode (Type-Safety & Standard)**
Untuk AI yang membantu pengembangan website:
- Selalu minta AI menulis kode TypeScript yang **type-safe**.
- **JANGAN** toleransi penggunaan `as any`, `@ts-ignore`, atau bypass linter lainnya.
- Minta AI memeriksa compatibility Cloudflare Workers sebelum mendeploy (`.openkb/40-it-teknis/WORKERD_COMPATIBILITY_AUDIT.md`).

---

## ⚠️ Kegagalan AI yang Harus Diwaspadai (Hallucination & Bias)

AI tidak luput dari kesalahan. Beberapa "hallucination" (halusinasi/informasi palsu) yang sering terjadi:

1. **Membuat Link Fiktif:** AI sering kali mengarang link Google Drive atau link dokumen yang tidak ada. Selalu periksa link yang dihasilkan AI.
2. **Kekeliruan Data Keuangan:** AI bisa salah menghitung persentase atau menjumlahkan angka di laporan keuangan. Wajib gunakan kalkulator atau spreadsheet lokal untuk verifikasi ganda.
3. **Melupakan Aturan Custom Domain:** AI sering berasumsi domain kita adalah `.id` padahal yang aktif dan benar adalah `amalshalih.or.id` (dengan `amalshalih.id` sebagai legacy redirect). Selalu ingatkan AI tentang kebijakan dual-domain kita.

---

## 🔄 Pemeliharaan OpenKB oleh AI

Ketika AI menemukan informasi yang sudah tidak relevan atau usang di dalam `.openkb/`:

1. AI **harus** memberi tahu operator tentang ketidakkonsistenan tersebut.
2. AI dapat membantu menulis draf perbaikan dokumen.
3. Operator melakukan peninjauan akhir dan melakukan git commit untuk menyimpan perubahan di repository `amalshalih/amalshalih`.

---

**Last Updated:** 7 Juni 2026  
**Maintained by:** timitasib@gmail.com (IT/Teknis)  
**Next Review:** 7 Desember 2026

---

*"AI adalah alat bantu yang kuat, namun kebijaksanaan dan akuntabilitas tetaplah milik manusia."*