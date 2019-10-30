---
layout: page
title: Usecase Diagram
permalink: /Usecase/
nav_order: 3
---

<img src="{{site.baseurl}}/assets/image/use-case.png">  
<br>
<br>

<h1><center> PENJELASAN USECASE GEOTAG PAUD </center></h1>

<hr>

## Login
<p> Usecase ini mencakup Skenario ketika user membuka aplikasinya, maka sistem akan memunculkan login dialog, maksud dari  login dialog tersebut ialah user diminta untuk  memasukkan username/email dan password lalu mengklik ok, agar dapat menggunakan aplikasi tersebut.</p>
<p> Jika benar maka user akan diarahkan kepada home fragment. Namun ketika user ada kesalahan dalam pengisian tersebut maka akan muncul pesan error dan user tidak diarahkan kemana - mana dan jika user tidak ada internet maka user tidak dapat login.</p>

<hr>

## Show Data
<p> Didalam usecase ini ketika user berhasil login, maka sistem akan mengambil data dari database dan sistem akan menampilkan data tersebut di Home Fragment dan Data Fragment.</p>

<hr>

## Take Photo
<p> Fungsi utama dari usecase ini adalah user mengmabil foto dan sistem akan menampilkannya di gallery fragment, yaitu caranya dengan user mengklik atau mengslide layout sampai ke gallery fragment, lalu user mengklik icon kamera di bawah, kemudian user menentukan jenis foto tersebut dan memberikan judul foto tersebut, setelah itu user mengklik ambil foto, selanjutnya user akan diarahkan ke kamera untuk mengambil foto, bila sudah user mengklik ceklis dan sistem akan memunculkannya di gallery fragment.</p>
<p> Fungsi lain dari usecase ini ialah User juga dapat melihat, mengambil ulang dan menghapus foto tersebut dengan cara mengklik foto yang sebelumnya diambil dan ketika diklik maka akan muncul tiga pilihan diatas.</p>

<hr>

## Get Location
<p> Fungsi usecase ini ialah user menyimpan posisi atau lokasi sekolah tersebut di server, dengan cara user mengklik atau mengslide layout sampai ke geotag fragment, lalu user mengklik icon marklocation (disebelah atas kanan maps), kemudian user diminta untuk menunggu sampai button (Menerima sinyal gps) berubah menjadi warna biru, setelah itu bila button sudah berwarna biru user diharapkan untuk mengklik button teresebut, lalu lokasi tersebut akan dikirim ke server yang kemudian disimpan juga didalam server.</p>
<p> Di usecase ini user juga bisa melakukan koreksi lokasi atau pindah lokasi bila saat penentuan lokasi awal kurang tepat.</p>

<hr>

## Send Data
<p> Usecase ini berfungsi untuk mengirim seluruh data sekolah ke server dan kemudian server menyimpannya, dengan cara user mengklik drawer (icon paling atas sebelah kiri) kemudian user mengklik Send Data.</p>

<hr>

## Help
<p> Usecase ini berfungsi untuk membantu user apabila ada suatu keluhan, kesalahan atau user kurang mengerti mengenai aplikasi ini, dengan cara user mengklik drawer (icon paling atas sebelah kiri) kemudian user mengklik Bantuan.</p>

<hr>

## Info
<p> Usecase ini berfungsi untuk memberitahu user tentang informasi singkat aplikasi tersebut, dengan cara user mengklik drawer (icon paling atas sebelah kiri) kemudian user mengklik Tentang.</p>

<hr>

## Logout
<p> Usecase ini berfungsi, apabila user ingin keluar dari akun yang sedang ia gunakan, dengan cara user mengklik drawer (icon paling atas sebelah kiri) kemudian user mengklik Logout.</p>