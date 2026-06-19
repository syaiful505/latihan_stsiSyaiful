# Rangkuman & Latihan Soal STSI4208 - Analisis dan Perancangan Sistem (UT)

---

## 📖 RANGKUMAN MATERI INTI

### 1. Konsep Dasar Sistem
- **Sistem**: kumpulan elemen yang saling berinteraksi untuk mencapai tujuan
- **Elemen sistem**: manusia, hardware, software, data, prosedur
- **Karakteristik sistem**: komponen, batasan, lingkungan, input, proses, output, umpan balik

### 2. SDLC (System Development Life Cycle)
Tahapan:
1. **Planning** - perencanaan, studi kelayakan, identifikasi proyek
2. **Analysis** - analisis kebutuhan, pengumpulan data, pemodelan
3. **Design** - perancangan sistem (DFD, ERD, UML, UI/UX)
4. **Implementation** - coding, testing, deployment
5. **Maintenance** - pemeliharaan, perbaikan

### 3. Metode Pengembangan Sistem
- **Waterfall** - sequential linear
- **Iterative** - pengulangan bertahap
- **Prototyping** - membuat purwarupa
- **Agile/Scrum** - iteratif cepat, kolaboratif

### 4. Analisis Kebutuhan
- **Kebutuhan Fungsional**: fitur yang harus ada (contoh: login, cetak laporan)
- **Kebutuhan Non-Fungsional**: keamanan, performa, usability
- **Teknik Elisitasi**: wawancara, kuesioner, observasi, studi dokumen, FGD

### 5. Data Flow Diagram (DFD)
- **Diagram Konteks** (level 0): gambaran umum sistem, 1 proses dengan entitas luar
- **DFD Level 0** (overview): proses utama dan data store
- **DFD Level 1+**: rincian proses
- **Simbol**: proses (lingkaran), entitas luar (persegi), data store (garis sejajar), aliran data (panah)

### 6. Entity Relationship Diagram (ERD)
- **Entitas**: objek data (Mahasiswa, Dosen, MataKuliah)
- **Atribut**: properti entitas (nim, nama, alamat)
- **Relasi**: hubungan antar entitas (1:1, 1:N, M:N)
- **Primary Key**: identifier unik
- **Foreign Key**: referensi ke entitas lain

### 7. UML (Unified Modeling Language)
Diagram utama:
- **Use Case Diagram** - interaksi aktor dengan sistem
- **Activity Diagram** - alur aktivitas bisnis
- **Sequence Diagram** - urutan interaksi objek
- **Class Diagram** - struktur kelas/objek

### 8. Perancangan Basis Data & Normalisasi
- **1NF**: hilangkan repeating group, atomik
- **2NF**: hilangkan partial dependency
- **3NF**: hilangkan transitive dependency
- **Tahapan**: requirements → conceptual → logical → physical → implementation

### 9. Perancangan Input/Output
- **Input**: form entri data, validasi, user-friendly
- **Output**: laporan (tabel, grafik), screen display, cetak
- **Prototyping**: mockup UI sebelum implementasi

### 10. Dokumentasi Sistem
- **SKPL** (Spesifikasi Kebutuhan Perangkat Lunak) / SRS
- **DPPL** (Deskripsi Perancangan Perangkat Lunak) / SDD
- Manual user, manual teknis

---

## 📝 SOAL LATIHAN ESSAY + JAWABAN

---

### SOAL 1: Perancangan Input dan Output
**Soal:** Perancangan Sistem Terinci terdiri atas perancangan Input dan perancangan Output. Jelaskan perbedaan keduanya dan berikan contoh hasil perancangan Input/Output dalam mengembangkan sistem!

**Jawaban:**

| Aspek | Perancangan Input | Perancangan Output |
|-------|-------------------|-------------------|
| Tujuan | Menerima data dari pengguna ke sistem | Menyajikan hasil olahan data ke pengguna |
| Fokus | Kemudahan entri, validasi data | Keterbacaan, relevansi informasi |
| Contoh | Form pendaftaran, form transaksi | Laporan penjualan, grafik, invoice |
| Validasi | Format data, range check, required field | Tidak ada (data sudah jadi) |

