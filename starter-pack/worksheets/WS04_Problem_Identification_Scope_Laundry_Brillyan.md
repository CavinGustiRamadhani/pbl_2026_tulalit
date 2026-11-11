# **WS04: Problem Identification & Scope**

**Mata Kuliah**: Konsep Sistem Informasi (KSI)  
**Kerangka Kerja**: Project-Based Learning (PBL) Level 1  
**Fase Learning Spine**: **Fase 2 — Frame (Problem Discovery & Scope)**  
**Minggu / Alokasi Waktu**: Minggu 2 / 14 Jam Belajar  
**Sub-CPMK / SFIA**: S-01.1 (Introduce - Problem Framing) | SFIA BUSA L1 (_Business Analysis_), IRMG L1  
**Penanggung Jawab Fase**: **Phase Lead 2 (Frame — Mahasiswa B)**  
**Keterkaitan Deliverable**: Sumber Utama Penyusunan **Deliverable D1 (Problem Brief - TPL-01)**

## **1\. Identifikasi Tim & Objek Proyek**

| **Elemen Informasi**          | **Rincian Identitas Kelompok & Mitra** |
| ----------------------------- | -------------------------------------- |
| **Nama Kelompok / Kelas**     | Tulalit / B                            |
| **Phase Lead 2 (Frame - M2)** | Fikajun Wolek Arifin                   |
| **Nama UMKM Mitra Lapangan**  | Brilian Laundry                        |
| **Pemilik / Kontak Mitra**    | Bu Erna / 0882007602228                |

## **2\. Matriks Problem Framing & Analisis Akar Masalah (Root Cause Analysis)**

Gunakan temuan wawancara sebagai dasar problem framing. Angka kuantitatif yang tidak tersedia dalam wawancara ditandai sebagai belum diukur dan perlu dikumpulkan melalui observasi lanjutan; jangan menganggapnya sebagai baseline faktual.

| No  | Kategori Observasi                  | Gejala Permukaan (Symptoms)                                                                                                                        | Akar Masalah Operasional (Root Cause)                                                                                                                                                        | Bukti Kuantitatif (Baseline Data)                                                                           |
| --- | ----------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| 1   | Pencatatan Pesanan Laundry          | Informasi pesanan dan data pelanggan masih dicatat secara manual sehingga pencarian atau penelusuran pesanan berpotensi memerlukan waktu tambahan. | Data pelanggan, berat laundry, serta laundry masuk dan keluar ditulis secara manual; komunikasi dengan pelanggan dilakukan melalui telepon.                                                  | Waktu transaksi dan jumlah pesanan harian tidak disebutkan dalam wawancara; perlu pengukuran langsung.      |
| 2   | Identifikasi dan Penyerahan Pakaian | Pernah terjadi pakaian atau kaus kaki hilang/terlepas dari jemuran, sehingga proses identifikasi pakaian perlu diperhatikan.                       | Pemisahan pakaian dilakukan per pelanggan, tetapi identifikasi terutama mengandalkan nama pada kantong dan ingatan; jumlah pakaian belum selalu dicatat secara konsisten.                    | Jumlah kejadian pakaian hilang dan tingkat kesalahan tidak dikuantifikasi dalam wawancara.                  |
| 3   | Pencatatan Keuangan                 | Pemilik belum memiliki pencatatan keuangan yang terperinci sehingga rangkuman pendapatan dan pengeluaran belum terdokumentasi secara sistematis.   | Pencatatan keuangan masih sederhana/manual; uang operasional digunakan untuk kebutuhan seperti plastik, pewangi, deterjen, listrik, dan perbaikan. Keuangan laundry dan Warmindo dipisahkan. | Durasi rekapitulasi dan nilai selisih keuangan tidak disebutkan dalam wawancara; perlu pengukuran langsung. |

## **3\. Perumusan Problem Statement Kontekstual**

