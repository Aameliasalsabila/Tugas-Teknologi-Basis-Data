# Tugas-Teknologi-Basis-Data
# Menyimpan dan Mengakses Banyak Gambar dengan Python

Repositori ini berisi implementasi tiga metode utama untuk menyimpan dan mengakses banyak gambar menggunakan Python. Jika kamu bekerja dengan dataset gambar besar untuk tugas seperti klasifikasi atau deteksi objek menggunakan CNN, metode penyimpanan yang efisien sangat penting.

## 📌 Metode Penyimpanan
1. **Menyimpan gambar sebagai file `.png` atau `.jpg` di disk**
2. **Menggunakan database LMDB untuk akses cepat**
3. **Menyimpan gambar dalam format HDF5 yang terstruktur**

## 🔍 Analisis Performa
- Kapan metode penyimpanan alternatif lebih baik?
- Perbandingan kecepatan membaca & menulis gambar tunggal vs. banyak gambar
- Pengaruh metode penyimpanan terhadap penggunaan disk

## 📂 Dataset yang Digunakan
Dataset yang digunakan dalam repositori ini adalah **CIFAR-10**, yaitu kumpulan 60.000 gambar berwarna (32x32 piksel) yang termasuk dalam beberapa kategori seperti kucing, anjing, dan pesawat terbang.

Saat dataset ini diekstrak, file gambar tidak langsung bisa dibaca karena telah diserialkan menggunakan **cPickle**. Oleh karena itu, kita akan membahas juga bagaimana melakukan deserialisasi dengan `pickle` untuk membaca dataset dengan benar.

## 🚀 Persiapan
### Instalasi Dependensi
Pastikan kamu memiliki Python terinstal, lalu jalankan perintah berikut untuk menginstal pustaka yang diperlukan:

```bash
pip install numpy opencv-python lmdb h5py matplotlib
```

### Menjalankan Kode
Gunakan skrip Python dalam repositori ini untuk menyimpan dan membaca gambar menggunakan metode yang berbeda. Contoh cara menjalankan salah satu metode:

```bash
python save_images.py
```

## ⚠️ Catatan Penting
- `pickle` dapat digunakan untuk menyimpan data, tetapi memiliki risiko keamanan karena dapat mengeksekusi kode arbitrer saat memuat objek yang tidak tepercaya.
- Pemilihan metode penyimpanan tergantung pada ukuran dataset dan kecepatan akses yang dibutuhkan.

---
✨ Selamat bereksperimen dengan metode penyimpanan gambar! 🚀
