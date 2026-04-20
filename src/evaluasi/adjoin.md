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

---

hitung determinan A dengan mengekspansi sepanjang baris ketiga:

```math
\begin{align*}
\det A &= 0 \begin{vmatrix} 2 & -3 \\ -2 & -1 \end{vmatrix} - 0 \begin{vmatrix} 0 & -3 \\ 1 & -1 \end{vmatrix} + 1 \begin{vmatrix} 0 & 2 \\ 1 & -2 \end{vmatrix} \\
&= 1((0)(-2) - (1)(2)) \\
&= 1(0 - 2) = -2
\end{align*}
```

hitung adjoin dari A menggunakan rumus $(\operatorname{adj} A)_{ij} = (-1)^{i+j} M_{ji}$:

```math
\begin{align*}
\operatorname{adj} A &= \begin{bmatrix}
+M_{11} & -M_{21} & +M_{31} \\
-M_{12} & +M_{22} & -M_{32} \\
+M_{13} & -M_{23} & +M_{33}
\end{bmatrix} \\
&= \begin{bmatrix}
+\begin{vmatrix} -2 & -1 \\ 0 & 1 \end{vmatrix} & -\begin{vmatrix} 2 & -3 \\ 0 & 1 \end{vmatrix} & +\begin{vmatrix} 2 & -3 \\ -2 & -1 \end{vmatrix} \\[10pt]
-\begin{vmatrix} 1 & -1 \\ 0 & 1 \end{vmatrix} & +\begin{vmatrix} 0 & -3 \\ 0 & 1 \end{vmatrix} & -\begin{vmatrix} 0 & -3 \\ 1 & -1 \end{vmatrix} \\[10pt]
+\begin{vmatrix} 1 & -2 \\ 0 & 0 \end{vmatrix} & -\begin{vmatrix} 0 & 2 \\ 0 & 0 \end{vmatrix} & +\begin{vmatrix} 0 & 2 \\ 1 & -2 \end{vmatrix}
\end{bmatrix} \\
&= \begin{bmatrix}
+((-2)(1) - (-1)(0)) & -((2)(1) - (-3)(0)) & +((2)(-1) - (-3)(-2)) \\
-((1)(1) - (-1)(0)) & +((0)(1) - (-3)(0)) & -((0)(-1) - (-3)(1)) \\
+((1)(0) - (-2)(0)) & -((0)(0) - (2)(0)) & +((0)(-2) - (2)(1))
\end{bmatrix} \\
&= \begin{bmatrix}
+(-2 - 0) & -(2 - 0) & +(-2 - 6) \\
-(1 - 0) & +(0 - 0) & -(0 - (-3)) \\
+(0 - 0) & -(0 - 0) & +(0 - 2)
\end{bmatrix}
= \begin{bmatrix}
-2 & -2 & -8 \\
-1 & 0 & -3 \\
0 & 0 & -2
\end{bmatrix}
\end{align*}
```

Sehingga invers matriksnya adalah:

```math
A^{-1} = \frac{1}{-2} \operatorname{adj} A
= \frac{1}{-2}
\begin{bmatrix}
-2 & -2 & -8 \\
-1 & 0 & -3 \\
0 & 0 & -2
\end{bmatrix}
```

# Soal 3

```math
A = \begin{bmatrix} 1 & -3 & 1 & 1 \\ -3 & 1 & 1 & 1 \\ 1 & 1 & -3 & 1 \\ 1 & 1 & 1 & -3 \end{bmatrix}
```

---


 hitung determinan A dengan mengekspansi sepanjang baris pertama:

