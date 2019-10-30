---
layout: page
title: Activity Diagram
permalink: /activityDiagram/
nav_order: 4
---
<img src="{{side.baseurl}}/assets/image/activityDiagram.jpeg">

# Activity Diagram

## Step 1:

User melakukan Login dengan cara mengisi kolom email dan password dari _Login Dialog_. Sistem akan mengecek akun User tersebut, jika benar maka User akan dibawa ke _HomeFragment_. Dan jika tidak benar, maka User akan tetap berada pada _Login Dialog_ sampai email dan password yang User masukkan benar. 

## Step 2:

User memilih menu sesuai kebutuhannya. Menu tersebut diantaranya :

1. **Drawer** (Dibuka dengan cara mengklik tombol garis tiga yang ada di pojok kiri atas):

	- Logout, yakni tombol untuk keluar dari akun yang sudah Login sebelumnya.

	- Kirim Data, yakni tombol untuk mengirim data dari gallery(Foto-Foto) dan geotag(Lokasi) dari User yang sedang Login.

	- Bantuan, yakni tombol yang akan mengarahkan User langsung ke browser untuk mengakses _website_ yang berisi bantuan.

	- Tentang, yakni tombol yang berfungsi untuk menampilkan dialog berisi info tentang aplikasinya.

2. **Fragment Menu** (Beberapa halaman diatas yang bisa diakses dengan cara diklik):

	- _HomeFragment_, yakni Fragment yang berisi tentang info singkat dari sekolah yang terkait pada data User yang sedang Login.

	- _DataFragment_, yakni Fragment yang berisikan info lebih detail mengenai sekolah yang terkait pada data User yang sedang Login, seperti jumlah siswa, guru, dll.

	- _GalleryFragment_, yakni Fragment yang berisikan Foto-Foto dengan kategori tertentu, seperti Plang Sekolah, Tampak Depan, dll.

	- _GeotagFragment_, yakni Fragment yang berisi Maps dan Lokasi dimana User berada sekarang.

## Step 3:

User bisa mengoperasikan masing-masing Menu berdasar kegunaannya, seperti:

1. **Drawer** (Dibuka dengan cara mengklik tombol garis tiga yang ada di pojok kiri atas):

	- Logout, dengan cara mengkliknya.

	- Kirim Data, dengan cara mengkliknya.

	- Bantuan, dengan cara mengkliknya.

	- Tentang, dengan cara mengkliknya kemudian akan muncul dialog berisi info tentang aplikasinya yang bisa ditutup.

2. **Fragment Menu** (Beberapa halaman diatas yang bisa diakses dengan cara diklik):

	- _HomeFragment_, dengan cara mengklik Fragment berjudul "Home".

	- _DataFragment_, dengan cara mengklik Fragment berjudul "Data".

	- _GalleryFragment_, dengan cara mengklik Fragment berjudul "Gallery". Didalam Fragment ini User bisa menggunakan fitur "Take Photo", "Retake Photo", dan "Delete Photo". 

		>-- Fitur "Take Photo" bisa diakses dengan mengklik tombol bergambar *kamera* lalu mengisi form dialog yang mencakup judul dan jenis. Setelahnya, User akan diarahkan untuk mengambil foto dengan aplikasi kamera yang sudah ada. Kemudian User yang ingin mengambil foto, harus mengambilnya dengan  keadaan landscape.

		>-- Fitur "Retake Photo" bisa diakses apabila User telah menambahkan foto sebelumnya. Cara mengaksesnya bisa dengan mengklik foto yang sudah tersedia, kemudian akan muncul dialog berisikan "Preview", "Delete", "Retake", dan "Ok" dimana User harus memilih "Retake" untuk mengambil ulang foto yang sudah ada judul dan jenis nya. Peraturan dan persyaratan untuk mengakses fitur "Retake Photo" sama dengan peraturan dan persyaratan untuk mengakses fitur "Take Photo".

		>-- Fitur "Delete Photo" bisa diakses apabila User telah menambahkan foto sebelumnya. Cara mengaksesnya bisa dengan mengklik foto yang sudah tersedia, kemudian akan muncul dialog berisikan "Preview", "Delete", "Retake", dan "Ok" dimana User harus memilih "Delete" untuk bisa menghapus foto.

	- _GeotagFragment_, dengan cara mengklik Fragment berjudul "Geotag". Didalam Fragment ini User bisa mengakses fitur untuk menyimpan lokasi dengan beberapa pilihan konfigurasi. Cara mengakses fitur-fitur ini adalah sebagai berikut.

		>-- Fitur menambahkan lokasi baru untuk suatu Sekolah. Fitur ini bisa diakses dengan cara mengklik tombol "Simpan Posisi" berwarna biru apabila persyaratan untuk akurasi dari lokasi nya sudah mencapai jarak yang ditentukan. Lalu akan ada dialog yang berisi "Baru/Koreksi", "Batal", dan "Pindah Posisi" dimana User harus mengklik "Baru/Koreksi" apabila sekolahnya tidak memiliki lokasi yang terdaftar sebelumnya.

		>-- Fitur memperbarui lokasi terbaru dari suatu Sekolah. Fitur ini bisa diakses dengan cara mengklik tombol "Simpan Posisi" berwarna biru apabila persyaratan untuk akurasi dari lokasi nya sudah mencapai jarak yang ditentukan. Lalu akan ada dialog yang berisi "Baru/Koreksi", "Batal", dan "Pindah Posisi" dimana User harus mengklik "Pindah Posisi" apabila sekolahnya sudah memiliki lokasi yang terdaftar sebelumnya.