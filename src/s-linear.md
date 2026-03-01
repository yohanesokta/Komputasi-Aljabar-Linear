
# Sistem Persamaan Linear dan Eliminasi Gaussian

## Teori, Representasi Matriks, dan Metode Penyelesaian

Sistem persamaan linear merupakan salah satu topik fundamental dalam aljabar linear. Pembahasan ini menjadi dasar bagi berbagai konsep lanjutan seperti ruang vektor, kebebasan linear, rank matriks, serta transformasi linear. Persamaan linier adalah sebuah persamaan aljabar, yang tiap sukunya menganndung konstanta, atau perkalian konstanta dengan variabel tunggal. Persamaan ini dapat dikatakan linier dikarenakan hubungan matematis ini dapat digambarkan sebagai garis lurus dalam Sistem Koordinat Kartesius.

Setiap suku pada persamaan linier mengandung konstanta atau perkalian konstanta dengan variabel tunggal. Dalam persamaan liiner akan ada beberapa hal penting, seperti variabel, koefisien, dan juga konstanta.


# 1. Persamaan Linear

## 1.1 Ekspresi Linear

Sebuah ekspresi linear dalam $$n$$ variabel $$x_1, x_2, \dots, x_n$$ adalah ekspresi berbentuk

$$
a_1x_1 + a_2x_2 + \dots + a_nx_n
$$

dengan koefisien $$a_1, a_2, \dots, a_n \in \mathbb{R}$$.

Disebut linear karena:

* Setiap variabel berpangkat satu,
* Tidak ada perkalian antar variabel,
* Tidak ada fungsi nonlinear dari variabel.

---

## 1.2 Persamaan Linear

Persamaan linear adalah persamaan yang dapat dituliskan dalam bentuk baku:

$$
a_1x_1 + a_2x_2 + \dots + a_nx_n = b
$$

Jika $$b = 0$$, maka persamaan disebut **homogen**.
Jika $$b \neq 0$$, maka disebut **nonhomogen**.

Contoh persamaan linear:

$$
4x - 3y + 2z = 5
$$

Contoh persamaan nonlinear:

$$
x^2 + y = 3
$$

Karena terdapat pangkat dua pada variabel.

---

# 2. Sistem Persamaan Linear

Sistem persamaan linear adalah kumpulan beberapa persamaan linear yang harus dipenuhi secara bersamaan.

Secara umum, sistem dengan $$m$$ persamaan dan $$n$$ variabel dapat ditulis sebagai:

$$
\begin{aligned}
a_{11}x_1 + a_{12}x_2 + \dots + a_{1n}x_n &= b_1 \
a_{21}x_1 + a_{22}x_2 + \dots + a_{2n}x_n &= b_2 \
\vdots \
a_{m1}x_1 + a_{m2}x_2 + \dots + a_{mn}x_n &= b_m
\end{aligned}
$$

Indeks pertama menunjukkan baris (persamaan ke-$$i$$), sedangkan indeks kedua menunjukkan kolom (variabel ke-$$j$$).

---

## 2.1 Solusi Sistem Linear

Solusi sistem adalah suatu $$n$$-tuple

$$
(s_1, s_2, \dots, s_n)
$$

yang jika disubstitusikan ke seluruh persamaan menghasilkan pernyataan benar.

Secara umum, sistem linear memiliki tiga kemungkinan:

1. Tidak memiliki solusi (tidak konsisten).
2. Memiliki tepat satu solusi.
3. Memiliki tak hingga banyak solusi.

---

# 3. Representasi Matriks

Sistem linear dapat ditulis lebih ringkas menggunakan matriks.

Jika

$$
A =
\begin{bmatrix}
a_{11} & a_{12} & \dots & a_{1n} \
a_{21} & a_{22} & \dots & a_{2n} \
\vdots & \vdots & \ddots & \vdots \
a_{m1} & a_{m2} & \dots & a_{mn}
\end{bmatrix}
$$

dan

$$
X =
\begin{bmatrix}
x_1 \
x_2 \
\vdots \
x_n
\end{bmatrix},
\quad
b =
\begin{bmatrix}
b_1 \
b_2 \
\vdots \
b_m
\end{bmatrix},
$$

maka sistem dapat dituliskan sebagai

$$
AX = b
$$

Ini disebut representasi matriks dari sistem linear.

---

## 3.1 Matriks Augmentasi

Untuk keperluan eliminasi, kita sering menggunakan **matriks augmentasi**, yaitu matriks yang memuat koefisien dan konstanta sekaligus:

$$
[A \mid b]
$$

Contoh sistem:

$$
\begin{aligned}
x + 2y - z &= 3 \
3x - y + 2z &= 5 \
2x + y + z &= 4
\end{aligned}
$$

Matriks augmentasinya:

$$
\begin{bmatrix}
1 & 2 & -1 & 3 \
3 & -1 & 2 & 5 \
2 & 1 & 1 & 4
\end{bmatrix}
$$

Matriks ini mengandung seluruh informasi sistem.

---

# 4. Operasi Baris Elementer

Untuk menyederhanakan sistem, kita menggunakan tiga operasi baris elementer:

### 1. Perkalian skalar