```math
\begin{align*}
\det A &= 1 \begin{vmatrix} 1 & 1 & 1 \\ 1 & -3 & 1 \\ 1 & 1 & -3 \end{vmatrix} - (-3) \begin{vmatrix} -3 & 1 & 1 \\ 1 & -3 & 1 \\ 1 & 1 & -3 \end{vmatrix} + 1 \begin{vmatrix} -3 & 1 & 1 \\ 1 & 1 & 1 \\ 1 & 1 & -3 \end{vmatrix} - 1 \begin{vmatrix} -3 & 1 & 1 \\ 1 & 1 & -3 \\ 1 & 1 & 1 \end{vmatrix} \\
&= 1( 1(-3 \cdot -3 - 1 \cdot 1) - 1(1 \cdot -3 - 1 \cdot 1) + 1(1 \cdot 1 - -3 \cdot 1) ) \\
&\quad + 3( -3(-3 \cdot -3 - 1 \cdot 1) - 1(1 \cdot -3 - 1 \cdot 1) + 1(1 \cdot 1 - -3 \cdot 1) ) \\
&\quad + 1( -3(1 \cdot -3 - 1 \cdot 1) - 1(1 \cdot -3 - 1 \cdot 1) + 1(1 \cdot 1 - 1 \cdot 1) ) \\
&\quad - 1( -3(1 \cdot 1 - -3 \cdot 1) - 1(1 \cdot 1 - -3 \cdot 1) + 1(1 \cdot 1 - 1 \cdot 1) ) \\
&= 1( 1(8) - 1(-4) + 1(4) ) + 3( -3(8) - 1(-4) + 1(4) ) \\
&\quad + 1( -3(-4) - 1(-4) + 1(0) ) - 1( -3(4) - 1(4) + 1(0) ) \\
&= 1(8 + 4 + 4) + 3(-24 + 4 + 4) + 1(12 + 4 + 0) - 1(-12 - 4 + 0) \\
&= 1(16) + 3(-16) + 1(16) - 1(-16) \\
&= 16 - 48 + 16 + 16 = 0
\end{align*}
```

hitung adjoin dari A menggunakan rumus $(\operatorname{adj} A)_{ij} = (-1)^{i+j} M_{ji}$:

