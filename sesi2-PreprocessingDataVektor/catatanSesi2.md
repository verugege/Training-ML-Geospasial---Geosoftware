# 2 Preprocessing Data Vektor untuk Machine Learning

## ML terbagi 2 type :
- Supervise : kita punya data dan kunci jawaban, tinggal kita labeli data sesuai dengan kunci jawaban yang benar
- Unsupervise : ga punya kunci jawaban, tapi kita gunakan karakteristik datanya (bentuk, warna, ukuran dan tekstur)

Pada ml karena data merupakan informasi yang paling berharga sehingga pengolahan data menjadi point yg sangat penting

## Perbersihan data geospasial jenis vektor :
- Menangani geometri :
projection tidak sesuai, lokasinya tidak tepat
- Menghapus data duplikat
- Mengisi nilai yang hilang (NaN)
bisa dihapus atau di isi dengan 0 atau diisi dengan nilai default atau di isi nilai rata2, jangan sampai muncul nilai null

## UTM
jika kita punya GCS mesti konvert ke PCS karena punya perhitungan yang lebih akurat untuk pengukuran luas dan jarak
![image](https://github.com/user-attachments/assets/db5d7172-8408-4c64-9eb7-cd50d0b18a22)

![image](https://github.com/user-attachments/assets/20a91e7e-f3d1-4cce-8c13-6f53d62ef4e9)


Kenapa harus di ubah ke format EPSG?
karena EPSG adalah jenis proyeksi, biasanya kita dapat nilai koordinat jadi harus di konversi terlebih dahulu 

buka : https://epsg.io/
search : UTM zone 48S


SNI : srgi203/UTM zone 48S
dipake di Indonesia lo bro
canggih nya sudah bisa memperhitungkan pergerakan lempeng tektonik (indo terus bergerak), waktu dan gravity
sehingga akurasinya bisa lebih tinggi si srgi2013
sebenernya pake EPSG4988

tapi untuk training kali ini kita pake  WGS 84 / UTM zone 48S EPSG:32748 

## Fitur Engineering
- Fitur geometry Contoh nambah satu kolom untuk luas area
- Fitur Topologi Contoh nambah satu kolom Jarak ke objek lain misal jarak ke rumah sakit
- Fitur Kategori Contoh nambah satu kolom untuk kondisi jalan rusak/rusak parah/bagus
- Fitur numerik Contoh nambah satu kolom berisi nilai populasi, curah hujan ketinggian dan sebagainya
- Fitur Temporal berhubungan dengan waktu nambah satu kolom misal rentang waktu, tanggal pengambilan data

## Teknik label data - Label Encoding dan One hot encoding
- Label encoding : buat kolom baru dan merubah data original dibuat kolom berisi menjadi angka (rawan bencana, tinggi tsunawi, kekuatan gempa)
cocok untuk data yang punya tingkatan misal tinggi, medium, rendah
![image](https://github.com/user-attachments/assets/99b8787a-23ab-4c71-bf38-de649e7e3a18)


- One hot encoding :
contoh data merah kuning hijau / tidak punya hirarky / tingkatan gunakan one hot encoding

ML lebih mudah mengolah data numeric makanya harus di encode ke angka/numerik
![image](https://github.com/user-attachments/assets/6ef5543a-47ae-45d3-b33d-364d023a93d1)

Lanjut praktek di google colab bro
![image](https://github.com/user-attachments/assets/c5dcbef0-1a6c-4d44-a55f-97d93f214de0)


## Praktek
check data.info()
fitur (preditor)
target (label/keyword/kunci jawaban)

setelah melihat data check ada null atau tida
terus tentukan mana fitur mana target

check data.info()
type data yg digunakan mesti numeric(Float)
jadi nanti yang bentuk object mesti dirubah ke numerik dengan teknik encoding/one hot encoding

misal target resiko_kredit
fitur bisa menggunakan yng sudah ada atau membuat fitur baru dari data yg ada

kalau mau main main bisa download ata di :
https://www.indonesia-geospasial.com/p/sitemap.html

ini bro datanya harus dikonversi dulu dari GSC ke PSC
![image](https://github.com/user-attachments/assets/7cbea85a-2777-4b8a-a2a6-f8ca913c34cc)

Mas misalnya daerah nya berada di 2 zona UTM gimana? Kaya misalnya mau meneliti Jatim dan Jateng?
pilih UTM yang paling besar/bisa cek situs ini https://epsg.io



