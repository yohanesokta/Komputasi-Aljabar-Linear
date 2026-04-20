---
title: Evaluasi Invers
date: 2026-04-20
---
## Rumus
```math
\begin{align*}
(\operatorname{adj} A)_{ij} &= (-1)^{i+j} M_{ji}\\
A^{-1} &= \frac{1}{\det A} \operatorname{adj} A.
\end{align*}
```

# Soal 1

```math
A = \begin{bmatrix} -7 & -5 \\ 1 & 4 \end{bmatrix}
```

---
## Determinan A
```math
\begin{align*}
 \det(A) = a.d - b.c\\
 \det(A) = (-7 * 4) - (-5 * 1)\\
 \det(A) = -28 + 5 = -23
 \end{align*}
```
---
## Cari adjoin
```math
\begin{align*}
 \operatorname{adj}(A) = \begin{bmatrix} d & -b \\ -c & a \end{bmatrix}\\
 \operatorname{adj}(A) = \begin{bmatrix} 4 & 5 \\ -1 & -7 \end{bmatrix}
\end{align*}
```

```math
    \begin{align*}
    A^{-1} &= \frac{1}{\det A} \operatorname{adj}\\
    A^{-1} &= \frac{1}{-23} \begin{bmatrix} 4 & 5 \\ -1 & -7 \end{bmatrix}\\
    A^{-1} &= \begin{bmatrix} -4/23 & -5/23 \\ 1/23 & 7/23 \end{bmatrix}\\
    \end{align*}
```

# Soal 2

```math
A = \begin{bmatrix} 0 & 2 & -3 \\ 1 & -2 & -1 \\ 0 & 0 & 1 \end{bmatrix}
```


# Soal 3
```math
A = \begin{bmatrix} 1 & -3 & 1 & 1 \\ -3 & 1 & 1 & 1 \\ 1 & 1 & -3 & 1 \\ 1 & 1 & 1 & -3 \end{bmatrix}.
```