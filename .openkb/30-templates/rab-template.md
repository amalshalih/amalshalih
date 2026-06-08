# 📊 RAB Template (Rencana Anggaran Biaya)

> Template perencanaan anggaran untuk kegiatan dan program Yayasan ASIB

**Last Updated:** 7 Juni 2026  
**Status:** 🟢 Active  
**Applies to:** Pengurus, Bendahara, Koordinator Program, PIC Kegiatan

---

## 📋 Informasi Template

**Tools:** Google Sheets (primary), Excel (alternative)  
**Use Case:** Proposal kegiatan, budget planning, financial approval  
**Approval Flow:** PIC → Koordinator → Bendahara → Pengurus

---

## 📊 Template Structure

### **Sheet 1: Cover & Summary**

```
┌─────────────────────────────────────────────────────────────────────────┐
│                    YAYASAN AMAL SHALIH INSAN BANTUL                      │
│                          RENCANA ANGGARAN BIAYA                          │
│                                                                          │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  NAMA KEGIATAN    : [Nama Kegiatan/Program]                              │
│  TEMA             : [Tema Kegiatan]                                      │
│  WAKTU PELAKSANAAN: [Hari, Tanggal, Jam]                                 │
│  LOKASI           : [Alamat Lengkap]                                     │
│  PENANGGUNG JAWAB : [Nama PIC]                                           │
│  KOORDINATOR      : [Nama Koordinator]                                   │
│                                                                          │
├─────────────────────────────────────────────────────────────────────────┤
│  RINGKASAN ANGGARAN                                                      │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  TOTAL PENGELUARAN    : Rp [XXX,XXX,XXX]                                 │
│  (-) Dana Kas Yayasan : Rp [XXX,XXX,XXX]                                 │
│  (-) Donasi Terikat   : Rp [XXX,XXX,XXX]                                 │
│                                                                          │
│  = DEFISIT/SURPLUS    : Rp [XXX,XXX,XXX]                                 │
│                                                                          │
│  SUMBER DANA:                                                            │
│  1. Kas Yayasan       : Rp [XXX,XXX,XXX] ([XX]%)                         │
│  2.Donasi Terikat     : Rp [XXX,XXX,XXX] ([XX]%)                         │
│  3. Sponsorship       : Rp [XXX,XXX,XXX] ([XX]%)                         │
│  4. Lain-lain         : Rp [XXX,XXX,XXX] ([XX]%)                         │
│                                                                          │
├─────────────────────────────────────────────────────────────────────────┤
│  STATUS: ⏳ Draft / 👀 Review / ✅ Approved / ❌ Rejected                │
│                                                                          │
│  Disetujui oleh:                       Dibuat oleh:                      │
│                                                                          │
│                                                                          │
│  [Nama Pengurus]                       [Nama PIC]                        │
│  Pengurus                              PIC Kegiatan                      │
│                                                                          │
│  Tanggal: ___________                  Tanggal: ___________              │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

### **Sheet 2: Detailed Budget (Main Sheet)**

**Format:**
```
┌──────────────────────────────────────────────────────────────────────────┐
│  RENCANA ANGGARAN BIAYA - DETAIL                                         │
│  Kegiatan: [Nama Kegiatan]                                               │
└──────────────────────────────────────────────────────────────────────────┘

┌─────┬──────────────┬───────────────────────┬──────┬───────────┬─────────┬────────────┐
│ No  │ Kategori     │ Uraian                │ Vol  │ Unit      │ Harga   │ Total      │
│     │              │                       │      │           │ Satuan  │            │
├─────┼──────────────┼───────────────────────┼──────┼───────────┼─────────┼────────────┤
│ 1   │ KESEKRETARIATAN                      │      │           │         │            │
├─────┼──────────────┼───────────────────────┼──────┼───────────┼─────────┼────────────┤
│ 1.1 │              │ Proposal & Surat      │ 10   │ Lembar    │ 500     │ 5,000      │
│ 1.2 │              │ Spanduk               │ 1    │ Buah      │ 150,000 │ 150,000    │
│ 1.3 │              │ ID Card Panitia       │ 20   │ Lembar    │ 5,000   │ 100,000    │
│ 1.4 │              │ ATK Panitia           │ 1    │ Paket     │ 100,000 │ 100,000    │
├─────┴──────────────┴───────────────────────┴──────┴───────────┴─────────┼────────────┤
│                                                                          │ Subtotal:  │
│                                                                          │ 355,000    │
└──────────────────────────────────────────────────────────────────────────┴────────────┘

