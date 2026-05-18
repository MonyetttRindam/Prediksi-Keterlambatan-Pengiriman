# 📦 Shipping Delivery Time Prediction

Machine learning project to predict whether a shipment will arrive on time or be delayed using customer transaction and logistics data.

---

## 👨‍💻 Author

**Muhammad Abil Khoiri**
Computer Engineering Student | AI & Data Science Enthusiast

---

# 📌 Project Overview

This project aims to build a classification model for predicting shipping delivery timeliness based on customer transactions and logistics information. The workflow includes:

* Exploratory Data Analysis (EDA)
* Data Preprocessing
* Feature Engineering
* Feature Selection
* Model Training & Evaluation
* Kaggle Submission

---

# 📂 Dataset Features

The dataset contains several logistics and transaction-related features:

| Feature                       | Description                      |
| ----------------------------- | -------------------------------- |
| `blok_gudang`                 | Warehouse block location         |
| `mode_pengiriman`             | Shipping method used             |
| `panggilan_layanan_pelanggan` | Number of customer service calls |
| `rating_pelanggan`            | Customer rating                  |
| `harga_produk`                | Product price                    |
| `pembelian_sebelumnya`        | Previous purchases               |
| `kepentingan_produk`          | Product importance               |
| `jenis_kelamin`               | Customer gender                  |
| `diskon_ditawarkan`           | Discount offered                 |
| `berat_dalam_gram`            | Product weight in grams          |

### 🎯 Target Variable

| Value | Meaning |
| ----- | ------- |
| `0`   | Delayed |
| `1`   | On Time |

---

# ⚙️ Project Workflow

## 1️⃣ Exploratory Data Analysis (EDA)

Performed data exploration to analyze:

* Feature distributions
* Correlation matrix
* Missing values
* Outliers
* Data skewness

### 📊 Key Insights

* `diskon_ditawarkan` showed moderate positive correlation with delivery timeliness.
* `berat_dalam_gram` showed moderate negative correlation.
* Features such as `jenis_kelamin` and `blok_gudang` had minimal contribution.

---

## 2️⃣ Data Preprocessing

### 🔤 Encoding

Applied **Label Encoding** for categorical features:

* `blok_gudang`
* `mode_pengiriman`
* `kepentingan_produk`
* `jenis_kelamin`

### 🩹 Handling Missing Values

* Median imputation for numerical features
* Mode imputation for categorical features

### 📉 Outlier Handling

Applied:

* `log1p transformation`
* `IQR-based capping`

### 📏 Feature Scaling

Used:

* `StandardScaler`

---

# 🛠️ Feature Engineering

Created several engineered features to improve model performance.

| Feature                     | Description                        |
| --------------------------- | ---------------------------------- |
| `harga_setelah_diskon`      | Final product price after discount |
| `berat_per_diskon`          | Weight-to-discount ratio           |
| `produk_ringan`             | Lightweight product indicator      |
| `diskon_tinggi`             | High discount indicator            |
| `skor_pelanggan`            | Customer satisfaction score        |
| `high_value_order`          | High-value order indicator         |
| `is_frequent_buyer`         | Loyal customer indicator           |
| `produk_penting_dan_ringan` | Important & lightweight product    |
| `customer_loyalty`          | Customer loyalty score             |

---

# 🤖 Models Used

The following machine learning models were evaluated:

* Logistic Regression
* Random Forest
* XGBoost
* Gradient Boosting

---

# 📊 Model Performance

## 🥇 Best Model: Gradient Boosting

| Metric    | Score  |
| --------- | ------ |
| Accuracy  | 66.78% |
| Precision | 70.11% |
| Recall    | 90.09% |
| F1-Score  | 78.85% |
| AUC Score | 72.71% |

### ✅ Why Gradient Boosting?

Gradient Boosting achieved:

* Highest Recall
* Best F1-Score
* Highest AUC Score
* Better capability in capturing complex logistics patterns

---

# 🏆 Kaggle Submission

The final Gradient Boosting model achieved a strong Kaggle submission score using the **sMAPE** evaluation metric.

---

# 💻 Tech Stack

* Python
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* Matplotlib
* Seaborn

---

# 📈 Key Takeaways

* Feature engineering significantly improved model performance.
* Gradient Boosting outperformed other baseline models.
* Proper preprocessing and outlier handling improved model stability.

---

# 🚀 Future Improvements

* Hyperparameter tuning
* Ensemble learning
* Cross-validation optimization
* Model deployment with Streamlit
* Advanced feature importance analysis

---

# 📬 Contact

* GitHub: https://github.com/yourusername
* LinkedIn: https://linkedin.com/in/yourusername
