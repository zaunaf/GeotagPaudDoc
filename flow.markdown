---
layout: page
title: Flow Diagram
permalink: /flowDiagram/
nav_order: 6
---

# Flow Diagram 
&nbsp; &nbsp; Untuk Dokumentasi Geotag Paud kami juga menggunakan Flow Diagram untuk menjelaskan Fitur Galeri dari Aplikasi Geotag Paud ini. 

## &nbsp; Flow Diagram Galeri <br/>
 &nbsp; &nbsp; &nbsp; Galeri adalah bagian dari Aplikasi Geotag Paud yang memungkinkan pengguna untuk mengambil Foto,
 Menghapus, atau Mengganti Foto apabila terjadi kesalahan. Disini pengguna juga bisa mengambil Foto Operator yaitu Foto pengguna
 yang menjadi Operator dari Sekolah / Paud tersebut<br/>

<img src="{{site.baseurl}}/assets/image/GaleriFlow.jpeg">

<!--<br/> &nbsp; &nbsp; &nbsp; Ketika membuka Galeri, GaleriFragment akan mempersiapkan (prepare) beberapa hal terlebih dahulu seperti mempersiapkan 
Auth,Preferensi,Floating Action Button, serta Path penyimpanan Foto. Foto yang diambil akan tersimpan di penyimpanan Lokal Android. 

<br/> &nbsp; &nbsp; &nbsp; Ketika Pengguna mengambil Foto maka Foto akan tersimpan sesuai dengan Path yang ditentukan. Ketika User mengganti / retake Foto maka Foto yang sebelumnya akan diganti dengan Foto yang diambil ulang. Sementara ketika user menghapus / Delete Foto maka Status Foto akan diubah menjadi -1 agar Foto tidak ditampilkan di Galeri Geotag Paud.<br/><br/>-->


<br/> &nbsp; &nbsp; &nbsp; Ketika user membuka Galeri, GaleriFragment akan mempersiapkan (prepare) Auth, Preferensi yang digunakan, Path File, serta Floating Action Button. Aplikasi akan mengecek permission ke Camera dan Storage. Apabila Aplikasi tidak diizinkan untuk mengakses Camera atau Storage maka akan muncul pesan Error<br/> 

<br/> &nbsp; &nbsp; &nbsp; Apabila diizinkan, maka user bisa mengklik Floating Action Button dengan icon Kamera di pojok Kanan bawah layar. Ketika di klik maka akan muncul Dialog yang meminta User untuk memilih Jenis Foto dan memasukan Judul Foto. Setelah itu, Aplikasi akan membuka Kamera untuk mengambil Foto. Foto kemudian akan di Validasi dengan mengecek Orientasi dan Posisi Foto. Kemudian, Sistem akan membuat Thumbnail Foto di penyimpanan Lokal Android dan juga mengubah ukuran Fotonya. Kemudian Foto tersebut akan dimasukan ke Database Lokal Android dan akan di Populate agar Foto tersebut bisa muncul di GaleriFragment.<br/>

<br/> &nbsp; &nbsp; &nbsp; Kemudian, Apabila User mengklik Card Foto maka akan muncul Dialog dengan 3 pilihan yaitu "OK", "Retake", dan "Delete". Ketika User mengklik OK atau mengklik diluar area Dialog maka Dialog akan tertutup kembali. Apabila mengklik Delete maka Foto yang dipilih Statusnya akan berubah menjadi -1 yang membuat Foto data data yang berkaitan dengan Foto tersebut tidak akan ditampilkan di GaleriFragment.<br/> 


<br/> &nbsp; &nbsp; &nbsp; Apabila, User mengklik Retake, Aplikasi akan membuka Kamera untuk mengambil ulang Foto. Foto kemudian akan di Validasi dengan mengecek Orientasi dan Posisi Foto. Kemudian, Sistem akan membuat Thumbnail Foto di penyimpanan Lokal Android dan juga mengubah ukuran Fotonya Kemudian Foto tersebut akan menimpa Foto sebelumnya di Database Lokal Android dan akan di Populate kembali agar Foto tersebut bisa muncul di GaleriFragment<br/>
<br/>

