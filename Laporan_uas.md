# Laporan UAS Kecerdasan Buatan

## Prediksi Hasil Pertandingan Sepak Bola Internasional Menggunakan Algoritma Decision Tree dan Random Forest

Nama : Fikri Juan Septriana

NIM : 2406021

Program Studi : Teknik Informatika

# 1. Business Understanding

## 1.1 Latar Belakang

Kecerdasan Buatan (Artificial Intelligence/AI) merupakan salah satu bidang ilmu komputer yang berkembang sangat pesat dan telah diterapkan pada berbagai sektor, termasuk kesehatan, pendidikan, bisnis, transportasi, hingga olahraga. Salah satu cabang AI yang banyak digunakan adalah **Machine Learning**, yaitu metode yang memungkinkan komputer mempelajari pola dari data untuk menghasilkan prediksi atau keputusan tanpa harus diprogram secara eksplisit (Géron, 2022).

Dalam dunia olahraga, khususnya sepak bola, setiap pertandingan menghasilkan data yang sangat beragam, seperti tanggal pertandingan, tim yang bertanding, skor akhir, lokasi pertandingan, turnamen, serta berbagai informasi lainnya. Data tersebut terus bertambah setiap tahunnya dan menjadi sumber informasi yang sangat berharga apabila dianalisis menggunakan teknik Machine Learning.

Prediksi hasil pertandingan sepak bola merupakan salah satu permasalahan klasifikasi yang menarik karena hasil pertandingan dipengaruhi oleh banyak faktor, seperti kualitas tim, keuntungan bermain di kandang (*home advantage*), pengalaman bertanding, lokasi pertandingan, hingga jenis kompetisi yang diikuti. Dengan memanfaatkan data historis pertandingan, model Machine Learning dapat mempelajari pola-pola yang muncul sehingga mampu menghasilkan prediksi terhadap hasil pertandingan berikutnya.

Pada penelitian ini digunakan dataset **International Football Results from 1872 to 2026** yang berisi data pertandingan sepak bola internasional dari tahun 1872 hingga 2026. Dataset tersebut mencakup informasi mengenai tim tuan rumah, tim tamu, skor pertandingan, turnamen, kota, negara, serta status venue pertandingan.

Penelitian ini menerapkan dua algoritma klasifikasi, yaitu **Decision Tree** dan **Random Forest**. Decision Tree dipilih karena memiliki struktur yang sederhana dan mudah dipahami, sedangkan Random Forest dipilih karena mampu meningkatkan performa prediksi melalui metode *ensemble learning* dengan menggabungkan banyak pohon keputusan (Breiman, 2001). Hasil dari kedua algoritma kemudian dibandingkan menggunakan beberapa metrik evaluasi untuk menentukan model yang memiliki performa terbaik dalam memprediksi hasil pertandingan sepak bola internasional.

---

## 1.2 Identifikasi Permasalahan

Berdasarkan latar belakang tersebut, beberapa permasalahan yang dapat diidentifikasi adalah sebagai berikut.

1. Banyaknya data pertandingan sepak bola internasional belum dimanfaatkan secara optimal untuk menghasilkan informasi yang berguna.
2. Sulit menentukan hasil pertandingan hanya berdasarkan pengamatan secara manual karena jumlah data yang sangat besar.
3. Diperlukan model Machine Learning yang mampu mempelajari pola dari data historis pertandingan.
4. Belum diketahui algoritma yang memiliki performa lebih baik antara Decision Tree dan Random Forest pada dataset yang digunakan.

---

## 1.3 Rumusan Masalah

Rumusan masalah pada penelitian ini adalah sebagai berikut.

1. Bagaimana membangun model Machine Learning untuk memprediksi hasil pertandingan sepak bola internasional?
2. Bagaimana proses pengolahan dataset agar siap digunakan dalam proses klasifikasi?
3. Bagaimana performa algoritma Decision Tree dalam memprediksi hasil pertandingan?
4. Bagaimana performa algoritma Random Forest dalam memprediksi hasil pertandingan?
5. Algoritma manakah yang memberikan hasil prediksi terbaik berdasarkan metrik evaluasi?

---

## 1.4 Tujuan Penelitian

Penelitian ini memiliki beberapa tujuan, yaitu:

