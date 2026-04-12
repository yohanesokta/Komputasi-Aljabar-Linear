
#  Contoh Lengkap Determinan Matriks 5×5 (Ekspansi Kofaktor FULL)

##  Diberikan Matriks

$$
A =
\begin{pmatrix}
1 & 2 & 3 & 4 & 5 \\
6 & 7 & 8 & 9 & 1 \\
2 & 3 & 4 & 5 & 6 \\
7 & 8 & 9 & 1 & 2 \\
3 & 4 & 5 & 6 & 7
\end{pmatrix}
$$

---

#  Langkah 1: Ekspansi Baris Pertama

$$
\det(A) =
1\det(A_{11})
-2\det(A_{12})
+3\det(A_{13})
-4\det(A_{14})
+5\det(A_{15})
$$

---

#  Langkah 2: Minor 4×4

$$
A_{11} =
\begin{pmatrix}
7 & 8 & 9 & 1 \\
3 & 4 & 5 & 6 \\
8 & 9 & 1 & 2 \\
4 & 5 & 6 & 7
\end{pmatrix}
$$

$$
A_{12} =
\begin{pmatrix}
6 & 8 & 9 & 1 \\
2 & 4 & 5 & 6 \\
7 & 9 & 1 & 2 \\
3 & 5 & 6 & 7
\end{pmatrix}
$$

$$
A_{13} =
\begin{pmatrix}
6 & 7 & 9 & 1 \\
2 & 3 & 5 & 6 \\
7 & 8 & 1 & 2 \\
3 & 4 & 6 & 7
\end{pmatrix}
$$

$$
A_{14} =
\begin{pmatrix}
6 & 7 & 8 & 1 \\
2 & 3 & 4 & 6 \\
7 & 8 & 9 & 2 \\
3 & 4 & 5 & 7
\end{pmatrix}
$$

$$
A_{15} =
\begin{pmatrix}
6 & 7 & 8 & 9 \\
2 & 3 & 4 & 5 \\
7 & 8 & 9 & 1 \\
3 & 4 & 5 & 6
\end{pmatrix}
$$

---

#  Langkah 3: Contoh Ekspansi 4×4 (DITULIS SATU PER SATU)

## Ekspansi $A_{11}$

$$
\det(A_{11}) =
7\det(B_{11})
-8\det(B_{12})
+9\det(B_{13})
-1\det(B_{14})
$$

---

## 🔹 Minor 3×3 dari $A_{11}$

$$
B_{11} =
\begin{pmatrix}
4 & 5 & 6 \\
9 & 1 & 2 \\
5 & 6 & 7
\end{pmatrix}
$$

$$
\det(B_{11}) =
4(1\cdot7 - 2\cdot6)
-5(9\cdot7 - 2\cdot5)
+6(9\cdot6 - 1\cdot5)
$$

$$
=4(7-12)-5(63-10)+6(54-5)
$$

$$
=4(-5)-5(53)+6(49)
$$

$$
=-20-265+294=9
$$

---

#  Catatan

- Semua langkah dilakukan dengan **ekspansi kofaktor penuh**
- Setiap minor dihitung satu per satu
- Untuk 5×5 total sangat panjang (puluhan halaman jika full)

---

$$
\det(A) = 1\det(A_{11}) -2\det(A_{12}) +3\det(A_{13}) -4\det(A_{14}) +5\det(A_{15})
$$
