# Marketing ADs Performance Analytics & Growth Dashboard

## Ringkasan
Membangun 1 dasbor Tableau interaktif untuk menganalisis efektivitas kampanye iklan digital (*Marketing ADs*), optimasi *funnel* konversi, dan efisiensi biaya akuisisi (*Customer Acquisition Cost* / CAC). Proyek ini memberikan rekomendasi strategis mengenai alokasi anggaran iklan, optimasi kanal organik, dan penanganan kebocoran *funnel* dari tayangan iklan hingga pembelian.

## Problem Statement
Efektivitas iklan Meta Ads dan kanal berbayar (*Paid Ads*) menghadapi tantangan efisiensi tingginya biaya akuisisi ($214.684,45 CAC) serta sensitivitas minat beli pengguna. Selain itu, terjadi penurunan *funnel* yang drastis dari 442.700 tayangan iklan menjadi hanya 150 transaksi pembelian akhir. Perusahaan juga menghadapi penurunan retensi pelanggan dari bulan ke bulan, sehingga diperlukan evaluasi strategi iklan, perbaikan UX/UI *checkout*, dan penguatan kanal organik ber-CAC $0.

## Data Exploration
- **Sumber:** Dataset `data_marketing_growth_analytics.csv`
- **Ukuran:** 800 baris × 15 kolom
- **Periode & Perangkat:** Kunjungan Januari–Maret (Mobile, Desktop, Tablet)
- **Kanal Utama:** Paid Ads, Social Media, Organic Search, Email, Referral
- **Kolom Utama:** `user_id`, `first_visit_date`, `channel`, `source`, `device`, `sessions`, `page_views`, `impressions`, `clicks`, `add_to_cart`, `purchase`, `revenue`, `ad_cost`, `retention_month`

## Cleaning & Preparation Data
- **Missing Value**: 0 (Tidak ada missing value)
- **Duplikasi**: 0 (0,00% duplikat)
- **Data Type & Typo**: Mengonversi `first_visit_date` menjadi format DATE; tidak ditemukan data typo
- **Outlier**: Terdeteksi *outlier* pada nilai transaksi/revenue menggunakan pengetesan *Z-Score*, tetapi dipertahankan karena merupakan wajar dari dinamika data penjualan murni

## Visualization Output
- **KPI Utama:** 442.700 Total Tayangan · 19.493 Klik · 8.043 View · 3.305 Kunjungan · 150 Penjualan · $41.003.905,00 Pendapatan Kotor · $10.948.907,00 Biaya Iklan · **3,745 ROAS**
- **Pertumbuhan Keuntungan Real:** Penjualan iklan dalam 3 bulan ini menghasilkan tingkat margin keuntungan nyata sebesar **73,30%** ($30,05J net profit).
- **Perilaku Perangkat (Mobile vs Tablet):** Pengguna **Mobile** mendominasi kunjungan sebesar **62,59%** (5.034 views) dikarenakan kemudahan aksesibilitas seluler, dibandingkan **3,61%** pada Tablet (290 views).
- **Efisiensi Kanal & CAC:** **Paid Ads** menghasilkan pendapatan tertinggi ($13.177.258,00) tetapi satu-satunya kanal dengan biaya akuisisi (**$214.684,45 CAC**). **Social Media** ($10,51J) dan **Organic Search** ($7,97J) menghasilkan omset masif tanpa biaya iklan (**$0 CAC**).
- **Retensi Pelanggan & Dropping:** Pelanggan aktif di bulan ke-1 mencatatkan volume 25 pembelian ($7,00J laba kotor), namun retensi mengalami tren penurunan drastis hingga bulan Maret.

## Conclusion
- Terjadi kebocoran *funnel* konversi yang drastis pada tahap awal (klik) dan tahap akhir (*checkout*).
- Penurunan retensi transaksi pelanggan dari bulan ke bulan berisiko menyebabkan kehilangan pelanggan tetap, yang dipicu oleh kurang menariknya iklan, kendala produk, atau hambatan pada proses alur transaksi.

## Recommendation
- Menyederhanakan alur *checkout*, menyediakan beragam opsi pembayaran, dan mengaktifkan *abandoned cart email reminder* untuk menjaring kembali pengguna yang batal bertransaksi.
- Memprioritaskan optimasi UX/UI pada perangkat **Mobile** dan mengurangi alokasi sumber daya perbaikan bug khusus Tablet yang tidak signifikan.
- Memperkuat strategi *content marketing*, SEO, dan komunitas di kanal **Social Media & Organic Search** untuk memaksimalkan margin keuntungan bersih ($0 CAC).
- Menerapkan fitur *rating & review* paska-pembelian guna mengidentifikasi secara cepat kendala pada iklan, produk, maupun aplikasi/website.

## Tools yang Digunakan
Tableau Public · Python (Pandas, Z-Score EDA) · Calculated Fields · Funnel Analytics · Scatter Plot · Dual Axis Chart

---
*Bagian dari Portofolio Graphic Design & Data Analytics Career Accelerator — Tempat Belajar (2026)*
*Disusun oleh: Raka Dewa Dipa Mahesa Arsandy*