1. Mengolah dataset pertandingan sepak bola internasional menjadi data yang siap digunakan dalam proses Machine Learning.
2. Melakukan analisis terhadap karakteristik dataset menggunakan Exploratory Data Analysis (EDA).
3. Membangun model klasifikasi menggunakan algoritma Decision Tree.
4. Membangun model klasifikasi menggunakan algoritma Random Forest.
5. Membandingkan performa kedua algoritma berdasarkan nilai Accuracy, Precision, Recall, dan F1-Score.
6. Menentukan model terbaik yang dapat digunakan untuk memprediksi hasil pertandingan sepak bola internasional.

---

## 1.5 Manfaat Penelitian

Adapun manfaat yang diharapkan dari penelitian ini adalah sebagai berikut.

### Manfaat Akademis

- Menambah pemahaman mengenai penerapan Machine Learning pada bidang olahraga.
- Menjadi referensi bagi penelitian selanjutnya mengenai prediksi hasil pertandingan sepak bola.

### Manfaat Praktis

- Membantu analis olahraga dalam memahami pola pertandingan berdasarkan data historis.
- Memberikan contoh penerapan algoritma Decision Tree dan Random Forest pada kasus klasifikasi.
- Menjadi media pembelajaran bagi mahasiswa dalam menerapkan proses Machine Learning secara lengkap.

---

## 1.6 Pengguna Sistem

Model prediksi yang dibangun pada penelitian ini dapat dimanfaatkan oleh beberapa pihak, antara lain:

- Mahasiswa sebagai media pembelajaran Machine Learning.
- Peneliti yang melakukan penelitian pada bidang data mining atau kecerdasan buatan.
- Analis pertandingan sepak bola sebagai alat bantu analisis data.
- Pengembang aplikasi olahraga yang membutuhkan model prediksi pertandingan.

---

## 1.7 Solusi yang Diusulkan

Solusi yang diusulkan dalam penelitian ini adalah membangun sistem prediksi hasil pertandingan sepak bola internasional menggunakan algoritma Decision Tree dan Random Forest.

Tahapan penelitian meliputi:

1. Mengumpulkan dan memahami dataset.
2. Melakukan Exploratory Data Analysis (EDA).
3. Melakukan Feature Engineering.
4. Menyiapkan data melalui proses Data Preparation.
5. Melatih model menggunakan algoritma Decision Tree.
6. Melatih model menggunakan algoritma Random Forest.
7. Mengevaluasi performa model menggunakan metrik Accuracy, Precision, Recall, F1-Score, Classification Report, dan Confusion Matrix.
8. Membandingkan kedua model untuk menentukan model terbaik.

Melalui tahapan tersebut diharapkan diperoleh model Machine Learning yang mampu memberikan prediksi hasil pertandingan dengan tingkat akurasi yang baik sehingga dapat digunakan sebagai dasar dalam analisis pertandingan sepak bola internasional.

---

# 3. Exploratory Data Analysis (EDA)

## 3.1 Pengertian Exploratory Data Analysis

Exploratory Data Analysis (EDA) merupakan tahapan awal dalam proses analisis data yang bertujuan untuk memahami karakteristik dataset sebelum dilakukan proses pemodelan. Menurut Han, Kamber, dan Pei (2012), EDA membantu peneliti menemukan pola, hubungan antarvariabel, distribusi data, serta mendeteksi adanya anomali atau ketidakseimbangan data yang dapat memengaruhi performa model Machine Learning.

Pada penelitian ini, EDA dilakukan untuk memperoleh gambaran umum mengenai data pertandingan sepak bola internasional, sehingga dapat diketahui karakteristik data yang akan digunakan pada proses klasifikasi.

---

## 3.2 Pemeriksaan Struktur Dataset

Tahap pertama dilakukan dengan menampilkan beberapa data teratas menggunakan fungsi `head()`, melihat jumlah baris dan kolom menggunakan `shape`, mengetahui tipe data setiap atribut menggunakan `info()`, serta memperoleh statistik deskriptif menggunakan `describe()`.

Tujuan dari tahapan ini adalah untuk memastikan bahwa dataset telah berhasil dimuat dengan baik dan memahami karakteristik masing-masing atribut.

---

## 3.3 Pemeriksaan Missing Value

Missing value merupakan data yang kosong atau tidak memiliki nilai pada suatu atribut. Keberadaan missing value dapat memengaruhi proses pembelajaran model sehingga perlu diperiksa sebelum dilakukan pemodelan.