$$
r_i \rightarrow c r_i, \quad c \neq 0
$$

### 2. Pertukaran baris

$$
r_i \leftrightarrow r_j
$$

### 3. Penjumlahan kelipatan baris

$$
r_i \rightarrow r_i + c r_j
$$

Dua matriks disebut ekuivalen baris jika salah satunya dapat diperoleh dari yang lain melalui urutan hingga operasi tersebut.

---

# 5. Bentuk Eselon Baris

Sesuai definisi formal dalam PDF, matriks berada dalam bentuk eselon baris jika:

1. Semua baris nol berada di bagian bawah.
2. Entri tak nol pertama pada setiap baris tak nol (pivot) berada lebih ke kanan dibanding pivot pada baris di atasnya.
3. Semua elemen di bawah pivot bernilai nol.

Jika tambahan syarat berikut dipenuhi:

* Setiap pivot bernilai 1,
* Setiap kolom pivot hanya memiliki satu entri tak nol,

maka matriks berada dalam bentuk eselon baris tereduksi.

---

# 6. Eliminasi Gaussian

Eliminasi Gaussian adalah algoritma sistematis untuk mengubah matriks augmentasi menjadi bentuk eselon baris.

Langkah-langkah umumnya:

1. Cari kolom tak nol paling kiri.
2. Tukar baris agar entri tak nol berada di posisi atas.
3. Skala agar pivot bernilai 1.
4. Nolkan semua elemen di bawah pivot.
5. Ulangi pada submatriks di bawahnya.

---

## Contoh Eliminasi Gaussian

Gunakan sistem:

$$
\begin{aligned}
x + y + z &= 6 \
2x + 3y + z &= 14 \
x + 2y + 2z &= 10
\end{aligned}
$$

Matriks augmentasi:

$$
\begin{bmatrix}
1 & 1 & 1 & 6 \
2 & 3 & 1 & 14 \
1 & 2 & 2 & 10
\end{bmatrix}
$$

Langkah eliminasi:

$$
r_2 \rightarrow r_2 - 2r_1
$$

$$
r_3 \rightarrow r_3 - r_1
$$

Hasil:

$$
\begin{bmatrix}
1 & 1 & 1 & 6 \
0 & 1 & -1 & 2 \
0 & 1 & 1 & 4
\end{bmatrix}
$$

Kemudian:

$$
r_3 \rightarrow r_3 - r_2
$$

$$
\begin{bmatrix}
1 & 1 & 1 & 6 \
0 & 1 & -1 & 2 \
0 & 0 & 2 & 2
\end{bmatrix}
$$

Skalakan:

$$
r_3 \rightarrow \frac{1}{2} r_3
$$

$$
\begin{bmatrix}
1 & 1 & 1 & 6 \
0 & 1 & -1 & 2 \
0 & 0 & 1 & 1
\end{bmatrix}
$$

Bentuk eselon baris diperoleh.

---

# 7. Eliminasi Gauss–Jordan

Untuk memperoleh bentuk eselon baris tereduksi, kita nolkan elemen di atas pivot.

$$
r_2 \rightarrow r_2 + r_3
$$

$$
r_1 \rightarrow r_1 - r_3
$$

$$
r_1 \rightarrow r_1 - r_2
$$

Hasil akhir:

$$
\begin{bmatrix}
1 & 0 & 0 & 2 \
0 & 1 & 0 & 3 \
0 & 0 & 1 & 1
\end{bmatrix}
$$

Sehingga solusi sistem:

$$
x = 2, \quad y = 3, \quad z = 1
$$

---

# 8. Teorema Penting

Berdasarkan teorema dalam PDF:

1. Setiap matriks ekuivalen baris dengan suatu matriks dalam bentuk eselon baris.
2. Setiap matriks ekuivalen baris dengan suatu matriks dalam bentuk eselon baris tereduksi.
3. Bentuk eselon baris tereduksi bersifat unik.

Bentuk eselon biasa tidak selalu unik.

---

# 9. Struktur Solusi

Jika dalam reduksi muncul baris:

$$
0 = 5
$$

maka sistem tidak konsisten.

Jika terdapat variabel bebas, maka solusi tak hingga dan dapat dinyatakan parametrik.

Contoh:

$$
\begin{aligned}
x + y + z &= 4 \
2x + 2y + 2z &= 8
\end{aligned}
$$

Setelah reduksi:

$$
x + y + z = 4
$$

Misalkan:

$$
y = s, \quad z = t
$$

maka:

$$
x = 4 - s - t
$$

Solusi parametrik:

$$
(x, y, z) = (4 - s - t, s, t)
$$

---

# Penutup

Materi sistem persamaan linear dan eliminasi Gaussian bukan sekadar prosedur komputasi, tetapi merupakan fondasi struktural dalam aljabar linear. Dengan memahami bagaimana sistem direpresentasikan dalam matriks dan bagaimana operasi baris bekerja, kita memperoleh alat yang sangat kuat untuk menganalisis konsistensi, jumlah solusi, serta struktur ruang solusi.

Jika diperlukan, saya dapat menambahkan bagian pembuktian formal teorema atau memperluas pembahasan menuju konsep rank dan ruang solusi sebagai subruang vektor.
