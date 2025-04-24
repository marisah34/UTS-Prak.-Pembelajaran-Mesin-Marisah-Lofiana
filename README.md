# Klasifikasi Jeruk vs Anggur menggunakan Naive Bayes

Nama: Marisah Lofiana

NIM: 1227050068

## Deskripsi
Proyek kali ini bertujuan untuk membangun model klasifikasi buah antara jeruk (orange) dan anggur (grapefruit) menggunakan algoritma **Naive Bayes**. Dimana Datasetnya diambil dari [Kaggle - Oranges vs Grapefruit](https://www.kaggle.com/datasets/joshmcadams/oranges-vs-grapefruit).

## Tahapan Proyek

### **Import Library**
Pada tahap ini, saya akan mengimpor berbagai library yang akan saya gunakan untuk analisis data dan pembuatan model. Library yang digunakan antara lain:
- **pandas** dan **numpy** untuk pengolahan data.
- **matplotlib** dan **seaborn** untuk visualisasi.
- **scikit-learn** untuk model Naive Bayes, cross-validation, dan evaluasi model.

### **Load Dataset**
Dataset buah dimuat dari file CSV menggunakan **pandas**. Dataset ini berisi fitur seperti ukuran, berat, dan warna RGB dari buah-buahan yang akan digunakan sebagai input dalam klasifikasi.

### **Eksplorasi Data**
Langkah awal eksplorasi dilakukan untuk memahami struktur dan kualitas data:
- Menampilkan data sample awal (head()). 
- Memeriksa Nilai yang hilang (isnull().sum())
- Melihat distribusi label pada kolom 'name' menggunakan value_counts().

### **Exploratory Data Analysis (EDA)**
EDA dilakukan untuk memahami karakteristik data melalui visualisasi:

**Countplot**: Menunjukkan distribusi jumlah masing-masing jenis buah.

**Heatmap**: Menampilkan korelasi antar fitur numerik, membantu memahami hubungan antar variabel

###  **Preprocessing**
- Fitur numerik seperti diameter, berat, dan RGB dipilih untuk digunakan dalam model.

- Data dinormalisasi menggunakan StandardScaler dari scikit-learn agar fitur memiliki skala yang sebanding.

###  **Split Dataset**
Data dibagi menjadi dua bagian:

- Training Data: 80% data digunakan untuk melatih model.

- Testing Data: 20% sisanya digunakan untuk menguji performa model. Pembagian dilakukan menggunakan train_test_split() dari sklearn.

### **Buat dan Latih Model**
Model klasifikasi yang digunakan adalah **Gaussian Naive Bayes** dari sklearn.naive_bayes. Model ini dilatih menggunakan data latih (X_train, y_train).


### **Prediksi dan Evaluasi**
Setelah pelatihan, model digunakan untuk memprediksi data uji (X_test). Evaluasi performa dilakukan dengan:

- Confusion Matrix: Untuk membandingkan hasil prediksi dengan label asli.

- Classification Report: Menyediakan metrik seperti akurasi, precision, recall, dan F1-score.

## Persyaratan
Untuk menjalankan proyek ini, pastikan Anda memiliki lingkungan Python dengan versi 3.x dan beberapa library berikut:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`

### Instalasi
Untuk menginstal library yang dibutuhkan, jalankan perintah berikut:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
