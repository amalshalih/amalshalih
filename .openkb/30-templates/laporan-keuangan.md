# 📊 Laporan Keuangan Template

> Template laporan keuangan bulanan dan tahunan untuk Yayasan Amal Shalih Insan Bantul

**Last Updated:** 7 Juni 2026  
**Status:** 🟢 Active  
**Applies to:** Bendahara, Pengurus, Auditor

---

## 📋 Informasi Template

**Frequency:** Bulanan (internal), Tahunan (publik & audit)  
**Tools:** Google Sheets (primary), Excel (alternative)  
**Compliance:** Standar Akuntansi Keuangan (SAK) untuk Organisasi Nirlaba  
**Audit:** Annual external audit recommended

---

## 📊 Template Laporan Bulanan

### **Cover Page**

```
┌─────────────────────────────────────────────────────────────────────────┐
│                    YAYASAN AMAL SHALIH INSAN BANTUL                      │
│                          LAPORAN KEUANGAN BULANAN                        │
│                                                                          │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  Periode        : [Bulan] [YYYY]                                         │
│  Tanggal        : [DD] [Bulan] [YYYY]                                    │
│  Disiapkan oleh : [Nama Bendahara]                                       │
│  Direview oleh  : [Nama Pengurus]                                        │
│                                                                          │
│  Status         : ⏳ Draft / 👀 Review / ✅ Final                        │
│                                                                          │
├─────────────────────────────────────────────────────────────────────────┤
│  HIGHLIGHT BULAN INI                                                     │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  💰 Total Pemasukan     : Rp [XXX,XXX,XXX]  ([+X%] vs bulan lalu)        │
│  📦 Total Pengeluaran   : Rp [XXX,XXX,XXX]  ([+X%] vs bulan lalu)        │
│  💵 Surplus/(Defisit)   : Rp [XXX,XXX,XXX]                               │
│  🏦 Saldo Akhir         : Rp [XXX,XXX,XXX]                               │
│                                                                          │
│  📊 Pemasukan vs Target : [XX]% (Target: Rp XXX)                          │
│  📦 Pengeluaran vs Budget: [XX]% (Budget: Rp XXX)                         │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

### **Sheet 1: Ringkasan Keuangan (Summary)**

```
┌──────────────────────────────────────────────────────────────────────────┐
│  RINGKASAN KEUANGAN - [BULAN YYYY]                                       │
└──────────────────────────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────────────────────────┐
│  A. PEMASUKAN                                                            │
├──────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  1. Donasi Masuk                                                         │
│     - Donasi Umum                Rp XXX,XXX,XXX                          │
│     - Donasi Terikat             Rp XXX,XXX,XXX                          │
│     - Donasi Mendesak            Rp XXX,XXX,XXX                          │
│     - Donasi Barang (estimasi)   Rp XXX,XXX,XXX                          │
│     ─────────────────────────────────────────────                         │
│     Subtotal Donasi              Rp XXX,XXX,XXX                          │
│                                                                          │
│  2. Pendapatan Lain-lain                                                 │
│     - Bunga Bank                 Rp XXX,XXX                              │
│     - Pendapatan Usaha*          Rp XXX,XXX                              │
│     - Sponsorship                Rp XXX,XXX                              │
│     ─────────────────────────────────────────────                         │
│     Subtotal Lain-lain           Rp XXX,XXX                              │
│                                                                          │
│  ═══════════════════════════════════════════════════════════════════     │
│  TOTAL PEMASUKAN                 Rp XXX,XXX,XXX                          │
│  ═══════════════════════════════════════════════════════════════════     │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘

*Jika yayasan memiliki unit usaha