Pemeriksaan dilakukan menggunakan fungsi:

```python
df.isnull().sum()
```

Berdasarkan hasil pemeriksaan, dataset tidak memiliki missing value sehingga seluruh data dapat langsung digunakan pada proses selanjutnya tanpa perlu dilakukan imputasi data.

---

## 3.4 Pemeriksaan Data Duplikat

Data duplikat merupakan data yang memiliki isi yang sama dengan data lainnya. Data duplikat dapat menyebabkan model mempelajari pola yang sama secara berulang sehingga memengaruhi hasil prediksi.

Pemeriksaan dilakukan menggunakan fungsi:

```python
df.duplicated().sum()
```

Apabila ditemukan data duplikat maka dilakukan penghapusan menggunakan fungsi `drop_duplicates()`.

---

## 3.5 Distribusi Hasil Pertandingan

Distribusi hasil pertandingan divisualisasikan menggunakan diagram batang berdasarkan tiga kelas target, yaitu:

- Home Win
- Draw
- Away Win

Visualisasi ini bertujuan untuk mengetahui keseimbangan jumlah data pada setiap kelas.

### Analisis

Berdasarkan hasil visualisasi diketahui bahwa kemenangan tim tuan rumah (Home Win) memiliki jumlah data paling banyak dibandingkan hasil seri (Draw) maupun kemenangan tim tamu (Away Win). Hal ini menunjukkan adanya kecenderungan keuntungan bermain di kandang (home advantage).

---

## 3.6 Distribusi Jumlah Gol

Analisis distribusi jumlah gol dilakukan terhadap atribut `home_score` dan `away_score`.

Visualisasi ini bertujuan mengetahui pola jumlah gol yang dicetak selama pertandingan.

### Analisis

Sebagian besar pertandingan menghasilkan jumlah gol yang relatif rendah, yaitu antara 0 hingga 3 gol. Jumlah pertandingan dengan skor tinggi memiliki frekuensi yang lebih sedikit dibandingkan skor rendah.

---

## 3.7 Turnamen dengan Jumlah Pertandingan Terbanyak

Analisis dilakukan untuk mengetahui turnamen yang paling sering muncul dalam dataset.

Visualisasi menggunakan diagram batang berdasarkan jumlah pertandingan setiap turnamen.

### Analisis

Hasil visualisasi menunjukkan bahwa beberapa turnamen internasional memiliki jumlah pertandingan jauh lebih banyak dibandingkan turnamen lainnya. Hal ini menunjukkan bahwa turnamen tersebut diselenggarakan secara rutin dalam jangka waktu yang panjang.

---

## 3.8 Negara Penyelenggara Terbanyak

Visualisasi dilakukan untuk mengetahui negara yang paling sering menjadi lokasi penyelenggaraan pertandingan internasional.

### Analisis

Negara-negara dengan jumlah pertandingan terbanyak menunjukkan bahwa negara tersebut sering menjadi tuan rumah penyelenggaraan kompetisi internasional maupun pertandingan persahabatan.

---

## 3.9 Tim Tuan Rumah Terbanyak

Visualisasi dilakukan untuk mengetahui tim nasional yang paling sering bermain sebagai tim tuan rumah.

### Analisis

Beberapa negara memiliki jumlah pertandingan kandang yang jauh lebih banyak dibandingkan negara lain. Hal ini dipengaruhi oleh frekuensi penyelenggaraan pertandingan internasional di negara tersebut.

---

## 3.10 Tim Tamu Terbanyak

Analisis dilakukan terhadap jumlah pertandingan setiap tim sebagai tim tamu.

### Analisis

Visualisasi menunjukkan bahwa beberapa negara memiliki frekuensi pertandingan tandang yang tinggi karena aktif mengikuti berbagai kompetisi internasional.

---

## 3.11 Distribusi Pertandingan Berdasarkan Tahun

Distribusi pertandingan berdasarkan tahun bertujuan mengetahui perkembangan jumlah pertandingan internasional dari waktu ke waktu.

### Analisis

Jumlah pertandingan mengalami peningkatan yang signifikan pada era modern. Hal ini menunjukkan semakin berkembangnya kompetisi sepak bola internasional serta meningkatnya jumlah turnamen yang diselenggarakan.

---

## 3.12 Heatmap Korelasi

Heatmap digunakan untuk mengetahui hubungan antar atribut numerik pada dataset.

