# Laporan Proyek Machine Learning - Juan Anemao Sokhi Zidomi

## [Rekomendasi Game berdasarkan Genre di platform Game Steam](https://www.kaggle.com/datasets/nikatomashvili/steam-games-dataset)
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
### Goals
### Solusi Statements

## Data Understandings
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Pada dataset ini menjelaskan informasi game di steam seperti judul game, popular tags dan lain-lain.

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

Berikut ini adalah deskripsi dataset Steam Game Dataset yang dipakai pada proyek ini:

1. Statistik dataset

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
2. Info dataset
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
   
3. Dimensi dataset
   
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
   
4. Duplikasi dataset

   Skrip:
   ```python
      jumlah_duplikat=Game_df.duplicated().sum()
      print("Jumlah duplikat data:", jumlah_duplikat)
   ```

   Hasil:
   
      Jumlah duplikat data: 0
   
5. Info  nilai missing

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
   
    Kesimpulan deskripsi dataset:
   - Dari statistik dataframe diatas bahwa semua kolom bertipe kategorikal atau object
   - Dimensi dataset game di Steam adalah 71700 baris dan 16 kolom
   - Pada dataframe diatas tidak terdapat data terdupilikasi
   - Pada dataframe diatas terdapat banyak nilai missing value dan hampir setiap kolom sehingga dilakukan drop nilai NaN
   
   ### EDA
   <br>
   1. Visualisasi review summary game di Steam
   <br>
   
      ![Visualisasi](https://raw.githubusercontent.com/Junazidomi/latihan-branch/refs/heads/main/vis11.png)
   
   2. Visualisasi tahun rilis game
       ![Visualisasi](https://raw.githubusercontent.com/Junazidomi/latihan-branch/refs/heads/main/vis11.png)
   4. Visualisasi distribusi harga game di Steam
   
## Data Preparation

## Modeling and Result

## Evaluation
