# Dataset

Data transaksi kartu kredit untuk kebutuhan EDA dan model klasifikasi fraud.

- **File:** `data/fraud_train.txt` (berformat CSV, ~1,7 MB)
- **Ukuran:** 13.125 baris × 28 kolom (plus 1 baris header)
- **Target:** `flag_transaksi_fraud` (1 = fraud, 0 = normal; proporsi fraud ~6,8%)

## Lokasi file

```text
data/fraud_train.txt
```

Notebook (`notebooks/01-eda-model-klasifikasi-fraud-kartu-kredit.ipynb`) membaca dataset dari lokasi tersebut.

## Catatan

- Semua kolom sudah berupa kode anonim, tidak memuat data pribadi.
