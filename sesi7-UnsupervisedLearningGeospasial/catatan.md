# Sesi 7: Unsupervised Learning untuk Data Geospasial

Sesi ini berfokus pada algoritma clustering populer, K-Means, membahas prinsip kerjanya dan metode untuk menentukan jumlah cluster yang optimal (misalnya, metode Elbow). 
Kita juga akan mempelajari cara mengevaluasi hasil clustering menggunakan metriks internal dan eksternal. 
Lebih lanjut, sesi ini akan mendemonstrasikan aplikasi praktis clustering dalam analisis geospasial, seperti segmentasi citra satelit untuk mengidentifikasi area dengan karakteristik serupa (misalnya, jenis vegetasi, area perkotaan) 
dan konsep dasar deteksi anomali spasial untuk menemukan lokasi yang berbeda secara signifikan dari lingkungannya.

![image](https://github.com/user-attachments/assets/81e3e80f-249d-43fd-bc03-4c9a589d9f00)

## Perbedaan
Supervised -> punya kunci jawaban, harus ada labeling, data training, target

x -> fitur/prediktor 

y -> target

displite, ditraining x dan y dan baru melakukan prediction

Unsupervised

tidak perlu membagi x dan y, langsung input semua data ke model

pake K-M (K-Means), nanti si K-M akan mengklasifikasi data sesuai dengan pola/struktur dalam data/karakteristik dalam data

![image](https://github.com/user-attachments/assets/fca5ecb5-7a25-4c09-9429-ae11eecf04f5)

## Algoritma K-Means

![image](https://github.com/user-attachments/assets/1636b943-71a7-4525-8765-349a15aff6b2)

## Penentuan Nilai K (jumlah cluster)

![image](https://github.com/user-attachments/assets/e6a5dca9-00ac-415b-aefc-9d2fd06149f8)

1. Metode Elbow
mencari titik yg berupa siku, itu yg dijadikan nilai (gambar contoh idealnya, tapi biasa keadaan real memang agak sulit untuk melihat elbow nya

kalau grafiknya tdk terlihat siku gmn kak?

nah kalau tidak terlihat siku

menggunakan method Silhouette Score

2. Silhouette Score

![image](https://github.com/user-attachments/assets/1e027fec-b7c7-4f42-8d8e-1ed659941654)

Jumlah K = 2 
karena nilai Silhouette Score paling tinggi yaitu 0.50

## Lanjut ke colab

![image](https://github.com/user-attachments/assets/6ae760b7-5705-4269-a2da-140032d690ec)

rencananya akan membagi / mengkelompokan nilai 

R = 0 - 255

G = 0 - 255

B = 0 - 255

nanti kita cari apakah dia akan menjadi berapa cluster/kelas dari tiap warna tersebut

## Persiapan data

![image](https://github.com/user-attachments/assets/a9310ec9-0a3b-4d88-82e6-e18c0b8451d7)

merubah nilai 3D (Band, Height, Width) -> menjadi data tabular


## mentukan K pake elbow

![image](https://github.com/user-attachments/assets/4d7bb548-ce3f-4190-8bf8-bca91d935363)
cara menentukan elbow nya cari selisi antar K

Nilai dimana titik - titik selanjutnya paling kecil dari yg lain
![image](https://github.com/user-attachments/assets/dc364e1c-2bee-489a-becf-5fe617088152)

## Analisa hasil
![image](https://github.com/user-attachments/assets/565e3224-d1a6-402c-8207-40ed767de1a9)

- Cluster 0 = lahan terbuka
- Cluster 1 = noise / awan
- Cluster 2 = Tanah perkotaan
- Cluster 3 = Vegetasi 

