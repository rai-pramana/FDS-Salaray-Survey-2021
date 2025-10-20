# Salary Survey 2021 - Data Analysis Project

## 📋 Deskripsi Proyek

Proyek ini merupakan analisis data komprehensif terhadap survei gaji tahun 2021 yang dilakukan sebagai bagian dari mata kuliah **Foundation of Data Science (B)**. Proyek ini mengeksplorasi faktor-faktor yang mempengaruhi gaji responden, termasuk industri, pengalaman kerja, jenis kelamin, dan tingkat pendidikan.

### Anggota Kelompok 1:

-   I Made Dwika Dyananda Kumara (2105551074)
-   Made Wahyu Adwitya Pramana (2105551092)
-   I Kadek Rai Pramana (2105551094)

## 🎯 Tujuan Analisis

Proyek ini bertujuan untuk menjawab pertanyaan-pertanyaan berikut:

1. **Industri mana yang memberikan gaji tertinggi/terendah?**
2. **Bagaimana pengalaman kerja mempengaruhi gaji?**
3. **Bagaimana jenis kelamin mempengaruhi gaji?**
4. **Bagaimana tingkat pendidikan mempengaruhi gaji?**

## 📊 Dataset

Dataset berisi survei gaji dari **27.946 responden** dengan 18 kolom yang mencakup:

-   Informasi demografis (usia, jenis kelamin, ras)
-   Informasi pekerjaan (industri, jabatan, pengalaman kerja)
-   Informasi geografis (negara, negara bagian, kota)
-   Informasi gaji (gaji tahunan, kompensasi tambahan, mata uang)
-   Tingkat pendidikan

## 🔧 Teknologi & Library

Proyek ini menggunakan Python dengan library berikut:

-   **Pandas**: Manipulasi dan analisis data
-   **NumPy**: Operasi numerik
-   **Matplotlib & Seaborn**: Visualisasi data
-   **SciPy**: Uji statistik
-   **Statsmodels**: Pemodelan statistik
-   **Scikit-learn**: Machine learning dan regresi
-   **Pingouin**: Analisis varian Welch
-   **gdown**: Download file dari Google Drive

## 📁 Struktur Proyek

```
FDS-Salaray-Survey-2021/
│
├── README.md
├── EDA_salary.ipynb                          # Notebook EDA alternatif
└── UTS_FDS_Kelompok 1_salaray_survey_2021.ipynb  # Notebook utama (lengkap)
```

## 🚀 Cara Menggunakan

### 1. Clone Repository

```bash
git clone https://github.com/rai-pramana/FDS-Salaray-Survey-2021.git
cd FDS-Salaray-Survey-2021
```

