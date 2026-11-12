# **TPL-07 — Template AI Usage Disclosure & Verification Note**

> **Kategori**: Supporting Evidence (Lampiran Wajib Portfolio)  
> **Mata Kuliah**: Integrasi Lintas MK (Konsep SI, Dasar Pemrograman, Kom. Profesional, B. Inggris)  
> **Sub-CPMK / SFIA**: S-11.1, S-12.1 (Introduce) \| SFIA Generic Level 1–2 (*Ethical AI Literacy*)  
> **Sumber Worksheet**: Dipenuhi bertahap pada setiap fase (*WS01–WS16*) dan dikonsolidasikan pada `WS15`  
> **Petunjuk**: Lampirkan dokumen ini pada setiap pengumpulan tugas (*Core Artifacts D1–D4*). AI digunakan sebagai *co-pilot* (augmentasi). Seluruh klaim wajib diverifikasi secara manual.

---

## **Header Transparansi AI**

* **Nama Proyek**: Digital Problem Framing & Solution Prototype —Tini Laundry dan Kos Putri  
* **Nama Kelompok**: Tim Tulalit
* **Anggota Tim**:  1. Muhammad Subhan Zulfikar / 2600016057  
                    2. Satrio Gemintang Mahameru / 2600016061  
                    3. Cavin Gusti Ramadhani / 2600016064  
                    4. Fikajun Wolek Arifin / 2638016029  
                    5. Brian Ash-Shidiq Saputra / 2600016083
* **Tanggal Pelaporan**: 12/10/2026

---

### **1\. Daftar Penggunaan AI Co-Pilot (*AI Usage Disclosure*)**

Tabel pengungkapan seluruh interaksi bersama alat bantu GenAI (seperti ChatGPT, Claude, GitHub Copilot) sepanjang pengerjaan proyek:

| Kode Artefak | Tool AI yang Digunakan | Bagian / Tugas yang Dibantu AI | Rincian Prompt Utama yang Diberikan | Modifikasi Mandiri yang Dilakukan Mahasiswa |
| :---- | :---- | :---- | :---- | :---- |
| **D1 (Problem Brief)** | Chat GPT  | Membantu merapikan Problem Brief, juga mengoreksi rumusan masalah, serta penjelasan kondisi sistem berjalan. | *"Bantu saya merapikan dokumen Problem Brief (D1), mengoreksi rumusan masalah, serta memperjelas penjelasan mengenai kondisi sistem berjalan (As-Is) agar sesuai dengan temuan observasi dan wawancara Brilian Laundry."* | Mengeliminasi klaim yang terlalu umum, memasukkan angka baseline kuantitatif riil hasil observasi mitra, Menyesuaikan rumusan masalah dan kondisi sistem berjalan berdasarkan hasil observasi serta wawancara, Memperbaiki isi Problem Brief agar sesuai dengan kondisi aktual dan kebutuhan Brilian Laundry. |
| **D2 (System Design)** | Claude | Membantu menyusun draf D2 dari isi WS05, WS06, dan WS07 | Berikan template D2 dari worksheet 05, 06, 07 sebagai bahan, dan isi bagian-bagian D2 dari bahan tersebut | Menentukan sendiri user story dan prioritasnya, mengisi angka baseline dan target dari wawancara dengan Bu Erna, dan menghapus fitur yang di luar cakupan. |
| **D3 (Code Prototype)** | GitHub Copilot | *Autocomplete* fungsi penanganan *input error validation* Python | `# Fungsi untuk memvalidasi input jumlah barang agar berupa angka bulat positif` | Memeriksa ulang logika *looping WHILE*, menguji dengan kasus uji ekstrim, dan menambahkan komentar penjelas. |
| **D4 (Portfolio)** | ChatGPT-4o | Penerjemahan *Executive Summary* ke dalam Bahasa Inggris | *"Translate this executive summary to professional business English within 200 words..."* | Memeriksa keakuratan istilah teknis SI dan memastikan batas kata berada dalam rentang 150–250 kata. |
| **WS03** | ChatGPT | Membantu mengevaluasi hasil observasi dan wawancara,dan memperjelas deskripsi proses bisnis berjalan (As-Is). | *"Bantu saya mengevaluasi hasil observasi dan wawancara Brilian Laundry, menyusun deskripsi proses bisnis berjalan (As-Is), serta memperbaiki isi dokumen agar sesuai dengan kondisi aktual berdasarkan hasil observasi dan wawancara."* | Menyesuaikan deskripsi proses bisnis dengan hasil observasi dan wawancara, Memperbaiki informasi pencatatan pelanggan, jumlah pakaian, identifikasi, dan pemisahan pakaian sesuai kondisi aktual mitra. | 
| **WS04** | ChatGPT | Membantu merumuskan indikator keberhasilan solusi dan mengoreksi kalimat yang rumpang | *"Bantu saya menganalisis hasil WS03 untuk merumuskan indikator keberhasilan solusi yang realistis dan dapat diukur,serta membenahi kaidah kebahasaan. "* | Menyesuaikan rumusan masalah berdasarkan temuan WS03, Memfokuskan ruang lingkup sistem pada pencatatan identitas pesanan dan jumlah pakaian, Mengeliminasi klaim yang terlalu umum dan memastikan indikator keberhasilan dapat diukur. |
| **WS05** | ChatGPT | Membantu mengoreksi User Story dan Given-WhenThen | *"Bantu saya mengoreksi 3 user story yang sudah saya buat berdasarkan permasalahan pada D1 dan ws04 serta koreksi given-when-then"* | Menyesuaikan User Story dengan kebutuhan pemilik laundry serta memeriksa skenario penerimaan agar sesuai dengan fungsi sistem yang direncanakan. |
| **WS07** | ChatGPT | Pemeriksaan dan perbaikan isi dokumen | *"	Meminta koreksi terhadap isi WS07 agar lebih jelas dan konsisten"* | Memilih dan memperbaiki bagian yang sesuai dengan hasil diskusi kelompok |

