# uts-so-09011282530065
# Tugas Besar UTS Sistem Operasi
## 1. Identitas
- **Nama:** Meila Irtiyah Dekha Putri
- **NIM:** 09011282530065
- **Kelas:** SKU3B

## 2. Deskripsi
Repositori ini berisi sekumpulan shell script otomatisasi Linux untuk mencari file teks praktikum berformat `.txt` (termasuk di dalam subdirektori), mengarsip dan mengompresnya ke dalam format `.tar.gz` dengan penamaan berbasis waktu (*timestamp*), serta mencatat aktivitas ke dalam file *log*. Dilengkapi juga dengan skrip perulangan latar belakang (*background loop*) dan manajemen alias.

## 3. Cara Menjalankan
- **Backup Manual:**
```bash
./script/backup.sh

## 4. Fitur Pengembangan

**Pencarian Otomatis Berdasarkan Ekstensi:** Skrip dirancang untuk mendeteksi dan memfilter file teks `.txt` secara rekursif hingga ke dalam subdirektori.
**Manajemen Log Aktivitas:** Setiap proses backup atau eksekusi perintah dicatat secara otomatis ke dalam file *log*.
**Integrasi Alias Kustom:** Mempermudah pemanggilan skrip utama dengan mendefinisikan alias khusus pada sistem shell.

## 5. Bukti Job Control

Pengujian pengelolaan proses latar belakang (*background processes*) menggunakan perintah manajemen job Linux:

**Menjalankan Proses di Latar Belakang:**
  ```bash
  ./script/background_loop.sh &
Melihat Daftar Job Aktif:
jobs -l
Mengembalikan Job ke Latar Depan:
fg %1
Menghentikan Job secara Paksa:
kill -9 <PID>

## 6. Kendala dan Solusi
Kendala 1: Hak akses file (permission) skrip belum bisa dieksekusi (Permission denied).

Solusi: Memberikan izin eksekusi menggunakan perintah chmod +x script/*.sh.

Kendala 2: Proses latar belakang terus berjalan di terminal.

Solusi: Memantau proses menggunakan ps aux lalu menghentikannya menggunakan perintah kill.
