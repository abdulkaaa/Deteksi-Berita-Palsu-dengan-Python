# Deteksi-Berita-Palsu-dengan-Python
Penerapan Passive Aggressive Classifier dalam pendeteksian berita palsu dengan Python.

Sebelumnya, percobaan ini telah dilakukan oleh [Data-Flair](https://data-flair.training/).

Saya melakukan percobaan ini dengan menggunakan Google Colaboratory.

Hasil percobaan yang saya lakukan dapat dilihat [di sini](https://colab.research.google.com/drive/1devttGsOx6KMDdLcOROAu0hK006NLVPR?usp=sharing).

## Data
- Dataset yang digunakan pada proyek python ini yaitu news.csv.
- Dataset ini memiliki bentuk 6335×4.
- Kolom pertama menyatakan berita, kolom kedua berisi judul, kolom ketiga berisi teks dari berita, dan kolom keempat berisi label yang menunjukkan apakah berita tersebut nayata (REAL) atau palsu (FAKE).

## Langkah Percobaan
Berikut merupakan langkah-langkah yang dilakukan dalam percobaan ini.

1.  Melakukan *import* semua *Library* yang diperlukan;

```
import numpy as np
import pandas as pd
import itertools
from sklearn.model_selection import train_test_split
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.linear_model import PassiveAggressiveClassifier
from sklearn.metrics import accuracy_score, confusion_matrix
```

2.  Membaca data dan mengubahnya ke dalam *dataframe* dengan *pd.read_csv()*

```
dataframenya = pd.read_csv("news.csv")
```

3.  Menampilkan *shape* dan lima baris pertama dari data

```
print("shape : ", dataframenya.shape)
dataframenya.head()
```
4.  Menampilkan label-label dari lima baris pertama dataset

```
labels = dataframenya.label
labels.head()
```

5.  Membagi dataset menjadi *training* dan *testing sets*

```
x_train, x_test, y_train, y_test = train_test_split(dataframenya['text'], labels, test_size=0.2, random_state=7)
```

