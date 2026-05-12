# T4_Mobile

Room Database - CRUD Mahasiswa

---

# Nama  : Arya Rayan Utama
# NIM   : F1D02310106
# Kelas : Mobile C

---

# Fitur Utama

- Login Authentication
- Menampilkan daftar mahasiswa
- Menambahkan data mahasiswa
- Mengedit data mahasiswa
- Menghapus data mahasiswa
- Detail informasi mahasiswa
- Catatan mahasiswa berbasis file `.txt`
- Dark Mode
- Pengaturan notifikasi
- Student Directory
- Profil Admin

---

# Teknologi yang Digunakan

| Teknologi             | Kegunaan                                   |
|-----------------------|--------------------------------------------|
| Kotlin                | Bahasa pemrograman utama Android           |
| Room Database         | Penyimpanan data mahasiswa                 |
| SharedPreferences     | Menyimpan sesi login & pengaturan aplikasi |
| Internal File Storage | Menyimpan catatan mahasiswa                |
| RecyclerView          | Menampilkan list data mahasiswa            |
| ViewBinding           | Menghubungkan layout XML dengan Activity   |
| Coroutines            | Operasi asynchronous pada database         |

---

# Metode Penyimpanan Data

| Metode                | Digunakan Untuk                                         |
|-----------------------|---------------------------------------------------------|
| Room Database         | CRUD data mahasiswa (Nama, NIM, Prodi, Email, Semester) |
| SharedPreferences     | Session login, dark mode, ukuran font, notifikasi       |
| Internal File Storage | Menyimpan catatan mahasiswa dalam file `.txt`           |

---

# Alasan Pemilihan Metode

## Room Database
Digunakan karena data mahasiswa bersifat terstruktur dan membutuhkan proses CRUD serta pencarian data yang efisien.

## SharedPreferences
Cocok digunakan untuk menyimpan data ringan berbentuk key-value seperti status login dan pengaturan aplikasi.

## Internal File Storage
Digunakan untuk menyimpan catatan mahasiswa berupa teks bebas tanpa memerlukan struktur tabel database.

---

# Kendala dan Solusi

**1. Migrasi Database**
Saat skema Room berubah (versi 1 → 2), digunakan `fallbackToDestructiveMigration()` agar tidak crash. Konsekuensinya data terhapus saat versi naik — cukup untuk tahap development.

**2. Duplikasi FileHelper**
Terdapat dua file `FileHelper.kt` di package berbeda. Diselesaikan dengan mengacu hanya pada versi di `utils/` yang lebih lengkap.

**3. Coroutine Tanpa ViewModel**
Operasi Room berjalan di `suspend fun` tanpa ViewModel, sehingga lifecycle management dilakukan manual menggunakan `lifecycleScope` di Activity/Fragment.


# Hasil Screenshot

# Halaman Login
<img width="1080" height="2424" alt="image" src="https://github.com/user-attachments/assets/a6bf1fb5-13a8-43a4-828b-0cc7b5a4d552" />

# Daftar Mahasiswa 
<img width="1080" height="2424" alt="image" src="https://github.com/user-attachments/assets/e9e13d43-74b1-4fbc-86ec-b4a26a826176" />

# Detail Mahasiswa
<img width="1080" height="2424" alt="image" src="https://github.com/user-attachments/assets/e23a520f-c09d-4ee0-92f4-9cb6ed0697b7" />

# Student Directory
<img width="1080" height="2424" alt="image" src="https://github.com/user-attachments/assets/2c67a768-6fc2-44ec-89fe-39bdadc3b864" />

# Edit Data Mahasiswa 
<img width="1080" height="2424" alt="image" src="https://github.com/user-attachments/assets/48f06a25-d5cc-41ea-8889-1ff7b429f6e5" />

# Hapus Data Mahasiswa
<img width="1080" height="2424" alt="image" src="https://github.com/user-attachments/assets/e558e61e-89a6-4fa5-84c9-7cc346a1883f" />

# Profie Admin
<img width="1080" height="2424" alt="image" src="https://github.com/user-attachments/assets/73bbcb46-e5c5-47b2-8e7f-fecc57cc82ab" />
