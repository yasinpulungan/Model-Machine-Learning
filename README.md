Capstone Modul 3 - Travel Claim 

# 1 Business Problem

## 1.1 Context 
Dalam memulai awal tahun sebuah perusahaan asuransi  asal Singapura ingin menyusun rencana anggaran keuangan untuk setahun kedepan. Dari data customer yang melakukan dan tidak melakukan claim sebelumnya, perushaan ingin memprediksi siapa saja customer yang akan melakukan claim kedepannya agar perusahaan membuat renca keuangan yang baik serta dapat mengalokasikan keuangan untuk diputar pada bisnis lainnya.


## 1.2 Problem Statement
Perusahaan dalam membuat rencana anggaran, ingin memprediksi pada produk asuransi perjalanan mereka manakah customer yang akan melakukan claim serta yang tidak akan melakukan claim, agar perusahaan dapat menyiapkan dana tidak bergerak yang dibutuhkan, agar perushaan tetap memiliki dana yang cukup, apabila sewaktu-waktu customer melakukan claim, dan dana lainnya tetap bisa digunakan untuk mengembangkan bisnis lainnya.


## 1.3 Goals
Dengan bantuan machine learning kita ingin memprediksi customer mana saja yang akan melakukan claim dan mana yang tidak melakukan claim, dari hasil yang didapatkan kita akan memberikan perkiraan dana tidak bergerak yang akan dibutuhkan perusahaan untuk tetap diam dan tidak dipergunakan untuk bisnis lainnya, sehingga perusahaan tetap bisa mencairkan dana claim customer dan membuat citra perusahaan tetap baik serta dapat mengalokasikan dana yang diperlukan untuk mengembangkan bisnis lainnya.

## 1.4 Analytic Approach
Dari feature-feature yang telah dipilih nanti, kita akan membuat model klafikasi untuk memprediksi customer mana yang berpotensi untuk melakukan claim dan customer mana yang tidak akan melakukan claim asuransi.

## 1.5 Matrix Evaluation 

Target :                 
* 1 : Customer Melakukan Claim                 
* 0 : Customer Tidak Melakukan Claim            

![image-2.png](attachment:image-2.png)

* TP = dapat memprediksi customer yang berpotensi untuk melakukan claim
* TN = dapat memprediksi customer yang tidak akan melakukan claim
* FP = salah memprediksi customer yang berpotensi melakukan claim asuransi tetapi kenyataanya tidak melakukan claim asuransi   
    cons : Terjadinya idle cash yang mengakibatkan tidak produktifnya perencanaan keuangan perusahaan
* FN = salah memprediksi customer yang tidak akan melakukan claim asuransi tetapi kenyataanya customer melakukan claim asuransi <br>
    cons : Perusahaan memerlukan dana yang tidak dipersiapkan sebelumnya yang mengakibatkan claim jadi lebih lambat dan reputasi perusahaan menurun
    

Berdasarkan problem statement disini kita tidak ingin salah dalam memprediksi customer mana yang akan melakukan claim dan tidak, dari konsekuensi yang diberikan disini kita ingin menekan nilai False Positive (FP) dan False Negative (FN). agar memastikan prediksi yang kita lakukan sesuai. dari data yang diberikan, kita melihat bahwa data yang diberikan merupakan data imbalance. oleh karena itu matrix evaluasi yang kita pilih ialah yang memiliki nilai F1 yang paling tinggi.


#  Kesimpulan

Model yang dipilih adalah XGBoost Random Under Sampling Setelah Hyperparameter Tuning