Atribut yang dianalisis meliputi:

- Home Score
- Away Score
- Year
- Month
- Day

### Analisis

Berdasarkan heatmap korelasi, sebagian besar atribut memiliki hubungan yang relatif rendah satu sama lain. Hal ini menunjukkan bahwa setiap atribut memberikan informasi yang berbeda sehingga layak digunakan sebagai fitur dalam proses klasifikasi.

---

# 4. Feature Engineering

## 4.1 Pengertian Feature Engineering

Feature Engineering merupakan proses membangun atau memodifikasi atribut sehingga menghasilkan fitur baru yang lebih informatif bagi model Machine Learning. Menurut Géron (2022), Feature Engineering merupakan salah satu tahapan yang paling penting karena kualitas fitur sangat memengaruhi performa model.

---

## 4.2 Konversi Tanggal

Kolom `date` diubah ke dalam format **datetime** agar informasi tanggal dapat diproses lebih lanjut.

Selanjutnya dibuat tiga fitur baru, yaitu:

- Year
- Month
- Day

Ketiga fitur tersebut diharapkan dapat membantu model mempelajari pola pertandingan berdasarkan waktu pelaksanaan.

---

## 4.3 Pembuatan Target

Target klasifikasi dibentuk berdasarkan perbandingan antara jumlah gol tim tuan rumah (`home_score`) dan tim tamu (`away_score`).

Kriteria klasifikasi adalah sebagai berikut:

- **Home Win**, apabila home_score > away_score.
- **Away Win**, apabila away_score > home_score.
- **Draw**, apabila home_score = away_score.

Target tersebut kemudian disimpan pada atribut `result`.

---

# 5. Data Preparation

## 5.1 Pengertian Data Preparation

Data Preparation merupakan proses menyiapkan data agar dapat digunakan oleh algoritma Machine Learning. Tahapan ini meliputi pemilihan fitur, transformasi data, encoding, dan pembagian dataset menjadi data latih dan data uji.

---

## 5.2 Pemilihan Fitur

Berdasarkan hasil Feature Engineering, atribut yang digunakan pada proses pemodelan adalah:

- home_team
- away_team
- tournament
- city
- country
- neutral
- year
- month
- day

Sedangkan atribut `result` digunakan sebagai variabel target.

---

## 5.3 Label Encoding

Karena sebagian besar atribut berupa data kategorikal, dilakukan proses Label Encoding agar data dapat diproses oleh algoritma Machine Learning.

Label Encoding mengubah setiap kategori menjadi representasi bilangan bulat tanpa mengubah jumlah data.

---

## 5.4 Pembagian Dataset

Dataset dibagi menjadi dua bagian, yaitu:

- **Data Training sebesar 80%**
- **Data Testing sebesar 20%**

Pembagian dilakukan menggunakan fungsi `train_test_split()` dengan parameter `stratify` agar proporsi setiap kelas tetap seimbang pada data latih maupun data uji.

Tahapan ini bertujuan agar model dapat dilatih menggunakan data training dan kemudian dievaluasi menggunakan data testing yang belum pernah dilihat sebelumnya.

---

# 6. Modeling

## 6.1 Pengertian Modeling

Modeling merupakan tahapan dalam proses Machine Learning yang bertujuan membangun model berdasarkan data yang telah dipersiapkan pada tahap sebelumnya. Pada penelitian ini digunakan dua algoritma klasifikasi, yaitu **Decision Tree Classifier** dan **Random Forest Classifier**. Kedua algoritma dipilih karena mampu menangani data kategorikal maupun numerik serta memiliki performa yang baik dalam permasalahan klasifikasi multikelas.

Dataset yang telah melalui proses Feature Engineering dan Data Preparation dibagi menjadi dua bagian, yaitu data latih (training) sebesar 80% dan data uji (testing) sebesar 20%. Data latih digunakan untuk membangun model, sedangkan data uji digunakan untuk mengevaluasi kemampuan model dalam melakukan prediksi terhadap data yang belum pernah dilihat sebelumnya.

---

## 6.2 Algoritma Decision Tree

Decision Tree merupakan algoritma klasifikasi yang membangun struktur pohon keputusan berdasarkan atribut yang memberikan informasi terbaik terhadap proses klasifikasi. Setiap simpul pada pohon merepresentasikan suatu atribut, sedangkan cabang menunjukkan hasil dari proses pembagian data. Proses tersebut terus dilakukan hingga seluruh data berhasil diklasifikasikan atau memenuhi kriteria penghentian tertentu (Quinlan, 1986).