**Contoh Perancangan Input:** Form pendaftaran mahasiswa baru dengan field: Nama, NIM, Tempat Lahir, Tanggal Lahir, Alamat, No HP, dilengkapi validasi (NIM harus angka 10 digit, No HP harus angka).

**Contoh Perancangan Output:** Laporan data mahasiswa per semester dalam bentuk tabel yang menampilkan NIM, Nama, IPK, Status, dan bisa diexport ke PDF/Excel.

---

### SOAL 2: Tujuan Perancangan Output
**Soal:** Sebutkan tujuan perancangan Output dan buatlah contoh perancangan Output pada sebuah organisasi!

**Jawaban:**

**Tujuan perancangan output:**
1. Menyajikan informasi yang akurat dan tepat waktu
2. Memudahkan pengambilan keputusan
3. Memenuhi kebutuhan pengguna (user-friendly)
4. Mendukung operasional bisnis
5. Dokumentasi dan arsip

**Contoh:** Sistem Informasi Perpustakaan
- Output cetak: Kartu anggota, label buku, slip peminjaman
- Output layar: Daftar buku tersedia, histori peminjaman
- Output grafik: Grafik peminjaman per bulan
- Output laporan: Laporan buku paling sering dipinjam, laporan denda

---

### SOAL 3: Tahapan Perancangan Basis Data
**Soal:** Sebutkan dan jelaskan 6 tahapan perancangan basis data!

**Jawaban:**
1. **Pengumpulan dan Analisis Kebutuhan** - mengidentifikasi data apa saja yang dibutuhkan user, aturan bisnis, dan batasan
2. **Perancangan Konseptual** - membuat ERD, mendefinisikan entitas, atribut, dan relasi tanpa mempertimbangkan teknis
3. **Pemilihan DBMS** - memilih sistem manajemen basis data (MySQL, PostgreSQL, Oracle, SQL Server) sesuai kebutuhan
4. **Perancangan Logikal** - mapping ERD ke skema relasional (tabel, primary key, foreign key, normalisasi)
5. **Perancangan Fisikal** - menentukan struktur penyimpanan fisik (indexing, partisi, tipe data)
6. **Implementasi** - membuat database actual dengan DDL SQL, mengisi data awal, dan pengujian

---

### SOAL 4: Entity Relationship Diagram (ERD)
**Soal:** Rancanglah diagram E-R dari kasus aplikasi database sederhana untuk sistem informasi akademis suatu universitas. Entities: mahasiswa, dosen, mata_kuliah, ruang.

**Jawaban:**

**Entitas dan Atribut:**
- **Mahasiswa** (nim, nama, alamat, tgl_lahir, no_hp, email)
- **Dosen** (nip, nama, alamat, no_hp, email, spesialisasi)
- **MataKuliah** (kode_mk, nama_mk, sks, semester)
- **Ruang** (kode_ruang, nama_ruang, kapasitas, lokasi)

**Relasi:**
- Mahasiswa - MataKuliah (M:N) melalui **KRS** (nim, kode_mk, semester, nilai)
- Dosen - MataKuliah (1:N) → satu dosen mengajar banyak mata kuliah
- MataKuliah - Ruang (M:N) melalui **Jadwal** (kode_mk, kode_ruang, hari, jam)

**Derajat Kardinalitas:**
- Mahasiswa : KRS = 1 : N (satu mahasiswa bisa ambil banyak MK)
- KRS : MataKuliah = N : 1 (banyak mahasiswa ambil satu MK)
- Dosen : MataKuliah = 1 : N (satu dosen ajar banyak MK)
- MataKuliah : Jadwal = 1 : N
- Ruang : Jadwal = 1 : N

---

### SOAL 5: Use Case & Activity Diagram
**Soal:** Buatlah use case diagram dan activity diagram untuk proses pendaftaran mahasiswa baru di Universitas!

**Jawaban:**

**Use Case Diagram:**
- **Aktor:** Calon Mahasiswa, Staff Administrasi, Keuangan
- **Use Case:**
  - Calon Mahasiswa: Mendaftar Akun, Mengisi Form Pendaftaran, Upload Dokumen, Cek Status
  - Staff Administrasi: Verifikasi Data, Validasi Dokumen, Menentukan Jadwal Tes
  - Keuangan: Memverifikasi Pembayaran

