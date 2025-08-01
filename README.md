# OpenWrt Firmware Porting Workflow 🚀

Workflow ini mengekstrak `rootfs` dari firmware sumber, kemudian membangun kembali image firmware baru menggunakan kernel dan bootloader yang sesuai untuk perangkat tujuan yang dipilih.

***
## 🔧 Cara Penggunaan

Untuk menjalankan workflow ini, ikuti langkah-langkah berikut:

1.  Fork Repo ini.
2.  Buka tab **Actions** pada repositori GitHub Anda.
3.  Pada sidebar kiri, klik pada workflow **"Porting Openwrt Amlogic"**.
4.  Klik tombol **"Run workflow"** yang muncul di sebelah kanan.
5.  Isi sesuai dengan SOC tujuan Porting:
    * **`Copy link file firmware`**: Masukkan link URL lengkap ke file firmware (`.img`, `.img.gz`, atau `.img.xz`) yang ingin Anda porting.
    * **`Pilih target board device`**: Pilih seri SoC atau nama spesifik perangkat Amlogic tujuan Anda dari menu dropdown.
    * **`Pilih versi kernel`**: Pilih versi kernel yang ingin digunakan pada firmware baru.
    * **`Set Nama Builder`** (Opsional): Masukkan nama Anda atau nama kustom yang akan tertera pada informasi build.
6.  Klik tombol hijau **"Run workflow"** untuk memulai proses.

Proses build akan berjalan dan Anda bisa memantau progresnya langsung di halaman "Actions".


***
## 📦 Output

Setelah workflow berhasil diselesaikan, hasilnya dapat ditemukan di:
-   **GitHub Releases**: Sebuah rilis baru akan dibuat secara otomatis dengan tag `Build-[nama_board]-[id_run]`.
-   **Artifacts**: Rilis tersebut akan berisi file firmware yang sudah di-porting dengan format `img.gz`

Nama file akan mengikuti format: **`[Nama_Firmware_Asli]_[Board_Tujuan].img.gz`**.

***
## 🙏 Ucapan Terima Kasih

Workflow ini sangat bergantung pada action luar biasa yang dibuat oleh
**ophub**. [ophub/amlogic-s9xxx-openwrt](https://github.com/ophub/amlogic-s9xxx-openwrt).
**Om Haris**. (https://github.com/Haris131/extract-img)
**Om Edi**. (https://github.com/edikurexe/extract-img)
