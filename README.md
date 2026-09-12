# Deteksi Fraud Kartu Kredit — EDA & Klasifikasi

Tugas Data Mining: eksplorasi data transaksi kartu kredit dan pembangunan model machine learning untuk mendeteksi transaksi penipuan.

- **Stack:** Python 3.11, Jupyter, pandas, scikit-learn, imbalanced-learn (SMOTE), XGBoost
- **Hasil utama:** XGBoost mencapai akurasi validasi ~96,8%, terbaik dari 4 model yang diuji

## Anggota — Kelompok 3

| Nama | NIM |
|---|---|
| Boy Aditya Rohmaulana | 2203488 |
| Defrizal Yahdiyan Risyad | 2206131 |
| Muhamad Furqon Al-Haqqi | 2207207 |
| Raya Cahya Nurani | 2205714 |
| Septiani Eka Putri | 2206000 |


## Dataset

13.125 baris × 28 kolom. Target `flag_transaksi_fraud` (1 = fraud, 0 = normal) dengan proporsi fraud ~6,8%.

File dataset `fraud_train.txt` tidak disertakan di repo. Lihat `data/README.md` untuk penempatan file.

## Cara menjalankan

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt

# taruh dataset di data/fraud_train.txt, lalu:
jupyter notebook notebooks/01-eda-model-klasifikasi-fraud-kartu-kredit.ipynb
```

## Isi notebook

1. **Data understanding** — dimensi data, sampel, tipe data, statistik deskriptif, dan kamus 28 fitur.
2. **Data preparation** — seleksi kolom, penanganan duplikat dan missing value, serta konversi tipe kategori.
3. **Analysis** — distribusi target, analisis univariat, bivariat dengan penanganan outlier (IQR), serta analisis multivariat.
4. **Modelling** — encoding, penanganan imbalance dengan SMOTE, split data 80/20, lalu perbandingan Naive Bayes, Decision Tree, Random Forest, dan XGBoost beserta confusion matrix dan feature importance.

## Hasil model

| Model | Akurasi validasi |
|---|---|
| Naive Bayes | ~67,15% |
| Decision Tree | ~93,74% |
| Random Forest (`max_depth=10`, `n_estimators=50`) | ~92,11% |
| **XGBoost (`n_estimators=50`, `max_depth=7`)** | **~96,80%** |
