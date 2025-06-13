## Deteksi Anomali Transaksi dengan Unsupervised Learning##

Pada proyek Capstone Project saya mendapatkan jobdesk untuk mengerjakan Fitur Deteksi Anomali Transaksi ini bertujuan untuk mendeteksi anomali pada data transaksi keuangan menggunakan metode unsupervised learning, yakni tanpa memerlukan label sebelumnya. Dua algoritma utama yang digunakan adalah Isolation Forest dan One-Class SVM.

## Alur Proses##
1. Pembersihan Data
- Menghapus nilai null dan duplikat.
- Konversi tipe data waktu dan identifikasi akun unik.

2. Rekayasa Fitur

a. Ekstraksi fitur waktu seperti:
- Jam transaksi (hour)
- Hari dalam seminggu (dayofweek)
- Tanggal (day)

b. Penghitungan frekuensi transaksi harian per akun.
c. Encoding fitur kategori dan normalisasi data numerik.

3. Preprocessing Pipeline
Dibuat dengan ColumnTransformer:
- OneHotEncoder untuk fitur kategorikal.
- StandardScaler untuk fitur numerik.

4. Modeling
Dua model digunakan secara terpisah:
- Isolation Forest
- One-Class SVM

Masing-masing model dilatih pada data yang telah diproses untuk mendeteksi anomali.
5. Evaluasi & Visualisasi
- Distribusi hasil prediksi divisualisasikan.
- Transaksi yang terdeteksi sebagai anomali dianalisis lebih lanjut.
