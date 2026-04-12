
# Adjoint dan Invers Matriks 5x5 (Metode Kofaktor)


```math
(\mathrm{adj}\,A)_{ij} = (-1)^{i+j} M_{ji}
```

Jika ingin ditulis dengan penjelasan minor:

```math
M_{ji} = \det(A_{ji})
```

Sehingga bisa juga ditulis:

```math
(\mathrm{adj}\,A)_{ij} = (-1)^{i+j} \det(A_{ji})
```

Ini adalah rumus elemen ke-((i,j)) dari adjoint matriks.


## Diberikan Matriks

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

# 1. Kofaktor

Rumus kofaktor:

$$
C_{ij} = (-1)^{i+j} \det(A_{ij})
$$

Contoh:

## C11

Coret baris 1 kolom 1:

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
C_{11} = (+1)\det(A_{11})
$$

---

## C12

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
C_{12} = (-1)\det(A_{12})
$$

---

Proses ini dilakukan untuk semua elemen sampai C55.

---

# 2. Matriks Kofaktor

$$
C =
\begin{pmatrix}
C_{11} & C_{12} & C_{13} & C_{14} & C_{15} \\
C_{21} & C_{22} & C_{23} & C_{24} & C_{25} \\
C_{31} & C_{32} & C_{33} & C_{34} & C_{35} \\
C_{41} & C_{42} & C_{43} & C_{44} & C_{45} \\
C_{51} & C_{52} & C_{53} & C_{54} & C_{55}
\end{pmatrix}
$$

---

# 3. Adjoint

Transpose matriks kofaktor:

$$
\text{adj}(A) =
\begin{pmatrix}
C_{11} & C_{21} & C_{31} & C_{41} & C_{51} \\
C_{12} & C_{22} & C_{32} & C_{42} & C_{52} \\
C_{13} & C_{23} & C_{33} & C_{43} & C_{53} \\
C_{14} & C_{24} & C_{34} & C_{44} & C_{54} \\
C_{15} & C_{25} & C_{35} & C_{45} & C_{55}
\end{pmatrix}
$$

---

# 4. Invers Matriks

Jika determinan tidak nol:

$$
A^{-1} = \frac{1}{\det(A)} \text{adj}(A)
$$

---

# 5. Bentuk Akhir

$$
A^{-1} =
\frac{1}{\det(A)}
\begin{pmatrix}
C_{11} & C_{21} & C_{31} & C_{41} & C_{51} \\
C_{12} & C_{22} & C_{32} & C_{42} & C_{52} \\
C_{13} & C_{23} & C_{33} & C_{43} & C_{53} \\
C_{14} & C_{24} & C_{34} & C_{44} & C_{54} \\
C_{15} & C_{25} & C_{35} & C_{45} & C_{55}
\end{pmatrix}
$$