┌──────────────────────────────────────────────────────────────────────────┐
│  B. PENGELUARAN                                                          │
├──────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  1. Program Sosial                                                       │
│     - Sembako                    Rp XXX,XXX,XXX                          │
│     - Pendidikan                 Rp XXX,XXX,XXX                          │
│     - Kesehatan                  Rp XXX,XXX,XXX                          │
│     - Bencana                    Rp XXX,XXX,XXX                          │
│     ─────────────────────────────────────────────                         │
│     Subtotal Program             Rp XXX,XXX,XXX                          │
│                                                                          │
│  2. Biaya Operasional                                                    │
│     - Gaji Honorarium            Rp XXX,XXX                              │
│     - Transport                  Rp XXX,XXX                              │
│     - Konsumsi                   Rp XXX,XXX                              │
│     - ATK & Administrasi         Rp XXX,XXX                              │
│     - Listrik, Air, Internet     Rp XXX,XXX                              │
│     - Sewa Kantor                Rp XXX,XXX                              │
│     ─────────────────────────────────────────────                         │
│     Subtotal Operasional         Rp XXX,XXX                              │
│                                                                          │
│  3. Biaya Fundraising                                                    │
│     - Marketing & Sosmed         Rp XXX,XXX                              │
│     - Event Fundraising          Rp XXX,XXX                              │
│     - Cetak Materi               Rp XXX,XXX                              │
│     ─────────────────────────────────────────────                         │
│     Subtotal Fundraising         Rp XXX,XXX                              │
│                                                                          │
│  4. Biaya Lain-lain                                                      │
│     - Audit & Akuntan            Rp XXX,XXX                              │
│     - Perizinan                  Rp XXX,XXX                              │
│     - Dana Darurat               Rp XXX,XXX                              │
│     ─────────────────────────────────────────────                         │
│     Subtotal Lain-lain           Rp XXX,XXX                              │
│                                                                          │
│  ═══════════════════════════════════════════════════════════════════     │
│  TOTAL PENGELUARAN               Rp XXX,XXX,XXX                          │
│  ═══════════════════════════════════════════════════════════════════     │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────────────────────────┐
│  C. SURPLUS / (DEFISIT)                                                  │
├──────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  Total Pemasukan                 Rp XXX,XXX,XXX                          │
│  Total Pengeluaran               Rp XXX,XXX,XXX                          │
│  ─────────────────────────────────────────────                           │
│  SURPLUS / (DEFISIT)             Rp XXX,XXX,XXX                          │
│                                                                          │
│  Ratio Efisiensi:                                                        │
│  - Program / Total Pengeluaran   = [XX]%  (Target: min 80%)              │
│  - Operasional / Total Pemasukan = [XX]%  (Target: max 15%)              │
│  - Fundraising / Total Pemasukan = [XX]%  (Target: max 5%)               │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────────────────────────┐
│  D. SALDO KAS                                                            │
├──────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  Saldo Awal Bulan                Rp XXX,XXX,XXX                          │
│  (+) Surplus / (Defisit)         Rp XXX,XXX,XXX                          │
│  ─────────────────────────────────────────────                           │
│  SALDO AKHIR BULAN               Rp XXX,XXX,XXX                          │
│                                                                          │
│  Komposisi Saldo:                                                        │
│  - Bank BSI                      Rp XXX,XXX,XXX  ([XX]%)                 │
│  - Kas Tunai                     Rp XXX,XXX      ([XX]%)                 │
│  - Kas Bank Lain                 Rp XXX,XXX,XXX  ([XX]%)                 │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘
```

---

### **Sheet 2: Detail Donasi Masuk**

```
┌──────────────────────────────────────────────────────────────────────────┐
│  DETAIL DONASI MASUK - [BULAN YYYY]                                      │
└──────────────────────────────────────────────────────────────────────────┘

┌──────┬────────────┬──────────────┬───────────┬─────────┬──────────────┐
│ Tgl  │ Kode       │ Donatur      │ Nominal   │ Channel │ Program      │
├──────┼────────────┼──────────────┼───────────┼─────────┼──────────────┤
│ 01/6 │ DON-001    │ H. Abdullah  │ 500,000   │ Transfer│ Sembako      │
│ 01/6 │ DON-002    │ Anonymous    │ 100,000   │ QRIS    │ Umum         │
│ 02/6 │ DON-003    │ PT ABC       │ 5,000,000 │ Transfer│ Pendidikan   │
│ ...  │ ...        │ ...          │ ...       │ ...     │ ...          │
├──────┴────────────┴──────────────┴───────────┴─────────┴──────────────┤
│ TOTAL DONASI MASUK:                    Rp XXX,XXX,XXX                  │
│ JUMLAH DONATUR:                        [XXX] donatur                   │
│ RATA-RATA DONASI:                      Rp XXX,XXX per donatur          │
└──────────────────────────────────────────────────────────────────────────┘

Breakdown per Kategori:
┌──────────────────┬──────────────┬────────────┬─────────────────────────┐
│ Kategori         │ Nominal      │ %          │ Jumlah Donatur          │
├──────────────────┼──────────────┼────────────┼─────────────────────────┤
│ Donasi Umum      │ Rp XXX,XXX   │ [XX]%      │ [XX] donatur            │
│ Donasi Sembako   │ Rp XXX,XXX   │ [XX]%      │ [XX] donatur            │
│ Donasi Pendidikan│ Rp XXX,XXX   │ [XX]%      │ [XX] donatur            │
│ Donasi Kesehatan │ Rp XXX,XXX   │ [XX]%      │ [XX] donatur            │
│ Donasi Mendesak  │ Rp XXX,XXX   │ [XX]%      │ [XX] donatur            │
├──────────────────┼──────────────┼────────────┼─────────────────────────┤
│ TOTAL            │ Rp XXX,XXX   │ 100%       │ [XXX] donatur           │
└──────────────────┴──────────────┴────────────┴─────────────────────────┘