Berdasarkan analisis di atas, rumuskan **Problem Statement** utama dalam 1–2 paragraf terstruktur.  
_Petunjuk_: Hindari mendefinisikan masalah sebagai _"Mitra belum memiliki aplikasi Python/komputer"_. Definisikan dari hambatan bisnis nyata mitra!

Rumusan Problem Statement Kelompok:  
"Brilian Laundry menjalankan pencatatan pesanan, data pelanggan, berat laundry, serta data laundry masuk dan keluar secara manual. Identifikasi pakaian terutama mengandalkan nama pada kantong dan ingatan, sementara jumlah pakaian belum selalu dicatat secara konsisten. Dalam wawancara juga disebutkan bahwa pakaian atau kaus kaki pernah hilang/terlepas dari jemuran. Selain itu, pencatatan keuangan usaha masih sederhana dan belum terperinci. Kondisi tersebut menunjukkan kebutuhan untuk meningkatkan keterlacakan pesanan dan pakaian serta kerapian pencatatan operasional dan keuangan melalui sistem informasi sederhana. Waktu transaksi, frekuensi kejadian kehilangan, dan durasi rekap belum diukur, sehingga diperlukan observasi lanjutan untuk menetapkan baseline kuantitatif."

## **4\. Menetapkan Batasan Sistem (System Boundary / Scope Alignment)**

Untuk mencegah terjadinya pembengkakan fitur (_Scope Creep_) yang membahayakan penyelesaian proyek dalam 1 semester, tentukan secara tegas apa yang **Masuk Cakupan (_In-Scope_)** dan apa yang **Di Luar Cakupan (_Out-of-Scope_)**:

┌───────────────────────────────────────────┐

│ SYSTEM BOUNDARY (BATASAN SISTEM) │

│ │

│ \[ IN-SCOPE: Fitur yang Akan Dibangun \] │

│ 1. Pencatatan pesanan laundry dan data pelanggan. │

│ 2. Pencatatan berat, jenis layanan, dan estimasi waktu selesai. │

│ 3. Pelacakan status laundry serta rekap data operasional harian. │

│  4. fitur pencatatan identitas dan jumlah pakaian. │

│─────────────────────────────────────────── │

│ │

│ \[ OUT-OF-SCOPE: Di Luar Cakupan Proyek \] │

│ 1. Integrasi pembayaran otomatis melalui e-wallet / QRIS. │

│ 2. Penggajian karyawan / manajemen HRD. │

│ 3. Integrasi pemesanan otomatis ke pemasok dan pengelolaan banyak cabang.│

### **Tabel Penegasan Cakupan Proyek (_Scope Alignment Table_)**

