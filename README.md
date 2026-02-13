# Final Project Visi Komputer - Image Stitching (Panorama) SIFT

Repositori ini berisi implementasi algoritma **Scale-Invariant Feature Transform (SIFT)** untuk menggabungkan dua buah citra (Image Stitching / Panorama) menjadi satu gambar yang utuh. Project ini disusun untuk memenuhi tugas Final Project Mata Kuliah Visi Komputer.

## Deskripsi Project
Program ini menggunakan Python dan pustaka OpenCV untuk melakukan:
1. **Feature Detection:** Mendeteksi titik unik (keypoints) menggunakan SIFT.
2. **Feature Matching:** Mencocokkan fitur dari dua gambar menggunakan `BFMatcher` (Brute-Force) dengan *Lowe's Ratio Test*.
3. **Homography & Warping:** Mencari matriks homografi menggunakan algoritma `RANSAC` dan menyatukan kedua gambar ke dalam satu kanvas pintar yang tidak memotong area negatif.

## Struktur Direktori
```text
UAS/
├── images/
│   ├── truckl.jpeg     # gambar sisi kiri
│   ├── truckr.jpeg     # gambar sisi kanan
│   ├── truk1.jpeg      # gambar sisi kiri
│   └── truk2.jpeg      # gambar sisi kanan
├── result/
│   └── result.png      # Hasil output visualisasi dan panorama
├── panorama.py         # Source code utama
└── Report.pdf          # Laporan Final Project (Format IEEE)
```

## Persiapan
Pastikan Python sudah terinstal di sistem. install libary yg dibutuhkan menggunakan:
```bash
pip install opencv-python matplotlib numpy
```
## Cara Menjalankan Program (How to Run)
### 1. Clone repositori ini atau download folder project.
```bash
pip clone https://github.com/cardinaldeacre/Panoramic-Image-Stitchin-with-Scale-Invariant-Feature-Transform-SIFT-
```
### 2. Buka terminal dan arahkan direktori ke direktori proyek.


### 3. Jalankan script Python dengan perintah berikut:
```bash
python panorama.py
```
### 4. Jendela matplotlib akan terbuka menampilkan 4 visualisai:
* Keypoints pada gambar 1 (mentah)
* Keypoints pada gambar 2 (mentah)
* Feature Matching antar kedua gambar
* Hasil akhir gamnbar panoramik
