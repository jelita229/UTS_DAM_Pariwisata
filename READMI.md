# Data Acquisition & Management – Pariwisata Bali

## Deskripsi Proyek

Repository ini merupakan dokumentasi pengerjaan Ujian Tengah Semester (UTS) mata kuliah Data Acquisition & Management.

Proyek ini berfokus pada pengumpulan dan pengelolaan data sektor pariwisata di Provinsi Bali. Data yang digunakan berkaitan dengan jumlah wisatawan domestik dan wisatawan mancanegara berdasarkan data statistik Badan Pusat Statistik (BPS) Provinsi Bali.

Tujuan proyek ini adalah menerapkan proses akuisisi data, pemeriksaan kualitas data, pengelolaan metadata, serta dokumentasi sumber data agar data dapat digunakan untuk analisis secara terstruktur dan dapat ditelusuri.

## Sumber Data

Dataset utama diperoleh dari BPS Provinsi Bali:

1. **Wisatawan Domestik Bulanan ke Bali (2004–2025)**  
   Sumber: https://bali.bps.go.id/id/statistics-table/1/MjkjMQ%3D%3D/banyaknya-wisatawan-domestik-bulanan-ke-bali-2004-2025.html

2. **Wisatawan Mancanegara Bulanan ke Bali (1982–2008)**  
   Sumber: https://bali.bps.go.id/id/statistics-table/1/MjEjMQ%3D%3D/banyaknya-wisatawan-mancanegara-bulanan-ke-bali--1982-2008.html

## Metode Pengerjaan

Proses pengerjaan mengikuti lima bagian utama dalam instruksi UTS:

1. **Pembacaan dan identifikasi dataset**  
   Membaca file CSV, mengidentifikasi struktur data, jumlah baris dan kolom, tipe data, cakupan waktu, ukuran file, serta estimasi kebutuhan penyimpanan.

2. **Etika dan kualitas data**  
   Memeriksa ketentuan penggunaan sumber data, mengidentifikasi kemungkinan PII atau quasi-identifier, serta menyusun Data Ethics Checklist.

3. **Akuisisi data melalui API**  
   Mengambil data dari API yang relevan dengan topik pariwisata, menangani respons HTTP, dan melakukan normalisasi data JSON menjadi tabel.

4. **Pemeriksaan robots.txt dan web scraping**  
   Memeriksa aturan robots.txt sebelum mengambil data dari halaman web statis yang diizinkan.

5. **Penggabungan dan penyimpanan data**  
   Menggabungkan minimal dua sumber data menggunakan merge, melakukan validasi, memeriksa duplikasi, dan menyimpan hasil pengolahan beserta metadata.

## Struktur Repository

```text
project_data_aquisisi/
│
├── README.md
│
├── notebook/
│   └── analisis_akuisisi_data.ipynb
│
├── data/
│   ├── raw/
│   │   └── file_bps/
│   │       ├── Banyaknya Wisatawan Domestik Bulanan ke Bali, 2004-2025.csv
│   │       └── Banyaknya Wisatawan Mancanegara Bulanan ke Bali, 1982-2008.csv
│   │
│   └── processed/
│       └── (hasil pengolahan dan penggabungan data)
│
├── metadata/
│   └── (catatan provenance dan Data Ethics Checklist)
│
└── evidence/
    └── (bukti pemeriksaan sumber dan robots.txt)
```

*Struktur folder dapat disesuaikan dengan nama file dan folder yang benar-benar terdapat di repository.*

## Tools dan Library

- Python
- Google Colab
- Pandas
- Requests
- BeautifulSoup
- Matplotlib
- GitHub

## Dokumentasi dan Reproducibility

Seluruh proses pengumpulan dan pengolahan data didokumentasikan dalam notebook Jupyter (`.ipynb`). Notebook memuat tahapan pembacaan dataset, pemeriksaan data, pencatatan metadata, akuisisi data, dan pengolahan sesuai instruksi UTS.

Untuk mereproduksi proses pengerjaan, pengguna dapat membuka notebook melalui Google Colab atau mengunduh file `.ipynb`, menyiapkan library yang dibutuhkan, memastikan koneksi internet tersedia untuk proses akuisisi, kemudian menjalankan seluruh sel dari bagian awal hingga akhir secara berurutan.

## Catatan

- Sumber data utama berasal dari BPS Provinsi Bali.
- Setiap sumber data perlu disertai URL, tanggal akses, informasi lisensi atau ketentuan penggunaan, dan hash MD5.
- Data mentah disimpan terpisah dari data hasil pengolahan.
- Hasil akhir dan kelengkapan setiap tahapan harus diverifikasi melalui output notebook sebelum dinyatakan selesai.