┌─────┬──────────────┬───────────────────────┬──────┬───────────┬─────────┬────────────┐
│ 2   │ ACARA & VENUE                          │      │           │         │            │
├─────┼──────────────┼───────────────────────┼──────┼───────────┼─────────┼────────────┤
│ 2.1 │              │ Sewa Tempat           │ 1    │ Hari      │ 500,000 │ 500,000    │
│ 2.2 │              │ Sound System          │ 1    │ Paket     │ 750,000 │ 750,000    │
│ 2.3 │              │ Dekorasi              │ 1    │ Paket     │ 300,000 │ 300,000    │
│ 2.4 │              │ Dokumentasi           │ 1    │ Paket     │ 400,000 │ 400,000    │
├─────┴──────────────┴───────────────────────┴──────┴───────────┴─────────┼────────────┤
│                                                                          │ Subtotal:  │
│                                                                          │ 1,950,000  │
└──────────────────────────────────────────────────────────────────────────┴────────────┘

┌─────┬──────────────┬───────────────────────┬──────┬───────────┬─────────┬────────────┐
│ 3   │ KONSUMSI                             │      │           │         │            │
├─────┼──────────────┼───────────────────────┼──────┼───────────┼─────────┼────────────┤
│ 3.1 │              │ Makan Panitia         │ 20   │ Orang     │ 25,000  │ 500,000    │
│ 3.2 │              │ Snack Peserta         │ 100  │ Box       │ 10,000  │ 1,000,000  │
│ 3.3 │              │ Air Mineral           │ 10   │ Dus       │ 50,000  │ 500,000    │
│ 3.4 │              │ Makan Penerima        │ 150  │ Paket     │ 20,000  │ 3,000,000  │
├─────┴──────────────┴───────────────────────┴──────┴───────────┴─────────┼────────────┤
│                                                                          │ Subtotal:  │
│                                                                          │ 5,000,000  │
└──────────────────────────────────────────────────────────────────────────┴────────────┘

┌─────┬──────────────┬───────────────────────┬──────┬───────────┬─────────┬────────────┐
│ 4   │ BANTUAN LANGSUNG                       │      │           │         │            │
├─────┼──────────────┼───────────────────────┼──────┼───────────┼─────────┼────────────┤
│ 4.1 │              │ Sembako               │ 150  │ Paket     │ 150,000 │ 22,500,000 │
│ 4.2 │              │ Uang Tunai            │ 50   │ Orang     │ 100,000 │ 5,000,000  │
│ 4.3 │              │ Pakaian Layak         │ 100  │ Paket     │ 75,000  │ 7,500,000  │
├─────┴──────────────┴───────────────────────┴──────┴───────────┴─────────┼────────────┤
│                                                                          │ Subtotal:  │
│                                                                          │ 35,000,000 │
└──────────────────────────────────────────────────────────────────────────┴────────────┘

┌─────┬──────────────┬───────────────────────┬──────┬───────────┬─────────┬────────────┐
│ 5   │ TRANSPORTASI                           │      │           │         │            │
├─────┼──────────────┼───────────────────────┼──────┼───────────┼─────────┼────────────┤
│ 5.1 │              │ Transport Panitia     │ 10   │ Orang     │ 50,000  │ 500,000    │
│ 5.2 │              │ Transport Relawan     │ 20   │ Orang     │ 30,000  │ 600,000    │
│ 5.3 │              │ Transport Penerima    │ 50   │ Orang     │ 40,000  │ 2,000,000  │
├─────┴──────────────┴───────────────────────┴──────┴───────────┴─────────┼────────────┤
│                                                                          │ Subtotal:  │
│                                                                          │ 3,100,000  │
└──────────────────────────────────────────────────────────────────────────┴────────────┘

┌─────┬──────────────┬───────────────────────┬──────┬───────────┬─────────┬────────────┐
│ 6   │ LAIN-LAIN                              │      │           │         │            │
├─────┼──────────────┼───────────────────────┼──────┼───────────┼─────────┼────────────┤
│ 6.1 │              │ Dana Tak Terduga      │ 1    │ LS        │ 1,000,00│ 1,000,000  │
│     │              │ (5% dari total)       │      │           │ 0       │            │
├─────┴──────────────┴───────────────────────┴──────┴───────────┴─────────┼────────────┤
│                                                                          │ Subtotal:  │
│                                                                          │ 1,000,000  │
└──────────────────────────────────────────────────────────────────────────┴────────────┘

