# 🎯 Sentiment Analysis — Komentar TikTok Koperasi Desa Merah Putih (KDMP)

Proyek analisis sentimen terhadap komentar TikTok terkait program **Koperasi Desa Merah Putih (KDMP)** menggunakan model IndoBERT.

---

## 📊 Hasil

| Sentimen | Jumlah | Persentase |
|----------|--------|------------|
| Negatif  | 5.619  | 56.2%      |
| Positif  | 2.195  | 22.0%      |
| Netral   | 2.186  | 21.9%      |

> Analisis dilakukan pada sample 10.000 komentar dari total 440.000+ komentar dataset TikTok KDMP.

---

## 🛠️ Tech Stack

- **Python 3**
- **IndoBERT** — `mdhugol/indonesia-bert-sentiment-classification`
- **Transformers** (HuggingFace)
- **Pandas, NumPy**
- **Matplotlib, Seaborn, WordCloud**
- **Sastrawi** — stemmer & stopword Bahasa Indonesia
- **Kagglehub** — auto-download dataset

---

## 📁 Struktur Project

```
├── sentiment_analysis_kdmp.ipynb   # Notebook utama
├── requirements.txt                # Library yang dibutuhkan
├── hasil_sentimen_kdmp.csv         # Output hasil prediksi (sample 10k)
├── images/
│   ├── sentiment_distribution.png  # Bar chart & pie chart
│   ├── wordcloud_sentiment.png      # Word cloud per sentimen
│   └── confidence_distribution.png # Distribusi confidence score
└── README.md
```

---

## 🚀 Cara Menjalankan

### 1. Buka di Google Colab
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

### 2. Setup Kaggle API
- Buka [kaggle.com](https://kaggle.com) → Settings → API → **Create New Token**
- Masukkan `username` dan `key` di cell pertama notebook

### 3. Jalankan semua cell
```
Runtime → Run all
```
Dataset akan otomatis ter-download via `kagglehub`.

---

## 📦 Dataset

- **Sumber:** [sinryurifal/dataset-komentar-tiktok-koperasi-desa-merah-putih](https://www.kaggle.com/datasets/sinryurifal/dataset-komentar-tiktok-koperasi-desa-merah-putih)
- **Total data:** 440.102 komentar
- **Platform:** TikTok
- **Topik:** Koperasi Desa Merah Putih (KDMP)

---

## 🔄 Alur Analisis

```
Download Dataset (Kaggle)
        ↓
Preprocessing Teks
(lowercase, hapus mention/hashtag/URL, stopword removal)
        ↓
Prediksi Sentimen (IndoBERT)
        ↓
Visualisasi & Ekspor CSV
```

---

## 📌 Catatan

- Gunakan **GPU (T4)** di Google Colab untuk hasil lebih cepat
- Untuk full dataset 421k, hapus cell sampling dan estimasi waktu ~1-2 jam
- Model: `mdhugol/indonesia-bert-sentiment-classification` (3 label: Positif, Netral, Negatif)

---

## 👤 Author

**Maulana Hasyim**  
[LinkedIn](https://linkedin.com/in/) · [Kaggle](https://kaggle.com/sinryurifal)
