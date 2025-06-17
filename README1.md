
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
- Membuat dan Mengaktifkan Virtual Envirotment
   ```bash
      python   -m venv venv
   ```
- Aktifkan Envirotment
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
## Business Dashboard
Adapun Business Dashboard yang dibuat berdasarkan segmen:
1. Berdasarkan Kondisi siswa dengan Tingkat Dropout
   ![Dashboard](https://raw.githubusercontent.com/Junazidomi/latihan-branch/refs/heads/main/Dashb%20(1).png)

2. Berdasarkan metode pendaftaran dan urutan jurusan yang dipilih siswa dengan tingkat dropout
   ![Dashboard](https://raw.githubusercontent.com/Junazidomi/latihan-branch/refs/heads/main/Dashb%20(2).png)
3. Berdasarkan apakah siswa debtor dan gender dengan tingkat dropout
   ![Dashboard](https://raw.githubusercontent.com/Junazidomi/latihan-branch/refs/heads/main/Dashb%20(4).png)
4. Berdasarkan kategori Admission Grade dengan tingkat dropout
   ![Dashboard](https://raw.githubusercontent.com/Junazidomi/latihan-branch/refs/heads/main/Dashb%20(3).png)

## Menjalankan Sistem Machine Learning
Jelaskan cara menjalankan protoype sistem machine learning yang telah dibuat. Selain itu, sertakan juga link untuk mengakses prototype tersebut.

```

```

## Conclusion
Jelaskan konklusi dari proyek yang dikerjakan.

### Rekomendasi Action Items
Berikan beberapa rekomendasi action items yang harus dilakukan perusahaan guna menyelesaikan permasalahan atau mencapai target mereka.
- action item 1
- action item 2

