# dashboard-bi-kmeans-kinerja-akademik-siswa
Pengembangan Dashboard Business Intelligence Untuk Klasterisasi Kinerja Akademik Siswa Menggunakan Algoritma K-Means Berdasarkan Nilai Mata Pelajaran

## Deskripsi

Repository ini berisi implementasi Tugas Akhir mengenai pengembangan *Dashboard Business Intelligence* untuk melakukan klasterisasi kinerja akademik siswa menggunakan algoritma *K-Means Clustering* berdasarkan nilai rata-rata mata pelajaran.

Penelitian ini merupakan pengembangan dari *Dashboard Business Intelligence* yang telah dibuat pada kegiatan Kerja Praktik (KP). Pengembangan dilakukan dengan menambahkan proses *clustering* untuk mengelompokkan siswa berdasarkan pola nilai akademik.

## Tujuan

Sistem dikembangkan untuk:

* Mengolah data nilai akademik siswa.
* Membentuk fitur berdasarkan rata-rata nilai setiap mata pelajaran.
* Melakukan standardisasi data sebelum proses *clustering*.
* Mengelompokkan siswa menggunakan algoritma *K-Means*.
* Mengevaluasi hasil *clustering* menggunakan *Elbow Method* dan *Silhouette Score*.
* Menampilkan hasil analisis melalui *Dashboard Business Intelligence*.

## Metode

Tahapan utama pengolahan data dalam sistem meliputi:

1. Input dataset nilai akademik siswa.
2. Pembersihan dan pengolahan data.
3. Pembentukan fitur rata-rata nilai mata pelajaran.
4. Standardisasi data menggunakan `StandardScaler`.
5. Penerapan algoritma *K-Means Clustering*.
6. Evaluasi hasil *clustering* menggunakan *Elbow Method* dan *Silhouette Score*.
7. Penyajian hasil melalui *Dashboard* berbasis *Streamlit*.

### Konfigurasi Clustering

Konfigurasi utama penelitian menggunakan:

```text
Jumlah Cluster (K) = 3
Random State = 42
n_init = 10
```

Hasil *clustering* dengan K=3 diinterpretasikan menjadi tiga kelompok karakteristik siswa:

* **Nilai Rendah**
* **Nilai Sedang**
* **Nilai Tinggi**

K=2 digunakan sebagai pengujian tambahan untuk membandingkan kualitas hasil *clustering* berdasarkan *Silhouette Score*, tetapi tidak digunakan sebagai konfigurasi utama sistem.

## Dataset

Dataset penelitian terdiri dari data akademik siswa yang dibagi menjadi dua fase:

* **Fase A**: 86 siswa dengan 7 mata pelajaran.
* **Fase B/C**: 151 siswa dengan 8 mata pelajaran.

Fitur yang digunakan dalam proses *clustering* berupa rata-rata nilai setiap mata pelajaran, yang dihitung dari nilai Harian, PTS, dan PAS.

Dataset asli tidak disertakan dalam repository karena mengandung data akademik siswa.

## Fitur Mata Pelajaran

Fitur yang digunakan dalam proses *clustering* meliputi:

* `Rata_Agama`
* `Rata_PKN`
* `Rata_Bahasa Indonesia`
* `Rata_Matematika`
* `Rata_SBDP`
* `Rata_PJOK`
* `Rata_Mulok`
* `Rata_IPAS` *(untuk data yang memiliki mata pelajaran IPAS)*

## Teknologi yang Digunakan

* **Python**
* **Google Colab**
* **Streamlit**
* **Cloudflare Tunnel**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **Matplotlib**
* **Seaborn**

## Evaluasi

Kualitas hasil *clustering* dievaluasi menggunakan *Elbow Method* dan *Silhouette Score*.

Pada konfigurasi utama K=3 diperoleh:

| Dataset  | Jumlah Siswa |  K | Silhouette Score |
| -------- | -----------: | -: | ---------------: |
| Fase A   |           86 |  3 |            0,258 |
| Fase B/C |          151 |  3 |            0,329 |

Pengujian tambahan dengan K=2 menghasilkan nilai *Silhouette Score* yang lebih tinggi, tetapi K=3 tetap digunakan sebagai konfigurasi utama karena penelitian membutuhkan tiga kelompok karakteristik siswa.

## Dashboard

*Dashboard Business Intelligence* dikembangkan menggunakan *Streamlit*. Dashboard menampilkan informasi hasil pengelompokan siswa, antara lain:

* Jumlah siswa pada setiap *cluster*.
* Karakteristik masing-masing *cluster*.
* Rata-rata nilai mata pelajaran.
* Distribusi siswa berdasarkan kategori.
* *Heatmap* profil *cluster*.
* *Scatter plot* hasil *clustering*.

## Struktur Repository

```text
dashboard-bi-kmeans-kinerja-akademik-siswa/
│
├── Coding_TA.ipynb
├── README.md
└── ...
```

File notebook berisi implementasi kode yang digunakan dalam proses penelitian.

## Cara Menjalankan

Implementasi penelitian dikembangkan dan dijalankan melalui Google Colab. Aplikasi *Dashboard* menggunakan Streamlit dan dapat diakses melalui *Cloudflare Tunnel* ketika program dijalankan.

Secara umum, proses penggunaan sistem adalah:

```text
Upload Dataset
      ↓
Pengolahan Data
      ↓
Pembentukan Fitur
      ↓
Standardisasi
      ↓
K-Means (K=3)
      ↓
Evaluasi
      ↓
Hasil Clustering
      ↓
Dashboard Business Intelligence
```

## Hasil

Sistem berhasil melakukan pengelompokan siswa menjadi tiga kelompok karakteristik berdasarkan pola rata-rata nilai mata pelajaran. Hasil *clustering* kemudian disajikan melalui *Dashboard Business Intelligence* untuk membantu pengguna melihat distribusi dan karakteristik kinerja akademik siswa.

## Penulis
