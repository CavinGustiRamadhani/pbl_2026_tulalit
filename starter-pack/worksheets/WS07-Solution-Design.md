# **WORKBOOK: LEMBAR KERJA MAHASISWA (WS07)** 

# **Simple Solution Design — IPO, Flowchart & Pseudocode** 

# **INFORMASI UTAMA** 

- **Mata Kuliah** : Konsep Sistem Informasi (KSI) 

- **Kerangka Kerja** : Project-Based Learning (PBL) Level 1 

- **Learning Moment** : _Fase 4: Design (Minggu 5–6)_ 

- **Sub-CPMK / SFIA** : S-03.1 (Intermediate) | SFIA ARCH L2, DESN L2 

- **Keterkaitan Deliverable** : Sumber utama pembuatan **Deliverable D2 (System & Solution Design - TPL-02)** 

- **Phase Lead** : Satrio Gemintang Mahameru 

# **RUANG KERJA TIM (WORKSPACE)** 

# **1. IDENTIFIKASI KELOMPOK & SOLUSI** 

- Nama Tim: Tulalit / Kelas B 

- Nama UMKM Mitra: Brilian Laundry 

- Judul Solusi SI: Sistem Informasi Pengelolaan Pesanan dan Identitas Pakaian Brilian Laundry 

- Phase Lead 4 (Design): Satrio Gemintang Mahameru 

# **2. PEMETAAN ARSITEKTUR 4 LAPISAN SI (M05)** 

Petakan solusi Anda ke dalam 4 lapisan arsitektur terintegrasi: 

|**Lapisan Arsitektur**|**Komponen Solusi Tim**|**Keterangan & Batasan**|
|---|---|---|
|**1. Process Layer** _(Alur Kerja To-Be)_|Proses To-Be: pemilik memasukkan data<br>pelanggan dan pesanan; mencatat berat,<br>jenis layanan, estimasi selesai, serta<br>rincian jenis/warna/jumlah pakaian;<br>menyimpan pesanan; memperbarui<br>status pengerjaan; lalu melihat rekap<br>operasional harian.|Alur transaksi kasir To-Be yang lebih<br>efisien dibanding_As-Is_.|
|**2. Data Layer** _(Struktur Data Logis)_|Entitas logis: Pelanggan (ID, nama);<br>Transaksi/Pesanan (ID transaksi,<br>tanggal, ID pelanggan, berat, jenis<br>layanan, estimasi selesai, status);<br>Rincian Pakaian (ID rincian, ID transaksi,<br>jenis pakaian, warna, jumlah); Rekap<br>Operasional (tanggal, jumlah transaksi,<br>ringkasan pesanan).|Entitas data: Tabel Menu/Produk, Tabel<br>Transaksi, & Tabel Stok.|



|**Lapisan Arsitektur**|**Komponen Solusi Tim**|**Keterangan & Batasan**|
|---|---|---|
|**3. Application Layer** _(Modul Program)_|Modul: (1) Input data pelanggan dan<br>pesanan; (2) pencatatan identitas serta<br>jumlah pakaian; (3)<br>pemantauan/perubahan status laundry;<br>(4) rekap operasional harian. Sistem<br>digunakan oleh pemilik/pengelola.|Modul Utama: Login, Input Transaksi,<br>Hitung Total/Diskon, & Rekap.|
|**4. Infrastructure Layer** _(Perangkat_<br>_Fisik)_|Perangkat: laptop/PC, keyboard, mouse,<br>dan monitor. Perangkat lunak: aplikasi<br>sederhana berbasis Python. Sistem<br>berjalan secara lokal pada laptop/PC<br>dan tidak memerlukan internet, sesuai<br>pemetaan WS06.|Hardware: Laptop/Tablet POS; Net: Wi-<br>Fi/4G; OS: Windows/Android.|



# **3. SPESIFIKASI IPO (INPUT - PROCESSING - OUTPUT - STORAGE - CONTROL)** 

Fitur Fungsional Utama 1: Pencatatan Pesanan dan Identitas/Jumlah Pakaian 

- Input: Nama pelanggan; tanggal transaksi; berat laundry; jenis layanan; estimasi selesai; serta rincian setiap jenis pakaian berupa jenis, warna, dan jumlah. 

- Processing: Sistem memeriksa kelengkapan data pesanan; memvalidasi jumlah pakaian harus berupa bilangan bulat lebih dari 0; mengulang input rincian selama masih ada jenis pakaian yang akan ditambahkan; kemudian mengaitkan rincian pakaian dengan ID transaksi. 

- Output: Konfirmasi bahwa pesanan berhasil disimpan dan ringkasan pesanan yang memuat identitas pelanggan serta daftar jenis, warna, dan jumlah pakaian. 

- Storage: Data disimpan secara lokal pada basis data/tabel Pelanggan, Transaksi_Pesanan, dan Rincian_Pakaian dengan ID transaksi sebagai penghubung. 

- Control (Error Handling): Tolak penyimpanan jika nama pelanggan atau data wajib lain kosong; tolak jumlah yang kosong, bukan angka, nol, atau negatif; tampilkan pesan kesalahan dan minta pengguna memperbaiki input. Jangan simpan transaksi sebelum seluruh validasi berhasil. 

Fitur Fungsional Utama 2: Pemantauan Status Laundry dan Rekap Operasional Harian 