**Activity Diagram - Proses Pendaftaran Mahasiswa Baru:**
1. Calon mahasiswa membuka website PMB
2. Sistem menampilkan form registrasi
3. Calon mahasiswa mengisi data diri
4. Sistem validasi data (jika valid → lanjut, jika tidak → kembali ke step 2)
5. Upload dokumen (ijazah, KK, KTP, foto)
6. Sistem verifikasi dokumen
7. Staff admin memverifikasi kelengkapan
8. Sistem generate nomor pendaftaran
9. Calon mahasiswa melakukan pembayaran
10. Keuangan memverifikasi pembayaran
11. Sistem mengirim kartu ujian
12. Selesai

---

### SOAL 6: DFD - Diagram Konteks
**Soal:** Sebuah perusahaan taksi mengembangkan sistem pemesanan taksi (SiPeTax). Spesifikasi: (1) melayani permintaan pesanan pelanggan, (2) menerima status dan lokasi armada dari pengemudi, (3) mendistribusikan pesanan ke PDA pengemudi, (4) laporan pengangkutan ke manager. Buat Diagram Konteks dan DFD Level 0!

**Jawaban:**

**Diagram Konteks (Level 0):**
```
[Pelanggan] ----(data pesanan)---> [Sistem SiPeTax] ----(info pesanan)---> [Pelanggan]
                    <---(konfirmasi)---                        ---(status)---->
                       
[Pengemudi] ----(lokasi & status)---> [Sistem SiPeTax] ----(distribusi pesanan)---> [Pengemudi]
                    <---(konfirmasi)---                        ---(info)---->

[Manager] <---(laporan pengangkutan)--- [Sistem SiPeTax]
```
Entitas Luar: Pelanggan, Pengemudi, Manager

**DFD Level 0 (Proses Utama):**
- **1.0 Kelola Pesanan**: menerima pesanan, konfirmasi ke pelanggan
- **2.0 Kelola Armada**: terima lokasi & status pengemudi
- **3.0 Distribusi Pesanan**: kirim pesanan ke PDA pengemudi terdekat
- **4.0 Buat Laporan**: generate laporan untuk manager

Data Store: D1-Pesanan, D2-Armada, D3-Laporan

---

### SOAL 7: Analisis Sistem - Studi Kelayakan
**Soal:** Sebutkan jenis-jenis studi kelayakan dalam analisis sistem!

**Jawaban:**
1. **Kelayakan Teknis** - apakah teknologi yang dibutuhkan tersedia? apakah tim punya kemampuan?
2. **Kelayakan Ekonomi** - apakah manfaat > biaya? analisis cost-benefit, ROI, payback period
3. **Kelayakan Operasional** - apakah user siap? apakah proses bisnis mendukung?
4. **Kelayakan Jadwal** - apakah bisa selesai tepat waktu?
5. **Kelayakan Hukum** - apakah sesuai regulasi & perundangan?

---

### SOAL 8: Normalisasi Database
**Soal:** Lakukan normalisasi 1NF, 2NF, dan 3NF pada tabel berikut:
Tabel: TransaksiPenjualan (no_transaksi, tgl, id_pelanggan, nama_pelanggan, id_barang, nama_barang, harga, qty, total)

**Jawaban:**

**1NF (hilangkan repeating group, setiap field atomik):**
Sudah 1NF karena semua field atomik.

**2NF (hilangkan partial dependency - tergantung sebagian dari PK):**
PK komposit: (no_transaksi, id_barang)

- **Transaksi** (no_transaksi, tgl, id_pelanggan, nama_pelanggan)
- **DetailTransaksi** (no_transaksi, id_barang, qty, harga)
- **Barang** (id_barang, nama_barang)

**3NF (hilangkan transitive dependency):**
- **Transaksi** (no_transaksi, tgl, id_pelanggan)
- **Pelanggan** (id_pelanggan, nama_pelanggan)
- **DetailTransaksi** (no_transaksi, id_barang, qty, harga)
- **Barang** (id_barang, nama_barang)

