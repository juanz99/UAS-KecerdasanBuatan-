# Prediksi Hasil Pertandingan Sepak Bola Internasional Menggunakan Decision Tree dan Random Forest

## Deskripsi Proyek

Proyek ini merupakan tugas UAS Mata Kuliah Kecerdasan Buatan yang bertujuan membangun model Machine Learning untuk memprediksi hasil pertandingan sepak bola internasional menggunakan dataset **International Football Results from 1872 to 2026**.

Model yang digunakan pada penelitian ini adalah:

- Decision Tree Classifier
- Random Forest Classifier

Tahapan pengerjaan mengikuti proses Machine Learning yang terdiri dari Data Understanding, Exploratory Data Analysis (EDA), Feature Engineering, Data Preparation, Modeling, Evaluation, hingga Kesimpulan.

---

## Dataset

**Nama Dataset**

International Football Results from 1872 to 2026

**Sumber Dataset**

Kaggle

Dataset berisi informasi pertandingan sepak bola internasional yang meliputi:

- Tanggal pertandingan
- Tim tuan rumah
- Tim tamu
- Skor pertandingan
- Turnamen
- Kota
- Negara
- Status venue netral

---

## Struktur Repository

```text
UAS-KecerdasanBuatan/
│
├── README.md
├── Laporan_uas.md
├── uas_model.ipynb
│
├── data/
│   ├── dataset/
│   │   └── results.csv
│   │
│   └── jurnal/
│       ├── jurnal1.pdf
│       ├── jurnal2.pdf
│       ├── jurnal3.pdf
│       ├── jurnal4.pdf
│       └── jurnal5.pdf
```

---

## Library yang Digunakan

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## Tahapan Pengerjaan

1. Import Library
2. Load Dataset
3. Data Understanding
4. Exploratory Data Analysis (EDA)
5. Feature Engineering
6. Data Preparation
7. Modeling Decision Tree
8. Modeling Random Forest
9. Evaluation
10. Kesimpulan

---

## Algoritma

- Decision Tree
- Random Forest

---

## Metrik Evaluasi

Model dievaluasi menggunakan:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- Classification Report

---

## Cara Menjalankan Notebook

1. Install seluruh library yang dibutuhkan.
2. Letakkan dataset `results.csv` pada folder `data/dataset`.
3. Buka file `uas_model.ipynb`.
4. Jalankan notebook dari cell pertama hingga terakhir secara berurutan.
5. Lihat hasil evaluasi serta perbandingan kedua model.

---

## Penulis

Nama : Fikri Juan Septriana

NIM : 2406021

Program Studi : Teknik Informatika

Mata Kuliah : Kecerdasan Buatan