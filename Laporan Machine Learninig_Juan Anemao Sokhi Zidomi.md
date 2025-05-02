# Laporan Machine Learning_Juan Anemao Sokhi Zidomi
## [Faktor Yang Mempengaruhi Ujian Siswa](https://www.kaggle.com/datasets/lainguyn123/student-performance-factors)


&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Pada zaman sekarang, kualitas pendidikan pada siswa persekolahan dapat ditentukan dari hasil nilai ujian sehingga siswa tersebut dapat di kategorikan. Namun pencapaian dalam nilai pada ujian tidak hanya ditentukan oleh kecerdasan siswa, tetapi dipengaruhi oleh berbagai faktor internal maupun eksternal. Faktor seperti manajemen waktu, motivasi belajar, kebiasaan belajar serta lingkungan yang mempengaruhi siswa dalam performa ujian (Wintre & Yaffe, 2000; Nonis & Hudson, 2010).
<br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Mencari tahu dan memahami apa yang memengaruhi hasil ujian siswa sangat penting. Ini akan memberikan dasar yang kuat untuk membangun metode pembelajaran atau solusi yang lebih baik. Sebagai contoh, jika diketahui bahwa motivasi intrinsik sangat penting untuk prestasi akademik, maka pendekatan pembelajaran yang memungkinkan siswa untuk menjadi merdeka dan relevan dengan materi akan lebih efektif (Ryan & Deci, 2000).
<br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Hasil penelitian yang dilakukan oleh Broadbent dan Poon (2015) menunjukkan bahwa penggunaan teknologi pembelajaran dan strategi belajar mandiri dapat meningkatkan prestasi akademik. Ini menunjukkan bahwa solusi untuk masalah ini tidak hanya harus bersifat teoritis tetapi juga praktis. Oleh karena itu, proyek ini akan berkonsentrasi pada mengidentifikasi komponen utama yang memengaruhi hasil ujian siswa dan mengembangkan metode yang berbasis bukti untuk meningkatkan prestasi akademik.
<br>
#### Referensi
1. Wintre, M. G., & Yaffe, M. (2000). First-year students’ adjustment to university life as a function of relationships with parents. Journal of Adolescent Research, 15(1), 9–37.
2. Ryan, R. M., & Deci, E. L. (2000). Intrinsic and extrinsic motivations: Classic definitions and new directions. Contemporary Educational Psychology, 25(1), 54–67.
3. Broadbent, J., & Poon, W. L. (2015). Self-regulated learning strategies & academic achievement in online higher education learning environments: A systematic review. The Internet and Higher Education, 27, 1–13.

## Business Understandings

### Problem Statements

1. Banyak antara mahasiswa mengalami penurunan performa pada ujian meskipun memiliki kehadiran bagus pada saat kelas, sehingga dapat disimpulkan bahwa ada beberapa faktor lain yang mempengaruhi performa siswa pada ujian
2. Belum ada sistem yang efektif yang mengidentifikasi yang dapat mempengaruhi performa ujian siswa
3. Strategi pembelajaran dan intervensi akademik bersifat umum sehingga pemetaan faktor yang mempengaruhi nilai ujian siswa

### Goals
1. Mengidentifikasi faktor-faktor yang dapat mempengaruhi performa ujian mahasiswa seperti motivasi belajar, lingkungan, kualitas guru, faktor ekonomi dan lain-lain
2. Mengembangkan model prediktif berbasis AI untuk melakukan prediksi nilai ujian mahasiswa berdasarkan data-data survei dari siswa
3. Merancang strategi personalisasi pembelajaran dan rekomendasi intervensi berdasarkan hasil klasifikasi faktor risiko, sehingga setiap mahasiswa mendapat saran yang relevan dan berdampak terhadap peningkatan performa akademik.
### Solusi Statements

1. Menggunakan algoritma mesin seperti LARS, GradientBossting , Linear Regression dan Random Forest Regressor untuk membangun model prediktif untuk menentukan nilai Ujian siswa berdasarkan karakteristik dalam berbasi regresi
2. Melakukan feature selection dan hyperparameter tuning menggunakan metode Grid Search dan Recursive Feature Elimination (RFE) untuk meningkatkan akurasi model prediksi. Ini akan membantu mengidentifikasi faktor paling signifikan dalam dataset dan meningkatkan kinerja model.
3. Mengintegrasikan model dengan sistem dashboard rekomendasi untuk mahasiswa dan dosen, yang memberikan peringatan dini bagi mahasiswa berisiko rendah serta saran peningkatan berdasarkan hasil model prediktif.

