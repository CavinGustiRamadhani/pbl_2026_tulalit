# D2 — System & Solution Design

**Project**: Digital Problem Framing Mini Project — [Brilian Laundry]
**Tim**: [Fikajun wolek arifin, Muhammad subhan zulfikar, Cavin gusti ramadhani, Brian Ash-Shidiq Saputra, Satrio gemintang mahameru] | **Tanggal**: [12/11/1016] | **Versi**: [v1.0]
**Template**: TPL-02

> **Petunjuk**: Hapus teks dalam `[...]` setelah diisi.
> Worksheet terkait: WS05, WS06, WS07

---

## 1. Daftar Kebutuhan (User Story)

| # | User Story | Prioritas |
|---|---|---|
| 1 | Sebagai [Pemilik Usaha], saya ingin [mencatat identitas dan jumlah pakaian pelanggan berdasarkan s etiap transaksi laundry secara terstruktur] sehingga [saya dapat mengetahui jenis dan jumlah pakaian milik setiap pelanggan sehingga proses identifikasi dan pemeriksaan pakaian menjadi lebih mudah] | [Tinggi] |
| 2 | Sebagai [Pemilik Usaha], saya ingin [mencatat data pelanggan, berat laundry, jenis layanan, serta status pengerjaan setiap pesanan] sehingga [saya dapat mengelola pesanan dengan lebih terstruktur dan mengetahui perkembangan setiap pesanan laundry] | [Tinggi] |
| 3 | Sebagai [Pemilik Usaha], saya ingin [melihat rekap data operasional harian yang mencakup jumlah transaksi dan ringkasan pesanan laundry] sehingga [saya dapat memantau aktivitas usaha dan mengetahui jumlah pesanan tanpa harus memeriksa catatan secara manual satu per satu] | [Sedang] |
| 4 | *(tambah jika perlu)* | |

## 2. Kriteria Penerimaan

| # | Kriteria Penerimaan (terukur & dapat diuji) |
|---|---|
| 1 | Skenario 1A--Transaksi Penjualan Berhasil (Happy Path). Given Pemilik usaha sedang menginput pesanan laundry pelanggan dan telah mengisi data pelanggan serta informasi pakaian; When Pemilik usaha memasukkan jenis pakaian, warna, dan jumlah pakaian, kemudian mengklik tombol "Simpan Pesanan"; Then Sistem menyimpan data pesanan beserta identitas dan jumlah pakaian pelanggan sehingga informasi tersebut dapat dilihat kembali berdasarkan transaksi |
| 2 | Skenario 1B--Penanganan Pembayaran Kurang / Eror (Exception Path). Given Pemilik usaha sedang menginput pesanan laundry baru pada sistem; When Pemilik usaha mengisi data pelanggan, tetapi mengosongkan informasi jumlah pakaian, kemudian mengklik tombol "Simpan Pesanan"; Then Sistem menolak penyimpanan transaksi dan menampilkan peringatan bahwa jumlah pakaian wajib diisi sehingga data pesanan tidak tersimpan sebelum informasi dilengkapi |
| 3 | |

## 3. Success Metrics

| Metrik | Baseline (Sekarang) | Target | Cara Mengukur |
|---|---|---|---|
| Durasi pelayanan transaksi per pelanggan (efisiensi--waktu) | 5 menit | Maksimal 5 menit | Stopwatch sampel 10 transaksi |
| Durasi rekapitulasi harian pemilik (efisiensi--waktu) | 10-30 menit | Maksimal 10 menit | Wawancara & uji coba langsung |
| Kelengkapan pencatatan identitas pakaian (efektivitas--akurasi) | Belum konsisten, informasi jenis, warna, dan jumlah pakaian belum tercatat secara lengkap | 100% data pakaian pada transaksi uji coba memiliki identitas yang diperlukan | Audit sampel data transaksi |
| Frekuensi kesalahan identifikasi pakaian (efektivitas--kualitas) | Pernah terjadi pakaian hilang atau terlepas dari jemuran; frekuensi belum terukur | 0 kesalahan identifikasi pada transaksi uji coba | Audit data dan uji coba langsung |

## 4. Desain Solusi

### 4.1 Konsep Solusi (ringkasan)

_[1. Sistem dapat mencatat data pelanggan dan pesanan laundry secara terstruktur.
2. Sistem dapat mencatat berat, jenis layanan, serta jumlah pakaian dalam setiap pesanan.
3. Sistem dapat membantu pemilik mengidentifikasi pakaian berdasarkan data pesanan pelanggan.
4. Sistem dapat menampilkan status pengerjaan laundry hingga pakaian siap diambil.
5. Sistem dapat membantu menghasilkan rekap data operasional harian.]_

