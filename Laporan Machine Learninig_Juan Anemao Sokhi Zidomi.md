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

1. Menggunakan algoritma mesin seperti LARS, Linear Regression dan lain-lain untuk membangun model prediktif untuk menentukan nilai Ujian siswa berdasarkan karakteristik 
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