Pada penelitian ini, algoritma Decision Tree digunakan sebagai model dasar untuk melakukan klasifikasi hasil pertandingan sepak bola internasional menjadi tiga kategori, yaitu **Home Win**, **Draw**, dan **Away Win**.

### Langkah-langkah Modeling Decision Tree

1. Menentukan data latih dan data uji.
2. Membentuk model Decision Tree menggunakan `DecisionTreeClassifier`.
3. Melatih model menggunakan data training.
4. Melakukan prediksi terhadap data testing.
5. Menghitung tingkat akurasi model.

### Kelebihan Decision Tree

- Mudah dipahami dan diinterpretasikan.
- Mampu menangani data kategorikal maupun numerik.
- Tidak memerlukan proses normalisasi data.
- Proses pelatihan relatif cepat.

### Kekurangan Decision Tree

- Rentan mengalami overfitting apabila pohon terlalu dalam.
- Performa dapat menurun apabila data mengandung banyak variasi.

---

## 6.3 Algoritma Random Forest

Random Forest merupakan metode ensemble learning yang dikembangkan dari Decision Tree. Algoritma ini membangun banyak pohon keputusan secara acak, kemudian hasil prediksi setiap pohon digabungkan menggunakan mekanisme voting sehingga menghasilkan prediksi akhir yang lebih stabil dan akurat (Breiman, 2001).

Penggunaan Random Forest diharapkan mampu mengurangi overfitting yang sering terjadi pada Decision Tree serta meningkatkan kemampuan generalisasi model.

### Langkah-langkah Modeling Random Forest

1. Menentukan data training dan data testing.
2. Membentuk model Random Forest menggunakan `RandomForestClassifier`.
3. Melatih model menggunakan data training.
4. Melakukan prediksi terhadap data testing.
5. Menghitung tingkat akurasi model.

### Kelebihan Random Forest

- Memiliki akurasi yang tinggi.
- Mengurangi risiko overfitting.
- Lebih stabil dibandingkan Decision Tree.
- Mampu menangani dataset berukuran besar.

### Kekurangan Random Forest

- Membutuhkan waktu pelatihan yang lebih lama.
- Membutuhkan memori yang lebih besar.
- Interpretasi model lebih sulit dibandingkan Decision Tree.

---

## 6.4 Perbandingan Algoritma

Pada penelitian ini dilakukan perbandingan antara Decision Tree dan Random Forest berdasarkan beberapa metrik evaluasi, yaitu Accuracy, Precision, Recall, dan F1-Score. Model dengan nilai evaluasi terbaik dipilih sebagai model utama untuk melakukan prediksi hasil pertandingan sepak bola internasional.

---

# 7. Evaluation

## 7.1 Pengertian Evaluation

Evaluation merupakan tahapan untuk mengukur performa model Machine Learning setelah proses pelatihan selesai dilakukan. Evaluasi bertujuan mengetahui kemampuan model dalam melakukan prediksi terhadap data yang belum pernah digunakan selama proses pelatihan.

Pada penelitian ini digunakan beberapa metrik evaluasi yang umum digunakan pada permasalahan klasifikasi, yaitu Accuracy, Precision, Recall, F1-Score, Classification Report, dan Confusion Matrix.

---

## 7.2 Accuracy

Accuracy merupakan persentase jumlah prediksi yang benar dibandingkan dengan seluruh jumlah data yang diuji.

Semakin tinggi nilai Accuracy, semakin baik kemampuan model dalam melakukan klasifikasi.

Nilai Accuracy diperoleh menggunakan fungsi:

```python
accuracy_score(y_test, y_pred)
```

---

## 7.3 Precision

Precision menunjukkan seberapa banyak prediksi yang dilakukan model benar dibandingkan seluruh prediksi pada suatu kelas.

Semakin tinggi nilai Precision maka semakin sedikit prediksi yang salah.

Perhitungan dilakukan menggunakan fungsi:

```python
precision_score(y_test, y_pred, average='weighted')
```

---

## 7.4 Recall

Recall menunjukkan kemampuan model dalam menemukan seluruh data yang benar pada setiap kelas.

Semakin tinggi nilai Recall menunjukkan semakin baik kemampuan model mengenali seluruh kelas target.

