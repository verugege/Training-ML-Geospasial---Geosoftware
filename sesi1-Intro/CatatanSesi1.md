# Intro
## Tradisional Programing VS Machine Learning

![image](https://github.com/user-attachments/assets/521bd103-d304-4668-b7f9-3058bd458c3d)

Pertanyaan :
Seberapa banyak kunci jawaban yg diperlukan sehingga rules yg dihasilkan ML bisa dikatakan layak digunakan pada system?
dan bagaimana cara / metode menentukan bahwa rules yang telah dibuat layak digunakan?

jawaban :
Suatu model machine learning dapat dikatakan layak digunakan untuk system apabila telah memenuhi standar akurasi tertentu yang diharapkan.
Setiap study kasus atau data memiliki rentang standar akurasi yang berbeda tergantung tingkat kerumitan atau kompleksitas tugas/task yang dikerjakan. 
Semakin sulit task tersebut, maka rentang tingkat standar akurasinya bisa semakin rendah. 
Sedangkan semakin mudah task maka rentang standar akurasinya semakin tinggi.
Contohnya apabila memetakan tubuh air dan non-tubuh air dari citra satelit, maka task tersebut tergolong mudah, sehingga standar akurasi 90% dapat mudah didapatkan.

## Jenis Machine Learning
![image](https://github.com/user-attachments/assets/6ccc6dc5-c345-4328-bb57-83a671f5832c)

Perbedaan Supervised Learning dan Unsupervised Learning :
- Supervised Learning : kita menentukan input raw data dan melakukan labeling pada data (punya kunci jawaban)
- Unsupervised : kita menentukan kemiripan fitur2/persamaan dari data yang ada (belum punya kunci jawaban)

## Data spasial Vektor VS Raster

![image](https://github.com/user-attachments/assets/ec620c73-7c11-48c7-a6ac-15d233ec2a3e)

Pertanyaan :
apa pertimbangan untuk pemilihan data raster atau data vector kak? 

jawaban :
Pertimbangannya terkait tujuan penggunaan datanya. Apabila data yang dibutuhkan seperti citra satelit, data DEM, maka data raster dapat digunakan. Namun apabila data yang digunakan seperti batas wilayah, maka data vektor dapat digunakan.

raster : ukuran pixel menggambarkan luasan area, misal 1 pixel menggambarkan 1x1 km, 3x3 km, 10x10 m dsb
makin tinggi pixenya makin tinggi resolusinya. tapi nanti size raster akan lebih besar

## Sistem Koordinat dan Proyeksi - Geographic Coordinate System (GCS) & Projected Coordinate System (PCS)

![image](https://github.com/user-attachments/assets/493854db-35a5-405b-8511-db2118035109)

PCS lebih untuk perhitungan geometri/ jarak luas daerah
GCS untuk penetuan posisi saja, kalau untuk perhitungan mending trasnform ke PCS dl
karena nanti jika di hitung akan ada perbedaan antara PCS dan GCS

Pertanyaan :
Boleh dijelaskan lagi secara lebih sederhana kak penggunaan secara umum ML pada pengolahan data geospasial beserta aplikasinya?
Jawaban : 
ML adalah model/algortima yang dapat digunakan pada data geospasial. Artinya data geospasial digunakan sebagai input datanya, ML sebagai model/algoritmanya untuk tujuan tertentu. Contohnya adalah kita dapat menggunakan citra satelit sebagai input data untuk memetakan penutup/penggunaan lahan menggunakan model ML. Misalnya memetakan vegetasi menggunakan data citra satelit dengan model ML.


 ## Lanjut praktek di google colab
 - membuat google colab dari gdrive
 - check version python
 - import library
 - membuat dataframe
 - menghubungkan gdrive ke google colab
 - check status gdrive tersambung pada google colab atau tidak
