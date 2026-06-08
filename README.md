# 🏍️ Prediksi Harga Sepeda Motor Bekas (Multiple Linear Regression)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fardan16/uas-statistika-dan-probabilitas/blob/main/Aplikasi_Prediksi.ipynb)

**Tugas Mata Kuliah Statistika dan Probabilitas**
* **Nama:** Fardan Yudhistira
* **NIM:** F5512520080
* **Program Studi:** S1 Teknik Informatika
* **Institusi:** Universitas Tadulako

---

## 📌 Deskripsi Project
Project ini adalah implementasi pemodelan **Regresi Linear Berganda (*Multiple Linear Regression*)** menggunakan bahasa pemrograman Python untuk memprediksi harga jual sepeda motor bekas berdasarkan spesifikasinya. 

Berbeda dengan pendekatan *Machine Learning* konvensional yang menggunakan *library black-box* (seperti `scikit-learn`), sistem prediksi ini **dibangun dari nol menggunakan operasi Aljabar Matriks (Normal Equation)** dengan bantuan library NumPy.

## ✨ Fitur Utama
1. **Analisis Matriks Aljabar:** Menghitung bobot koefisien dari 5 variabel prediktor secara matematis menggunakan *Matrix Inversion* dan *Dot Product* untuk meminimalkan *error*.
2. **Koreksi Depresiasi Otomatis:** Sistem menentukan rata-rata nilai penyusutan harga kendaraan (sekitar Rp 1,6 Juta/tahun akibat bertambahnya umur dan jarak tempuh), lalu mengoreksi hasil prediksinya agar sesuai dengan kondisi probabilitas pasar saat ini.
3. **Interactive UI/UX:** Dilengkapi dengan antarmuka pengguna berbasis HTML/CSS 

## 📊 Variabel Dataset
Dataset yang digunakan (`motor_second.csv`) yang berasal dari https://www.kaggle.com/datasets/yakubianacolyte/dataset-penjualan-sepeda-motor-bekas dan telah dibersihkan menjadi format murni numerik dengan variabel berikut:
* **Target (Y):** Harga Jual Bekas (dalam ribuan Rupiah)
* **Prediktor (X):**
  - Tahun Pembuatan
  - Jarak Tempuh / Odometer (km)
  - Biaya Pajak Kendaraan (Ribuan Rp)
  - Konsumsi BBM (km/liter)
  - Kapasitas Mesin (CC)

## 🚀 Cara Menjalankan Aplikasi

### Opsi 1: Menjalankan Langsung di Browser (Rekomendasi)
Aplikasi ini dapat dijalankan langsung tanpa perlu instalasi di komputer lokal. Cukup klik tombol **Open in Colab** di bagian atas halaman ini. Setelah Google Colab terbuka:
1. Upload file `motor_second.csv` ke dalam *file explorer* di sisi kiri Colab.
2. Klik menu **Runtime > Run All**.
3. *Scroll* ke bagian paling bawah untuk mencoba aplikasi kalkulator prediksinya!

### Opsi 2: Menjalankan Secara Lokal (VS Code / Jupyter)
1. *Clone repository* ini ke komputermu.
2. Pastikan Python 3 sudah terinstal di sistem.
3. Buka terminal di dalam folder project dan instal *dependencies* yang dibutuhkan:
   ```bash
   pip install pandas numpy ipywidgets