Top 10 Donatur (Bulan Ini):
┌─────┬──────────────────────┬────────────────┬──────────────────────────┐
│ No  │ Nama Donatur         │ Total Donasi   │ Frekuensi                │
├─────┼──────────────────────┼────────────────┼──────────────────────────┤
│ 1   │ [Nama]               │ Rp XXX,XXX,XXX │ [X] kali                 │
│ 2   │ [Nama]               │ Rp XXX,XXX,XXX │ [X] kali                 │
│ 3   │ [Nama]               │ Rp XXX,XXX,XXX │ [X] kali                 │
│ ... │ ...                  │ ...            │ ...                      │
└─────┴──────────────────────┴────────────────┴──────────────────────────┘
```

---

### **Sheet 3: Detail Pengeluaran per Program**

```
┌──────────────────────────────────────────────────────────────────────────┐
│  DETAIL PENGELUARAN PER PROGRAM - [BULAN YYYY]                           │
└──────────────────────────────────────────────────────────────────────────┘

PROGRAM: [Nama Program]
PIC: [Nama PIC]
Periode: [DD-MM] [Bulan] [YYYY]

┌──────┬────────────┬──────────────────────┬──────┬───────────┬──────────┐
│ Tgl  │ Kode       │ Uraian               │ Vol  │ Harga     │ Total    │
│      │            │                      │      │ Satuan    │          │
├──────┼────────────┼──────────────────────┼──────┼───────────┼──────────┤
│ 05/6 │ OUT-001    │ Beras Premium 5kg    │ 150  │ 65,000    │ 9,750,00 │
│ 05/6 │ OUT-002    │ Minyak Goreng 2L     │ 150  │ 35,000    │ 5,250,00 │
│ 05/6 │ OUT-003    │ Gula Pasir 1kg       │ 150  │ 14,000    │ 2,100,00 │
│ ...  │ ...        │ ...                  │ ...  │ ...       │ ...      │
├──────┴────────────┴──────────────────────┴──────┴───────────┴──────────┤
│ TOTAL PROGRAM [Nama]:                    Rp XX,XXX,XXX                  │
│ JUMLAH PENERIMA:                       [XXX] keluarga/orang             │
│ BIAYA PER PENERIMA:                    Rp XXX,XXX                       │
└──────────────────────────────────────────────────────────────────────────┘

