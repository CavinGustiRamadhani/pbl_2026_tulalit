# **WORKBOOK: LEMBAR KERJA MAHASISWA WS05** 

## **Formulasi Kebutuhan Fungsional: User Story & Acceptance Criteria** 

Mata Kuliah: **Konsep Sistem Informasi (KSI)** Kerangka Kerja: **Project-Based Learning (PBL) Level 1** Fase Learning Spine: **Fase 3 — Define (Minggu 3)** Sub-CPMK / SFIA: **S-01.1 (Intermediate - Problem Framing) & S-03.1 (Intermediate - Pemetaan SI)** | **SFIA BUSA L1, REQM L2** Keterkaitan Deliverable: **Bahan Utama Deliverable D2 (System & Solution Design - TPL-02)** 

### **1. Identifikasi Kelompok & Rotasi Kepemimpinan** 

- **Nama Kelompok** : Tulalit 

- **Objek UMKM Mitra** : Brilian Laundry (Laundry) 

- **Phase Lead 3 (Define)** : Cavin Gusti Ramadhani 260016064 

Anggota Tim : 

1. Muhammad Subhan Zulfikar 2600016057 

2. Fikajun Wolek Arifin 2638016029 

3. Satrio Gemintang Mahameru 2600016061 

4. Brian Ash-Shidiq Saputra 2600016083 

### **2. Landasan Konseptual: Analisis Sistem "What" vs "How"** 

Dalam tahap _Systems Analysis_ , fokus utama tim adalah menentukan **APA (** **_What_ )** yang dibutuhkan pengguna bisnis untuk memecahkan masalahnya, **BUKAN BAGAIMANA (** **_How_ )** sistem dibangun secara teknis (Marakas & O'Brien, 2013). 

- **User Story** merepresentasikan kebutuhan fungsional dari sudut pandang pengguna bisnis dengan pola: 

{"Sebagai [Peran Pengguna], Saya ingin [Kemampuan/Fitur], Sehingga [Manfaat Bisnis Nyata]"} 

- **Acceptance Criteria (Given-When-Then)** mendefinisikan batas kondisi kapan sebuah f itur dinyatakan selesai dan memenuhi syarat penerimaan pengguna (Rainer et al., 2021). 

### **3. Workspace A: Formulasi User Story Fungsional** 

Petakan minimal **3 User Story Utama** yang langsung menjawab akar masalah pada D1 / WS04: 

#### **User Story 1 (Prioritas Utama / Core Feature)** 

- **Sebagai (** **_As a_ )** : _Pemilik Usaha_ 

- **Saya ingin (** **_I want to_ )** : mencatat identitas dan jumlah pakaian pelanggan berdasarkan s etiap transaksi laundry secara terstruktur. 

- **Sehingga (** **_So that_ )** : saya dapat mengetahui jenis dan jumlah pakaian milik setiap pelanggan sehingga proses identifikasi dan pemeriksaan pakaian menjadi lebih mudah. 

#### **User Story 2 (Fitur Manajemen Stok / Data)** 

- **Sebagai (** **_As a_ )** : Pemilik Usaha 

- **Saya ingin (** **_I want to_ )** : mencatat data pelanggan, berat laundry, jenis layanan, serta status pengerjaan setiap pesanan. 

- **Sehingga (** **_So that_ )** : saya dapat mengelola pesanan dengan lebih terstruktur dan mengetahui perkembangan setiap pesanan laundry. 

#### **User Story 3 (Fitur Pelaporan / Informasi)** 

- **Sebagai (** **_As a_ )** : Pemilik Usaha 

- **Saya ingin (** **_I want to_ )** : melihat rekap data operasional harian yang mencakup jumlah transaksi dan ringkasan pesanan laundry. 

- **Sehingga (** **_So that_ )** : saya dapat memantau aktivitas usaha dan mengetahui jumlah pesanan tanpa harus memeriksa catatan secara manual satu per satu. 

### **4. Workspace B: Acceptance Criteria Berbasis Skenario (Given-WhenThen)** 

Susun kriteria penerimaan terstruktur untuk **User Story 1** (mencakup Skenario Sukses dan Skenario Penanganan Eror): 

#### **Skenario 1A: Transaksi Penjualan Berhasil (Happy Path)** 

- **Diberikan (** **_Given_ )** : Pemilik usaha sedang menginput pesanan laundry pelanggan dan telah mengisi data pelanggan serta informasi pakaian. 

- **Ketika (** **_When_ )** : Pemilik usaha memasukkan jenis pakaian, warna, dan jumlah pakaian, kemudian mengklik tombol "Simpan Pesanan". 

- **Maka (** **_Then_ )** : Sistem menyimpan data pesanan beserta identitas dan jumlah pakaian pelanggan sehingga informasi tersebut dapat dilihat kembali berdasarkan transaksi. 

#### **Skenario 1B: Penanganan Pembayaran Kurang / Eror (Exception Path)** 

- **Diberikan (** **_Given_ )** : Pemilik usaha sedang menginput pesanan laundry baru pada sistem. 

- ● **Ketika (** **_When_ )** : Pemilik usaha mengisi data pelanggan, tetapi mengosongkan informasi jumlah pakaian, kemudian mengklik tombol "Simpan Pesanan". 

- **Maka (** **_Then_ )** : Sistem menolak penyimpanan transaksi dan menampilkan peringatan bahwa jumlah pakaian wajib diisi sehingga data pesanan tidak tersimpan sebelum informasi dilengkapi. 

### **5. Workspace C: Catatan Validasi Kebutuhan dengan Mitra (Field Confirmation)** 

- **Tanggal Validasi** : 11/11/2026 

- **Narahubung Mitra** : Bu Erna  (Pemilik / Staf Kasir) 

- **Hasil Konfirmasi User Story** : 

   - [✔] Seluruh User Story disetujui mitra 
 

### **6. Verifikasi Integritas AI (TPL-07) & Pengesahan** 

- **Penggunaan AI Co-pilot** : 

Apakah tim menggunakan AI untuk membantu merumuskan skenario _Given-When-Then_ ? [✔] Ya  [ ] Tidak 

_(Jika Ya, wajib melampirkan formulir_ **_TPL-07: AI Usage Disclosure & Verification Note_** _)_ . 

**Tanda Tangan Tim & Pengesahan Dosen** : 

- **Phase Lead 3** : Cavin Gusti Ramadhani         (Tanggal: 11/11/2026) 

- **Dosen Coach** : _______________________ (Tanggal: __________)  [ ] Approved 

