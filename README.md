# Kubeconfig Manager

Kubeconfig Manager adalah skrip bash sederhana yang memungkinkan Anda untuk dengan mudah mengganti kubeconfig aktif di sistem Anda. Skrip ini menggunakan fuzzy finder (fzf) untuk memberikan antarmuka yang nyaman dalam memilih kubeconfig.

## Fitur

- Menampilkan daftar kubeconfig yang tersedia menggunakan fuzzy finder
- Mengubah kubeconfig aktif dengan cepat
- Simpel dan mudah digunakan

## Prasyarat

Sebelum menggunakan skrip ini, pastikan Anda telah menginstal:

1. `bash` (biasanya sudah terinstal di sebagian besar sistem Unix-like)
2. `fzf` (Fuzzy Finder) - [Panduan Instalasi fzf](https://github.com/junegunn/fzf#installation)

## Instalasi

1. Clone repositori ini atau unduh file `kube` ke sistem Anda.

2. Buat file `kube` dapat dieksekusi:
3. Pindahkan file `kube` ke direktori yang ada dalam PATH Anda, misalnya:
   sudo mv kube /usr/local/bin/
4. Buat direktori untuk menyimpan file-file kubeconfig Anda (jika belum ada):
   mkdir -p ~/.kube/config-file
5. Pindahkan atau salin file-file kubeconfig Anda ke direktori `~/.kube/config-file/`.

## Penggunaan

1. Buka terminal.

2. Jalankan skrip dengan mengetikkan:
   kube
3. Gunakan fuzzy finder untuk memilih kubeconfig yang ingin Anda gunakan.

4. Tekan Enter untuk mengonfirmasi pilihan Anda.

Skrip akan secara otomatis mengubah kubeconfig aktif Anda ke file yang dipilih.

## Catatan

- Skrip ini mengasumsikan bahwa file kubeconfig aktif Anda berada di `~/.kube/config`.
- Semua file kubeconfig yang ingin Anda kelola harus disimpan di direktori `~/.kube/config-file/`.

## Kontribusi

Kontribusi untuk proyek ini sangat diterima. Jangan ragu untuk membuat issue atau pull request.