Summary Semua Program:
┌──────────────────────┬────────────────┬────────────┬────────────────────┐
│ Nama Program         │ Anggaran       │ Realisasi  │ Variance           │
├──────────────────────┼────────────────┼────────────┼────────────────────┤
│ Jumat Berkah         │ Rp 15,000,000  │ Rp 14,500K │ +500K (Under)      │
│ Beasiswa Pendidikan  │ Rp 10,000,000  │ Rp 10,200K │ -200K (Over)       │
│ Bantuan Medis        │ Rp 8,000,000   │ Rp 7,800K  │ +200K (Under)      │
│ Tanggap Bencana      │ Rp 20,000,000  │ Rp 0       │ +20M (Unused)      │
├──────────────────────┼────────────────┼────────────┼────────────────────┤
│ TOTAL                │ Rp 53,000,000  │ Rp 32,500K │ +20.5M (38% used)  │
└──────────────────────┴────────────────┴────────────┴────────────────────┘
```

---

### **Sheet 4: Laporan Arus Kas (Cash Flow)**

```
┌──────────────────────────────────────────────────────────────────────────┐
│  LAPORAN ARUS KAS - [BULAN YYYY]                                         │
└──────────────────────────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────────────────────────┤
│  ARUS KAS DARI AKTIVITAS OPERASIONAL                                     │
├──────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  Penerimaan:                                                             │
│  - Penerimaan Donasi              Rp XXX,XXX,XXX                         │
│  - Penerimaan Lain-lain           Rp XXX,XXX                             │
│  ─────────────────────────────────────────────                           │
│  Total Penerimaan Operasional     Rp XXX,XXX,XXX                         │
│                                                                          │
│  Pengeluaran:                                                            │
│  - Program Sosial                 Rp (XXX,XXX,XXX)                       │
│  - Biaya Operasional              Rp (XX,XXX,XXX)                        │
│  - Biaya Fundraising              Rp (X,XXX,XXX)                         │
│  ─────────────────────────────────────────────                           │
│  Total Pengeluaran Operasional    Rp (XXX,XXX,XXX)                       │
│                                                                          │
│  ═══════════════════════════════════════════════════════════════════     │
│  KAS BERSIH DARI AKTIVITAS OPERASIONAL  Rp XXX,XXX,XXX                  │
│  ═══════════════════════════════════════════════════════════════════     │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────────────────────────┤
│  ARUS KAS DARI AKTIVITAS INVESTASI (jika ada)                            │
├──────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  - Pembelian Aset Tetap           Rp (X,XXX,XXX)                         │
│  - Penjualan Aset                 Rp XXX,XXX                             │
│  ─────────────────────────────────────────────                           │
│  KAS BERSIH DARI AKTIVITAS INVESTASI    Rp (X,XXX,XXX)                  │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────────────────────────┤
│  ARUS KAS DARI AKTIVITAS PENDANAAN (jika ada)                            │
├──────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  - Pinjaman/Dana Hibah            Rp XXX,XXX,XXX                         │
│  - Pembayaran Pinjaman            Rp (X,XXX,XXX)                         │
│  ─────────────────────────────────────────────                           │
│  KAS BERSIH DARI AKTIVITAS PENDANAAN    Rp XXX,XXX,XXX                  │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────────────────────────┤
│  KENAIKAN / (PENURUNAN) KAS                                              │
├──────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  Kas Bersih dari Aktivitas                                              │
│  Operasional                    Rp XXX,XXX,XXX                          │
│  Kas Bersih dari Aktivitas Investasi    Rp (X,XXX,XXX)                  │
│  Kas Bersih dari Aktivitas Pendanaan    Rp XXX,XXX,XXX                  │
│  ─────────────────────────────────────────────                           │
│  KENAIKAN / (PENURUNAN) KAS     Rp XXX,XXX,XXX                          │
│                                                                          │
│  Saldo Kas Awal Periode         Rp XXX,XXX,XXX                          │
│  ─────────────────────────────────────────────                           │
│  SALDO KAS AKHIR PERIODE        Rp XXX,XXX,XXX                          │
│  ═══════════════════════════════════════════════════════════════════     │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘
```

---

### **Sheet 5: Neraca (Balance Sheet)**

```
┌──────────────────────────────────────────────────────────────────────────┐
│  NERACA - [DD BULAN YYYY]                                                │
└──────────────────────────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────────────────────────┤
│  ASET                                                                    │
├──────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  ASET LANCAR                                                             │
│  - Kas dan Bank                   Rp XXX,XXX,XXX                         │
│  - Piutang                        Rp X,XXX,XXX                           │
│  - Perlengkapan                   Rp X,XXX,XXX                           │
│  - Biaya Dibayar Dimuka           Rp X,XXX,XXX                           │
│  ─────────────────────────────────────────────                           │
│  Total Aset Lancar                Rp XXX,XXX,XXX                         │
│                                                                          │
│  ASET TETAP                                                              │
│  - Kendaraan                      Rp XXX,XXX,XXX                         │
│  - Peralatan Kantor               Rp XX,XXX,XXX                          │
│  - Akumulasi Penyusutan           Rp (XX,XXX,XXX)                        │
│  - Aset Lainnya                   Rp X,XXX,XXX                           │
│  ─────────────────────────────────────────────                           │
│  Total Aset Tetap                 Rp XXX,XXX,XXX                         │
│                                                                          │
│  ═══════════════════════════════════════════════════════════════════     │
│  TOTAL ASET                       Rp XXX,XXX,XXX                         │
│  ═══════════════════════════════════════════════════════════════════     │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────────────────────────┤
│  LIABILITAS                                                              │
├──────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  LIABILITAS JANGKA PENDEK                                                │
│  - Utang Usaha                    Rp X,XXX,XXX                           │
│  - Biaya Masih Harus Dibayar      Rp X,XXX,XXX                           │
│  - Dana Yang Belum Disalurkan     Rp XX,XXX,XXX                          │
│  ─────────────────────────────────────────────                           │
│  Total Liabilitas Jangka Pendek   Rp XX,XXX,XXX                          │
│                                                                          │
│  LIABILITAS JANGKA PANJANG                                              │
│  - Pinjaman Jangka Panjang        Rp X,XXX,XXX                           │
│  ─────────────────────────────────────────────                           │
│  Total Liabilitas Jangka Panjang  Rp X,XXX,XXX                           │
│                                                                          │
│  ═══════════════════════════════════════════════════════════════════     │
│  TOTAL LIABILITAS                 Rp XX,XXX,XXX                          │
│  ═══════════════════════════════════════════════════════════════════     │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────────────────────────┤
│  SALDO DANA                                                              │
├──────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  - Saldo Dana Awal Tahun          Rp XXX,XXX,XXX                         │
│  - Surplus / (Defisit) Berjalan   Rp XX,XXX,XXX                          │
│  - Penyesuaian                    Rp X,XXX,XXX                           │
│  ─────────────────────────────────────────────                           │
│  Total Saldo Dana                 Rp XXX,XXX,XXX                         │
│                                                                          │
│  ═══════════════════════════════════════════════════════════════════     │
│  TOTAL LIABILITAS + SALDO DANA    Rp XXX,XXX,XXX                         │
│  ═══════════════════════════════════════════════════════════════════     │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘

