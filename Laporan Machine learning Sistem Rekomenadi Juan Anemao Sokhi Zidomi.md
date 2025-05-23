# Laporan Proyek Machine Learning - Juan Anemao Sokhi Zidomi
## Project Overview

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Industri game telah mengalami pertumbuhan pesat dalam satu dekade terakhir. Menurut laporan dari Newzoo, pasar game global mencapai pendapatan lebih dari $184 miliyar pada tahun 2023, dengan platform digital seperti Steam menyumbang bagian besar dari pendapatan tersebut (Newzoo, 2023). Steam sendiri merupakan salah satu platform distribusi game digital terbesar di dunia, dengan lebih dari 50000 judul game dan jutaan pengguna aktif setiap harinya (Valve Corporation,2023). Dengan volume konten yang sangat besar ini, pengguna seringkali mengalami kesulitan dalam menemukan game yang sesuai dengan preferensi mereka. Hal ini menciptakan kebutuhan akan sistem rekomendasi game yang cerdas dan relevan.
<br><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Masalah utama yang dihadapi adalah information overload, dimana pengguna dihadapkan banyak pilihan tanpa alat bantu dalam menyaring informasi pengguna. Tanpa sistem rekomendasi yang baik, pengguna akan melewatkan game sebenarnya sesuai dengan preferensi pengguna dan pengembang game kecil (indie developer) berpotensi kehilangan audiens karena kalah bersaing dengan pengembang game populer. Pengembangan sistem rekomendasi game yang efektif dapat meningkatkan pengalaman pengguna dan sekaligus membantu pengembang pasar yang lebih tepat. Sistem rekomendasi ini dapat dibangun berdasarkan interaksi pengguna seperti genre, developer game, developer game, ulasan atau yang berkaitan preferensi pengguna di Steam.
<br><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Salah satu pendekatan yang digunakan untuk membangun sistem rekomendasi yaitu Content-Based Filtering (Ricci et al., 2015). Dengan adanya sistem rekomendasi game ini, dapat meningkatkan kepuasaan pengguna dan mendorong pertumbuhan bisnis melalui peningkatan penjualan dan keterlibatan pengguna.
<br>

Referensi:

1. Newzoo. (2023). Global Games Market Report. [Online]. Tersedia: https://www.newzoo.com/
2. Valve Corporation. (2023). Steamworks Documentation. [Online]. Tersedia: https://partner.steamgames.com/doc/home
3. Ricci, F., Rokach, L., & Shapira, B. (2015). Recommender Systems Handbook. Springer.
## Business Understandings

### Problem Statements
Berikut adalah problem statements pada proyek ini:
- Kesulitan menemukan game sesuai dengan preferensi pengguna
- Ketimpangan eksposur untuk game idle atau kurang populer
### Goals
Berikut adalah Goals yang akan dicapai:
- Membangun sistem rekomendasi yang dapat secara otomatis yang dapat menyarankan game sesuai dengan preferensi pengguna di Steam
- Memberikan peluang yang lebih merata untuk semua game
  
### Solusi Statements
- Mengembangkan sistem rekomendasi menggunakan pendekatan content base filtering berdasarkan cosine similarity dan jaccard similarity untuk mengukur kesamaan antar game berdasarkan atribut kontennya. 
- Sistem diuji dan dievaluasi menentukan pendekatan yang paling optimal dalam menyarankan game yang sesuai dengan preferensi pengguna
  
## Data Understandings
### Pengatar Dataset
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Pada dataset yang digunakan pada proyek ini, menjelaskan bahwa steam memiliki game dengan judul yang berbeda-beda. Selain itu, dataset ini memberikan informasi atau gambaran tentang game tersebut seperti harga game , harga setelah diskon di steam jika sedang ada event menarik, pengembang, publisher , review penngguna , genre game dan lain-lain. Hal ini dapat membantu dalam melakukan sistem rekomendasi. Dataset yang digunakan diambil dari platform penyedia dataset yaitu kaggle dan dataset contributor yaitu Nika Tomashvili. Untuk mengakses dataset, dapat melalui link berikut: 

