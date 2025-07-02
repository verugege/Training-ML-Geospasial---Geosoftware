# Sesi 6: Algoritma Supervised Learning Lanjutan untuk Data Raster

## Metode Validasi Silang Spasial (Spasial Cross Validation)
- Leave-One-Area-Out : Melatih model di semua area, KECUALI SATU dan menguji di area yg ditinggalkan tadi
- Block Cross-Validation : Membagi wilayah menjadi blok blok / grid dan melakukan k-fold berdasarkan blok

![image](https://github.com/user-attachments/assets/8c5753e2-7661-4ee3-adb4-aabc7a7f1f2a)

## Klasifikasi Citra
- Pendekatan berbasis pixel
- Pendekatan berbasis objek (area sudah diklasifikasikan sesuai kemiripan band)

![image](https://github.com/user-attachments/assets/3969ad44-c3f6-4f10-a646-686b25edb278)

## Metrik Evaluasi Klasifikasi

- Accuracy
- precision - ketepatan (contoh model untuk check email spam atau tidak - kepercayaan sistem)
- Recall - model yng digunakan menemukan semua data (kelengkapan) contoh model mencari kanker atau tidak
- F1 Score - kasus data yang tidak seimbang (ketika jumlah instance positif dan negatif sangat berbeda


![image](https://github.com/user-attachments/assets/f99fdd8a-2e0e-4210-b0e7-2b0353a8cc24)

## Lanjut Latihan Gcolab
Image : menggunakan image sebagai prediktor

Mask : sebagai Label, unutk menentukan label bisa di digitasi mannual agar hasilnya bagus, karena proses label ini paling penting (penyediaan kunci jawaban)

![image](https://github.com/user-attachments/assets/24264028-c9dc-4716-94cd-d1b88d096be6)

dari data itu di preprocessing dulu sehingga bisa di olah oleh machine learning

![image](https://github.com/user-attachments/assets/50571bc2-d504-427b-bc28-dbb880876609)
