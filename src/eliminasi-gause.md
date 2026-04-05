---
title: Eliminasi Gauss 
date: 2026-03-08
---
# Eliminasi Gauss 

## Pengertian

Eliminasi Gauss adalah metode dalam **aljabar linier** yang digunakan
untuk menyelesaikan sistem persamaan linier. Metode ini bekerja dengan
cara mengubah kumpulan persamaan menjadi **bentuk matriks**, lalu
menyederhanakannya menggunakan **operasi baris elementer** sampai
matriks menjadi lebih mudah dianalisis.

Jika jumlah variabel hanya dua, biasanya kita bisa menggunakan metode
grafik atau substitusi. Namun ketika jumlah variabel semakin banyak
seperti **3, 4, atau 5 variabel**, perhitungan menjadi lebih rumit. Di
sinilah eliminasi Gauss sangat membantu karena langkahnya sistematis dan
terstruktur.

Secara umum proses eliminasi Gauss dilakukan melalui beberapa tahap
berikut.

------------------------------------------------------------------------

## Langkah--Langkah Metode Eliminasi Gauss

### 1. Menuliskan Sistem Persamaan

Langkah pertama adalah menuliskan sistem persamaan linier yang akan
diselesaikan.

Contoh bentuk umum:

$$
\begin{aligned}
a_{11}x_1 + a_{12}x_2 + a_{13}x_3 + a_{14}x_4 + a_{15}x_5 &= b_1 \\
a_{21}x_1 + a_{22}x_2 + a_{23}x_3 + a_{24}x_4 + a_{25}x_5 &= b_2 \\
a_{31}x_1 + a_{32}x_2 + a_{33}x_3 + a_{34}x_4 + a_{35}x_5 &= b_3 \\
a_{41}x_1 + a_{42}x_2 + a_{43}x_3 + a_{44}x_4 + a_{45}x_5 &= b_4 \\
a_{51}x_1 + a_{52}x_2 + a_{53}x_3 + a_{54}x_4 + a_{55}x_5 &= b_5
\end{aligned}
$$

Persamaan ini terdiri dari: - beberapa **variabel**
($x_1, x_2, x_3, ...$) - **koefisien** ($a_{ij}$) - dan **konstanta**
($b_i$)

------------------------------------------------------------------------

### 2. Mengubah Persamaan Menjadi Matriks Augmentasi

Setelah persamaan ditulis, langkah berikutnya adalah mengubahnya menjadi
**matriks augmentasi**.

Matriks augmentasi adalah matriks yang berisi: - koefisien variabel -
serta konstanta di kolom terakhir.

Contoh bentuknya:

$$
\begin{bmatrix}
a_{11} & a_{12} & a_{13} & a_{14} & a_{15} & b_1 \\
a_{21} & a_{22} & a_{23} & a_{24} & a_{25} & b_2 \\
a_{31} & a_{32} & a_{33} & a_{34} & a_{35} & b_3 \\
a_{41} & a_{42} & a_{43} & a_{44} & a_{45} & b_4 \\
a_{51} & a_{52} & a_{53} & a_{54} & a_{55} & b_5
\end{bmatrix}
$$

Dengan bentuk matriks ini, perhitungan menjadi lebih mudah dilakukan.

------------------------------------------------------------------------

### 3. Melakukan Operasi Baris Elementer

Untuk menyederhanakan matriks, kita menggunakan **operasi baris
elementer**.

Terdapat tiga jenis operasi yang dapat dilakukan.

**a. Menukar dua baris**

$$
R_i \leftrightarrow R_j
$$

Digunakan jika kita ingin menukar posisi baris agar pivot lebih mudah
digunakan.

**b. Mengalikan baris dengan konstanta bukan nol**

$$
R_i \rightarrow kR_i
$$

Digunakan untuk mengubah nilai pada baris.

**c. Menambahkan kelipatan baris lain ke suatu baris**

$$
R_i \rightarrow R_i + kR_j
$$

Digunakan untuk menghilangkan elemen tertentu pada kolom.

Operasi-operasi ini **tidak mengubah solusi** dari sistem persamaan.

------------------------------------------------------------------------

### 4. Membentuk Matriks Eselon Baris

Tujuan dari eliminasi Gauss adalah mengubah matriks menjadi **bentuk
eselon baris**.

Ciri-ciri matriks eselon baris:

1.  Elemen utama (pivot) pada setiap baris berada lebih ke kanan dari
    baris sebelumnya.
2.  Semua elemen di bawah pivot bernilai **nol**.
3.  Jika terdapat baris nol, maka baris tersebut berada di bagian bawah.

Contoh bentuk sederhana:

$$
\begin{bmatrix}
1 & * & * & * \\
0 & 1 & * & * \\
0 & 0 & 1 & *
\end{bmatrix}
$$

Simbol $*$ menunjukkan nilai bebas.

------------------------------------------------------------------------

### 5. Menentukan Solusi dengan Substitusi Balik

