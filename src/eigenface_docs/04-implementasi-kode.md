# Membedah Kode (Variabel Bahasa Indonesia)

Agar kamu tidak bingung dengan istilah bahasa Inggris, kode ini sudah diubah menggunakan istilah yang kita gunakan sehari-hari.

## Struktur Variabel Utama

| Nama Variabel | Apa Isinya? | Perannya |
| :--- | :--- | :--- |
| **`rata_rata`** | 1 Baris Angka | Wajah standar manusia. |
| **`A`** | Matriks (Gambar x Pixel) | Kumpulan wajah yang sudah dikurangi rata-rata. |
| **`C`** | Matriks Kecil | Peta hubungan antar gambar dalam dataset. |
| **`nilai_eigen`** | Daftar Angka | Skor tingkat kepentingan sebuah fitur wajah. |
| **`U`** | Matriks Vektor | Hubungan antar gambar (siapa mirip siapa). |
| **`wajah_eigen`** | Matriks Fitur | Inilah "Wajah Hantu" yang menjadi dasar pengenalan. |

## Alur Kerja Fungsi `train()`
Fungsi ini adalah saat komputer "belajar":
1. Ambil semua gambar.
2. Hitung `rata_rata`.
3. Kurangi tiap gambar dengan `rata_rata` (simpan di `A`).
4. Hitung kemiripan gambar di `C`.
5. Cari fitur utama menggunakan fungsi `hitung_eigen_manual`.
6. Simpan hasil akhirnya di `wajah_eigen`.

## Alur Kerja Fungsi `predict()`
Fungsi ini saat komputer "menebak":
1. Ambil foto baru dari kamera.
2. Kurangi dengan `rata_rata`.
3. Proyeksikan ke ruang `wajah_eigen` (dicari "persentase" gabungan wajah hantunya).
4. Bandingkan persentase ini dengan semua orang yang sudah dipelajari.
5. Jika sangat mirip dengan Budi, maka muncul tulisan "Budi".