---

### SOAL 9: UML - Perbedaan Diagram
**Soal:** Jelaskan perbedaan Use Case Diagram, Activity Diagram, Sequence Diagram, dan Class Diagram!

**Jawaban:**

| Diagram | Fungsi | Elemen Utama |
|---------|--------|-------------|
| **Use Case** | Menunjukkan siapa yang menggunakan sistem dan apa saja yang bisa dilakukan | Aktor, Use Case, Relasi (include/extend) |
| **Activity** | Alur proses/aktivitas bisnis | Start, Activity, Decision, Fork, Join, End |
| **Sequence** | Urutan interaksi antar objek secara kronologis | Lifeline, Activation, Message, Return |
| **Class** | Struktur statis kelas, atribut, dan method | Class, Atribut, Method, Association, Inheritance |

---

### SOAL 10: Studi Kasus Lengkap
**Soal:** Kepala perpustakaan akan mengembangkan otomasi sistem perpustakaan dengan barcode/QR code scanner. Entitas: peminjam, penerbit, kepala perpustakaan. Buat DFD Context dan DFD Level 1!

**Jawaban:**

**Diagram Konteks:**
```
[Peminjam] ----(data peminjaman)---> [Sistem Perpustakaan] ----(info buku)---> [Peminjam]
               <---(konfirmasi)---                     ---(laporan)---> [Kepala Perpustakaan]

[Penerbit] ----(data buku baru)---> [Sistem Perpustakaan]
```

**DFD Level 1 (Proses):**
- 1.0 Pendataan Buku (input data buku baru oleh petugas)
- 2.0 Peminjaman Buku (scan barcode anggota & buku, simpan transaksi)
- 3.0 Pengembalian Buku (scan barcode, hitung denda jika telat)
- 4.0 Laporan (laporan peminjaman, pengembalian, denda ke Kepala Perpustakaan)

Data Store: D1-Buku, D2-Anggota, D3-Transaksi

---

### SOAL 11: Metode Pengembangan
**Soal:** Jelaskan perbedaan metode Waterfall, Prototyping, dan Agile!

**Jawaban:**

| Aspek | Waterfall | Prototyping | Agile |
|-------|-----------|-------------|-------|
| Pendekatan | Sequential linear | Iteratif dengan purwarupa | Iteratif, incremental |
| Perubahan | Sulit diakomodasi | Mudah | Sangat mudah |
| Dokumentasi | Lengkap | Sedang | Minimal |
| Keterlibatan user | Awal & akhir | Terus menerus | Terus menerus |
| Cocok untuk | Proyek jelas & stabil | Kebutuhan belum jelas | Proyek dinamis & cepat |
| Contoh | Sistem pemerintahan | Startup aplikasi baru | Scrum, XP, Kanban |

---

### SOAL 12: Kebutuhan Fungsional vs Non-Fungsional
**Soal:** Jelaskan perbedaan kebutuhan fungsional dan non-fungsional, berikan 3 contoh masing-masing untuk sistem e-commerce!

**Jawaban:**

**Kebutuhan Fungsional** (apa yang sistem LAKUKAN):
1. Pengguna dapat login menggunakan email dan password
2. Sistem dapat menampilkan daftar produk berdasarkan kategori
3. Sistem dapat memproses pembayaran via transfer bank/ kartu kredit
4. Admin dapat menambah/mengedit/menghapus produk
5. Sistem dapat mengirim notifikasi status pesanan

**Kebutuhan Non-Fungsional** (BAGAIMANA sistem bekerja):
1. **Performa**: halaman harus loading < 3 detik
2. **Keamanan**: data pengguna harus dienkripsi (SSL/HTTPS)
3. **Usability**: sistem harus responsif di mobile & desktop
4. **Availability**: sistem harus uptime 99.9%
5. **Scalability**: sistem harus bisa layani 10.000 user bersamaan

---

### SOAL 13: PDCA & Bagan Terstruktur
**Soal:** Buatlah bagan terstruktur minimal 3 level untuk sistem informasi penerimaan mahasiswa baru berdasarkan DFD Level 0!

