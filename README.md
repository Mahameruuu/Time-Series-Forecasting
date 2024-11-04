# Demand Forecasting using Prophet

## 📋 Project Overview
Proyek ini menggunakan model **Prophet** untuk melakukan prediksi permintaan (`TOTALDEMAND`) berdasarkan data time series. Model ini cocok untuk menangkap pola musiman, tren jangka panjang, serta memperkirakan fluktuasi permintaan dalam data historis. Proyek ini diharapkan dapat membantu dalam pengambilan keputusan berdasarkan perkiraan permintaan masa depan.

## 🗂 Dataset
Dataset yang digunakan berisi beberapa kolom penting:
- `REGION`: Wilayah data permintaan.
- `SETTLEMENTDATE`: Tanggal dan waktu data permintaan tercatat.
- `TOTALDEMAND`: Jumlah total permintaan yang ingin diprediksi.
- `RRP`: Harga per unit energi (bisa digunakan sebagai analisis tambahan).
- `PERIODTYPE`: Jenis periode waktu (misalnya, harian atau jam).

> **Catatan**: Pastikan dataset sudah diatur dengan format kolom yang benar, dan simpan dalam file bernama `dataset.csv` di direktori utama proyek.

## 📊 Analysis & Modeling Steps
Langkah-langkah analisis dan modeling yang dilakukan dalam proyek ini:
1. **Data Preprocessing**:
   - Memuat dataset dan melakukan konversi kolom tanggal (`SETTLEMENTDATE`) ke format datetime.
   - Mengganti nama kolom untuk disesuaikan dengan format input Prophet (yaitu `ds` untuk tanggal dan `y` untuk target).

2. **Exploratory Data Analysis (EDA)**:
   - Visualisasi data awal untuk memeriksa pola atau tren pada data permintaan.

3. **Modeling dengan Prophet**:
   - Inisialisasi dan pelatihan model Prophet dengan data yang telah disiapkan.
   - Membuat prediksi untuk 30 hari ke depan.

4. **Evaluation & Visualization**:
   - Visualisasi hasil prediksi dan analisis tren menggunakan fungsi bawaan Prophet.
   - Menyimpan hasil prediksi ke dalam file CSV untuk analisis lebih lanjut.

## 🚀 Getting Started

### Prerequisites
Instal library yang diperlukan sebelum menjalankan proyek:
```bash
pip install pandas matplotlib prophet
