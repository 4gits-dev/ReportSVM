# ReportSVM
# Analisis Sentimen dengan SVM

Proyek ini menerapkan **Support Vector Machine (SVM)** untuk melakukan analisis sentimen terhadap ulasan film atau produk. Tujuannya adalah untuk mengklasifikasikan setiap ulasan ke dalam kategori **positif** atau **negatif**.

---

## 📂 Dataset

- Dataset berasal dari: [Kaggle UMICH SI650](https://www.kaggle.com/c/si650winter11/data)
- Format data: **TSV (Tab-Separated Values)**
- Setiap baris terdiri dari:
  - **Label**: `1` untuk sentimen positif, `0` untuk negatif
  - **Teks**: isi ulasan

> Contoh:
```tsv
1   Saya sangat menyukai Da Vinci Code.
0   Film ini membosankan dan terlalu panjang.