| No  | Modul / Fitur Sistem                                        | Status Cakupan (In-Scope / Out-of-Scope) | Alasan Pertimbangan Kelayakan (O'Brien)                                                                                                       |
| --- | ----------------------------------------------------------- | ---------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | Input Pesanan dan Data Pelanggan                            | IN-SCOPE                                 | Kelayakan operasional: membantu menyimpan informasi pelanggan dan pesanan secara lebih terstruktur dibandingkan catatan manual.               |
| 2   | Pencatatan Berat, Jenis Layanan, dan Status Laundry         | IN-SCOPE                                 | Kelayakan teknis: data dan status pesanan dapat dikelola menggunakan program sederhana; rincian kebutuhan perlu dikonfirmasi dengan mitra.    |
| 3   | Rekap Data Operasional Harian                               | IN-SCOPE                                 | Kelayakan ekonomi/operasional: membantu pemilik meninjau data pesanan dan catatan usaha dengan lebih teratur.                                 |
| 4  | Pencatatan identitas dan jumlah pakaian  |
IN-SCOPE       | Kelakayan Operasional: membantu pemilik mengidentifikasi dan memeriksa jumlah serta jenis pakaian milik setiap pelanggan secara lebih terstruktur sehingga meningkatkan keterlacakan pakaian. | 
| 5   | Pembayaran Online / Payment Gateway                         | OUT-OF-SCOPE                             | Tidak menjadi kebutuhan yang teridentifikasi dalam wawancara dan dapat menambah kompleksitas proyek.                                          |
| 6   | Penggajian, Multi-Cabang, dan Pemesanan Otomatis ke Pemasok | OUT-OF-SCOPE                             | Tidak sesuai dengan kebutuhan yang teridentifikasi saat wawancara awal; usaha dikelola oleh keluarga dan kebutuhan tersebut belum dinyatakan. |
## **5\. Target Metrik Keberhasilan Solusi (To-Be Targets)**

Target berikut merupakan usulan awal berdasarkan hasil wawancara, bukan hasil pengukuran. Validasi target setelah baseline waktu transaksi, kelengkapan pencatatan, dan durasi rekap dikumpulkan melalui observasi.

| Indikator Kinerja              | Kondisi As-Is (Baseline)                                                                                    | Target To-Be (Expected)                                                     | Estimasi Persentase Peningkatan                                |
| ------------------------------ | ----------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | -------------------------------------------------------------- |
| Kelengkapan pencatatan pesanan | Pencatatan manual; persentase kelengkapan belum diukur.                                                     | Usulan: seluruh pesanan yang masuk dicatat pada sistem.                     | Belum dapat dihitung sebelum baseline diukur.                  |
| Keterlacakan pakaian/pesanan   | Identifikasi terutama melalui nama pada kantong dan ingatan; jumlah pakaian belum selalu dicatat konsisten. | Usulan: setiap pesanan memiliki identitas dan status yang dapat ditelusuri. | Belum dapat dihitung; perlu data kejadian awal dan uji sistem. |
| Kerapian rekap data/keuangan   | Pencatatan keuangan sederhana dan belum terperinci; durasi rekap tidak disebutkan.                          | Usulan: rekap operasional harian dapat dibuat dari data yang tersimpan.     | Belum dapat dihitung sebelum durasi rekap diukur.              |

_Catatan validitas data: Dokumen ini disesuaikan dengan rekaman wawancara Laundry Brillyan. Angka 90 detik/transaksi, selisih stok 12%, dan durasi rekap 60–90 menit yang tercantum pada template awal tidak didukung oleh wawancara, sehingga tidak digunakan sebagai fakta. Usaha mitra juga merupakan laundry yang berdampingan dengan Warmindo; masalah stok barang ritel tidak dinyatakan sebagai masalah utama dalam wawancara._

## **6\. Refleksi & Lembar Pengesahan Phase Lead**

### **A. Pertanyaan Refleksi Tim**

1. _Bagaimana tim memastikan bahwa batasan proyek yang ditetapkan realistis untuk diselesaikan dalam 16 minggu?_
   - Jawab: Batasan awal difokuskan pada pencatatan pesanan, data pelanggan, berat/jenis layanan, status laundry, dan rekap operasional. Fitur tersebut relatif sesuai untuk proyek PBL Level 1 karena dapat dibuat sebagai program sederhana. Kelayakan dan prioritas fitur tetap perlu dikonfirmasi dengan mitra serta disesuaikan dengan kemampuan tim dan waktu pengerjaan.
2. _Apakah pemilik usaha mitra telah menyetujui batasan sistem yang diusulkan oleh kelompok?_
   - Jawab: Persetujuan pemilik terhadap batasan sistem belum dapat dipastikan dari rekaman wawancara yang tersedia. Kelompok perlu mengonfirmasi usulan cakupan ini kepada Bu Erna sebelum menetapkannya sebagai kebutuhan final.

### **B. Tanda Tangan Pengesahan Phase Lead 2**

Disusun oleh Phase Lead 2 (Frame): Fikajun Wolek Arifin — NIM: \[2638016029\]

Tanggal Penyusunan: \[29/10/2026\]

```
Tanda Tangan Phase Lead 2: ____________________
Diverifikasi oleh Dosen Pengampu / Coach:
```

Tanggal: \[isi tanggal\] | Status Checkpoint: \[diisi dosen\]

Catatan Dosen: \[diisi dosen\]