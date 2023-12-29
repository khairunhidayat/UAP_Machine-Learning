# UAP_Machine-Learning

Gambaran Umum
Repositori ini berisi contoh sederhana implementasi model klasifikasi gambar menggunakan Flask.untuk mengklasifikasikan gambar ke dalam tiga kelas. Aplikasi web memungkinkan pengguna mengunggah gambar dan mendapatkan prediksi secara real-time. me.

Struktur Proyek
|- static |- templates |- app.py |- model.h5 |- README.md

Dependensi
Pastikan untuk menginstal library yang dibutuhkan sebelum menjalankan aplikasi: bash pip install flask tensorflow

Pelatihan Model
Model klasifikasi gambar dilatih menggunakan Mobilenetv2. Model disimpan sebagai mod6.h5. Sesuaikan jumlah unit keluaran di lapisan terakhir dan fungsi aktivasi sesuai dengan jumlah kelas.

Overview Dataset
Splitting Dataset menggunakan: Training = 70%, Validation = 20%, Testing = 10%

Modelling
base_model = MobileNetV2(weights='imagenet', include_top=False, input_shape=(224, 224, 3))

Graph Loss dan Accuracy :
![Screenshot_16](https://github.com/khairunhidayat/UAP_Machine-Learning/assets/108686270/3946fa2c-9d90-402e-9243-29b31149161c)

Model Evaluasi : 
![Screenshot_17](https://github.com/khairunhidayat/UAP_Machine-Learning/assets/108686270/7d91d49c-93fd-4671-919c-6ae2787e084c)

Aplikasi Flask
Aplikasi web Flask (app.py) berfungsi sebagai antarmuka untuk model klasifikasi gambar. Aplikasi menggunakan model yang disimpan untuk membuat prediksi pada gambar yang diunggah oleh pengguna.

Cara Menjalankan
bash Copy code python app.py Buka browser dan akses [http://127.0.0.1:8000]. Anda dapat mengunggah gambar dan mendapatkan prediksi.
