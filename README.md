# 🏠 Analisis & Prediksi Harga Rumah Jakarta Selatan — Jaksel vs Tebet

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/USERNAME/REPO_NAME/blob/main/Portofolio_Analisis_Harga_Rumah_Jaksel_Tebet.ipynb)

> Ganti `USERNAME/REPO_NAME` di badge atas dengan username & nama repo GitHub kamu supaya tombol "Open in Colab" langsung berfungsi.

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
├── data/
│   ├── DATA_RUMAH.xlsx                # Data rumah Tebet (±1000 baris, ada judul listing)
│   └── HARGA_RUMAH_JAKSEL.xlsx        # Data rumah Jaksel umum (±1000 baris)
├── requirements.txt
└── README.md
```

## 🚀 Cara Menjalankan

### Opsi 1 — Google Colab (paling mudah)
Klik badge **"Open in Colab"** di atas. Notebook otomatis mendeteksi Colab dan meminta upload 2 file Excel jika belum ada di sesi — bisa juga clone repo ini langsung di Colab lewat cell:
```python
!git clone https://github.com/USERNAME/REPO_NAME.git
%cd REPO_NAME/data
```
lalu sesuaikan path load data di notebook ke folder `data/`.

### Opsi 2 — Lokal
```bash
git clone https://github.com/USERNAME/REPO_NAME.git
cd REPO_NAME
pip install -r requirements.txt
jupyter notebook Portofolio_Analisis_Harga_Rumah_Jaksel_Tebet.ipynb
```

## 📊 Ringkasan Temuan

- Luas bangunan & luas tanah adalah prediktor harga paling dominan.
- Fitur hasil text mining dari judul listing **terbukti meningkatkan akurasi model** dibanding model yang hanya memakai fitur struktural (lihat bagian *Ablation Study* di notebook).
- Segmentasi K-Means menghasilkan 3 klaster alami: Ekonomis, Menengah, Premium.
- Model terbaik (Gradient Boosting/Random Forest) mencapai performa yang solid untuk estimasi harga awal.

Detail lengkap, visualisasi, dan interpretasi ada di dalam notebook.

## 📄 Sumber Data

Dataset "Harga Rumah" (Jaksel & Tebet), dikumpulkan dari rumah123.com.

## 📬 Kontak

Tertarik diskusi lebih lanjut soal analisis ini atau proyek data lainnya? Jangan ragu untuk menghubungi saya!
