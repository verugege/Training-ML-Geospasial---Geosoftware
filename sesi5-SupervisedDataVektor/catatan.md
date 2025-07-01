# Sesi 5: Algoritma Supervised Learning Lanjutan untuk Data Vektor

## Decision Tree untuk data geospasial
bisa juga buat regresi selain digunakan untuk klasifikasi

![image](https://github.com/user-attachments/assets/7224351f-51e1-480c-9863-44832fd3eab6)


Root node : node paling atas

Gini Index : 0 = murni -> dari satu kelas yang sama, 1 = tidak murni -> terdiri dari banyak kelas

jika nilai gini indek tinggi berarti ketidak murnianya tinggi gini indek mendekati 1, banyak ketegori 

jika nilai gini indek rendah mendekati 0 berarti kerancuannya rendah y=1

0 = sangat murni

1 = sangat tidak murni

entropy = seberapa acak


![image](https://github.com/user-attachments/assets/ec1c873d-c749-451d-a000-9b75ef94e4db)

"kalau dijabarkan lebih banyak bakal berat buat teman2" kata pengajar :,-(

## Random Forest untuk data geospasial

![image](https://github.com/user-attachments/assets/39d18614-a611-4801-9f83-b9c3ce512dad)

intinya random forest itu kumpulan dari decision tree

nanti hasil tiap decision tree menghasilkan output atau label dan akan dilakukan majority voting (diambil keputusan yg paling banyak) dan di state di final class

## Esemble Machine Learning (bagging dan Boosting)

![image](https://github.com/user-attachments/assets/a8eff724-0701-4190-b70a-9ff29c192556)


Bagging systemnya paralel, contoh random forest

Boosting systemnya sequential, contoh XGboost

![image](https://github.com/user-attachments/assets/cb3357e1-e0f8-47ed-b661-c31b8832f1f1)


## Fungsi Confusion Matrix
![image](https://github.com/user-attachments/assets/90dd0175-a64c-4f0a-9dd9-31586fb29916)

Pembahasan

True positive artinya positifnya yang benar yang sama artinya “Memang Iya benar”. Pengetesan ini menyatakan bahwa pasien tersebut memang benar dia positif.

Analogi: Pasien positif dinyatakan positif oleh hasil pengetesan.

True Negative bisa diartikan “Memang Tidak” yang artinya bahwa nilai dari pengetesan tersebut memang harus nilainya negative untuk menyatakan kebenaran.

Analogi: Seorang pasien yang tidak tertular dilakukan pengetesan dan hasilnya Negative. Pengetesan ini menunjukan memang benar tidak sakit.

False Positive merupakan positif palsu yang artinya dipositifkan. Nilai dari posifitnya dipalsukan.

Analogi: Seorang pasien yang tidak sakit ketika dilakukan pengetesan yang seharusnya hasilnya negative tetapi ada faktor X sehingga hasilnya diubah menjadi positive. Faktor X yang dimaksud adalah beberapa faktor yang menjadi pertimbangan atau masalah lainnya. Kategori ini adalah pasien yang dipositifkan.

False Negative adalah nilai yang dinegatifkan atau nilai negatif dipalsukan.

Analogi: Pasien yang sakit dilakukan pengetesan dan hasil yang keluar adalah positif tertular, tetapi ada faktor X yang mempengaruhi sehingga hasil yang disampaikan adalah negative. Artinya hasil pengetesan tersebut dinegatifkan. Jika ada seorang pasien yang sebenarnya sakit terus dinyatakan negatif tertular maka akan sangat berbahaya. Pasien tersebut bisa menularkan kepada orang banyak.

Terimakasih dan saya terima kritik dan saran yang membangun.

God Bless You all

## Fungsi Heatmap
Mendapatkan feature importance(korelasi antar fitur), root node(gini index & entropy),

![image](https://github.com/user-attachments/assets/91d750d0-cbc3-4502-859c-c6796fd3967d)

