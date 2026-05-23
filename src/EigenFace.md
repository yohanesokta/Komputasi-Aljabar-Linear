---
title: Pengenalan Wajah dengan Metode Eigenface (SVD)
date: 2026-05-23
---

# Pengenalan Wajah dengan Metode Eigenface

Eigenface adalah salah satu metode pengenalan wajah yang paling awal dan populer, yang memanfaatkan teknik **Principal Component Analysis (PCA)** untuk mengurangi dimensi data citra wajah. Dalam proyek ini, PCA diimplementasikan menggunakan **Singular Value Decomposition (SVD)**.

## Langkah-langkah Perhitungan Eigenface

Proses perhitungan Eigenface dalam kode ini mengikuti alur matematis sebagai berikut:

### 1. Representasi Citra sebagai Vektor
Setiap citra wajah berukuran $W \times H$ diubah menjadi vektor baris tunggal dengan panjang $N = W \times H$. Jika kita memiliki $M$ citra latih, maka kita akan memiliki matriks data $D$ berukuran $M \times N$.

Dalam kode (`app.cpp`):
```cpp
Mat flat = item.image.reshape(1, 1);
flat.convertTo(flat, CV_32F);
data.push_back(flat);
```

### 2. Menghitung Rata-rata Wajah (Mean Face)
Langkah pertama adalah menghitung rata-rata dari seluruh vektor wajah dalam dataset.
$$\Psi = \frac{1}{M} \sum_{i=1}^{M} \Gamma_i$$
Dimana $\Gamma_i$ adalah vektor wajah ke-$i$.

Dalam kode (`eigenface.cpp`):
```cpp
reduce(data, mean, 0, REDUCE_AVG);
```

### 3. Normalisasi Data (Mean Centering)
Setiap vektor wajah dikurangi dengan rata-rata wajah untuk mendapatkan data yang terpusat.
$$\Phi_i = \Gamma_i - \Psi$$
Hasilnya disimpan dalam matriks $A$ (centered data).

Dalam kode (`eigenface.cpp`):
```cpp
Mat centered;
for (int i = 0; i < data.rows; i++) {
    centered.push_back(data.row(i) - mean);
}
```

### 4. Menghitung Komponen Utama dengan SVD
SVD digunakan untuk memfaktorkan matriks data $A$ yang telah dinormalisasi:
$$A = U \Sigma V^T$$
- $U$: Matriks eigenvector dari $AA^T$ (mewakili hubungan antar gambar).
- $\Sigma$: Matriks diagonal nilai singular.
- $V^T$: Matriks yang berisi **eigenvectors** dari $A^TA$ (mewakili fitur-fitur wajah utama atau "Eigenfaces").

Kita mengambil $k$ baris pertama dari $V^T$ sebagai basis ruang wajah (face space).

Dalam kode (`eigenface.cpp`):
```cpp
SVD svd(centered, SVD::MODIFY_A | SVD::FULL_UV);
eigenvectors = svd.vt(Range(0, components), Range::all());
```

### 5. Proyeksi ke Ruang Wajah (Face Space)
Setiap gambar (baik data latih maupun data uji) diproyeksikan ke dalam ruang wajah yang telah dibentuk oleh eigenvectors.
$$\Omega = \Phi \times V^T$$
Hasil proyeksi ini adalah vektor dengan dimensi rendah ($k$ komponen) yang mewakili fitur unik wajah tersebut.

Dalam kode (`eigenface.cpp`):
```cpp
Mat centered = sample - mean;
return centered * eigenvectors.t();
```

### 6. Proses Pengenalan (Recognition)
Untuk mengenali wajah baru (sampel):
1.  Proyeksikan sampel tersebut ke ruang wajah untuk mendapatkan vektor $\Omega_{test}$.
2.  Hitung jarak Euclidean (L2 Norm) antara $\Omega_{test}$ dengan seluruh proyeksi data latih ($\Omega_i$).
3.  Label dari data latih dengan jarak terkecil dianggap sebagai hasil prediksi.

Dalam kode (`eigenface.cpp`):
```cpp
double dist = norm(query, projections[i], NORM_L2);
if (dist < minDist) {
    minDist = dist;
    bestLabel = labels[i];
}
```

## Implementasi dalam Proyek

Proyek ini mengimplementasikan langkah-langkah di atas secara real-time:
1.  **Pelatihan**: Dataset dibaca dari `dataset/uang`, diproses (grayscale, histogram equalization, resize), lalu dilatih menggunakan kelas `EigenFace`.
2.  **Prediksi**: Kamera menangkap frame, mendeteksi area wajah, melakukan praproses yang sama, lalu memanggil fungsi `predict()` untuk mendapatkan identitas wajah tersebut.

### Struktur Kelas Utama
- `train()`: Melakukan Mean Centering dan SVD untuk mendapatkan `eigenvectors`.
- `project()`: Memetakan citra ke ruang dimensi rendah.
- `predict()`: Mencari tetangga terdekat (Nearest Neighbor) di ruang wajah.