[Link Dataset](https://www.kaggle.com/datasets/nikatomashvili/steam-games-dataset)

### Variabel atau Fitur
Variabel atau fitur yang terdapat pada dataset yang digunakan pada proyek ini di jelaskan di tabel dibawah:

| No | Atribute | Description |
|---------|---------|---------|
| 1 | Title | Judul Game di Steam |
| 2 | Original Price | Harga game sebelum diskon dalam bentuk US Dolar ($) |
| 3 | Discounted Price | Harga game setelah diskon dalam bentuk US Dolar ($) |
| 4 | Release Date | Tanggal rilis game |
| 5 | Link | Halaman link game pada Steam |
| 6 | Game Description | Ringkasan singkat tentang game |
| 7 | Recent Reviews Summary | Ringkasan umpan balik para pengguna baru baru ini  | 
| 8 | All Reviews Summary | Ringkasan umpan balik para pengguna sepanjang waktu  |
| 9 | Recent Reviews Number | Rangkuman Singkat jumlah review baru baru ini |
| 10 | All Reviews Number |  Rangkuman singkat jumlah review |
| 11 | Developer | Nama Pengembang Game | 
| 12 | Publisher | Nama Publisher Game |
| 13 | Supported Languages | Bahasa yang didukung pada game |
| 14 | Popular Tags | Genre Game |
| 15 | Game Features | Fitur yang terdapat pada game tersebut
| 16 | Minimum Requirements| Spesifikasi minimum supaya dapat menjalankan game |

### Jumlah Baris dan Kolom
Untuk mengetahui jimlah baris dan kolom dapat menggunakan perintah pada python sebagai berikut:
   
   Skrip:
   ```python
      jumlah_baris, jumlah_kolom=Game_df.shape
      print("Jumlah baris pada dataframe:", jumlah_baris)
      print("Jumlah kolom pada dataframe:, jumlah_kolom)
   ```
   Hasil:

      Jumlah baris pada dataframe: 71700
       <br>
      Jumlah Kolom pada dataframe: 16
   
   Kesimpulan:
   Berdasarkan hasil dari perintah diatas, dapat disimpulkan dataset dibangun kolom berjumlah 16 dan baris berjumlah 71700

### Identifikasi Kondisi Dataset
#### Statistik Dataset
Untuk melihat statistik dataset seperti mean, max, min , nilai yang sering muncul dan lain-lain dapat menggunakan perintah dibawah

   Skrip:
   ```python
      Game_df.describe()
   ```

   Hasil:

   |     | Title | Original Price | Discounted Price | Release Date | Link | Game Description | Recent Reviews Summary | All Reviews Summary  | Recent Reviews Number | All Reviews Number | Developer | Publisher | Supported Languages | Popular Tags | Game Features | Minimum Requirements |
   |-----------|---------------|------------|-------------|------------------|--------------------|--------------------|------------|-----------|---------------|------------|-------------|------------------|--------------------|--------------------|------------|------------|
   | count  | 71699 | 71700 | 71700 | 71569 | 71700 | 71489 | 56480 | 5371 | 56480 | 5371 | 71479 | 71183 | 71700 | 71700 | 71700 | 70576| 
   | unique | 71699 | 654 | 827 | 4441 | 71700 | 71090 | 18 | 7 | 13391 | 5296 | 45353 | 38543 | 11058| 65817 | 5418 | 63201 | 
   | top    |Pixel Gun 3D: PC Edition | Free | Free | Coming soon | https://store.steampowered.com/app/2524890/Pix... | Find the objects that are hidden on the map. | Very Positive | Very Positive | - Need more user reviews to generate a score | - 90% of the 624 user reviews for this game ar... | Choice of Games | Big Fish Games | ['English']	| ['Indie', 'Casual'] | ['Single-player'] | Requires a 64-bit processor and operating syst... |
   | freq   | 1 |	17585 | 17585 | 5887	| 1 | 34 | 11039 | 3151 | 18999 | 3 | 162 | 459 | 38083| 284 | 17262 | 274  |

   Kesimpulan:
   Berdasarkan hasil dari perinyah diatas, didapatkan bahwa dataset diatas bahwa game di steam memiliki rata-rata review positif  dari pengguna. Selain itu, game di Steam paling banyak game free atau dapat didapatkan secara gratis dan pada release year paling banyak game coming soon.
   
#### Info dataset
Untuk melakukan identifikasi kondisi tipe data jenis dataset dapat menggunakan perintah dibawah:
   Skrip:

   ```python
      Game_df.info()
   ```

   Hasil:
   | Index  | Column                      | Non-Null Count | Dtype  |
   |-----|-----------------------------|----------------|--------|
   | 0   | Title                       | 71699 non-null  | object |
   | 1   | Original Price              | 71700 non-null  | object |
   | 2   | Discounted Price            | 71700 non-null  | object |
   | 3   | Release Date                | 71569 non-null  | object |
   | 4   | Link                        | 71700 non-null  | object |
   | 5   | Game Description            | 71489 non-null  | object |
   | 6   | Recent Reviews Summary      | 56480 non-null  | object |
   | 7   | All Reviews Summary         | 5371 non-null   | object |
   | 8   | Recent Reviews Number       | 56480 non-null  | object |
   | 9   | All Reviews Number          | 5371 non-null   | object |
   | 10  | Developer                   | 71479 non-null  | object |
   | 11  | Publihser                   | 71183 non-null  | object |
   | 12  | Supported Languages         | 71700 non-null  | object |
   | 13  | Popular Tags                | 71700 non-null  | object |
   | 14  | Game Features               | 71700 non-null  | object |
   | 15  | Minimum Requirements        | 70576 non-null  | object |

   Kesimpulan:
   Berdasarkan hasil dari perintah diatas, didapatkan bahwa semua kolom pada dataset ini memiliki tipe object 

#### Duplikasi dataset
Data duplikat akan sangat menggangu sistem ketika dibangun. Untuk menghindari hal tersebut, melakukan identifikasi jumlah duplikat pada dataframe dengan perintah python sebagai berikut.

   Skrip:
   ```python
      jumlah_duplikat=Game_df.duplicated().sum()
      print("Jumlah duplikat data:", jumlah_duplikat)
   ```

   Hasil:
   
      Jumlah duplikat data: 0
   
   Kesimpulan:
   Berdasarkan hasil dari perintah diatas, didapatkan bahwa di dataset yang digunakan tidak memiliki duplikat data.
   
   #### Identifikasi Nilai Missing
   Dalam membangun suatu sistem, kondisi dataset harus bebas dari nilai NaN supaya sistem dapat bekerja secara optimal. Untuk mengidentfikasi kolom mana saja dan jumlah baris yang terdapat nilai NaN dapat menggunakan perintah python dibawah. 

   Skrip:
   ```python
      Game_df.isna().sum()
   ```
   Hasil:
   | Column                     | Missing Values |
   |----------------------------|----------------|
   | Title                      | 1              |
   | Original Price             | 0              |
   | Discounted Price           | 0              |
   | Release Date               | 131            |
   | Link                       | 0              |
   | Game Description           | 211            |
   | Recent Reviews Summary     | 15220          |
   | All Reviews Summary        | 66329          |
   | Recent Reviews Number      | 15220          |
   | All Reviews Number         | 66329          |
   | Developer                  | 221            |
   | Publisher                  | 517            |
   | Supported Languages        | 0              |
   | Popular Tags               | 0              |
   | Game Features              | 0              |
   | Minimum Requirements       | 1124           |
   
   Kesimpulan:
   Berdasarkan dari perintah diatas, didapatkan bahwa ada hampir semua kolom memiliki NaN Atau missing value dan paling banyak terdapat pada kolom All Review Summary dan All Reviews Number.
#### Identifikasi Kondisi Dataset Original Price
Pada proses ini, melakukan identifikasi kondisi kolom Original Price karena pada dasarnya price adalah kolom bertipe number. Untuk mengidentifikasi kolom Original Price dapat menggunakan perintah python dibawah.

Skrip:
```python
   Game_df['Original Price'].head()
```
Hasil:
|       | Original Price |
|-------|----------------|
|   0	  |     $29.99     |
|   1	  |     $14.99     |
|   2	  |      Free      |
|   3	  |     $34.78     |
|   4	  |      Free      |

Kesimpulan:
Berdasarkan hasil dari perintah diatas, kolom Original Price dapat diubah menjadi kolom number dengan cara melakukan pengubahan free menjadi 0 dan untuk yang tidak free diubah menjadi angka dengan cara menghapus tanda $

### EDA
<br>
Visualisasi review summary game di Steam
<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![Visualisasi](https://raw.githubusercontent.com/Junazidomi/latihan-branch/refs/heads/main/vis11.png)
<br>   
Kesimpulan: 
Dari visualisasi diatas didapatkan bahwa feedback dari pengguna game steam yaitu very positive hal ini menandakan bahwa semua game di Steam mendapatkan apresiasi positif dari pengguna

Visualisasi tahun rilis game
<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![Visualisasi](https://raw.githubusercontent.com/Junazidomi/latihan-branch/refs/heads/main/vis22.png)
<br> 

Kesimpulan:
Dari visualisasi diatas didapat bahwa game paling banyak di Steam adalah game rilis pada tahun 2020
Visualisasi distribusi harga game di Steam
<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![Visualisasi](https://raw.githubusercontent.com/Junazidomi/latihan-branch/refs/heads/main/vis33.png)

Kesimpulan:
Dari visualisasi diatas didapatkan bahwa game steam paling banyak harga 0 $ atau dapat dikatakan gratis dan harga game paling mahal pada sekitar 140$

## Data Preparation

Proses persiapan data yang dilakukan pada proyek ini sebagai berikut:

1. Melakukan hapus kolom yang berisi NaN atau missing value. Pada proses ini setelah dilakukan identifikasi dataset pada missing value atau NaN, maka dilakukan penanganan missing value yaitu menghapus baris yang memiliki NaN atau missing value. Hal ini bertujuan untuk mengoptimalkan sistem rekomendasi content-base filtering dan mendapatkan informasi yang secara lengkap supaya dapat memberikan rekomendasi secara akurat.
2. Melakukan drop kolom yang tidak digunakan. Hal ini penting dilakukan supaya dapat membuat sistem dapat bekerja secara optimal sesuai dengan informasi yang relevan.
3. Melakukan pengubahan nilai unik Free menjadi 0 kemudian menghapus $ pada harga setiap game selain free pada kolom Original Price dan mengganti kolom Original Price menjadi Original Price ($)
4. Melakukan format ulang tanggal rilis game dari tanggal rilis menjadi tahun rilis. Hal ini bertujuan untuk melakukan visualisasi tahun rilis game pada Steam. Selain itu, melakukan pengubahan nama kolom dari Release Date menjadi Release Year
5. Melakukan pemrosesan pada kolom Popular Tags dimana melakukan pengambilan 3 tag dari 20 genre. Selain itu, menghapus spasi pada tag supaya dapat diproses ke tahap selanjutnya
6. Melakukan preprocessing text menggunakan TfIdf vectorizer atau melakukan tokenisasi untuk mempresentasikan kolom target ke matriks agar dapat diproses.
    
## Modeling and Result
Adapun pendekatan yang dilakukan dalam membangun sistem rekomendasi adalah menggunakan sistem content-based filterng. Dalam membangun sistem rekomendasi content based filtering menggunakan 2 metode yaitu content-based filtering menggunakan cosine similarity dan Jaccard similarity.

1. Content-Base filtering Cosine similarity
   Cosine similarity adalah teknik mengukur kesamaan antara 2 vektor dan menentukan apakah kedua vektor tersebut menunjuk ke arah yang sama. Menghitung sudut cosinus antara 2 vektor, semakin kecil sudut cosinus semakin besar nilai cosine similarity. Adapun rumus Cosine similarity sebagai berikut:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![Rumus](https://raw.githubusercontent.com/Junazidomi/latihan-branch/refs/heads/main/cosinie.jpeg)

Kelebihan:
- Efektif jika representasi fitur kaya (TFIDF)
- Bisa Menangkap kedekatan semantik antar item masukan
- Cocok untuk data dengan banyak fitur numerik atau teks

Kekurangan:
- Perlu representasi fitur yang baik
- Kurang efektif jika sangat pars (fitur jarang muncul)
- Tidak bisa mengenali relasi antar item yang tidak mirip kontennya 

Adapun output rekomendasi sebagai berikut:

Script:
```python
    game_recom('Call of Duty®')
```

Hasil:
| Title                         | Popular Tags                   |
|------------------------------|---------------------------------|
| Counter-Strike: Global Offensive | FPS Shooter Multiplayer     |
| World War 3                  | FPS Multiplayer Shooter         |
| BattleBit Remastered         | FPS Shooter Multiplayer         |
| Battlefield 4™               | Multiplayer FPS Shooter         |
| SharpShooter3D               | Action FPS Shooter              |

      
2. Jaccard Similarity  adalah teknik yang dikenalkan Paul Jaccard,metode pengukuran kesamaan antara 2 himpunan dan dihitung sebagai perbandingan antara jumlah elemen yang sama (intersection) dengan jumlah total elemen unik himpunan.

  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![Rumus](https://raw.githubusercontent.com/Junazidomi/latihan-branch/refs/heads/main/jaccard.jpeg)


Kelebihan:
- Mudah dan cepat diimplementasikan 
- Cocok untuk data yang hanya memiliki informasi kategori
- Tidak terlalu sensitif terhadap noise dalam data
Kelemahan:
- Tidak mempertimbangkan frekuensi atau pentingnya fitur(tidak ada bobot)
- Kondisi presisi dalam konteks teks atau fitur yang kompleks
- Tidak bisa membedakan seberapa penting fitur yang tumpah tindih

Adapun output rekomendasi sebagai berikut:
```python
   print(game_recomjacc_tfidf("Call of Duty®"))
```
Hasil:
| Index | Title                            |
|-------|----------------------------------|
| 1     | Counter-Strike: Global Offensive |
| 19    | BattleBit Remastered             |
| 723   | Battlefield 4™                   |


## Evaluation
Evaluasi yang akan digunakan pada proyek ini adalah evaluasi metrik sistem rekomendasi sebagai berikut:

1. Precision
   Precision adalah metrik evaluasi yang mengukur proporsi item yang relevan dalam top K rekomendasi. Adapun rumus precision sebagai berikut:
   
           Precision@K = (Jumlah item relevan dalam Top-K) / K

2. Recall
   Recall adalah metrik evaluasi seberapa banyak item yang berhasil direkomendasikan dari semua item relevan yang diketahui. Adapun rumus recall sebagai berikut:

            Recall@K= Jumlah total item relevan / Jumlah item relevan dalam Top-K
​
3. F1 Score
   F1 Score adalah metrik evaluasi kombinasi dari precision dan recall. Adapun rumus F1 Score sebagai berikut:
   
            F1@K= (Precision@K+Recall@K) / 2⋅Precision@K⋅Recall@K
​
 Evaluasi setiap pendekatan
 
| Pendekatan Content-Base Filtering                | Precision |  Recall   | F1 Score |
|--------------------------------------------------|---------- |---------- |----------|
| Cosine Similarity                                | 0.7070837406321155  |  0.8496578690126935  | 0.7641103818522876 |
| Jaccard Similarity                               | 0.622  | 0.896  | 0.72 |

Kesimpulan:

1. Berdasarkan metrik evaluasi antara Cosine dan Jaccard Similarity didapatkan bahwa cosine similarity mempunyai F1 Score lebih besar. Selain itu, dari hasil rekomendasi cosine similarity memberikan rekomendasi game paling banyak daripada jaccard similarity berdasarkan genre. Dapat disimpulkan bahwa sistem rekomendasi akan dibangun menggunakan Content-Base Filtering menggunakan pendekatan Cosine Similarity
2. Sistem rekomendasi sudah dapat menyaring game sesuai dengan preferensi pengguna bukan menggunakan popularitas game. Hal ini akan membantu pengembang game kecil mendapatkan kesempatan merata dengan pengembang game besar dan rekomendasi game sesuai dengan prefrensi pengguna
