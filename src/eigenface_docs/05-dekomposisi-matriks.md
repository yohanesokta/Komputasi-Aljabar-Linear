# Apa itu Dekomposisi Matriks?

Jika kamu melihat angka $12$, kamu tahu itu berasal dari $3 \times 4$. Dalam matriks, kita melakukan hal yang sama tetapi lebih kompleks.

## Rumus SVD ($A = U \Sigma V^T$)
Dekomposisi Nilai Singular (SVD) memecah matriks data kita ($A$) menjadi tiga bagian:

1. **Matriks $U$ (Left Singular Vectors)**:
   Mewakili hubungan antar **Gambar**. Di sini kita tahu apakah Gambar 1 mirip dengan Gambar 2.
2. **Matriks $\Sigma$ atau $S$ (Singular Values)**:
   Berisi angka-angka di garis diagonal. Semakin besar angkanya, semakin penting fitur tersebut.
3. **Matriks $V^T$ (Right Singular Vectors)**:
   Inilah **Eigenfaces** kita. Ia mewakili hubungan antar **Pixel**. Isinya adalah pola-pola wajah (mata, hidung, mulut).

## Dimana Letaknya di Kode Kita?
Karena kita menghitung secara manual, dekomposisi ini terbagi di dua tempat dalam file `src/eigenface.cpp`:

- **Mendapatkan $U$ dan $\Sigma$**:
  Ada di fungsi `hitung_eigen_manual(C, nilai_eigen, U)`. Di sini kita memecah matriks kovarians $C$.
- **Mendapatkan $V^T$**:
  Ada di bagian loop:
  ```cpp
  Mat v_i = (A.t() * U.col(i)) / S;
  ```
  Rumus ini memindahkan informasi dari "hubungan antar gambar" ($U$) menjadi "fitur wajah" ($V$).

## Kenapa Harus Didekomposisi?
Tanpa dekomposisi, komputer akan kewalahan memproses ribuan pixel sekaligus. Dengan dekomposisi, kita hanya mengambil 20-100 fitur yang paling penting saja. Ini membuat program bisa berjalan sangat cepat di kamera laptopmu!
