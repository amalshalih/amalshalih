# 💰 SOP Donasi Handling & Keuangan

> Standard Operating Procedure untuk pengelolaan donasi masuk, pencatatan, penyaluran, dan pelaporan

**Last Updated:** 7 Juni 2026  
**Status:** 🟢 Active  
**Applies to:** Bendahara, Koordinator Media, Admin, Pengurus

---

## 📋 Daftar Isi

1. [Prinsip Dasar](#prinsip-dasar)
2. [Channel Donasi](#channel-donasi)
3. [Workflow Donasi Masuk](#workflow-donasi-masuk)
4. [Pencatatan & Validasi](#pencatatan--validasi)
5. [Penyaluran Donasi](#penyaluran-donasi)
6. [Pelaporan & Transparansi](#pelaporan--transparansi)
7. [Rekonsiliasi & Audit](#rekonsiliasi--audit)
8. [Template & Tools](#template--tools)

---

## 🎯 Prinsip Dasar

### **5 Prinsip Pengelolaan Donasi:**

1. **Amanah** — Donasi adalah titipan yang harus disalurkan sesuai tujuan
2. **Transparan** — Setiap rupiah dapat dilacak dari masuk → salur → laporkan
3. **Akuntabel** — Pencatatan rapi, dapat diaudit kapan saja
4. **Tepat Waktu** — Donasi segera salurkan (max 7 hari untuk donasi reguler)
5. **Tepat Sasaran** — Pastikan penerima manfaat sesuai kriteria

### **Donasi Classification:**

| Type | Definition | Handling Priority |
|------|------------|-------------------|
| **Donasi Umum** | Tidak指定program, disalurkan ke kebutuhan umum | Normal (7 hari) |
| **Donasi Terikat** | Untuk program tertentu (sembako, pendidikan, dll) | Normal (7 hari) |
| **Donasi Mendesak** | Untuk kasus urgent (bencana, medis darurat) | **HIGH (24-48 jam)** |
| **Donasi Rutin** | Donasi bulanan dari donatur tetap | Normal (sesuai jadwal program) |
| **Donasi Besar** (>Rp 5.000.000) | Perlu konfirmasi khusus & laporan khusus | **HIGH (konfirmasi dulu)** |

---

## 💳 Channel Donasi

### **1. Transfer Bank (BSI)**

**Account Details:**
```
Bank: Bank Syariah Indonesia (BSI)
No. Rek: 9515769570
Nama: Amal Shalih Insan Bantul
```

**Workflow:**
1. Donatur transfer ke rekening
2. Bendahara cek mutasi rekening (daily check)
3. Catat di spreadsheet
4. Konfirmasi ke donatur (WA/email)
5. Salurkan sesuai program
6. Laporan ke donatur

**Monitoring:**
- **Cek mutasi:** Setiap hari (pagi & sore)
- **Konfirmasi:** Max 24 jam setelah donasi masuk
- **Salurkan:** Max 7 hari (kecuali donasi terikat program)

### **2. QRIS (QR Code)**

**Setup:**
- QR Code tersedia di website, Instagram bio, materi promosi
- Scan → Donatur input nominal → Bayar via e-wallet/aplikasi bank
- Uang masuk ke rekening BSI yang sama

**Workflow:** Sama dengan transfer bank

### **3. Tunai (Langsung ke Kantor)**

**Process:**
1. Donatur datang ke kantor ASIB
2. Terima oleh Admin atau Bendahara
3. Terbitkan **Kwitansi Donasi** (rangkap 2: 1 untuk donatur, 1 untuk arsip)
4. Catat di spreadsheet
5. Setor tunai ke rekening (max 24 jam)

**Kwitansi Template:** [Lihat Template Kwitansi](../30-templates/kwitansi-donasi.md)

### **4. Online Donation (Website)**

**Process:**
1. Donatur klik "Donasi Sekarang" di website
2. Pilih nominal & program
3. Redirect ke payment gateway (Midtrans/Xendit — jika ada)
4. Pembayaran diproses
5. Notifikasi otomatis ke email donatur
6. Data masuk ke spreadsheet otomatis (jika terintegrasi)

**Current State:** Manual redirect ke info rekening & QRIS  
**Future:** Integrasi payment gateway untuk auto-recording

### **5. Donasi Barang**

**Examples:** Sembako, pakaian, buku, alat sekolah

**Process:**
1. Terima barang di kantor
2. Catat di **Inventory Donasi Barang** spreadsheet
3. Foto barang + dokumentasi
4. Salurkan ke penerima (max 7 hari)
5. Laporan ke donatur (foto penyaluran)

---

## 🔄 Workflow Donasi Masuk

### **Overview:**

```
┌─────────────┐
│  1. DONASI  │
│     MASUK   │
└──────┬──────┘
       │
       ▼
┌─────────────┐
│  2. CEK &   │
│   CATAT     │
│  (Bendahara)│
└──────┬──────┘
       │
       ▼
┌─────────────┐
│  3. KONFIRM │
│   (Admin)   │
└──────┬──────┘
       │
       ▼
┌─────────────┐
│  4. SALUR   │
│   (Tim)     │
└──────┬──────┘
       │
       ▼
┌─────────────┐
│  5. LAPOR   │
│   (Admin)   │
└─────────────┘
```

### **Step-by-Step:**

#### **1. Donasi Masuk**

**Sources:**
- Transfer bank (BSI)
- QRIS scan
- Tunai di kantor
- Donasi barang

#### **2. Cek & Catat (Bendahara)**

**Daily Check (2x sehari: 09:00 & 16:00):**

1. **Cek mutasi rekening BSI:**
   - Login BSI Mobile/Internet Banking
   - Cek mutasi hari ini
   - Screenshot/catat setiap donasi masuk

2. **Update Spreadsheet:**

**File:** `Keuangan/Donasi Masuk 2026.xlsx`

**Columns:**
```
| Tanggal | Waktu | Nama Donatur | Nominal | Channel | Program | Keterangan | Status Konfirmasi | Status Salur |
|---------|-------|--------------|---------|---------|---------|------------|-------------------|--------------|
| 17 Jun | 10:30 | H. Abdullah | 500.000 | Transfer | Sembako | Via WA | ✅ Confirmed | ⏳ Pending |
| 17 Jun | 14:15 | Anonymous | 100.000 | QRIS | Umum | - | ❌ Not Yet | ⏳ Pending |
```

3. **Kategorisasi:**
   - **Program:** Sembako, Pendidikan, Kesehatan, Umum, Mendesak
   - **Channel:** Transfer, QRIS, Tunai, Barang
   - **Status:** Pending, Confirmed, Disalurkan

#### **3. Konfirmasi ke Donatur (Admin)**

**Timeline:** Max 24 jam setelah donasi masuk

**Via WA (Template):**

```
Assalamu'alaikum Warahmatullahi Wabarakatuh

Kak [Nama Donatur] yang dirahmati Allah,

Terima kasih atas donasi sebesar Rp [Nominal] yang telah kami terima pada [Tanggal, Jam] melalui [Channel].

✅ Donasi telah kami catat dengan kode: [KODE-DONASI-YYYYMMDD-XXX]

InsyaAllah donasi akan segera kami salurkan kepada yang membutuhkan. Laporan penyaluran akan kami informasikan melalui [Email/WA/Instagram].

Untuk pertanyaan lebih lanjut, bisa reply WA ini atau email ke donasi@amalshalih.or.id

Jazakumullah khairan katsiran atas kepercayaan dan kebaikan Kakak.

Wassalamu'alaikum Warahmatullahi Wabarakatuh

Hormat kami,
Amal Shalih Insan Bantul
📞 08XX-XXXX-XXXX
🌐 amalshalih.or.id
```

**Via Email (Template):**

```
Subject: ✅ Konfirmasi Donasi - [Kode Donasi]

Assalamu'alaikum Warahmatullahi Wabarakatuh,

Kak [Nama] yang dirahmati Allah,

Terima kasih atas donasi sebesar Rp [Nominal] yang telah kami terima pada [Tanggal, Jam].

DETAIL DONASI:
━━━━━━━━━━━━━━━━━━━━
Kode Donasi    : [KODE-XXX]
Tanggal        : [DD MMM YYYY]
Nominal        : Rp [Nominal]
Channel        : [Transfer/QRIS/Tunai]
Program        : [Sembako/Pendidikan/Umum]
━━━━━━━━━━━━━━━━━━━━

Donasi ini insyaAllah akan segera kami salurkan kepada yang membutuhkan. Laporan penyaluran akan kami informasikan melalui [email/website/Instagram] dalam waktu 7 hari.

Untuk pertanyaan lebih lanjut, bisa reply email ini atau hubungi kami di:
📞 08XX-XXXX-XXXX
💬 donasi@amalshalih.or.id

Jazakumullah khairan katsiran.

Wassalamu'alaikum Warahmatullahi Wabarakatuh,

Hormat kami,

[Nama Admin/Bendahara]
Amal Shalih Insan Bantul
```

**Update Spreadsheet:**
- Kolom "Status Konfirmasi": ✅ Confirmed + tanggal

#### **4. Salurkan Donasi (Tim Program)**

**Timeline:** Max 7 hari untuk donasi reguler, 24-48 jam untuk donasi mendesak

**Process:**

1. **Planning (Rapat Program):**
   - Review donasi terkumpul minggu ini
   - Tentukan prioritas penyaluran
   - Assign PIC untuk setiap penyaluran

2. **Eksekusi Penyaluran:**
   - PIC siapkan daftar penerima
   - Beli barang (jika donasi barang) atau siapkan uang
   - Salurkan ke penerima
   - Dokumentasi (foto/video)

3. **Catat Penyaluran:**

**File:** `Keuangan/Donasi Disalurkan 2026.xlsx`

**Columns:**
```
| Tanggal Salur | Kode Donasi | Penerima | Lokasi | Nominal Salur | Program | PIC | Bukti |
|---------------|-------------|----------|--------|---------------|---------|-----|-------|
| 20 Jun | DON-20260617-001 | Pak Slamet | Sleman | 500.000 | Sembako | [Nama] | [Link Foto] |
```

4. **Update Spreadsheet Donasi Masuk:**
   - Kolom "Status Salur": ✅ Disalurkan + tanggal

#### **5. Laporkan ke Donatur (Admin)**

**Timeline:** Max 3 hari setelah penyaluran

**Via WA/Email (Template):**

```
Assalamu'alaikum Warahmatullahi Wabarakatuh

Kak [Nama Donatur] yang dirahmati Allah,

Alhamdulillah, donasi Kakak telah kami salurkan dengan detail:

LAPORAN PENYALURAN
━━━━━━━━━━━━━━━━━━━━
Kode Donasi    : [KODE-XXX]
Tanggal Salur  : [DD MMM YYYY]
Penerima       : [Nama/Kategori penerima]
Lokasi         : [Desa/Kecamatan/Kabupaten]
Bentuk         : [Sembako/Uang Tunai/Alat Sekolah/etc]
Nominal        : Rp [Nominal]
━━━━━━━━━━━━━━━━━━━━

[FOTO PENYALURAN - 2-3 foto]

Semoga donasi Kakak menjadi amal jariyah yang terus mengalir pahalanya. Aamiin Yaa Rabbal 'Alamiin.

Untuk laporan lengkap program ini, bisa cek di:
🌐 [Link blog/instagram post]

Jazakumullah khairan katsiran.

Wassalamu'alaikum Warahmatullahi Wabarakatuh,

Hormat kami,
Amal Shalih Insan Bantul
```

**Update Spreadsheet:**
- Kolom "Status Laporan": ✅ Reported + tanggal

---

## 📝 Pencatatan & Validasi

### **Spreadsheets Required:**

**1. Donasi Masuk** (`Keuangan/Donasi Masuk 2026.xlsx`)
- Track semua donasi yang masuk
- Status: Confirmed, Pending, Disalurkan, Reported

**2. Donasi Disalurkan** (`Keuangan/Donasi Disalurkan 2026.xlsx`)
- Track semua penyaluran
- Link ke donasi asli (via Kode Donasi)

**3. Rekap Bulanan** (`Keuangan/Rekap Bulanan/YYYY-MM.xlsx`)
- Summary donasi masuk per kategori
- Summary donasi disalurkan per program
- Saldo akhir bulan

**4. Donatur Database** (`Keuangan/Database Donatur.xlsx`)
- Nama, kontak, preferensi donasi
- History donasi per donatur
- Segmentasi: Aktif, Tidak Aktif (>3 bulan), Besar, Rutin

### **Validasi Checklist:**

**Setiap donasi masuk harus:**
- [ ] Tercatat di spreadsheet (max 24 jam)
- [ ] Dikonfirmasi ke donatur (max 24 jam)
- [ ] Diberi kode unik (KODE-YYYYMMDD-XXX)
- [ ] Dikategorikan (program, channel)

**Setiap penyaluran harus:**
- [ ] Ada dokumentasi (foto/video)
- [ ] Tercatat di spreadsheet (max 24 jam)
- [ ] Link ke donasi asli (traceable)
- [ ] Dilaporkan ke donatur (max 3 hari)

### **Audit Trail:**

**Setiap transaksi harus bisa ditelusuri:**
```
Donatur → Donasi Masuk → Kode Donasi → Penyaluran → Penerima → Laporan
```

**Jika ada pertanyaan:**
- "Donasi dari [Nama] tanggal [X] disalurkan kemana?" → Bisa jawab dalam 5 menit
- "Program [X] dananya dari mana saja?" → Bisa list semua donatur

---

## 📤 Penyaluran Donasi

### **Program-based Penyaluran:**

#### **1. Program Sembako Rutin**

**Frequency:** Mingguan/Bulanan  
**Target:** 50-100 keluarga per bulan  
**Budget:** Rp 150.000 - Rp 200.000 per paket

**Process:**
1. Bendahara alokasikan dana dari donasi "Sembako" + "Umum"
2. Admin + Relawan belanja sembako
3. Pack dalam kantong sembako
4. Distribusi ke penerima (data dari database)
5. Dokumentasi & laporan

#### **2. Program Pendidikan**

**Forms:**
- Beasiswa bulanan untuk anak yatim/dhuafa
- Bantuan alat sekolah (tahun ajaran baru)
- Biaya ujian/syahriah

**Process:**
1. Verifikasi penerima (survey jika perlu)
2. Tentukan nominal & durasi bantuan
3. Salurkan via transfer/tunai
4. Monitoring berkala (nilai sekolah, attendance)
5. Laporan ke donatur (progress penerima)

#### **3. Program Kesehatan**

**Forms:**
- Bantuan biaya berobat
- Bantuan ambulans
- Bantuan obat-obatan

**Priority:** 🚨 HIGH (urgent cases)

**Process:**
1. Terima aduan/kasus (via WA/email)
2. Survey & validasi (kunjungan/rumah sakit)
3. Estimasi biaya
4. Alokasikan dana (bisa gabungan beberapa donatur)
5. Salurkan ke RS/pasien
6. Follow-up progress

#### **4. Program Mendesak (Bencana)**

**Examples:** Banjir, gempa, kebakaran

**Response Time:** 24-48 jam

**Process:**
1. Monitor info bencana (media, jaringan relawan)
2. Assess kebutuhan (tim survey ke lokasi)
3. Launch campaign donasi (IG, WA, FB)
4. Kumpulkan donasi (cepat!)
5. Belanja kebutuhan (sembako, selimut, obat)
6. Distribusi ke pengungsi
7. Laporan real-time ke donatur

### **Approval Matrix:**

| Nominal | Approval Required | Timeline |
|---------|-------------------|----------|
| **< Rp 500.000** | Bendahara | Same day |
| **Rp 500.000 - 2.000.000** | Bendahara + Koordinator Program | 1-2 days |
| **Rp 2.000.000 - 5.000.000** | Pengurus | 2-3 days |
| **> Rp 5.000.000** | Rapat Pengurus | 3-5 days |
| **Urgent (medis/bencana)** | Bendahara (fast-track) | 24 hours |

---

## 📊 Pelaporan & Transparansi

### **Laporan Harian (Internal)**

**File:** `Keuangan/Laporan Harian/YYYY-MM-DD.md`

**Template:**
```markdown
# Laporan Harian - DD MMM YYYY

## Donasi Masuk
- Total: Rp XXX.XXX
- Count: XX donasi
- Largest: Rp XXX.XXX (Donatur: [Nama])

## Donasi Disalurkan
- Total: Rp XXX.XXX
- Program: [Nama Program]
- Penerima: XX keluarga/orang

## Saldo Kas
- BSI: Rp XXX.XXX
- Tunai: Rp XXX.XXX
- Total: Rp XXX.XXX

## Notes
- [Issue/catatan penting]
```

### **Laporan Mingguan (Internal)**

**File:** `Keuangan/Laporan Mingguan/YYYY-WXX.md`

**Template:**
```markdown
# Laporan Mingguan - Week XX (DD-DD MMM YYYY)

## Summary
| Kategori | Masuk | Disalurkan | Saldo |
|----------|-------|-------------|-------|
| Sembako | XXX | XXX | XXX |
| Pendidikan | XXX | XXX | XXX |
| Kesehatan | XXX | XXX | XXX |
| Umum | XXX | XXX | XXX |
| **TOTAL** | **XXX** | **XXX** | **XXX** |

## Highlight
- Donasi terbesar: Rp XXX dari [Nama]
- Penyaluran terbesar: Program [X] - Rp XXX
- Donatur baru: XX orang
- Issue: [Jika ada]

## Next Week Focus
- [Priority 1]
- [Priority 2]
```

### **Laporan Bulanan (Publik)**

**Publish:** Website blog, Instagram carousel, Facebook post  
**Timeline:** Max 10 hari setelah bulan berakhir

**Template:** [Lihat Template Laporan Bulanan](../30-templates/laporan-bulanan.md)

**Content:**
- Infografis: Donasi masuk vs disalurkan
- Breakdown per program
- Cerita dampak (testimonial penerima)
- Ucapan terima kasih ke donatur
- Call-to-action untuk bulan depan

### **Laporan Tahunan (Publik)**

**Publish:** Website, PDF download, printed untuk stakeholder  
**Timeline:** Max 3 bulan setelah tahun berakhir

**Content:**
- Executive summary
- Financial highlights (grafik, chart)
- Program highlights (cerita, foto)
- List donatur (dengan izin)
- Thank you message
- Plan tahun depan

---

## 🔍 Rekonsiliasi & Audit

### **Monthly Reconciliation (Bendahara)**

**Timeline:** Akhir bulan (tanggal 28-30)

**Checklist:**
1. [ ] Cocokkan mutasi bank dengan spreadsheet donasi masuk
2. [ ] Hitung total donasi masuk (bank + QRIS + tunai)
3. [ ] Hitung total donasi disalurkan
4. [ ] Hitung saldo seharusnya
5. [ ] Bandingkan dengan saldo bank aktual
6. [ ] Investigasi selisih (jika ada)
7. [ ] Buat laporan rekonsiliasi

**File:** `Keuangan/Rekonsiliasi/YYYY-MM-Rekonsiliasi.xlsx`

### **Quarterly Audit (Pengurus)**

**Timeline:** Setiap 3 bulan (Mar, Jun, Sep, Dec)

**Process:**
1. Pengurus review semua laporan bulanan
2. Sample check: Pilih 5-10 donasi random, trace dari masuk → salur
3. Review spreadsheet completeness
4. Cek dokumentasi penyaluran
5. Buat laporan audit (jika ada temuan)

**Template:** `Keuangan/Audit/YYYY-QX-Audit-Report.md`

### **Annual Audit (External - Optional)**

**Untuk kredibilitas:**
- Invite auditor independen (akuntan publik)
- Full audit financial records
- Issue audit opinion
- Publish summary untuk publik

---

## 🛠️ Template & Tools

### **Templates:**
- 📄 [Kwitansi Donasi](../30-templates/kwitansi-donasi.md)
- 📊 [Laporan Bulanan](../30-templates/laporan-bulanan.md)
- 📧 [Email Konfirmasi Donasi](../30-templates/email-donasi.md)
- 💬 [WA Templates Donasi](../30-templates/wa-donasi.md)

### **Tools:**
- **BSI Mobile/Internet Banking** — Cek mutasi rekening
- **Google Sheets** — Pencatatan donasi
- **Google Drive** — Storage dokumentasi
- **Trello** — Track workflow donasi
- **Canva** — Design laporan infografis

### **Kode Donasi Format:**

```
KODE-YYYYMMDD-XXX

Contoh: DON-20260617-001
- DON = Donasi
- 20260617 = Tanggal 17 Juni 2026
- 001 = Urutan ke-1 hari itu
```

---

## 📞 Contact & Escalation

| Issue | Contact |
|-------|---------|
| **Donasi Masuk (konfirmasi)** | Admin: amalshalih.insanbantul@gmail.com |
| **Donasi Disalurkan (laporan)** | Bendahara: [Email Bendahara] |
| **Komplain Donatur** | Pengurus: [Email Pengurus] |
| **Technical (payment gateway)** | IT: timitasib@gmail.com |

---

**Dokumen ini internal — jangan share ke pihak luar**  
**Last reviewed:** 7 Juni 2026  
**Next review:** 7 Desember 2026