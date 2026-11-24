# **WORKBOOK: LEMBAR KERJA MAHASISWA WS06** 

## **Success Metrics (BPI/DMAIC) & Pemetaan Komponen SI Awal** 

Mata Kuliah: **Konsep Sistem Informasi (KSI)** Kerangka Kerja: **Project-Based Learning (PBL) Level 1** Fase Learning Spine: **Fase 3 — Define (Minggu 4)** Sub-CPMK / SFIA: **S-01.1 (Intermediate - Problem Framing) & S-03.1 (Intermediate - Pemetaan SI)** | **SFIA BUSA L1, METR L2** Keterkaitan Deliverable: **Bahan Utama Deliverable D1 Final (TPL-01) & D2 Draf (TPL-02)** 

### **1. Identifikasi Kelompok & Rotasi Kepemimpinan** 

- **Nama Kelompok** : Tulalit 

- **Objek UMKM Mitra** : Brilian Laundry (Laundry) 

- **Phase Lead 3 (Define)** : Cavin Gusti Ramadhani 

- **Anggota Tim** : 1. Muhammad Subhan Zulfikar 2. Fikajun Wolek Arifin 3. Brian AshShidiq saputra 4. Satrio Gemintang Mahameru 

### **2. Landasan Konseptual: Metrik BPI & Pemetaan 5 Pilar SI** 

- **Business Process Improvement (BPI)** mengukur keberhasilan perbaikan proses bisnis melalui dua dimensi utama (Rainer et al., 2014): 

   - **Efisiensi (** **_Efficiency_ )** : Mengukur penghematan sumber daya ( _doing things well_ ), seperti efisiensi waktu siklus transaksi atau reduksi biaya operasional. 

   - **Efektivitas (** **_Effectiveness_ )** : Mengukur pencapaian kualitas/tujuan ( _doing the right things_ ), seperti akurasi data stok, penurunan angka selisih kasir, dan kepuasan pelanggan. 

- **Model 5 Pilar SI O'Brien** : Solusi sistem informasi dipetakan ke dalam pilar _People, Hardware, Software, Data,_ dan _Network_ (Marakas & O'Brien, 2013). 

### **3. Workspace A: Matrik Metrik Keberhasilan Bisnis (DMAIC Six Sigma)** 

|**Dimensi Metrik**|**Parameter**<br>**Kinerja**|**Kondisi**<br>**Baseline (As-Is)**|**Target Solusi**<br>**(To-Be)**|**Metode**<br>**Pengukuran**|
|---|---|---|---|---|
|**Efisiensi**<br>**(Waktu)**|Durasi<br>pelayanan<br>transaksi per<br>pelanggan|5 Menit|Maksimal 5<br>menit|Stopwatch<br>sampel 10<br>transaksi|
|**Efisiensi**<br>**(Waktu)**|Durasi<br>rekapitulasi<br>harian pemilik|10-30 menit|Maksimal 10<br>menit|Wawancara & uji<br>coba langsung|
|**Efektivitas**<br>**(Akurasi)**|Kelengkapan<br>pencatatan<br>identitas pakaian|Belum<br>konsisten,<br>informasi jenis,<br>warna, dan<br>jumlah pakaian<br>belum tercatat<br>secara lengkap|100% data<br>pakaian pada<br>transaksi uji<br>coba memiliki<br>identitas yang<br>diperlukan|Audit sampel<br>data transaksi|
|**Efektivitas**<br>**(Kualitas)**|Frekuensi<br>kesalahan<br>identifikasi<br>pakaian|Pernah terjadi<br>pakaian hilang<br>atau terlepas<br>dari jemuran;<br>frekuensi blum<br>terukur|0 kesalahan<br>identifikasi pada<br>transaksi uji<br>coba|Audit data dan<br>uji coba<br>langsung|



### **4. Workspace B: Pemetaan Arsitektur 5 Pilar SI Solusi Awal** 

┌────────────────────────────────────────────┐ │                      PETA 5 PILAR SISTEM INFORMASI                      │ ├────────────────────────────────────────────┤ 

│ 1. PEOPLE RESOURCES (Pengguna & Spesialis)                              │ 

- │ • Pengguna Akhir: Pemilik Brilian Laundry ( Bu erna) │ 

- │ • Pengelola Data: Pemilik Brilian Laundry yang bertanggung jawab memasukkan, memperbarui, dan mengelola pelanggan, transaksi, serta identitas pakaian. │ ├────────────────────────────────────────────┤ 

│ 2. HARDWARE RESOURCES (Perangkat Mesin & Media)                         │ 

> │ • Perangkat Fisik Input: Hp android untuk memasukkan data pelanggan, pesanan, berat, jenis layanan, dan identitas pakaian. │ 

> │ • Perangkat Fisik Output: Hp android untuk menampilkan data transaksi, identitas pakaian, status laundry, dan rekap operasional. │ 

- ├────────────────────────────────────────────┤ │ 3. SOFTWARE RESOURCES (Aplikasi & Prosedur Operational)                 │ │ • Aplikasi Program: Aplikasi pencacatan dan pengelolaan data Laundry berdasarkan Phyton. │ 

- │ • Prosedur Pengguna: Pemilik memasukkan data pelanggan dan pesanan, mencatat berat serta jenis layanan, memasukkan identitas pakaian, memperbarui status pengerjaan, dan melihat rekap operasional harian. │ 

├────────────────────────────────────────────┤ 

│ 4. DATA RESOURCES (Struktur Data & Basis Data)                          │ 

- │ • Data Transaksi: ID transaksi, tanggal transaksi, nama pelanggan, berat pakaian, jenis layanan, dan 

status pengerjaan. │ 

- 

- │ Data Produk/Stok: Jenis pakaian, warna pakaian, dan jumlah setiap jenis pakaian dalam transaksi. │ ├────────────────────────────────────────────┤ 

│ 5. NETWORK RESOURCES (Jaringan Communication & Media)                   │ 

- │ • Konektivitas: Sistem dijalankan secara lokal pada HP android tanpa memerlukan koneksi internet. │ 

└────────────────────────────────────────────┘ 

### **5. Workspace C: Lembar Persetujuan Formal Mitra (Sign-Off)** 

Dengan ini, pemilik / manajer UMKM mitra menyatakan setuju atas rumusan kebutuhan fungsional, target metrik keberhasilan, dan batas cakupan sistem yang dirancang oleh tim mahasiswa. 

- **Nama UMKM Mitra** : Brilian Laundry 

- **Nama Pemilik / Pengelola** : Bu Erna 

- **Tanggal Persetujuan** : 11/11/2026 

**Tanda Tangan Persetujuan Mitra** : 

_(Cap / Tanda Tangan Pemilik UMKM Mitra)_ 

### **6. Verifikasi Integritas AI (TPL-07) & Pengesahan** 

- **Penggunaan AI Co-pilot** : 

Apakah tim menggunakan AI untuk membantu merumuskan metrik BPI / diagram 5 pilar SI? [ ✔ ] Ya  [ ] Tidak 

**_TPL-07: AI Usage Disclosure & Verification Note_** : https://github.com/CavinGustiRamadhani/pbl_2026_tulalit/blob/main/docs/TPL-07%20%E2%80%94%20Template%20AI%20Usage%20Disclosure%20%26%20Verification%20Note.md 

#### **Tanda Tangan Tim & Pengesahan Dosen** : 

- **Phase Lead 3** : Cavin Gusti Ramadhani  (Tanggal: 11/11/2026) 

- **Dosen Coach** : _______________________ (Tanggal: __________)  [ ] Approved 

