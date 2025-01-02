# Prediksi Genre Lagu Menggunakan Algoritma KNN

## **Table of Content**
1. [**Pendahuluan**](#Pendahuluan)
2. [**Pemahaman Data**](#Pemahaman-Data)
3. [**Deskripsi Model**](#Deskripsi-Model)
4. [**Hasil Pemodelan**](#Hasil-Pemodelan)
5. [**Team**](#Team)

### **Pendahuluan** 
Musik adalah bagian integral dari kehidupan manusia, menghubungkan emosi dan budaya. Dalam era digital, platform streaming seperti Spotify menyediakan akses ke jutaan lagu sekaligus menawarkan metadata yang kaya untuk dianalisis.

Proyek ini memanfaatkan dataset yang diambil melalui paket spotifyr, mencakup 5.000 lagu dari enam genre utama: EDM, Latin, Pop, R&B, Rap, dan Rock. Tujuan utama proyek ini adalah:
1. Memahami fitur audio yang unik dari setiap lagu.
2. Memanfaatkan fitur tersebut untuk memprediksi genre dengan model KNN.

**Relevansi Proyek:**
Proyek ini mendukung analisis tren musik, pengelolaan playlist, dan personalisasi pengalaman pengguna pada platform streaming.

### Pemahaman Data
**Sumber Dataset:**
Dataset berasal dari Spotify melalui paket spotifyr, yang dikembangkan untuk mengakses metadata lagu dengan mudah. Data ini mencakup lagu-lagu dari enam kategori utama yang dipilih secara acak.

**Deskripsi Variabel Utama:**
- Metadata Lagu:
track_id, track_name, track_artist, track_album_name, track_album_release_date, track_popularity.
- Fitur Audio:
danceability, energy, key, loudness, mode, speechiness, acousticness, instrumentalness, liveness, valence, tempo, duration_ms.
- Genre dan Playlist:
playlist_name, playlist_id, playlist_genre, playlist_subgenre.

**Fungsi Subkelompok**
- Genre Lagu: Genre (EDM, Latin, Pop, R&B, Rap, Rock) merupakan variabel target utama, dan setiap genre memiliki karakteristik unik berdasarkan fitur audio seperti danceability, energy, dan tempo.
- Playlist Subgenre: Subgenre dapat memberikan informasi tambahan untuk mengelompokkan lagu berdasarkan tema atau suasana, yang mungkin lebih relevan untuk beberapa analisis.
- Popularitas Lagu: Subkelompok lagu dengan skor track_popularity tinggi dapat menunjukkan pola tertentu, seperti lagu dengan energi atau danceability tinggi lebih cenderung populer.
- Konteks Akustik: Lagu dengan nilai tinggi pada acousticness atau instrumentalness mungkin memiliki pola berbeda dibandingkan lagu dengan karakteristik sebaliknya.

**Fungsi Tren dari Waktu ke Waktu**

Tren waktu sangat penting dalam analisis dataset ini, terutama dalam konteks:

- Tanggal Rilis Album ```track_album_release_date``` : Tren musik dapat berubah dari waktu ke waktu, dan genre tertentu mungkin lebih dominan pada periode tertentu. Lagu lama mungkin memiliki nilai popularity lebih rendah dibandingkan lagu yang dirilis baru-baru ini.
- Perubahan Preferensi Audiens: Preferensi audiens terhadap atribut seperti energy atau tempo mungkin berubah seiring waktu.
- Inovasi Musik: Inovasi dalam genre tertentu, seperti penggunaan elemen akustik yang lebih tinggi dalam Pop modern, dapat menjadi tren menarik untuk dieksplorasi.

**Visualisasi Awal:**
- Distribusi Popularitas Lagu

  ![image](https://github.com/user-attachments/assets/647d973b-605f-4b41-80a5-dd5d71257eab)
- Korelasi Antar Atribut Audio
  
  ![image](https://github.com/user-attachments/assets/9507506a-fe6f-40b7-9003-a249ef775aa1)
- Rata-Rata Popularitas Lagu Berdasarkan Genre
  
![image](https://github.com/user-attachments/assets/1787fb39-2dbd-45ef-81ab-856d88a163b6)
- Durasi Lagu vs Popularitas
  
![image](https://github.com/user-attachments/assets/a3767ca4-c143-48ab-8b78-4f51abaed348)
- Rata-Rata Popularitas Lagu Berdasarkan Tahun Rilis
  
![image](https://github.com/user-attachments/assets/d9b70af9-5e96-42e4-a67e-9e3ed09e3165)
- Distribusi Popularitas Berdasarkan Genre
  
![image](https://github.com/user-attachments/assets/561a00d6-d106-4ee8-b192-58949c241cde)
- Durasi Rata-Rata dan Pupularitas Berdasarkan Genre
  
![image](https://github.com/user-attachments/assets/f6e12873-597c-478e-bdd7-188bd36722d3)
- Distribusi Tingkat Energi dan Keakustikan Berdasarkan Genre
  
![image](https://github.com/user-attachments/assets/c96510cd-8fcc-4bcf-abac-824602428879)

### Deskripsi Model
#### K-Nearest Neighbor (KNN)
**Architecture**

![images](https://github.com/user-attachments/assets/8281a816-2ccf-41bc-b686-920138c3e259)

**Preprocesing**
- Handle Missing Value
- Normalization
- Encoding
- Train Data (80% Training data, 20% Test Data)

### Hasil Pemodelan 
- Classification Report
  
  ![image](https://github.com/user-attachments/assets/cf359cec-d7c2-4304-961a-8bd7501d7044)

- Confussion Matrix
  
  ![image](https://github.com/user-attachments/assets/6f74229b-d2c0-4091-8922-7b5eaac5b846)

### Team 
1. Riswanda Rafakansyah Hanandayu (202110370311357)
2. Annisa Nela Fadhila (202110370311396)
3. Nabila Romadhona (202110370311411)