Check: Total Aset = Total Liabilitas + Saldo Dana ✅
```

---

### **Sheet 6: Catatan atas Laporan Keuangan (CaLK)**

```
┌──────────────────────────────────────────────────────────────────────────┐
│  CATATAN ATAS LAPORAN KEUANGAN                                           │
│  [BULAN/YEAR] [YYYY]                                                     │
└──────────────────────────────────────────────────────────────────────────┘

1. INFORMASI UMUM

   a. Nama Yayasan    : Yayasan Amal Shalih Insan Bantul
   b. Alamat          : [Alamat Lengkap]
   c. Tanggal Pendirian: [DD MMM YYYY]
   d. Akta Notaris    : [Nomor & Tanggal]
   e. SK Kemenkumham  : [Nomor & Tanggal]
   f. NPWPP           : [Nomor]
   g. Bidang Kegiatan : Pendidikan Islam, Sosial Kemanusiaan, Keagamaan

2. KEBIJAKAN AKUNTANSI

   a. Dasar Penyusunan
      Laporan keuangan disusun berdasarkan Standar Akuntansi Keuangan
      (SAK) untuk Organisasi Nirlaba.
   
   b. Metode Pengakuan Donasi
      Donasi diakui sebagai pendapatan pada saat diterima.
      Donasi terikat diakui sebagai liabilitas sampai disalurkan.
   
   c. Metode Penilaian Aset
      Aset tetap dinilai berdasarkan harga perolehan dan
      disusutkan menggunakan metode garis lurus.

3. RINCIAN POS-POS LAPORAN KEUANGAN

   a. Kas dan Bank
      - Bank BSI         : Rp XXX,XXX,XXX
      - Kas Tunai        : Rp X,XXX,XXX
      - Total            : Rp XXX,XXX,XXX
   
   b. Donasi Terikat
      - Donasi Sembako   : Rp XX,XXX,XXX
      - Donasi Pendidikan: Rp XX,XXX,XXX
      - Total            : Rp XX,XXX,XXX
   
   c. Biaya Operasional
      - Honorarium       : Rp X,XXX,XXX
      - Transport        : Rp X,XXX,XXX
      - ATK              : Rp X,XXX,XXX
      - Total            : Rp X,XXX,XXX

4. PROGRAM YANG DILAKSANAKAN

   [List semua program dengan ringkasan anggaran & realisasi]

5. INFORMASI LAIN-LAIN

   - Transaksi dengan pihak berelasi (jika ada)
   - Komitmen & kontinjensi
   - Event setelah tanggal neraca
   - dll.
```

---

## 📊 Template Laporan Tahunan

### **Structure:**

```
LAPORAN TAHUNAN YAYASAN ASIB - [YYYY]

1. Surat dari Ketua Yayasan
2. Profil Yayasan
3. Highlights Tahun Ini
4. Laporan Keuangan (Full Set)
   - Laporan Realisasi Anggaran
   - Laporan Arus Kas
   - Neraca
   - CaLK
5. Laporan Program
6. Terima Kasih kepada Donatur
7. Rencana Tahun Depan
8. Lampiran (Audit Report jika ada)
```

---

## 📞 Contact & Support

| Role | Contact |
|------|---------|
| **Template Access** | Bendahara: [Email Bendahara] |
| **Financial Review** | Bendahara: [Email Bendahara] |
| **Audit Coordination** | Pengurus: [Email Pengurus] |
| **Approval** | Pengurus: [Email Pengurus] |

---

**Template ini living document - update sesuai kebutuhan!**

**Last reviewed:** 7 Juni 2026  
**Next review:** 7 Desember 2026  
**Maintained by:** Bendahara & Pengurus

---

*"Financial transparency is not just about compliance—it's about building trust with every stakeholder."*