# 🏠 Analisis & Prediksi Harga Rumah Jakarta Selatan — Jaksel vs Tebet

## 📌 Tentang Proyek

Proyek ini menganalisis dua dataset listing rumah dari kawasan Jakarta Selatan (data umum Jaksel dan data spesifik kecamatan Tebet, dikumpulkan dari rumah123.com) untuk menjawab pertanyaan bisnis:

1. Seberapa besar perbedaan harga antara pasar Jaksel (umum) dan Tebet (spesifik)?
2. Faktor apa yang paling memengaruhi harga rumah?
3. Bisakah **kata-kata di judul listing** ("mewah", "hook", "siap huni", dll) memberi sinyal tambahan terhadap harga? *(text mining — angle unik proyek ini)*
4. Bisakah dibuat model prediksi harga yang cukup akurat?
5. Segmen pasar apa saja yang terbentuk dari data?

## 🧰 Tech Stack

`pandas` `numpy` `matplotlib` `seaborn` `scipy` `scikit-learn` `wordcloud`

**Teknik yang didemonstrasikan:**
- Data Cleaning & Schema Harmonization (menggabungkan 2 dataset dengan skema kolom berbeda)
- Feature Engineering (harga/m², rasio bangunan, segmentasi kuantil)
- **Text Mining** dari judul listing (regex keyword extraction, word cloud, ablation study dampak fitur teks terhadap akurasi model)
- EDA & storytelling visual
- Uji statistik non-parametrik (Mann-Whitney U)
- Unsupervised Learning: segmentasi pasar dengan K-Means + PCA
- Supervised Learning: Linear Regression, Random Forest, Gradient Boosting — dengan evaluasi (MAE, RMSE, R², MAPE) dan feature importance

## 📂 Struktur Repo

```
.
├── Portofolio_Analisis_Harga_Rumah_Jaksel_Tebet.ipynb   # Notebook utama (sudah include output)
├── requirements.txt
└── README.md
```


## 📊 Ringkasan Temuan

- Luas bangunan & luas tanah adalah prediktor harga paling dominan.
- Fitur hasil text mining dari judul listing **terbukti meningkatkan akurasi model** dibanding model yang hanya memakai fitur struktural (lihat bagian *Ablation Study* di notebook).
- Segmentasi K-Means menghasilkan 3 klaster alami: Ekonomis, Menengah, Premium.
- Model terbaik (Gradient Boosting/Random Forest) mencapai performa yang solid untuk estimasi harga awal.

Detail lengkap, visualisasi, dan interpretasi ada di dalam notebook.

## 📄 Sumber Data

(https://www.kaggle.com/datasets/wisnuanggara/daftar-harga-rumah) 