### 4.2 Peta Komponen (IPO)

```
Input  ──▶  Proses  ──▶  Output
  │                           │
  └───── Data/Penyimpanan ────┘
```

- **Input**: [Fitur Fungsional Utama 1: Pencatatan Pesanan dan Identitas/Jumlah Pakaian: Nama pelanggan; tanggal transaksi; berat laundry; jenis layanan; estimasi selesai; serta rincian setiap jenis pakaian berupa jenis, warna, dan jumlah.
Fitur Fungsional Utama 2: Pemantauan Status Laundry dan Rekap Operasional Harian: ID transaksi atau tanggal yang dipilih; status pengerjaan baru (misalnya diterima, dicuci, dikeringkan, disetrika, siap diambil, diserahkan); serta permintaan periode/tanggal rekap. ]
- **Proses**: [Fitur Fungsional Utama 1: Sistem memeriksa kelengkapan data pesanan; memvalidasi jumlah pakaian harus berupa bilangan bulat lebih dari 0; mengulang input rincian selama masih ada jenis pakaian yang akan ditambahkan; kemudian mengaitkan rincian pakaian dengan ID transaksi. 
Fitur Fungsional Utama 2: Sistem mencari pesanan berdasarkan ID transaksi; memeriksa status yang dipilih; memperbarui status pesanan; dan menyusun rekap berdasarkan tanggal berupa jumlah transaksi serta ringkasan pesanan/status. Rekap bersifat operasional, bukan laporan laba-rugi terperinci. ]
- **Output**: [Fitur Fungsional Utama 1: Konfirmasi bahwa pesanan berhasil disimpan dan ringkasan pesanan yang memuat identitas pelanggan serta daftar jenis, warna, dan jumlah pakaian. 
Fitur Fungsional Utama 2: Informasi status terbaru setiap pesanan dan rekap operasional harian yang dapat dilihat pemilik.]
- **Data/Penyimpanan**: [Fitur Fungsional Utama 1: Data disimpan secara lokal pada basis data/tabel Pelanggan, Transaksi_Pesanan, dan Rincian_Pakaian dengan ID transaksi sebagai penghubung. 
Fitur Fungsional Utama 2: Perubahan status disimpan pada tabel Transaksi_Pesanan; data rekap diambil dari tabel Transaksi_Pesanan dan Rincian_Pakaian. Rekap dapat dihitung saat diminta sehingga tidak perlu menggandakan data transaksi. ]

### 4.3 Flowchart & Pseudocode

_[Tempel flowchart di `assets/` dan tulis pseudocode di bawah]_

```
[ALGORITMA Catat_Pesanan_dan_Identitas_Pakaian
KAMUS DATA:
    nama_pelanggan : STRING
    tanggal_transaksi, jenis_layanan, estimasi_selesai : STRING
    berat_laundry : REAL
    jenis_pakaian, warna_pakaian : STRING
    jumlah_pakaian : INTEGER
    daftar_rincian : ARRAY OF Rincian_Pakaian
    tambah_rincian : BOOLEAN
    id_transaksi : STRING

ALUR LOGIKA:
START
    READ nama_pelanggan, tanggal_transaksi
    READ berat_laundry, jenis_layanan, estimasi_selesai

    IF nama_pelanggan kosong OR tanggal_transaksi kosong OR
       berat_laundry <= 0 OR jenis_layanan kosong THEN
        PRINT 'Data pesanan belum lengkap atau tidak valid'
        STOP
    ENDIF

    daftar_rincian = kosong
    tambah_rincian = TRUE
    WHILE tambah_rincian = TRUE DO
        READ jenis_pakaian, warna_pakaian, jumlah_pakaian
        IF jenis_pakaian kosong OR warna_pakaian kosong OR
           jumlah_pakaian bukan bilangan bulat OR jumlah_pakaian <= 0 THEN
            PRINT 'Rincian pakaian tidak valid; silakan perbaiki'
        ELSE
]
```

## 5. Hasil Validasi Pemilik Usaha

- **Tanggal validasi**: [12/11/2026]
- **Feedback pemilik**: [Bu Erna (pemilik Brilian Laundry) menyetujui seluruh user story
(WS05) dan memberikan persetujuan formal atas rumusan kebutuhan fungsional, target metrik keberhasilan, dan batas cakupan sistem (WS06)]
- **Perubahan setelah validasi**: [Tidak ada perubahan yang tercatat pada WS05/WSO6; seluruh user story disetujui tanpa revisi. Validasi desain solusi (WS07) belum tercatat.]

---

**Status**: ⬜ Draf → ⬜ Review Tim → ⬜ Validasi Pemilik → ⬜ Final (GATE 1)