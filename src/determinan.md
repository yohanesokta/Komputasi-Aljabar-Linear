
# Perhitungan Determinan 3x3


$$
A =
\begin{pmatrix}
2 & 3 & 1 \\
4 & 1 & 5 \\
7 & 2 & 6
\end{pmatrix}
$$

---

## Langkah 1: Gunakan Rumus Ekspansi Baris Pertama

$$
\det(A) = a_{11}\det(A_{11}) - a_{12}\det(A_{12}) + a_{13}\det(A_{13})
$$

$$
\det(A) = 2\det(A_{11}) - 3\det(A_{12}) + 1\det(A_{13})
$$

---

## Langkah 2: Tentukan Minor

### Minor $A_{11}$ (coret baris 1 kolom 1)

$$
A_{11} =
\begin{pmatrix}
1 & 5 \\
2 & 6
\end{pmatrix}
$$

### Minor $A_{12}$ (coret baris 1 kolom 2)

$$
A_{12} =
\begin{pmatrix}
4 & 5 \\
7 & 6
\end{pmatrix}
$$

### Minor $A_{13}$ (coret baris 1 kolom 3)

$$
A_{13} =
\begin{pmatrix}
4 & 1 \\
7 & 2
\end{pmatrix}
$$

---

## Langkah 3: Hitung Determinan 2x2 (SATU PER SATU)

### 1. $\det(A_{11})$

$$
\det(A_{11}) = (1 \cdot 6) - (5 \cdot 2)
$$

$$
= 6 - 10
$$

$$
= -4
$$

---

### 2. $\det(A_{12})$

$$
\det(A_{12}) = (4 \cdot 6) - (5 \cdot 7)
$$

$$
= 24 - 35
$$

$$
= -11
$$

---

### 3. $\det(A_{13})$

$$
\det(A_{13}) = (4 \cdot 2) - (1 \cdot 7)
$$

$$
= 8 - 7
$$

$$
= 1
$$

---

## Langkah 4: Substitusi ke Rumus

$$
\det(A) = 2(-4) - 3(-11) + 1(1)
$$

$$
= -8 + 33 + 1
$$

$$
= 26
$$

---

## Hasil Akhir

$$
\det(A) = 26
$$

---

## Catatan Penting

- Semua langkah dilakukan **tanpa cara singkat**
- Menggunakan **ekspansi kofaktor sesuai teori**
- Setiap minor dihitung satu per satu