Perhitungan dilakukan menggunakan fungsi:

```python
recall_score(y_test, y_pred, average='weighted')
```

---

## 7.5 F1-Score

F1-Score merupakan rata-rata harmonik antara Precision dan Recall.

Nilai F1-Score digunakan ketika diperlukan keseimbangan antara Precision dan Recall sehingga mampu memberikan gambaran performa model secara keseluruhan.

Perhitungan dilakukan menggunakan fungsi:

```python
f1_score(y_test, y_pred, average='weighted')
```

---

## 7.6 Classification Report

Classification Report memberikan informasi performa model pada setiap kelas target, meliputi:

- Precision
- Recall
- F1-Score
- Support

Melalui laporan ini dapat diketahui kemampuan model dalam mengklasifikasikan setiap kategori hasil pertandingan.

---

## 7.7 Confusion Matrix

Confusion Matrix merupakan tabel yang menunjukkan jumlah prediksi benar dan prediksi salah pada setiap kelas.

Visualisasi Confusion Matrix memudahkan analisis terhadap kesalahan prediksi yang dilakukan model sehingga dapat diketahui kelas mana yang paling sering mengalami kesalahan klasifikasi.

---

## 7.8 Hasil Evaluasi

Hasil evaluasi kedua model dibandingkan menggunakan tabel berikut.

| Model | Accuracy | Precision | Recall | F1-Score |
|--------|---------:|----------:|-------:|---------:|
| Decision Tree | *(Isi sesuai hasil notebook)* | *(Isi sesuai hasil notebook)* | *(Isi sesuai hasil notebook)* | *(Isi sesuai hasil notebook)* |
| Random Forest | *(Isi sesuai hasil notebook)* | *(Isi sesuai hasil notebook)* | *(Isi sesuai hasil notebook)* | *(Isi sesuai hasil notebook)* |

---

## 7.9 Analisis Hasil

Berdasarkan hasil evaluasi, kedua algoritma mampu melakukan klasifikasi hasil pertandingan sepak bola internasional dengan baik. Namun demikian, model yang memiliki nilai Accuracy, Precision, Recall, dan F1-Score lebih tinggi dipilih sebagai model terbaik.

Selain melihat nilai metrik evaluasi, analisis juga dilakukan terhadap Confusion Matrix untuk mengetahui distribusi prediksi yang benar maupun prediksi yang salah pada masing-masing kelas.

Apabila Random Forest menghasilkan nilai evaluasi yang lebih tinggi dibandingkan Decision Tree, maka dapat disimpulkan bahwa metode ensemble learning mampu meningkatkan kemampuan model dalam melakukan klasifikasi hasil pertandingan. Sebaliknya, apabila Decision Tree memberikan hasil yang lebih baik, maka model tersebut dipilih sebagai model utama pada penelitian ini.

---

# 8. Kesimpulan

Berdasarkan penelitian yang telah dilakukan mengenai prediksi hasil pertandingan sepak bola internasional menggunakan dataset **International Football Results from 1872 to 2026**, dapat diambil beberapa kesimpulan sebagai berikut.

1. Dataset berhasil diproses melalui tahapan **Business Understanding**, **Data Understanding**, **Exploratory Data Analysis (EDA)**, **Feature Engineering**, **Data Preparation**, **Modeling**, dan **Evaluation**. Setiap tahapan dilakukan secara sistematis sehingga data siap digunakan dalam proses pembelajaran Machine Learning.

2. Tahap Exploratory Data Analysis (EDA) memberikan gambaran mengenai karakteristik dataset, seperti distribusi hasil pertandingan, jumlah gol, turnamen yang paling sering diselenggarakan, negara penyelenggara, serta pola pertandingan berdasarkan waktu. Informasi tersebut membantu dalam memahami kondisi data sebelum dilakukan pemodelan.

3. Feature Engineering berhasil menghasilkan fitur baru berupa **year**, **month**, dan **day** dari atribut **date**, serta membentuk variabel target **result** yang terdiri atas tiga kelas, yaitu **Home Win**, **Draw**, dan **Away Win**. Penambahan fitur tersebut memberikan informasi yang lebih relevan bagi proses klasifikasi.

