# Dasar OpenCV untuk Pemula

Sebelum masuk ke rumus, kita harus tahu bagaimana komputer "melihat" gambar menggunakan library bernama **OpenCV**.

## 1. Gambar adalah Matriks (Grid Angka)
Bagi komputer, gambar bukanlah warna-warni indah, melainkan kumpulan angka di dalam kotak-kotak kecil (Pixel).
- Jika gambar hitam putih (Grayscale), satu kotak berisi angka 0 (Hitam) sampai 255 (Putih).
- Di OpenCV, kotak besar berisi angka ini disimpan dalam tipe data bernama **`Mat`** (singkatan dari Matrix).

## 2. Kenapa Harus Grayscale?
Dalam pengenalan wajah, warna baju atau warna kulit seringkali berubah karena lampu. Yang paling stabil adalah **bayangan dan bentuk wajah**. Itulah kenapa kita mengubah gambar menjadi abu-abu (Grayscale) agar komputer lebih fokus pada bentuk, bukan warna.

## 3. Fungsi Penting yang Digunakan
Dalam kode kita, ada beberapa perintah OpenCV yang sering muncul:

- **`reshape(1, 1)`**: Bayangkan gambar kotak $64 \times 64$. Fungsi ini "membongkar" kotak itu dan menyusunnya menjadi satu baris panjang ($1 \times 4096$). Ini memudahkan kita menghitung secara matematis.
- **`convertTo(CV_32F)`**: Gambar aslinya adalah angka bulat (0, 1, 2). Agar perhitungan kita akurat (bisa pakai koma), kita ubah menjadi tipe *Float* (32-bit).
- **`reduce(..., REDUCE_AVG)`**: Fungsi ini digunakan untuk menjumlahkan semua gambar dan membaginya dengan jumlah gambar untuk mendapatkan **rata-rata**.
- **`equalizeHist`**: Ini seperti "memperbaiki kontras". Jika foto terlalu gelap atau terang, fungsi ini meratakannya agar ciri wajah lebih jelas.
