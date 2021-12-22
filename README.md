# Deteksi-Berita-Palsu-dengan-Python
Penerapan TF-IDF Vectorizer dan Passive Aggressive Classifier dalam pendeteksian berita palsu dengan Python.

Sebelumnya, percobaan ini telah dilakukan oleh [Data-Flair](https://data-flair.training/).

Saya melakukan percobaan ini dengan menggunakan Google Colaboratory.

Hasil percobaan yang saya lakukan dapat dilihat [di sini](https://colab.research.google.com/drive/1devttGsOx6KMDdLcOROAu0hK006NLVPR?usp=sharing).

## TF-IDF Vectorizer
- TF atau term frequency adalah skema pembobotan yang digunakan untuk menentukan relevansi dokumen dengan sebuah term (kata). TF menentukan bobot relevansi sebuah dokumen dan term berdasarkan frekuensi kemunculan term pada dokumen terkait [1].
- IDF atau Inverse Document Frequency merupakan jumlah dokumen di mana terdapat term yang bersangkutan. IDF mengurangi bobot TF suatu term dengan membaginya dengan frekuensi term terhadap koleksi dokumen (DF). Jadi sebuah term yang memiliki bobot TF yang besar namun dengan bobot DF yang besar pula tidak akan memiliki pengaruh yang besar dalam menentukan sebuah relevansi [1].

## Passive Aggressive Classifier
- Passive Aggressive Classifier adalah algoritma pembelajaran online di mana kita melatih sistem secara bertahap. Model dilatih dan diterapkan dalam produksi dengan cara yang terus dipelajari saat kumpulan data baru tiba [2].
- Algoritma berkerja secara Pasif jika prediksinya benar. Algoritma akan mempertahankan model dan tidak lakukan perubahan apa pun. Hal ini karena data dalam contoh tidak cukup untuk menyebabkan perubahan dalam model.
- Algoritma berkerja secara Agresif jika prediksi salah. Algoritma akan melakukan perubahan pada model.

## Data
- Dataset yang digunakan pada proyek ini yaitu news.csv yang terdapat dalam file Dataset_news.rar
- Dataset ini memiliki bentuk 6335×4
- Kolom pertama menyatakan berita, kolom kedua berisi judul, kolom ketiga berisi teks dari berita, dan kolom keempat berisi label yang menunjukkan apakah berita tersebut nyata (REAL) atau palsu (FAKE)

## Langkah Percobaan
Berikut merupakan langkah-langkah yang dilakukan dalam percobaan ini.

1.  Melakukan *import* semua *Library* yang diperlukan;
2.  Membaca data dan mengubahnya ke dalam *dataframe* dengan *pd.read_csv()*;
3.  Menampilkan *shape* dan lima baris pertama dari data;
4.  Menampilkan label-label dari lima baris pertama dataset;
5.  Membagi dataset menjadi *training* dan *testing sets*;
6.  


### Daftar Pustaka
[1] [Prasetia Utama. 2016. "TF-IDF VSM Menggunakan Python".](https://prasetiautamacv.wordpress.com/2016/07/31/tf-idf-vsm-menggunakan-python/)

[2] [Aman Kharwal. 2021. "Pengklasifikasi Agresif Pasif dalam Pembelajaran Mesin".](https://thecleverprogrammer.com/2021/02/10/passive-aggressive-classifier-in-machine-learning/)

[3] [alokesh985. 2020. "Passive Aggressive Classifiers".](https://www.geeksforgeeks.org/passive-aggressive-classifiers/)