### 2. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scipy statsmodels scikit-learn pingouin gdown openpyxl
```

### 3. Jalankan Notebook

Buka salah satu notebook menggunakan Jupyter Notebook atau Google Colab:

-   `UTS_FDS_Kelompok 1_salaray_survey_2021.ipynb` - Analisis lengkap dengan pembersihan data detail
-   `EDA_salary.ipynb` - Analisis EDA yang lebih ringkas

## 📖 Alur Kerja Analisis

### 1. **Pengumpulan Data**

-   Download dataset dari Google Drive menggunakan `gdown`
-   Load data menggunakan Pandas

### 2. **Pembersihan Data (Data Cleaning)**

Proses pembersihan data yang ekstensif meliputi:

-   Menghapus kolom yang tidak diperlukan
-   Menangani nilai kosong (null values)
-   Mengganti nama kolom untuk kemudahan
-   Membersihkan data kategorikal (industry, job_title, country, dll)
-   Menstandarisasi mata uang menjadi USD
-   Menghapus outliers menggunakan metode IQR

### 3. **Transformasi Data**

-   Mengonversi rentang usia kategorikal menjadi numerik
-   Mengonversi pengalaman kerja kategorikal menjadi numerik
-   Encoding tingkat pendidikan
-   Menghitung total penghasilan (gaji tahunan + kompensasi)
-   Konversi semua mata uang ke USD

### 4. **Analisis Deskriptif (Univariat)**

Analisis distribusi untuk setiap variabel:

-   Rentang usia
-   Industri
-   Jabatan pekerjaan
-   Mata uang
-   Negara dan kota
-   Pengalaman kerja
-   Tingkat pendidikan
-   Jenis kelamin
-   Ras

### 5. **Analisis Bivariat & Multivariat**

-   Analisis hubungan antar variabel
-   Korelasi antara variabel numerik
-   Uji statistik (t-test, ANOVA, Chi-square)

### 6. **Pemodelan & Prediksi**

-   Regresi linear untuk prediksi gaji
-   Evaluasi model menggunakan MSE, MAE, dan R²

## 📈 Temuan Utama

### Distribusi Data

-   **Rentang usia terpopuler**: 25-34 tahun (11.817 responden)
-   **Industri terpopuler**: Computing or Tech (3.873 responden)
-   **Jabatan terpopuler**: Software Engineer (331 responden)
-   **Negara terpopuler**: United States (21.243 responden)
-   **Kota terpopuler**: Boston (761 responden)
-   **Tingkat pendidikan terpopuler**: College Degree (12.613 responden)
-   **Jenis kelamin terpopuler**: Woman (20.103 responden)

### Insight Gaji

-   **Industri dengan gaji tertinggi**: Law & Legal
-   **Industri dengan gaji terendah**: Education
-   **Pengalaman kerja**: Semakin tinggi pengalaman kerja, semakin tinggi rata-rata gaji
-   **Jenis kelamin**: Terdapat perbedaan gaji antara pria dan wanita
-   **Pendidikan**: Tingkat pendidikan yang lebih tinggi berkorelasi dengan gaji yang lebih tinggi

## 📊 Visualisasi

Proyek ini menghasilkan berbagai visualisasi, termasuk:

-   Histogram untuk distribusi data
-   Boxplot untuk mengidentifikasi outliers
-   Bar plot untuk perbandingan kategorikal
-   Scatter plot untuk hubungan antar variabel
-   Heatmap untuk korelasi

## 🧹 Pembersihan Data Detail

### Handling Missing Values

-   Industry: 72 nilai kosong → dihapus
-   City: 79 nilai kosong → dihapus
-   Education: 214 nilai kosong → dihapus
-   Gender: 167 nilai kosong → dihapus
-   Race: 169 nilai kosong → dihapus
-   Monetary Compensation: 7256 nilai kosong → diisi dengan 0

### Outlier Treatment

-   Menggunakan metode IQR (Interquartile Range)
-   Menghitung batas bawah dan batas atas
-   Menghapus data di luar batas yang ditentukan

### Standardisasi

-   34 mata uang berbeda distandarisasi
-   97 negara berbeda dibersihkan dan distandarisasi
-   Konversi semua gaji ke USD menggunakan exchange rate

## 📝 Metodologi Statistik

-   **Analisis Deskriptif**: Mean, median, standar deviasi, kuartil
-   **Uji Hipotesis**: T-test, ANOVA, Chi-square
-   **Regresi**: Linear regression untuk prediksi
-   **Evaluasi Model**: MSE, MAE, R²

## 🤝 Kontribusi

Proyek ini merupakan bagian dari tugas akademik. Untuk kontribusi atau pertanyaan, silakan hubungi anggota kelompok melalui repository GitHub.

## 📄 Lisensi

Proyek ini dibuat untuk keperluan akademik dalam mata kuliah Foundation of Data Science.

## 🔗 Link Penting

-   **Repository**: [GitHub - FDS-Salaray-Survey-2021](https://github.com/rai-pramana/FDS-Salaray-Survey-2021)

---

**Catatan**: Dataset asli berisi 27.946 responden. Setelah pembersihan data dan penghapusan outliers, dataset final berisi 25.716 entri yang valid untuk analisis.