---

### **2\. Catatan Verifikasi Manual (*Verification Note*)**

Tabel pembuktian verifikasi manual yang dilakukan mahasiswa untuk menjamin kebenaran output GenAI dan mencegah *cognitive atrophy*:

| Kode Artefak | Aspek Output AI yang Diverifikasi | Metode Verifikasi Manual yang Dilakukan | Hasil Verifikasi & Tindakan Koreksi |
| :---- | :---- | :---- | :---- |
| **D1** | Ketepatan rumusan masalah dan penjelasan kondisi sistem berjalan | Mencocokkan isi Problem Brief dengan hasil observasi dan wawancara Brilian Laundry pada `WS03` | Memperbaiki rumusan masalah dan deskripsi kondisi sistem berjalan agar sesuai dengan temuan aktual mitra. |
| **D2** | Isi D2 apakah sama dengan WS05-07, angka metrik, cakupan fitur | Dicek ulang satu per satu dengan Worksheet yang terkait dengan D2 dan hasil persetujuan Bu Erna | Isinya sudah cocok sesuai dengan Worksheet, dan teks template yang tidak relevan kami tidak pakai |
| **D3** | Stabilitas kode program Python dan penanganan eror | Menjalankan *script* di lingkungan komputer (*terminal execution*) dengan 5 *test cases* | Memperbaiki bug *ZeroDivisionError* pada kalkulasi diskon yang dihasilkan oleh AI. |
| **D4** | Tata bahasa Inggris dan keaslian narasi refleksi | Memeriksa keaslian refleksi pribadi menggunakan *checking* mandiri dan pembacaan ulang | Mengganti frasa generik AI dengan pengalaman pribadi nyata saat menghadapi hambatan observasi lapangan. |
| **WS03** | Keakuratan deskripsi proses bisnis As-Is | Membandingkan hasil AI dengan catatan observasi dan wawancara langsung dengan pemilik Brilian Laundry | Mengoreksi informasi pencatatan pelanggan, jumlah pakaian, identifikasi pakaian, dan fasilitas operasional sesuai kondisi aktual. |
| **WS04** | Ketepatan indikator keberhasilan solusi | Memeriksa kesesuaian hasil analisis dengan temuan WS03 dan kebutuhan pemilik Brilian Laundry | Menyesuaikan indikator keberhasilan agar realistis dan terukur. |
| **WS05** | Kesesuaian User Story dan Acceptance Criteria dengan kebutuhan pemilik Brilian Laundry | Memeriksa kesesuaian User Story dan skenario Given-When-Then dengan permasalahan pada D1 dan WS04 serta hasil konfirmasi mitra | Menyesuaikan kebutuhan fungsional dan skenario penerimaan agar sesuai dengan kebutuhan pemilik laundry. |
| **WS07** | IPO dan validasi data | Memeriksa kesesuaian input, proses, output, penyimpanan, dan penanganan kesalahan | Memastikan setiap bagian sudah sesuai dengan fitur yang dirancang |
|  |  |  |  |

---

### **3\. Pernyataan Kejujuran Akademis & Integritas Teknologi**

> **Komitmen Integritas**:  
> *"Kami yang bertanda tangan di bawah ini menyatakan dengan sejujurnya bahwa seluruh daftar penggunaan AI di atas telah dilaporkan secara transparan dan akurat. Kami menegaskan bahwa AI hanya digunakan sebagai sarana pendamping (co-pilot), dan seluruh logika analisis, desain arsitektur, kode program, serta refleksi akhir telah ditelaah, dimodifikasi, dan diverifikasi secara mandiri oleh tim kami. Kami siap mempertanggungjawabkan seluruh penalaran logis (reasoning chain) karya ini pada ujian lisan individu (Oral Defense & Code Walkthrough)."*

**Tanda Tangan Seluruh Anggota Kelompok**:

1. **Muhammad Subhan Zulfikar** — Tanda Tangan: `_______________` — Tanggal: \[DD/MM/YYYY\]  
2. **Satrio Gemintang Mahameru** — Tanda Tangan: `___________________` — Tanggal: \[DD/MM/YYYY\]  
3. **Cavin Gusti Ramadhani** — Tanda Tangan: `___________________` — Tanggal: \[DD/MM/YYYY\]  
4. **Fikajun Wolek Arifin**— Tanda Tangan: `___________________` — Tanggal: \[DD/MM/YYYY\]
5. **Brian Ash-Shidiq Saputra**— Tanda Tangan: `___________________` — Tanggal: \[DD/MM/YYYY\]

---

