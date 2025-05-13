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

## Alur Proses
Import Library
Menggunakan pustaka berikut:

scikit-learn, TextBlob, nltk, pandas, matplotlib, seaborn

Pra-pemrosesan Data

Tokenisasi

Menghapus stopwords

Vektorisasi dengan TfidfVectorizer

Membagi Data

python
Salin
Edit
X_train, X_test, y_train, y_test = train_test_split(df['text'], df['liked'], test_size=0.2)
Modeling dengan SVM

python
Salin
Edit
text_clf = Pipeline([
    ('tfidf', TfidfVectorizer()),
    ('clf', SVC(kernel='linear')),
])
text_clf.fit(X_train, y_train)
Evaluasi Model

python
Salin
Edit
from sklearn.metrics import classification_report
print(classification_report(y_test, text_clf.predict(X_test)))
⚠️ Masalah dan Keterbatasan
Dataset saat ini hanya berisi ulasan positif (label = 1)

Tanpa contoh negatif, model tidak dapat belajar membedakan dua kelas

Model bisa tampak akurasi tinggi, tetapi gagal dalam klasifikasi nyata

✅ Rekomendasi
Tambahkan data dengan label 0 untuk melatih model klasifikasi biner

Gunakan cross-validation untuk evaluasi yang lebih menyeluruh

Tambahkan visualisasi:

Distribusi sentimen

Confusion matrix

Word cloud

📊 Visualisasi yang Disarankan
Distribusi Sentimen

Kurva Pembelajaran (Learning Curve)

Kurva ROC

Word Cloud per sentimen

> Contoh:
```tsv
1   Saya sangat menyukai Da Vinci Code.
0   Film ini membosankan dan terlalu panjang.