┌──────────────────────────────────────────────────────────────────────────┴────────────┐
│  TOTAL KESELURUHAN                                                      Rp 46,405,000 │
└───────────────────────────────────────────────────────────────────────────────────────┘
```

---

### **Sheet 3: Timeline Pengeluaran**

```
┌──────────────────────────────────────────────────────────────────────────┐
│  TIMELINE PENGELUARAN                                                    │
│  Kegiatan: [Nama Kegiatan]                                               │
└──────────────────────────────────────────────────────────────────────────┘

┌─────┬──────────────┬───────────────────────┬─────────────┬──────────────┐
│ No  │ Kategori     │ Total Anggaran        │ Waktu       │ Keterangan   │
│     │              │                       │ Pencairan   │              │
├─────┼──────────────┼───────────────────────┼─────────────┼──────────────┤
│ 1   │ Kesekretariatan│ Rp    355,000      │ H-14        │ Proposal,    │
│     │              │                       │             │ Spanduk      │
├─────┼──────────────┼───────────────────────┼─────────────┼──────────────┤
│ 2   │ Acara & Venue│ Rp  1,950,000      │ H-7         │ DP Tempat,   │
│     │              │                       │             │ Sound        │
├─────┼──────────────┼───────────────────────┼─────────────┼──────────────┤
│ 3   │ Konsumsi     │ Rp  5,000,000      │ H-3         │ Booking      │
│     │              │                       │             │ Katering     │
├─────┼──────────────┼───────────────────────┼─────────────┼──────────────┤
│ 4   │ Bantuan      │ Rp 35,000,000      │ H-1         │ Belanja      │
│     │ Langsung     │                       │             │ Sembako      │
├─────┼──────────────┼───────────────────────┼─────────────┼──────────────┤
│ 5   │ Transportasi │ Rp  3,100,000      │ H-1         │ Persiapan    │
├─────┼──────────────┼───────────────────────┼─────────────┼──────────────┤
│ 6   │ Lain-lain    │ Rp  1,000,000      │ Sesuai      │ Dana         │
│     │              │                       │ Kebutuhan   │ Darurat      │
├─────┴──────────────┴──────────────────────┴─────────────┴──────────────┤
│  TOTAL          │ Rp 46,405,000                                        │
└──────────────────────────────────────────────────────────────────────────┘

Keterangan:
H = Hari pelaksanaan kegiatan
```

---

### **Sheet 4: Sumber Dana**

```
┌──────────────────────────────────────────────────────────────────────────┐
│  SUMBER DANA                                                             │
│  Kegiatan: [Nama Kegiatan]                                               │
└──────────────────────────────────────────────────────────────────────────┘

┌─────┬──────────────┬───────────────────────┬─────────────┬──────────────┐
│ No  │ Sumber Dana  │ Nominal               │ Status      │ Keterangan   │
│     │              │                       │             │              │
├─────┼──────────────┼───────────────────────┼─────────────┼──────────────┤
│ 1   │ Kas Yayasan  │ Rp 10,000,000        │ ✅ Available│ Sudah di     │
│     │              │                       │             │ rekening     │
├─────┼──────────────┼───────────────────────┼─────────────┼──────────────┤
│ 2   │ Donasi       │ Rp 25,000,000        │ ⏳ Pending  │ Campaign     │
│     │ Terikat      │                       │             │ Instagram    │
├─────┼──────────────┼───────────────────────┼─────────────┼──────────────┤
│ 3   │ Sponsorship  │ Rp 10,000,000        │ 👀 Promised│ PT XYZ       │
│     │              │                       │             │ (LOI signed) │
├─────┼──────────────┼───────────────────────┼─────────────┼──────────────┤
│ 4   │ Donatur      │ Rp 1,405,000         │ ⏳ Pending  │ Individual   │
│     │ Individual   │                       │             │ donors       │
├─────┴──────────────┴──────────────────────┴─────────────┴──────────────┤
│  TOTAL            │ Rp 46,405,000                                      │
│  ✅ Confirmed     │ Rp 10,000,000 (21.5%)                              │
│  ⏳ Pending       │ Rp 36,405,000 (78.5%)                              │
└──────────────────────────────────────────────────────────────────────────┘

Risk Assessment:
⚠️ 78.5% dana masih pending - perlu aggressive fundraising
```

---

## 📝 Kategori Budget (Standard)

### **1. Kesekretariat (5-10% dari total)**

```
Items:
- Proposal printing & binding
- Surat-menyurat (perangko, amplop)
- Spanduk/banner
- ID Card panitia
- ATK (pulpen, kertas, map, etc)
- Fotocopy & dokumentasi admin

