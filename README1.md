
# Proyek Akhir: Menyelesaikan masalah Jaya Jaya Maju

## Business Understanding
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Jaya-Jaya institut merupakan salah satu institut pendidikan perguruan yang telah bardiri sejak tahun 2000. Hingga saat ini, Jaya=-jaya institut telah mencetak banyak lulusan denan reputasi dengan baik. Namun, terdapat banyak juga siswa yang tidak menyelesaikan pendidikannya alias droput. Jumlah dropout yang tinggi ini tentunya menjadi salah satu masalah besar untuk sebuah institusi pendidikan. Oleh karena itu, Jaya-Jaya ingin mendeteksi secepat mungkin siswa yang mungkin akan melakukan dropout sehingga dapat diberi bimbingan khusus

### Permasalahan Bisnis
Permasalahan Bisnis yang di alami Jaya Institut
- Tingginya angka siswa dropout, yang berdampak pada reputasi, kualitas lulusan, dan stabilitas keuangan institusi
- Belum adanya sistem deteksi dini untuk  mengidentifikasi siswa yang berisiko tinggi mengalami dropout
- Kebutuhan akan intervensi berbasis data agar bimbingan dapat diberikan tepat sasaran kepada siswa yang membutuhkan 

### Cakupan Proyek
Berikut cakupan proyek pada proyek ini:
1. Eksplorasi dan Analisis data
   - Melakukan proses pembersihan dan mempersiapkan data untuk kebutuhan analisis
   - Melakukan Analisis dan Eksplorasi data
2. Membangun sistem machine
   - Membangun sistem machine learning untuk melakukan prediksi mahasiswa yang mengalami Dropout
3. Membangun Dashboard yang sederana
   - Mendesain dan mengimplementasikan dashboard interaktif 

### Persiapan

Sumber data: [Dataset](https://raw.githubusercontent.com/dicodingacademy/dicoding_dataset/refs/heads/main/students_performance/data.csv)

Setup environment:
- Menyiapkan Docker
   ```
       docker pull metabase/metabase:v0.46.4
       docker run -p 3000:3000 --name metabase metabase/metabase
   ```

Username dan Password Metabase:
```
   User     :root@mail.com
   Password :root123
```
## Business Dashboard
Adapun Business Dashboard yang dibuat berdasarkan segmen:
1. Berdasarkan Kondisi siswa dengan Tingkat Dropout
   
   ![Dashboard](https://raw.githubusercontent.com/Junazidomi/latihan-branch/refs/heads/main/Dashb%20(1).png)
   
   Kesimpulan:
   Dari segmen ini pada grafik Graduation status by international , didapatkan bahwa siswa yang yang mengalami droput sedikit pada kategori 'no', pada grafik kedua displaced by Graduation status siswa mayoritas dropout pada kategori 'yes'. Pada grafik ke 3, dapat disiumpulkan yang tidak mengalami dropout pada kategori 'no ' pada scholarship holder
   
3. Berdasarkan metode pendaftaran dan urutan jurusan yang dipilih siswa dengan tingkat dropout
   
   ![Dashboard](https://raw.githubusercontent.com/Junazidomi/latihan-branch/refs/heads/main/Dashb%20(2).png)
   
   Kesimpulan:
   Berdasarkan segmen ini, dapat dilihat ada 2 garfik .Grafik pertama berdasarkan pemilihan urutan jurusan siswa, pada pilihan 1 banyak siswa mengalami dropout dan yang paling banyak graduate, sedangkan pada grafik ke 2, metode pendaftaran 1 memiliki banyak graduate dan kategori other paling banyak kasus dropout
   
3. Berdasarkan apakah siswa debtor dan gender dengan tingkat dropout
   
   ![Dashboard](https://raw.githubusercontent.com/Junazidomi/latihan-branch/refs/heads/main/Dashb%20(4).png)
   
   Kesimpulan:
   Berdasarkan segmen ini dibagi menjadi 2 yaitu gender dan debtor.Berdasarkan grafik gender by Graduation Status, bahwa yang female dan male memiliki proporsi sama DropOut dan yang paling banyak Graduate adalah Female, sedangkan pada grafik debtor by  GraduationStatus bahwa kasus dropout mahasiswa paling sedkit pada kategori 'no '
4. Berdasarkan kategori Admission Grade dengan tingkat dropout
   
   ![Dashboard](https://raw.githubusercontent.com/Junazidomi/latihan-branch/refs/heads/main/Dashb%20(3).png)

   Kesimpulan:
   Berdasarkan grafik  diatas, kategori admission grade low memiliki banyak student dropout dibandingkan dengan kategori lain, dan yang paling sedikit pada kategori very high. Untuk siswa graduated  paling banyak kategori Low dan yang paling sedikit Very High
   

## Menjalankan Sistem Machine Learning
Cara Menjalankan sistem machine learning 
- Membuat dan Mengaktifkan Virtual Environment
   ```bash
      python   -m venv venv
   ```
- Aktifkan Environment
  - Windows
    ```bash
    venv\Scripts\activate
    ```
  - MacOS/Linux
    ```bash
    source  venv/bin/activate
    ```
- Install Dependecies
    ```bash
    pip install -r requirements.txt
    ```
- Jalankan Web App
  ```bash
    streamlit run Tugas.py
    ```
Link Untuk mengakses Web App:
Web App (https://tugasml-uxunhs7mx9cn7m5ixrbx9s.streamlit.app/)


## Conclusion
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Proyek ini dapat melakukan prediksi terhadap siswa yang akan dropout di Jaya-Jaya Institute, dengan menggunakan pendekatan machine learning sehingga sistem dapat melakukan prediksi berdasarkan data yang diberikan. Selain itu, setelah dilakukan proses eksploarasi pada dataset dengan menggunakan metode feature selection di dapatkan bahwa faktor siswa akan mengalami dropout yaitu Educational_special_needs, Debtor, Tuition_fees_up_to_date, Scholarship_holder, International, Curricular_units_1st_sem_credited, Curricular_units_1st_sem_approved, Curricular_units_2nd_sem_credited, Curricular_units_2nd_sem_enrolled,dan Curricular_units_2nd_sem_approved.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Selain itu, dengan diterapkannya sistem Dashboard yang interaktif menggunakan Docker Metabase, dapat memantau kondisi teknisi dari siswa, mengidentifikasi droput  berdasarkan data serta memudahkan dalam pengambilan keputusan.Dengan adanya sistem pemantauan ini diharapkan dapat proaktif dalam memantau siswa yang mengalami dropout dan memberikan penanganan tepat.

### Rekomendasi Action Items
Rekomendasi Action Items yang dapat dilakukan oleh perusahaan Jaya Jaya Institute sebagai berikut:
- Membangun dashboard analitik untuk memantau perkembangan kondisi akademik di Jaya-Jaya Institut supaya dapat mengambil langkah selanjutnya betdasarkan data
- Membangun sistem machine learning yang dapat melakukan prediksi siswa yang mana saja yang dropout dan daapat memberikan perlakuan khusus yang tepat sasaran
- Melakukan survey pada mahasiswa untuk menilai sistem pendidikan dan mengambil langkah untuk memperbaikinya