```math
\begin{align*}
\operatorname{adj} A &= \begin{bmatrix}
+M_{11} & -M_{21} & +M_{31} & -M_{41} \\
-M_{12} & +M_{22} & -M_{32} & +M_{42} \\
+M_{13} & -M_{23} & +M_{33} & -M_{43} \\
-M_{14} & +M_{24} & -M_{34} & +M_{44}
\end{bmatrix} \\[10pt]
&= \begin{bmatrix}
+\begin{vmatrix} 1 & 1 & 1 \\ 1 & -3 & 1 \\ 1 & 1 & -3 \end{vmatrix} & -\begin{vmatrix} -3 & 1 & 1 \\ 1 & -3 & 1 \\ 1 & 1 & -3 \end{vmatrix} & +\begin{vmatrix} -3 & 1 & 1 \\ 1 & 1 & 1 \\ 1 & 1 & -3 \end{vmatrix} & -\begin{vmatrix} -3 & 1 & 1 \\ 1 & 1 & -3 \\ 1 & 1 & 1 \end{vmatrix} \\[15pt]
-\begin{vmatrix} -3 & 1 & 1 \\ 1 & -3 & 1 \\ 1 & 1 & -3 \end{vmatrix} & +\begin{vmatrix} 1 & 1 & 1 \\ 1 & -3 & 1 \\ 1 & 1 & -3 \end{vmatrix} & -\begin{vmatrix} 1 & -3 & 1 \\ 1 & 1 & 1 \\ 1 & 1 & -3 \end{vmatrix} & +\begin{vmatrix} 1 & -3 & 1 \\ 1 & 1 & -3 \\ 1 & 1 & 1 \end{vmatrix} \\[15pt]
+\begin{vmatrix} -3 & 1 & 1 \\ 1 & 1 & 1 \\ 1 & 1 & -3 \end{vmatrix} & -\begin{vmatrix} 1 & 1 & 1 \\ -3 & 1 & 1 \\ 1 & 1 & -3 \end{vmatrix} & +\begin{vmatrix} 1 & -3 & 1 \\ -3 & 1 & 1 \\ 1 & 1 & -3 \end{vmatrix} & -\begin{vmatrix} 1 & -3 & 1 \\ -3 & 1 & 1 \\ 1 & 1 & 1 \end{vmatrix} \\[15pt]
-\begin{vmatrix} -3 & 1 & 1 \\ 1 & 1 & -3 \\ 1 & 1 & 1 \end{vmatrix} & +\begin{vmatrix} 1 & 1 & 1 \\ -3 & 1 & 1 \\ 1 & 1 & -3 \end{vmatrix} & -\begin{vmatrix} 1 & -3 & 1 \\ -3 & 1 & 1 \\ 1 & 1 & 1 \end{vmatrix} & +\begin{vmatrix} 1 & -3 & 1 \\ -3 & 1 & 1 \\ 1 & 1 & -3 \end{vmatrix}
\end{bmatrix} \\[10pt]
&= \begin{bmatrix}
+( 1((-3)(-3) - (1)(1)) - 1((1)(-3) - (1)(1)) + 1((1)(1) - (-3)(1)) ) & -( -3((-3)(-3) - (1)(1)) - 1((1)(-3) - (1)(1)) + 1((1)(1) - (-3)(1)) ) & +( -3((1)(-3) - (1)(1)) - 1((1)(-3) - (1)(1)) + 1((1)(1) - (1)(1)) ) & -( -3((1)(1) - (-3)(1)) - 1((1)(1) - (-3)(1)) + 1((1)(1) - (1)(1)) ) \\[15pt]
-( -3((-3)(-3) - (1)(1)) - 1((1)(-3) - (1)(1)) + 1((1)(1) - (-3)(1)) ) & +( 1((-3)(-3) - (1)(1)) - 1((1)(-3) - (1)(1)) + 1((1)(1) - (-3)(1)) ) & -( 1((1)(-3) - (1)(1)) - (-3)((1)(-3) - (1)(1)) + 1((1)(1) - (1)(1)) ) & +( 1((1)(1) - (-3)(1)) - (-3)((1)(1) - (-3)(1)) + 1((1)(1) - (1)(1)) ) \\[15pt]
+( -3((1)(-3) - (1)(1)) - 1((1)(-3) - (1)(1)) + 1((1)(1) - (1)(1)) ) & -( 1((1)(-3) - (1)(1)) - 1((-3)(-3) - (1)(1)) + 1((-3)(1) - (1)(1)) ) & +( 1((1)(-3) - (1)(1)) - (-3)((-3)(-3) - (1)(1)) + 1((-3)(1) - (1)(1)) ) & -( 1((1)(1) - (1)(1)) - (-3)((-3)(1) - (1)(1)) + 1((-3)(1) - (1)(1)) ) \\[15pt]
-( -3((1)(1) - (-3)(1)) - 1((1)(1) - (-3)(1)) + 1((1)(1) - (1)(1)) ) & +( 1((1)(-3) - (1)(1)) - 1((-3)(-3) - (1)(1)) + 1((-3)(1) - (1)(1)) ) & -( 1((1)(1) - (1)(1)) - (-3)((-3)(1) - (1)(1)) + 1((-3)(1) - (1)(1)) ) & +( 1((1)(-3) - (1)(1)) - (-3)((-3)(-3) - (1)(1)) + 1((-3)(1) - (1)(1)) )
\end{bmatrix} \\[10pt]
&= \begin{bmatrix}
+( 1(8) - 1(-4) + 1(4) ) & -( -3(8) - 1(-4) + 1(4) ) & +( -3(-4) - 1(-4) + 1(0) ) & -( -3(4) - 1(4) + 1(0) ) \\[10pt]
-( -3(8) - 1(-4) + 1(4) ) & +( 1(8) - 1(-4) + 1(4) ) & -( 1(-4) - (-3)(-4) + 1(0) ) & +( 1(4) - (-3)(4) + 1(0) ) \\[10pt]
+( -3(-4) - 1(-4) + 1(0) ) & -( 1(-4) - 1(8) + 1(-4) ) & +( 1(-4) - (-3)(8) + 1(-4) ) & -( 1(0) - (-3)(-4) + 1(-4) ) \\[10pt]
-( -3(4) - 1(4) + 1(0) ) & +( 1(-4) - 1(8) + 1(-4) ) & -( 1(0) - (-3)(-4) + 1(-4) ) & +( 1(-4) - (-3)(8) + 1(-4) )
\end{bmatrix} \\[10pt]
&= \begin{bmatrix}
+(16) & -(-16) & +(16) & -(-16) \\
-(-16) & +(16) & -(-16) & +(16) \\
+(16) & -(-16) & +(16) & -(-16) \\
-(-16) & +(16) & -(-16) & +(16)
\end{bmatrix} 
= \begin{bmatrix}
16 & 16 & 16 & 16 \\
16 & 16 & 16 & 16 \\
16 & 16 & 16 & 16 \\
16 & 16 & 16 & 16
\end{bmatrix}
\end{align*}
```

Sehingga invers matriksnya dirumuskan dengan:

```math
A^{-1} = \frac{1}{\det{A}} \operatorname{adj} A
= \frac{1}{0}
\begin{bmatrix}
16 & 16 & 16 & 16 \\
16 & 16 & 16 & 16 \\
16 & 16 & 16 & 16 \\
16 & 16 & 16 & 16
\end{bmatrix}
```

Karena $\det(A) = 0$, maka operasi invers ini bernilai tak terdefinisi 

matriks A adalah singular atau tidak memiliki invers