Setelah matriks berada pada bentuk eselon baris, kita dapat mencari
solusi dengan **substitusi balik**.

Artinya: - kita mulai dari baris paling bawah - lalu menghitung variabel
satu per satu sampai ke atas.

Metode ini mempermudah penyelesaian sistem persamaan dengan banyak
variabel.

------------------------------------------------------------------------

# Contoh Sistem Persamaan (5 Variabel)

Misalkan diberikan sistem berikut:

$$
\begin{aligned}
x_1 + 2x_2 + x_3 + x_4 + x_5 &= 10 \\
2x_1 + 3x_2 + 2x_3 + x_4 + x_5 &= 15 \\
3x_1 + 5x_2 + 3x_3 + 2x_4 + x_5 &= 22 \\
x_1 + x_2 + 2x_3 + 2x_4 + x_5 &= 12 \\
4x_1 + 6x_2 + 4x_3 + 3x_4 + 2x_5 &= 30
\end{aligned}
$$

------------------------------------------------------------------------

# Matriks Augmentasi

$$
\begin{bmatrix}
1 & 2 & 1 & 1 & 1 & 10 \\
2 & 3 & 2 & 1 & 1 & 15 \\
3 & 5 & 3 & 2 & 1 & 22 \\
1 & 1 & 2 & 2 & 1 & 12 \\
4 & 6 & 4 & 3 & 2 & 30
\end{bmatrix}
$$

------------------------------------------------------------------------

# Eliminasi Kolom Pertama

Gunakan baris pertama sebagai pivot.

$$
\begin{aligned}
R_2 &= R_2 - 2R_1 \\
R_3 &= R_3 - 3R_1 \\
R_4 &= R_4 - R_1 \\
R_5 &= R_5 - 4R_1
\end{aligned}
$$

Hasil:

$$
\begin{bmatrix}
1 & 2 & 1 & 1 & 1 & 10 \\
0 & -1 & 0 & -1 & -1 & -5 \\
0 & -1 & 0 & -1 & -2 & -8 \\
0 & -1 & 1 & 1 & 0 & 2 \\
0 & -2 & 0 & -1 & -2 & -10
\end{bmatrix}
$$

------------------------------------------------------------------------

# Eliminasi Kolom Kedua

Gunakan baris kedua sebagai pivot.

$$
\begin{aligned}
R_3 &= R_3 - R_2 \\
R_4 &= R_4 - R_2 \\
R_5 &= R_5 - 2R_2
\end{aligned}
$$

Hasil matriks:

$$
\begin{bmatrix}
1 & 2 & 1 & 1 & 1 & 10 \\
0 & -1 & 0 & -1 & -1 & -5 \\
0 & 0 & 0 & 0 & -1 & -3 \\
0 & 0 & 1 & 2 & 1 & 7 \\
0 & 0 & 0 & 1 & 0 & 0
\end{bmatrix}
$$

------------------------------------------------------------------------

# Menyusun Matriks Eselon Baris

Agar sesuai dengan bentuk eselon baris, kita tukar baris ke-3 dan ke-4:

$$
\begin{bmatrix}
1 & 2 & 1 & 1 & 1 & 10 \\
0 & -1 & 0 & -1 & -1 & -5 \\
0 & 0 & 1 & 2 & 1 & 7 \\
0 & 0 & 0 & 1 & 0 & 0 \\
0 & 0 & 0 & 0 & -1 & -3
\end{bmatrix}
$$

------------------------------------------------------------------------

# Substitusi Balik

Kita mulai dari baris paling bawah.

### Baris ke-5
$$
- x_5 = -3
$$
$$
x_5 = 3
$$

### Baris ke-4
$$
x_4 = 0
$$

### Baris ke-3
$$
x_3 + 2x_4 + x_5 = 7
$$
$$
x_3 + 0 + 3 = 7
$$
$$
x_3 = 4
$$

### Baris ke-2
$$
- x_2 - x_4 - x_5 = -5
$$
$$
- x_2 - 3 = -5
$$
$$
x_2 = 2
$$

### Baris ke-1
$$
x_1 + 2x_2 + x_3 + x_4 + x_5 = 10
$$
$$
x_1 + 4 + 4 + 0 + 3 = 10
$$
$$
x_1 = -1
$$

------------------------------------------------------------------------

# Hasil Akhir

$$
\begin{aligned}
x_1 &= -1 \\
x_2 &= 2 \\
x_3 &= 4 \\
x_4 &= 0 \\
x_5 &= 3
\end{aligned}
$$

------------------------------------------------------------------------

# Kesimpulan

Metode eliminasi Gauss adalah cara sistematis untuk menyelesaikan sistem
persamaan linier dengan mengubahnya ke dalam bentuk matriks dan
melakukan operasi baris elementer.

Dengan metode ini, persamaan yang kompleks dengan banyak variabel dapat
disederhanakan hingga mudah untuk menemukan solusinya.