# 📊 Analisa Hubungan Penjualan dan Keuntungan Perusahaan

## 📌 Overview Project
Project ini bertujuan untuk menganalisis hubungan antara nilai penjualan (Sales) dan keuntungan (Profit) perusahaan, serta mencari faktor lain yang memengaruhinya.

Analisis dilakukan menggunakan **Amazon dataset** yang berisi data transaksi periode 2011–2014, seperti tanggal pemesanan, lokasi pengiriman, kategori produk, nilai penjualan, kuantitas, dan keuntungan.

Melalui analisis ini diharapkan dapat diperoleh insight yang membantu perusahaan memahami sumber keuntungan, mengelola modal dengan lebih efisien, serta mengenali jenis barang yang berpotensi memberikan keuntungan maupun kerugian.

## ❗ Problem Statement
Industri ritel seperti Azko dan Neka mengalami pertumbuhan kinerja penjualan di tahun 2026. Peningkatan penjualan juga didukung oleh meningkatnya daya beli masyarakat yang lebih baik dari tahun sebelumnya.

> Sumber: Bisnis.com – *Pengelola Azko dan Neka (ACES) Kejar Target Penjualan hingga 8% Semester II/2026* (11 September 2026)

Dengan menganalisis data transaksi, kita dapat memahami apakah pertumbuhan penjualan benar-benar diikuti oleh pertumbuhan keuntungan. Insight dari analisis ini dapat membantu:

- Manajemen dalam menentukan batas modal yang efisien untuk setiap transaksi
- Tim produk dalam mengenali kategori barang yang menguntungkan dan yang merugi
- Tim sales dalam menentukan lokasi transaksi yang paling potensial

## ❓ Business Question
Beberapa pertanyaan yang ingin dijawab dalam analisis ini antara lain:

1. Apakah terdapat hubungan antara penjualan dan keuntungan perusahaan?
2. Faktor lain apa yang dapat memengaruhi penjualan dan keuntungan perusahaan?
3. Jenis barang apa yang berpotensi memberikan keuntungan dan kerugian bagi perusahaan?

## 📊 Dataset
- **Nama file:** `Amazon.xlsx`
- **Sumber:** [Google Drive](https://drive.google.com/drive/folders/1AWksosjsTfN-Y7sukK3GzkImtAqSpf_8)
- **Format:** Excel
- **Jumlah baris:** 3.203
- **Jumlah kolom:** 10

| Kolom | Deskripsi |
|---|---|
| Order ID | Kode unik untuk setiap transaksi |
| Order Date | Tanggal pelanggan melakukan pemesanan |
| Ship Date | Tanggal pesanan mulai dikirimkan |
| EmailID | Alamat email pelanggan |
| Geography | Lokasi pengiriman (negara, kota, negara bagian) |
| Category | Kategori produk yang dibeli |
| Product Name | Nama dan deskripsi detail produk |
| Sales | Total nilai penjualan produk |
| Quantity | Jumlah barang yang dibeli |
| Profit | Nilai keuntungan bersih dari penjualan produk |

## 🧹 Data Preparation
1. **Data Exploration:** tidak ditemukan inkonsistensi, missing value, maupun duplicate value, dan tipe data seluruh kolom sudah sesuai.
2. **Distribusi:** Sales (rata-rata 226,49, median 60,84), Quantity (rata-rata 3,82, median 3), dan Profit (rata-rata 33,84, median 11,16) cenderung miring ke kanan (skew right), dan tidak ada kolom yang terdistribusi normal.
3. **Outlier:** ditemukan outlier pada kolom Sales, Quantity, dan Profit. Outlier ditangani dengan **capping** (Sales dan Profit) serta **transformasi log** (Quantity).
4. **Feature Engineering:** dibuat kolom `Modal` (Sales dikurangi Profit) untuk mengetahui modal yang dibutuhkan perusahaan pada setiap transaksi.

## 🔍 Insight dari Data

Keuntungan perusahaan menunjukkan **pola naik setiap tahun**, dan terdapat **hubungan positif antara Sales dan Profit** sehingga penjualan yang tinggi cenderung menghasilkan keuntungan yang tinggi. Namun, Sales juga berhubungan kuat dengan **Modal**, sedangkan **hubungan Modal dengan Profit cenderung lemah**, sehingga modal yang besar belum tentu menghasilkan keuntungan yang besar. Dari sisi produk, **Copiers** menjadi kategori dengan keuntungan terbesar, dengan lokasi paling menguntungkan di **United States, Seattle, Washington**, sedangkan kategori **Machines** dan **Bookcases** justru mencatat kerugian. Perlu diingat bahwa data ini berasal dari tahun 2011–2014 sehingga kondisi saat ini mungkin sudah berbeda.

## 💡 Recommendation

Karena modal yang besar belum tentu memberikan keuntungan yang besar, disarankan untuk **menyusun aturan baku mengenai batas maksimal modal** per transaksi serta melakukan **penghematan biaya operasional dan produksi tanpa mengurangi kualitas produk**, agar pertumbuhan keuntungan setiap tahun tetap terjaga. Mengingat data yang digunakan berasal dari tahun 2011–2014, disarankan pula untuk **memvalidasi ulang dengan data terbaru** apakah Copiers dan lokasi Seattle masih menjadi sumber keuntungan terbesar. Terakhir, dapat dipertimbangkan **diskusi lebih lanjut mengenai kategori Machines dan Bookcases**, apakah akan tetap dilanjutkan dengan evaluasi menyeluruh atau dihentikan.

## 📈 Visualisasi (EDA)
Analisis eksplorasi dilakukan menggunakan:

- Line chart untuk tren keuntungan perusahaan per tahun
- Scatter plot untuk hubungan Sales dan Profit
- Heatmap untuk analisis bivariat
- Pairplot untuk analisis multivariat
- Bar chart untuk keuntungan berdasarkan kategori barang
- Crosstab untuk lokasi dengan keuntungan terbesar pada penjualan Copiers
- Filtering untuk kategori barang yang menyebabkan kerugian

## 📊 Presentasi Project
Untuk melihat penjelasan lengkap dari project ini, silakan lihat slide presentasi berikut:

🔗 [Link PPT](#) <!-- ganti dengan link presentasi Anda -->

## 🛠 Tools yang Digunakan
- **Python** (Data Exploration, Data Cleaning, Feature Engineering, dan EDA)
- **Pandas** dan **NumPy** (Pengolahan data)
- **Matplotlib** dan **Seaborn** (Visualisasi)

## 👤 Author
**Ahmad Malik Ibrahim**
Lulusan kedokteran dengan minat pada statistik, analisis, dan matematika, yang sedang menargetkan karir sebagai data analis.
