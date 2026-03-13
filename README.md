# 🏠Home-Electricity-Bill Forecasting
===

Proyek sederhana untuk memprediksi tagihan listrik bulanan menggunakan arsitektur ANN (Artificial Neural Network) dengan layer LSTM. Proyek ini mencakup pengolahan data kategori dengan One-Hot Encoding dan normalisasi data numerik.
---

## 📊Dataset
Data terdiri dari 20 bulan (campuran data asli dan dummy) dengan kolom: <br>
    - ID: tagihan
    - Month: Nama bulan (Januari - Desember).
    - Days: Jumlah hari dalam bulan tersebut.
    - Cost: Biaya tagihan listrik (Target).
---

## 🛠️Tech Stack
    - Python
    - TensorFlow/Keras (Model ANN & LSTM)
    - Scikit-Learn (OneHotEncoder & MinMaxScaler)
    - Pandas/Numpy (Data Manipulation)
    - Joblib (Object Serialization)
---

## 🔮Cara Melakukan Prediksi (Inference)

Untuk memprediksi bulan baru, jalankan prosedur berikut: <br>

    1. Load model .h5, encoder, dan scaler.
    2. Masukkan nama bulan dan jumlah hari.
    3. Transformasikan input menggunakan encoder yang di-load.
    4. Lakukan model.predict().
    5. Balikkan nilai prediksi ke satuan Rupiah menggunakan scaler.inverse_transform().