# 🤖 Repositori Aktivitas Otomatis

Selamat datang! Repositori ini berisi sebuah *script* sederhana yang berjalan secara otomatis setiap hari untuk melakukan *commit*.

## 🎯 Tujuan Proyek Ini

Tujuan utama dari repositori ini adalah sebagai sarana belajar dan eksplorasi, bukan untuk memalsukan metrik aktivitas. Secara spesifik, proyek ini bertujuan untuk:

* **Mempelajari cara kerja GitHub Actions** sebagai platform CI/CD (Continuous Integration/Continuous Deployment).
* **Memahami penggunaan jadwal `cron`** untuk automasi tugas rutin.
* **Berlatih menulis file konfigurasi** dalam format `.yml` (YAML).
* Mendemonstrasikan kemampuan untuk mengotomatisasi alur kerja `git`.

> **Catatan Penting:** Proyek ini adalah sebuah eksperimen teknis. Untuk melihat kontribusi dan proyek pengembangan perangkat lunak saya yang sebenarnya, silakan kunjungi repositori saya yang lain di profil ini.

## ⚙️ Bagaimana Cara Kerjanya?

Automasi ini dicapai sepenuhnya menggunakan **GitHub Actions**.

1.  Sebuah *workflow* yang didefinisikan di file `.github/workflows/auto_commit.yml` diatur untuk berjalan pada jadwal yang telah ditentukan.
2.  Setiap kali jadwalnya tiba (misalnya, setiap hari pada jam 12:00 WIB), GitHub akan menyiapkan sebuah *runner* (lingkungan virtual).
3.  *Runner* tersebut akan melakukan *checkout* kode dari repositori ini.
4.  Sebuah perintah *shell* kemudian dieksekusi untuk menambahkan baris baru ke file `activity.log`, yang berisi catatan waktu.
5.  Terakhir, *runner* akan mengonfigurasi `git`, lalu melakukan `commit` dan `push` perubahan tersebut kembali ke repositori.

## 🛠️ Teknologi yang Digunakan

* **GitHub Actions**
* **YAML**
* **Shell Script**

## 📄 Log Aktivitas

Semua *commit* otomatis yang dibuat oleh bot ini akan dicatat dalam file [activity.log](activity.log).