**Jawaban:**
```
Sistem Informasi PMB
├── Level 1: Kelola Pendaftaran
│   ├── Level 2: Input Data Pendaftar
│   ├── Level 2: Validasi Data
│   └── Level 2: Generate No Pendaftaran
├── Level 1: Kelola Pembayaran
│   ├── Level 2: Verifikasi Pembayaran
│   └── Level 2: Update Status Pembayaran
├── Level 1: Kelola Pengumuman
│   ├── Level 2: Input Hasil Seleksi
│   └── Level 2: Cetak Pengumuman
└── Level 1: Buat Laporan
    ├── Level 2: Laporan Pendaftar
    └── Level 2: Laporan Penerimaan
```

---

### SOAL 14: Teknik Pengumpulan Data
**Soal:** Sebutkan dan jelaskan 5 teknik pengumpulan data/elisitasi kebutuhan dalam analisis sistem!

**Jawaban:**
1. **Wawancara** - tanya jawab langsung dengan stakeholder, dapat data mendalam (kelebihan: detail, kekurangan: memakan waktu)
2. **Kuesioner** - daftar pertanyaan tertulis untuk banyak responden (kelebihan: cepat, kekurangan: kurang mendalam)
3. **Observasi** - mengamati langsung proses bisnis yang berjalan (kelebihan: data real, kekurangan: subjektif)
4. **Studi Dokumen** - mempelajari dokumen sistem yang ada (SOP, laporan, form) (kelebihan: data historis, kekurangan: mungkin sudah usang)
5. **FGD (Focus Group Discussion)** - diskusi kelompok terarah dengan beberapa stakeholder (kelebihan: banyak sudut pandang, kekurangan: dominasi peserta tertentu)

---

### SOAL 15: Diagram Konteks Sistem Pembayaran Elektronik
**Soal:** Buatlah Diagram Konteks dan DFD Level 0 untuk sistem pembayaran elektronik pada marketplace!

**Jawaban:**

**Diagram Konteks:**
```
[Pelanggan] ----(pesanan & pembayaran)---> [Sistem Pembayaran Elektronik] ----(konfirmasi)---> [Pelanggan]
[Marketplace] ----(data pesanan)---> [Sistem Pembayaran Elektronik] <---(status)---> [Marketplace]
[Bank/Gateway] <---(verifikasi)---> [Sistem Pembayaran Elektronik]
```

**DFD Level 0 - Proses:**
- 1.0 Registrasi Pesanan: menerima data pesanan dari marketplace
- 2.0 Proses Pembayaran: mengirim detail pembayaran ke gateway
- 3.0 Verifikasi Pembayaran: memverifikasi transaksi melalui bank
- 4.0 Konfirmasi Pesanan: mengirim status ke marketplace & pelanggan

Data Store: D1-Pesanan, D2-Detail Pembayaran, D3-Transaksi, D4-Status Pesanan

---

## ✅ TIPS MENJAWAB SOAL ESSAY UAS STSI4208

1. **Pahami konsep, bukan hafalan** - soal essay UT menguji pemahaman.
2. **Gambar diagram** - jika diminta DFD/ERD/UML, gambar dengan rapi, beri label jelas.
3. **Struktur jawaban**: definisi → penjelasan → contoh.
4. **Kasus studi**: baca skenario, identifikasi entitas/proses/data, baru gambar diagram.
5. **Sebutkan istilah teknis** dalam bahasa Indonesia/Inggris sesuai modul.
6. **kelola waktu**: soal bobot besar (30-40 poin) kerjakan lebih dulu.

**Topik yang paling sering muncul di UAS:**
- DFD (Context Diagram + Level 0/1) ⭐⭐⭐⭐⭐
- ERD + Normalisasi ⭐⭐⭐⭐
- Use Case Diagram + Activity Diagram ⭐⭐⭐⭐
- Perbedaan pendekatan terstruktur vs OOP ⭐⭐⭐
- Perancangan Input/Output ⭐⭐⭐
- Studi Kelayakan ⭐⭐⭐
- SDLC ⭐⭐⭐
- Sequence Diagram ⭐⭐

---

_Semoga membantu! Selamat belajar dan sukses ujian besok! 🎯_
