Prediksi Ketepatan Waktu Pengiriman 📦

Proyek machine learning untuk memprediksi apakah suatu pengiriman akan sampai tepat waktu atau terlambat berdasarkan data transaksi pelanggan dan logistik. Dataset berasal dari kompetisi berbasis file train.csv dan test.csv.

👨‍💻 Author

Muhammad Abil Khoiri
Mahasiswa Teknik Komputer – Fokus pada AI & Data Science

📌 Project Overview

Proyek ini bertujuan membangun model klasifikasi untuk memprediksi ketepatan waktu pengiriman menggunakan berbagai fitur transaksi dan logistik pelanggan. Beberapa tahapan utama yang dilakukan meliputi:

Exploratory Data Analysis (EDA)
Data Preprocessing
Feature Engineering
Feature Selection
Model Training & Evaluation
Kaggle Submission
📂 Dataset Features

Dataset terdiri dari berbagai fitur seperti:

blok_gudang
mode_pengiriman
panggilan_layanan_pelanggan
rating_pelanggan
harga_produk
pembelian_sebelumnya
kepentingan_produk
jenis_kelamin
diskon_ditawarkan
berat_dalam_gram
🎯 Target
pengiriman_tepat_waktu
0 = Terlambat
1 = Tepat Waktu
⚙️ Workflow Project
1️⃣ Exploratory Data Analysis (EDA)

Dilakukan analisis distribusi data, korelasi antar fitur, dan identifikasi pola penting.

Insight Penting
diskon_ditawarkan memiliki korelasi positif terhadap target.
berat_dalam_gram memiliki korelasi negatif sedang terhadap target.
Beberapa fitur seperti jenis_kelamin dan blok_gudang tidak memiliki korelasi signifikan.
2️⃣ Data Preprocessing
🔤 Encoding

Menggunakan Label Encoding pada fitur kategorikal:

blok_gudang
mode_pengiriman
kepentingan_produk
jenis_kelamin
🩹 Handling Missing Values
Median Imputation → fitur numerik
Mode Imputation → fitur kategorikal
📉 Outlier Handling

Menggunakan:

log1p transformation
IQR-based capping
📏 Feature Scaling

Menggunakan:

StandardScaler
3️⃣ Feature Engineering

Beberapa fitur baru yang dibuat:

Feature	Deskripsi
harga_setelah_diskon	Harga akhir setelah diskon
berat_per_diskon	Rasio berat produk terhadap diskon
produk_ringan	Produk dengan berat < 1000 gram
diskon_tinggi	Diskon lebih dari 50%
skor_pelanggan	Rating - customer service calls
high_value_order	Order bernilai tinggi dan penting
is_frequent_buyer	Pelanggan loyal
produk_penting_dan_ringan	Kombinasi produk penting & ringan
customer_loyalty	Skor loyalitas pelanggan
🤖 Models Used

Beberapa model machine learning yang diuji:

Logistic Regression
Random Forest
XGBoost
Gradient Boosting
📊 Model Evaluation
🔹 Gradient Boosting (Best Model)
Metric	Score
Accuracy	66.78%
Precision	70.11%
Recall	90.09%
F1-Score	78.85%
AUC	72.71%
📌 Why Gradient Boosting?

Gradient Boosting memberikan performa terbaik secara keseluruhan dengan:

Recall tertinggi
F1-score terbaik
AUC tertinggi
Stabil dalam menangani pola kompleks pada data logistik
🏆 Kaggle Submission

Model Gradient Boosting menghasilkan performa submission yang sangat baik pada kompetisi Kaggle menggunakan metric sMAPE.

🛠️ Tech Stack
Python
Pandas
NumPy
Scikit-learn
XGBoost
Matplotlib
Seaborn
📈 Key Takeaways
Feature engineering memberikan kontribusi besar terhadap peningkatan performa model.
Gradient Boosting lebih efektif dibanding Logistic Regression dan Random Forest pada dataset ini.
Handling outlier dan preprocessing yang konsisten membantu meningkatkan stabilitas model.
🚀 Future Improvements
Hyperparameter tuning
Ensemble learning
Cross-validation optimization
Feature importance analysis
Deployment menggunakan Streamlit atau Flask
