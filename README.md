# 📊 Prediksi Nasabah yang Berpotensi Membeli Deposito

Proyek ini dikembangkan dalam rangka kompetisi data science dengan tujuan membangun model machine learning untuk memprediksi apakah seorang nasabah akan membeli produk **deposito berjangka**.

---

# 🏦 Business Context

Dalam industri perbankan, efektivitas kampanye pemasaran sangat menentukan profitabilitas. Bank sering melakukan kampanye telemarketing atau outreach untuk menawarkan produk deposito berjangka kepada nasabah.

Namun, tantangan utamanya adalah:

* Tidak semua nasabah tertarik membeli deposito
* Biaya menghubungi nasabah cukup besar (telemarketing, SMS, email campaign)
* Tingkat respons biasanya rendah (data cenderung imbalanced)

Dengan memanfaatkan data historis seperti:

* Informasi demografis
* Riwayat pinjaman
* Hasil kampanye sebelumnya
* Indikator ekonomi makro

Bank dapat membangun model prediktif untuk meningkatkan efisiensi kampanye.

---

# ❗ Business Problem

Tanpa model prediksi:

* Bank menghubungi terlalu banyak nasabah yang tidak tertarik
* Biaya operasional meningkat
* Conversion rate rendah
* Tim marketing tidak bekerja secara optimal

Permasalahan utama:

> Bagaimana mengidentifikasi nasabah yang paling berpotensi membeli deposito agar kampanye menjadi lebih efektif dan efisien?

---

# 🎯 Business Objective

Membangun model klasifikasi yang dapat memprediksi:

* **1** → Nasabah diprediksi akan membeli deposito
* **0** → Nasabah diprediksi tidak akan membeli deposito

Tujuan akhirnya adalah:

* Meningkatkan conversion rate kampanye
* Mengurangi biaya marketing
* Mengoptimalkan alokasi sumber daya tim sales
* Meningkatkan pendapatan bank dari produk deposito

---

# 📈 Business Metrics

Karena dataset bersifat **imbalanced** (jumlah nasabah yang membeli deposito jauh lebih sedikit), maka metrik bisnis difokuskan pada:

### 1️⃣ Precision (untuk kelas 1)

Mengukur seberapa akurat model dalam memprediksi nasabah yang benar-benar membeli deposito.

👉 Penting untuk menghindari pemborosan biaya marketing.

---

### 2️⃣ Recall (untuk kelas 1)

Mengukur seberapa banyak nasabah potensial yang berhasil ditangkap oleh model.

👉 Penting agar tidak kehilangan calon pembeli potensial.

---

### 3️⃣ Conversion Rate Improvement

Membandingkan conversion rate sebelum dan sesudah menggunakan model.

---

### 4️⃣ Cost Efficiency

Mengukur penurunan biaya kontak terhadap nasabah yang tidak relevan.

---

# 🤖 Machine Learning Approach

## Target Variable

`berlangganan_deposito`

* 1 → Berlangganan deposito
* 0 → Tidak berlangganan

## Feature Selection

Beberapa fitur digunakan seperti:

* Demografi (usia, pendidikan, status_perkawinan)
* Riwayat kredit (gagal_bayar_sebelumnya, pinjaman)
* Riwayat kampanye sebelumnya
* Indikator ekonomi makro

---

# 📊 ML Metrics

Awalnya, tuning hyperparameter dilakukan menggunakan **ROC-AUC**.

Namun, karena dataset bersifat imbalanced, penggunaan ROC-AUC kurang optimal.

## ❌ Kelemahan ROC-AUC pada Imbalanced Data

ROC-AUC tetap terlihat tinggi meskipun model kurang baik dalam mendeteksi kelas minoritas.

---

## ✅ Metric yang Lebih Tepat: PR-AUC

**Precision-Recall AUC (PR-AUC)** lebih sesuai karena:

* Fokus pada performa kelas positif (nasabah yang membeli deposito)
* Lebih sensitif terhadap kesalahan pada kelas minoritas
* Lebih relevan dengan kebutuhan bisnis

---

# 🔧 Modeling Strategy

* Data preprocessing
* Encoding categorical variables
* Hyperparameter tuning
* Evaluasi model menggunakan:

  * PR-AUC (utama)
  * Precision
  * Recall
  * F1-Score

---

# 📌 Insight & Lesson Learned

Kesalahan utama dalam proyek ini:

> Menggunakan ROC-AUC sebagai metric tuning pada dataset imbalanced.

---

# 🚀 Dampak Bisnis yang Diharapkan

Dengan model ini, bank dapat:

* Mengurangi jumlah nasabah yang dihubungi secara acak
* Meningkatkan efisiensi kampanye
* Meningkatkan probabilitas closing
* Mengoptimalkan biaya operasional marketing

---

# 🧠 Kesimpulan

Proyek ini menunjukkan bahwa:

* Machine learning bukan hanya soal akurasi tinggi
* Pemilihan metric harus selaras dengan kondisi data dan tujuan bisnis
* Pada kasus imbalanced classification, PR-AUC jauh lebih relevan dibanding ROC-AUC
