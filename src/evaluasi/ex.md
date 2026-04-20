### Example 2.5.18

Gunakan rumus matriks adjoin untuk menghitung A^{-1}, dimana

```math
A =
\begin{bmatrix}
1 & 2 & 1 \\
-1 & 1 & -1 \\
0 & 2 & 2
\end{bmatrix}
````

---

### Solution

Pertama hitung determinan A dengan mengekspansi sepanjang baris ketiga:

```math
\det A = -2(-1 + 1) + 2(2 + 1) = 6
```

Selanjutnya, hitung adjoin dari A:

```math
\operatorname{adj} A =
\begin{bmatrix}
4 & -2 & -3 \\
2 & 2 & 0 \\
-2 & -2 & 3
\end{bmatrix}
```

Maka kita peroleh:

```math
A^{-1} = \frac{1}{6} \operatorname{adj} A
= \frac{1}{6}
\begin{bmatrix}
4 & -2 & -3 \\
2 & 2 & 0 \\
-2 & -2 & 3
\end{bmatrix}
```

