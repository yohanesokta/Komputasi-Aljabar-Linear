# Matematika di Balik Eigenface

Mungkin matematika terlihat menyeramkan, tapi di sini kita hanya menggunakan konsep dasar yang sangat logis.

## 1. Mencari Wajah Rata-rata (`rata_rata`)
Langkah pertama adalah mencari tahu seperti apa "wajah manusia pada umumnya". Kita menjumlahkan semua foto lalu membaginya dengan jumlah orang. 
Hasilnya adalah wajah yang sangat umum, tidak mirip siapapun secara spesifik.

## 2. Mencari Keunikan (`A` atau Data Terpusat)
Setelah punya wajah rata-rata, kita kurangi setiap foto dengan wajah rata-rata tersebut.
> **Foto Asli - Wajah Rata-rata = Keunikan Dirimu**

Jika kamu punya hidung lebih mancung dari rata-rata, maka bagian hidung akan memiliki angka positif. Jika lebih pesek, angkanya negatif. Inilah yang kita sebut sebagai **Data Terpusat (A)**.

## 3. Matriks Kovarians (`C`)
Kita ingin tahu: "Jika mata membesar, apakah alis biasanya ikut naik?". Hubungan antar pixel ini disimpan dalam **Matriks Kovarians**.
Dalam kode kita, kita menghitung hubungan antar gambar ($A \times A^T$) karena jumlah gambar biasanya lebih sedikit daripada jumlah pixel, sehingga komputer bekerja lebih cepat.

## 4. Nilai Eigen dan Vektor Eigen
Ini adalah inti dari Aljabar Linear:
- **Vektor Eigen**: Menunjukkan "arah" fitur wajah (misal: arah bentuk rahang).
- **Nilai Eigen**: Menunjukkan seberapa "penting" fitur tersebut. Fitur yang nilai eigen-nya besar berarti fitur itu sangat membedakan satu orang dengan orang lain.