4. Dua algoritma Machine Learning yang digunakan, yaitu **Decision Tree Classifier** dan **Random Forest Classifier**, berhasil diterapkan untuk membangun model klasifikasi hasil pertandingan sepak bola internasional. Kedua algoritma mampu mempelajari pola dari data historis sehingga dapat digunakan untuk melakukan prediksi terhadap data yang belum pernah dilihat sebelumnya.

5. Evaluasi model dilakukan menggunakan metrik **Accuracy**, **Precision**, **Recall**, **F1-Score**, **Classification Report**, dan **Confusion Matrix**. Metrik-metrik tersebut memberikan gambaran mengenai kemampuan masing-masing model dalam mengklasifikasikan hasil pertandingan.

6. Berdasarkan hasil evaluasi yang diperoleh pada notebook, model dengan nilai Accuracy, Precision, Recall, dan F1-Score tertinggi dipilih sebagai model terbaik. Model tersebut dinilai memiliki kemampuan yang lebih baik dalam melakukan prediksi hasil pertandingan dibandingkan model lainnya.

7. Penelitian ini menunjukkan bahwa penerapan algoritma Machine Learning mampu dimanfaatkan untuk membantu proses analisis dan prediksi hasil pertandingan sepak bola internasional berdasarkan data historis yang tersedia.

---

# 9. Saran

Berdasarkan hasil penelitian yang telah dilakukan, terdapat beberapa saran yang dapat menjadi pengembangan pada penelitian selanjutnya, yaitu sebagai berikut.

1. Menambahkan atribut atau fitur yang lebih lengkap, seperti **peringkat FIFA**, **statistik lima pertandingan terakhir**, **jumlah kemenangan**, **jumlah kekalahan**, **jumlah gol rata-rata**, serta **head-to-head** antar tim agar model memperoleh informasi yang lebih kaya.

2. Menggunakan algoritma Machine Learning lainnya, seperti **XGBoost**, **LightGBM**, **CatBoost**, **Gradient Boosting**, maupun **Support Vector Machine (SVM)** untuk membandingkan performa model yang lebih beragam.

3. Melakukan proses **Hyperparameter Tuning** menggunakan **GridSearchCV** atau **RandomizedSearchCV** sehingga parameter model dapat dioptimalkan dan menghasilkan performa yang lebih baik.

4. Menggunakan metode **Cross Validation** untuk memperoleh hasil evaluasi yang lebih stabil dan mengurangi kemungkinan bias akibat pembagian data training dan testing.

5. Mengembangkan penelitian ini menjadi sebuah aplikasi berbasis web atau desktop sehingga pengguna dapat melakukan prediksi hasil pertandingan secara langsung melalui antarmuka yang mudah digunakan.

6. Menggunakan dataset yang selalu diperbarui agar model dapat mempelajari kondisi terbaru dari setiap tim nasional sehingga hasil prediksi menjadi lebih relevan.

---

# 10. Daftar Pustaka

Breiman, L. (2001). *Random Forests*. Machine Learning, 45(1), 5–32. https://doi.org/10.1023/A:1010933404324

Géron, A. (2022). *Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow* (3rd ed.). O'Reilly Media.

Han, J., Kamber, M., & Pei, J. (2012). *Data Mining: Concepts and Techniques* (3rd ed.). Morgan Kaufmann.

Pedregosa, F., Varoquaux, G., Gramfort, A., Michel, V., Thirion, B., Grisel, O., Blondel, M., Prettenhofer, P., Weiss, R., Dubourg, V., Vanderplas, J., Passos, A., Cournapeau, D., Brucher, M., Perrot, M., & Duchesnay, É. (2011). *Scikit-learn: Machine Learning in Python*. Journal of Machine Learning Research, 12, 2825–2830.

Quinlan, J. R. (1986). *Induction of Decision Trees*. Machine Learning, 1(1), 81–106. https://doi.org/10.1007/BF00116251

Scikit-learn Developers. (2025). *Scikit-learn User Guide*. https://scikit-learn.org/stable/

Kaggle. (2026). *International Football Results from 1872 to 2026*. https://www.kaggle.com/

---

# Lampiran

Lampiran yang disertakan pada repository GitHub meliputi:

1. Notebook (`uas_model.ipynb`)
2. Dataset (`results.csv`)
3. README.md
4. Laporan_uas.md
5. Grafik hasil Exploratory Data Analysis (EDA)
6. Confusion Matrix Decision Tree
7. Confusion Matrix Random Forest
8. Grafik Perbandingan Performa Model