# Konsep dan Tujuan Eigenface

## Apa itu Pengenalan Wajah?
Bayangkan kamu sedang berada di gerbang sekolah. Satpam melihat wajahmu dan langsung tahu namamu. Bagaimana otak satpam melakukannya? Satpam tidak menghitung jumlah pori-pori kulitmu, tapi dia mengenali **pola unik** seperti bentuk mata, lebar hidung, atau garis rahang.

**Eigenface** adalah cara komputer meniru proses ini menggunakan matematika (Aljabar Linear).

## Tujuan Proyek
Tujuan utama proyek ini adalah membuat program yang bisa:
1. **Belajar**: Mengingat ciri-ciri wajah dari sekumpulan foto (Dataset).
2. **Mengenali**: Menentukan siapa orang yang ada di depan kamera secara *real-time*.

## Konsep Utama: "Wajah Hantu"
Dalam metode ini, kita akan membuat sekumpulan wajah dasar yang disebut **Eigenfaces**. Bentuknya terlihat seperti wajah hantu yang samar. 

Prinsipnya sederhana: **Setiap wajah manusia adalah gabungan dari beberapa wajah hantu ini.**
- Wajah Budi = (20% Wajah Hantu A) + (5% Wajah Hantu B) + ...
- Wajah Ani = (10% Wajah Hantu A) + (30% Wajah Hantu B) + ...

Dengan menyimpan "persentase" gabungan ini, komputer bisa mengenali orang tanpa harus menyimpan file gambar asli yang besar.
