# Identifikasi Nominal Mata Uang Rupiah

**Metode Local Binary Pattern (LBP) & Naive Bayes Classifier**

## 📌 Deskripsi

Aplikasi ini merupakan sistem **identifikasi nominal uang kertas Rupiah** berbasis **pengolahan citra digital** menggunakan metode **Local Binary Pattern (LBP)** sebagai ekstraksi fitur dan **Naive Bayes Classifier** sebagai metode klasifikasi.

Aplikasi dibangun menggunakan **Python** dengan antarmuka grafis **Tkinter**, sehingga pengguna dapat:

* Melihat dataset uang Rupiah
* Melakukan identifikasi nominal uang dari citra input
* Melihat plot persebaran data dan nilai akurasi sistem

---

## 🧠 Metode yang Digunakan

1. **Local Binary Pattern (LBP)**
   Digunakan untuk mengekstraksi fitur tekstur dari citra uang kertas.

2. **Naive Bayes Classifier (GaussianNB)**
   Digunakan untuk mengklasifikasikan fitur LBP ke dalam kelas nominal uang.

3. **Stratified K-Fold Cross Validation**
   Digunakan untuk mengukur performa sistem dan memperoleh nilai akurasi rata-rata.

---

## 🖥️ Fitur Aplikasi

### 1. Menu Home

* Input path gambar uang
* Proses identifikasi nominal uang
* Menampilkan:

  * Hasil prediksi nominal
  * Citra uang input
  * Plot hasil prediksi

### 2. Menu Dataset

* Menampilkan dataset uang Rupiah
* Dataset terdiri dari **8 kelas nominal**:

  * Rp1.000
  * Rp2.000
  * Rp5.000
  * Rp10.000
  * Rp20.000
  * Rp50.000
  * Rp75.000
  * Rp100.000
* Setiap kelas memiliki **15 citra**

### 3. Menu Plot

* Menampilkan plot persebaran fitur dataset
* Menampilkan nilai akurasi rata-rata sistem

---

## 📂 Struktur Folder

```
├── app.py
├── DATASET_UANG/
│   ├── 1RIBU/
│   ├── 2RIBU/
│   ├── 5RIBU/
│   ├── 10RIBU/
│   ├── 20RIBU/
│   ├── 50RIBU/
│   ├── 75RIBU/
│   └── 100RIBU/
├── FOTO_UANG/
│   ├── UANG1.jpg
│   ├── UANG2.jpg
│   └── ...
├── UI/
│   ├── Nav.jpg
│   ├── Home.jpg
│   ├── Dataset.jpg
│   └── Plot.jpg
├── plotData.jpg
└── plotPred.jpg
```

---

## ⚙️ Library yang Digunakan

Pastikan library berikut sudah terinstal:

```bash
pip install numpy opencv-python pillow scikit-image scikit-learn matplotlib
```

---

## ▶️ Cara Menjalankan Program

1. Pastikan struktur folder sesuai
2. Jalankan perintah berikut:

```bash
python app.py
```

3. Aplikasi GUI akan terbuka otomatis

---

## 🧪 Contoh Path Gambar untuk Identifikasi

Gunakan path berikut pada menu **Home**:

```
FOTO_UANG/UANG1.jpg
FOTO_UANG/UANG2.jpg
FOTO_UANG/UANG3.jpg
FOTO_UANG/UANG4.jpg
FOTO_UANG/UANG5.jpg
FOTO_UANG/UANG6.jpg
FOTO_UANG/UANG7.jpg
FOTO_UANG/UANG8.jpg
```

---

## 📊 Evaluasi Sistem

* Metode evaluasi: **5-Fold Cross Validation**
* Klasifier: **Gaussian Naive Bayes**
* Output evaluasi:

  * Akurasi tiap fold
  * Confusion Matrix
  * Rata-rata akurasi keseluruhan

---

## 📌 Catatan

* Dataset dan citra uji harus memiliki kualitas yang cukup agar hasil identifikasi optimal
* Sistem ini bersifat **offline** dan menggunakan citra statis

---
