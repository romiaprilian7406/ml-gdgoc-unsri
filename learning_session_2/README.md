## Alur Kerja Preprocessing

Proses yang dilakukan di dalam notebook mencakup:

1. **Memuat Data:** Membaca file CSV langsung dari URL.
2. **Eksplorasi Data Awal (EDA):** Mengecek struktur, tipe data, dan nilai kosong.
3. **Pembersihan Data:** Menghapus kolom yang tidak relevan (`PassengerId`, `Name`, `Ticket`, `Cabin`).
4. **Imputasi Nilai Kosong (Missing Values):** Mengisi nilai kosong pada kolom `Age` dengan nilai median, dan menghapus baris kosong pada `Embarked`.
5. **Encoding Data Kategorikal:** Menggunakan One-Hot Encoding (`pd.get_dummies`) dengan parameter `drop_first=True` untuk menghindari *Dummy Variable Trap*.
6. **Feature Scaling:** Menerapkan `MinMaxScaler` dan `StandardScaler` pada kolom numerik (`Age` dan `Fare`).