## Data Understandings

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Pada dataset ini menjelaskan beberapa faktor yang mempengaruhi performa ujian siswa yaitu faktor internal seperti motivasi siswa dan fakto eksternal seperti lingkungan dan keluarga yang berdampak pada performa ujian siswa. Berikut gambaran tentang fitur-fitur yang terdapat di dataset ini.
| Atribute | Description |
|---------|---------|
| Hours_Studied | Jumlah belajar siswa dalam 1 minggu dalam jam | 
| Attendance |  Persentase kehadiran siswa | 
| Parental_Involment | Tingkat keterlibatan orang tua dalam pendidikan siswa (Rendah, Sedang, Tinggi) |
| Access_to_Resoources | Ketersediaan sumber daya pendidikan (Rendah, Sedang, Tinggi)| 
| Extracurricular_Activities | Partisipasi siswa dalam ekstrakurikulre ( Iya, Tidak) |
| Sleep_Hours | Rata-rata berapa jam tidur siswa per malam |
| Previous_Scores | Nilai ujian sebelumnya |
| Motivation_Level | Tingkatan Motivasi siswa (Rendah, Sedang, Tinggi) |
| Internet_Access | Ketersediaan Internet (Iya, Tidak) |
| Tutoring_Sessions | jumlah waktu siswa menghadiri sesi tutor per bulan|
| Family_Income | Tingkatan pendapatan keluarga ( Rendaj, Sedang , Tinggi) |
| Teacher_Quality | Kualitas guru ( Rendah, Sedang, Tinggi) |
| School_Type | Jenis Sekolah (Private, Public) |
| Peer_Influence | Pengaruh teman sebaya terhadap prestasi akademik (Positif, Netral, Negatif) |
| Physical_Activity | Rata-rata jam yang dihabiskan dalam aktivitas fisik dalam 1 minggu |
| Learning_Disabilities | Adanya ketidakmampuan belajar (Ya, Tidak)|
| Parental_Education_Level | Pendidikan Orang Tua ( Sekolah Menengah Atas, Perguruan Tinggi, Pascasarjana) |
| Distance_from_Home | Jarak dari rumah (Dekat, Sedang, Jauh) |
| Gender | Jenis Kelamin siswa (Laki-Laki, Perempuan
| Exam_Score | Nilai Ujian Akhir |

### EDA

#### Visualisasi kolom bertipe kategori
<br> 
<img src="https://github.com/Junazidomi/latihan-branch/blob/main/Vis1.png" width="850" >

Kesimpulan:
1. Pada kolom Motivation Level siswa kolom medium paling tinggi 
2. Kualitas tenaga pengajar berada pada medium pada kolom Teacher Quality
3. Rata- rata siswa sudah memiliki akses ke internet sesuai dengan Internet_Access
4. Lingkunan belajar di dominasi positive dan netral sesuai dengan kolom Peer_influence
5. Keterlibatan orang tua berada pada medium pada Parental_Involment

#### Visulisasi Kolom bertipe numerik
<br> 
<img src="https://github.com/Junazidomi/latihan-branch/blob/main/Vis2.png" width="850" >

Kesimpulan:
1. Pada kolom Studied Hours, siswa paling banyak jumlah belajar adalah 20 jam per minggu
2. Pada Kolom Sleep_Hours siswa paling banyak banyak jumlah tidur adalah 7 jam per malam
3. Pada Exam Score bahwa rentang ujian siswa paling banyak adalah 65-70

#### Visualisasi antara Gender dan Motivasi siswa
<br> 
<img src="https://github.com/Junazidomi/latihan-branch/blob/main/vis3.png" width="850" >

Kesimpulan:
Motivasi belajar siswa berada pada level medium dan motivasi belajar di dominasi oleh laki-laki
#### Visualisasi antara Nilai ujian dengan jumlah waktu belajar dan persentase kehadiran
<img src="https://github.com/Junazidomi/latihan-branch/blob/main/vis5.png" width="850">

Kesimpulan:
Dapat dilihat dari grafik terdapat bahwa terdapat hubungan antara Exam Score dengan Hours_Studied dan Attedance
## Data Preparation

Proses persiapan data yang dilakukan adalah :
1. Melakukan hapus kolom Nan
   Pada bagian ini setelah dilakukan identifikasi nilai kosong atau NaN, maka dilakukan drop Nan karena nilai NaN dapat mempengaruhi kualitas model dalam melakukan prediksi 
2. Mengganti nilai tidak sesuai
   Pada bagian ini setelah melakukan identfikasi nilai max setiap kolom terdapat nilai yang tidak sewajarnya maka dilakukan perbaikan pada nilai tersebut karena akan mempengaruhi kualitas model atau akan menjadi nilai tidak sewajarnya
3. Melakukan Label Encode pada kolom kategori
   Pada bagian prepartion ini melakukan transormasi data kategori menjadi data numerical dengan menggunakan LabelEncoder sehingga data kategori bisa digunakan dalam proses modeling. Hal ini dilakukan karena ketika melakukan training model, data yang diminta adalah data numerik sehingga harus dilakukan transformasi dari kategori ke data numerik dengan menggunakan metode seperti onehot encoder, label encoder dan lain-lain
4. Melakukan pemisahan data train dan data test
   Pada Bagian ini melakukan pemisahan data train dan data test menggunakan library sklean train_test_split untuk memisahkan data dan label
6. Melakukan feature selection pada kolom yang akan digunakan
   Pada bagian ini ketika dilakukan training pada model tetapi didapat bahwa metrik evaluasi tidak maksimal maka dilakukan feature selection. Dengan cara ini dapat meningkatkan metrik evaluasi dengan memilih feature yang sesuai dengan fitur target. Metode yang biasa digunakan dalam melakukan feature selection yaitu Recursive Feature Elimination (RFE)
## Modeling

Dalam melakukan modeling, terdapat 4 algoritma regresi yang akan digunakan yaitu Least Angle Regression (LARS), Linear Regrssion, Random Forest Regressor dan Gradient Boosting Regressor. Tujuan di uji ke 4 algoritma tersebut adalah menentukan algoritma yang terbaik dalam memprediksi ujian siswa secara akurat dan andal

1. LARS( Least Angle Regressoon)
   LARS adalah algoritma regersi linear pada data dengan numlah fitur yang besar, bahkan lebih besar dari jumlah observasi

   Kelebihan:
   - Efisien untuk data berdimensi tinggi
   - Menghasilkan seluruh regularaztion path
   - Cepat dan ringan secara komputasi
      
   Kekurangan:
   - Tidak cocok data linear
   - Kurang fleksibel dibandingkan embedde method
   - Rentan terhadap noise
      
3. Linear Regression
   
   Linear Regression adalah algoritma yang mencoba menemukan garis lurus terbalik yang menggambarkan hubungan antara variabel independen (X) dengan variabel dependen (y)
   Kelebihan:
   - Sederhana dan mudah di interpretasikan
   - Cepat dan Efisien
   - Tersedia banyak Tools
     
   Kekurangan:
   - Hanya untuk hubungan linear
   - Sensitif terhadap outlier
      
3. Random Forest Regressor
   Random Forest Regressor adalaah algoritma prediktif ensemble decision tree yang meggabungkan beberapa tree dengan tujuan menghasilkan metrik yang optimal
   
   Kelebihan:
   - Akurasi tinggi
   - Mengurangi overfitting
   - Dapat menangani data non linear dan kompleks

   Kekurangan:
   - Kurang interpratif
   - Komputasi Berat
   - Kurang efisien untuk data real time atau low latency

   Improvement:
   Paremeter awal sebelum hypertune:

   - max_depth=None
   - min_samples_leaf=1
   - min_samples_split=2
   - n_estimators=500
   - 
   Evaluasi sebelum hypertune:
   - MAE= 0.336518	
   - MSE= 0.417358	
   - R2_Score= 0.571506

   Parameter setelah hypertune:
   - max_depth=20
   - min_samples_leaf=2
   - min_samples_split=5
   - n_estimators=200

   Evaluasi setelah hypertune:
   - MAE= 0.336518	
   - MSE= 0.417358	
   - R2_Score= 0.571506
   - 
5. Gradient Boosting Regressor
   Gradient Boosting Regressor adalah algoritma ensemble yang membangun model prediktif dalam bentuk sekumpulan pohon keputusan lemah yang dilatih secara berurutan untuk memperbaiki kesalahan dari model sebelumnya

   Kelebihan:
   - Akurasi tinggi
   - Bekerja baik pada data non linear
   - Dapat disesuaikan (fleksibel)

   Kekurangan :
   - Lambat dilatih
   - Rentan terhadap overfitting jika tidak di hypertune

   Improvement
   
   Parameter sebelum hypertune :
   - n_estimators=100
   - learning_rate=0.1
   - subsample=1.0
   - max_depth=3
     
   Evaluasi sebelum hypertune:
   - MAE=0.302242		
   - MSE= 0.360173
   - R2_Score= 0.645183

   Paremeter setelah hypertune:
    - n_estimators=100
   - learning_rate=0.8
   - subsample=1.0
   - max_depth=3

   Evaluasi setelah hypertune:
   - MAE= 0.297802		
   - MSE= 0.357524
   - R2_Score=0.647792
     
## Evaluation
