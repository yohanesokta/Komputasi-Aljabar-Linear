# Rumus Determinan (Ekspansi Kofaktor)



## Definisi Minor

$$
M_{ij} = \det(A_{ij})
$$

```math
A_{ij} = \text{matriks yang diperoleh dari } A \text{ dengan menghapus baris ke-} i \text{ dan kolom ke-} j
```

---

##  Ekspansi Baris ke-i

```math
\det(A) = \sum_{j=1}^{n} (-1)^{i+j} \, a_{ij} \, \det(A_{ij})
```

---

## Ekspansi Kolom ke-j

```math
\det(A) = \sum_{i=1}^{n} (-1)^{i+j} \, a_{ij} \, \det(A_{ij})
```

---

# Matriks Tanda (Cofactor Sign Matrix)

```math
\begin{pmatrix}
+ & - & + & - & + \\
- & + & - & + & - \\
+ & - & + & - & + \\
- & + & - & + & - \\
+ & - & + & - & +
\end{pmatrix}
```

---

# Kofaktor

```math
C_{ij} = (-1)^{i+j} \det(A_{ij})
```

---

# Adjoint Matriks

```math
\text{adj}(A) = (C_{ij})^T
```

---

# Hubungan Penting

```math
A \cdot \text{adj}(A) = \text{adj}(A) \cdot A = (\det A) I
```

---

# Invers Matriks

Jika:

```math
\det(A) \neq 0
```

maka:

```math
A^{-1} = \frac{1}{\det(A)} \text{adj}(A)
```

---

# Kasus Khusus 2×2 (Dasar)

```math
A =
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
```

```math
\det(A) = ad - bc
```

```math
\text{adj}(A) =
\begin{pmatrix}
d & -b \\
-c & a
\end{pmatrix}
```