- Input: ID transaksi atau tanggal yang dipilih; status pengerjaan baru (misalnya diterima, dicuci, dikeringkan, disetrika, siap diambil, diserahkan); serta permintaan periode/tanggal rekap. 

- Processing: Sistem mencari pesanan berdasarkan ID transaksi; memeriksa status yang dipilih; memperbarui status pesanan; dan menyusun rekap berdasarkan tanggal berupa jumlah transaksi serta ringkasan pesanan/status. Rekap bersifat operasional, bukan laporan laba-rugi terperinci. 

- Output: Informasi status terbaru setiap pesanan dan rekap operasional harian yang dapat dilihat pemilik. 

- Storage: Perubahan status disimpan pada tabel Transaksi_Pesanan; data rekap diambil dari tabel Transaksi_Pesanan dan Rincian_Pakaian. Rekap dapat dihitung saat diminta sehingga tidak perlu menggandakan data transaksi. 

- Control (Error Handling): Tampilkan pesan jika ID transaksi tidak ditemukan; tolak status kosong atau di luar daftar status yang ditetapkan; jika tanggal rekap tidak memiliki transaksi, tampilkan pesan bahwa tidak ada data pada tanggal tersebut. 

# **4. DIAGRAM ALIR (FLOWCHART) LOGIKA PROGRAM** 

_Petunjuk: Gambarkan diagram alir terstruktur menggunakan simbol standar (Persegi Panjang = Proses, Belah Ketupat = Keputusan IF-ELSE, Jajar Genjang = Input/Output, Oval = Start/End). Lampirkan hasil gambaran digital/foto kertas A3 di bawah ini._ 



<!-- Start of picture text -->
Pemilik memasukkan data pelanggan dan pesanan:<br>Tanggal, nama pelanggan, berat, layanan, estimasi selesai<br>Sistem memeriksa kelengkapan data pesanan<br>Data lengkap? “DataTampilkantidak valid”pesan<br>Ya<br>Masukkan jenis pakaian, warna, dan jumlah<br>untuk setMas i ap jenish ada jenis pakaian esTambahkan rincian<br>pakaian lain? pakaian berikutnya<br>Tidak<br>Sistem memvalidasi jumlah pesanan<br>(angka bulat dan lebih dari 0)<br>F Tidak Tampilkan pesan<br>Semua jumlah valid?a “Jumlah tidak sesuai”<br>Ya<br>Simpan data pelanggan, transaksi,<br>dan rincian pakaian ke basis data<br>Tampilkan konfirmasi / ringkasan pesanan<br><!-- End of picture text -->

# **5. PSEUDOCODE TERSTRUKTUR (INDEPENDEN TEKNOLOGI)** 

Tuliskan kode semu terstruktur ( _pseudocode_ ) untuk modul logika utama solusi Anda: 

ALGORITMA Catat_Pesanan_dan_Identitas_Pakaian KAMUS DATA: nama_pelanggan : STRING tanggal_transaksi, jenis_layanan, estimasi_selesai : STRING berat_laundry : REAL jenis_pakaian, warna_pakaian : STRING jumlah_pakaian : INTEGER daftar_rincian : ARRAY OF Rincian_Pakaian tambah_rincian : BOOLEAN id_transaksi : STRING 

ALUR LOGIKA: START READ nama_pelanggan, tanggal_transaksi READ berat_laundry, jenis_layanan, estimasi_selesai IF nama_pelanggan kosong OR tanggal_transaksi kosong OR berat_laundry <= 0 OR jenis_layanan kosong THEN PRINT 'Data pesanan belum lengkap atau tidak valid' STOP ENDIF daftar_rincian = kosong tambah_rincian = TRUE WHILE tambah_rincian = TRUE DO READ jenis_pakaian, warna_pakaian, jumlah_pakaian IF jenis_pakaian kosong OR warna_pakaian kosong OR jumlah_pakaian bukan bilangan bulat OR jumlah_pakaian <= 0 THEN PRINT 'Rincian pakaian tidak valid; silakan perbaiki' ELSE Catatan desain: Fitur pembayaran otomatis QRIS/e-wallet tidak dibuat karena termasuk out-of-scope. Sistem ini mencatat data operasional laundry; nominal tarif dan rumus perhitungan harga belum dirinci dalam dokumen kebutuhan yang tersedia, sehingga tidak diasumsikan dalam desain ini. 

Arsitektur 4 lapisan SI telah dipetakan sesuai kebutuhan Brilian Laundry. 

IPO kedua fitur telah mencakup Input, Processing, Output, Storage, dan Control. Flowchart menunjukkan validasi, percabangan IF-ELSE, dan perulangan input rincian pakaian yang memiliki kondisi berhenti. Pseudocode menggunakan logika umum dan tidak bergantung pada bahasa pemrograman tertentu. TPL-07:https://github.com/CavinGustiRamadhani/pbl_2026_tulalit/blob/main/docs/ <u>TPL-07%20%E2%80%94%20Template%20AI%20Usage%20Disclosure%20%26%20Verification%20Note. md</u> 

ELSE Tanggal Pengesahan: 11/11/2026 Tanda Tangan Phase Lead 4 (Design): ____________________ Tanda Tangan Dosen Pembimbing / Coach: ____________________ ENDIF 