Budgeting Tips:
- Print double-sided untuk hemat kertas
- Use digital proposal jika possible
- Re-use ID card dari kegiatan sebelumnya
```

### **2. Acara & Venue (10-20% dari total)**

```
Items:
- Sewa tempat/gedung
- Sound system & lighting
- Dekorasi & panggung
- Dokumentasi (foto/video)
- MC/Host honorarium
- Peralatan acara

Budgeting Tips:
- Book venue early untuk discount
- Use in-house sound jika ada
- Negotiate package deal
```

### **3. Konsumsi (15-25% dari total)**

```
Items:
- Makan panitia & relawan
- Snack peserta
- Makan penerima manfaat
- Air mineral
- Perlengkapan makan (sekali pakai)

Budgeting Tips:
- Bulk ordering untuk discount
- Simple menu (tidak perlu mewah)
- Avoid food waste (accurate headcount)
```

### **4. Bantuan Langsung (40-60% dari total)**

```
Items:
- Sembako paket
- Uang tunai
- Pakaian layak
- Alat sekolah
- Obat-obatan

Budgeting Tips:
- Beli grosir untuk harga lebih baik
- Coordinate dengan supplier tetap
- Quality control sebelum distribusi
```

### **5. Transportasi (5-10% dari total)**

```
Items:
- Transport panitia
- Transport relawan
- Transport penerima
- BBM kendaraan operasional
- Parkir & tol

Budgeting Tips:
- Carpooling untuk hemat
- Use public transport jika feasible
- Reimburse based on actual
```

### **6. Lain-lain / Dana Darurat (5%)**

```
Items:
- Dana tak terduga (5% dari total)
- Emergency purchases
- Price fluctuation buffer

Budgeting Tips:
- ALWAYS include 5% contingency
- Don't use unless necessary
- Return to kas if unused
```

---

## 💡 Budgeting Best Practices

### **DO (Lakukan):**

✅ **Be Realistic:**
```
- Research actual prices (don't guess)
- Get multiple quotes (min 3 vendors)
- Include buffer for inflation
- Account for emergencies (5%)
```

✅ **Be Detailed:**
```
- Break down every line item
- Specify quantity & unit
- Note unit price & total
- Add descriptions for clarity
```

✅ **Be Transparent:**
```
- Document all assumptions
- Show calculation basis
- Note conflicts of interest
- Disclose sponsorships
```

✅ **Be Efficient:**
```
- Maximize impact per rupiah
- Minimize overhead costs
- Bulk purchasing discounts
- Re-use resources when possible
```

### **DON'T (Jangan Lakukan):**

❌ **Underestimate Costs:**
```
- Don't guess prices
- Don't forget hidden costs
- Don't ignore inflation
- Don't skip contingency
```

❌ **Overbudget:**
```
- Don't pad numbers
- Don't include unnecessary items
- Don't inflate quantities
- Don't duplicate line items
```

❌ **Vague Descriptions:**
```
- Avoid "lain-lain" without details
- Avoid lump sums without breakdown
- Avoid unspecified quantities
```

❌ **Ignore Cash Flow:**
```
- Don't forget payment timing
- Don't assume immediate availability
- Don't skip approval timeline
```

---

## 📊 Approval Workflow

### **Approval Matrix:**

| Budget Amount | Approval Required | Timeline |
|---------------|-------------------|----------|
| **< Rp 1.000.000** | Koordinator Program | 1-2 days |
| **Rp 1-5 Juta** | Bendahara | 2-3 days |
| **Rp 5-10 Juta** | Pengurus (1) | 3-5 days |
| **> Rp 10 Juta** | Rapat Pengurus | 5-7 days |
| **> Rp 50 Juta** | Full Board + External Audit | 7-14 days |

### **Approval Process:**

```
1. PIC prepares RAB (Draft)
   ↓
2. Koordinator reviews (Check accuracy, necessity)
   ↓ Approve/Reject with comments
3. Bendahara reviews (Check budget availability)
   ↓ Approve/Reject with comments
4. Pengurus approves (Final approval)
   ↓ Approved → Budget allocated
5. Finance executes (Disbursement per timeline)
```

---

## 📞 Contact & Support

| Role | Contact |
|------|---------|
| **RAB Template Access** | Bendahara: [Email Bendahara] |
| **Budget Review** | Bendahara: [Email Bendahara] |
| **Approval** | Pengurus: [Email Pengurus] |
| **Disbursement** | Bendahara: [Email Bendahara] |

---

**Template ini living document - update sesuai kebutuhan!**

**Last reviewed:** 7 Juni 2026  
**Next review:** 7 Desember 2026  
**Maintained by:** Bendahara & Pengurus

---

*"A budget is telling your money where to go instead of wondering where it went." - Dave Ramsey*