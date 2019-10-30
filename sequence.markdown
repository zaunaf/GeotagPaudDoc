---
layout: page
title: Sequence Diagram
permalink: /sequenceDiagram/
nav_order: 5
---

# Sequence Diagram 
&nbsp; &nbsp; Berikut adalah Proses proses yang terjadi dalam Aplikasi "GeoTag Paud" dijelaskan mengunakan Sequence Diagram :

## &nbsp; 1. Sequence Diagram Login
<br/> &nbsp; &nbsp; &nbsp; Login adalah ketika Pengguna Aplikasi memasukan E-mail dan Password untuk mengakses Aplikasi.
Akun yang digunakan untuk Login disini adalah Akun yang sudah terdaftar dan terhubung dengan PAUD tertentu<br/>

<img src="{{site.baseurl}}/assets/image/login.png">

&nbsp; &nbsp; **User :** Pengguna Aplikasi GeoTag Paud yang sedang Login<br/>

&nbsp; &nbsp; **Login Dialog :** Dialog yang muncul untuk Login<br/>

&nbsp; &nbsp; **System :** Sistem Aplikasi Geotag<br/>

&nbsp; &nbsp; **Home Fragment :** Activity Home Fragment dari Aplikasi GeoTag Paud<br/> 

&nbsp; &nbsp; **BackEnd :** Backend dari Aplikasi GeoTag Paud<br/>

&nbsp; &nbsp; &nbsp; Proses Login terjadi ketika user membuka Aplikasi. Sistem akan melakukan pengecekan terlebih dahulu, apakah User sudah login atau belum. Apabila sudah Login maka Sistem akan meminta Id, Token, beserta Data User dan Sekolah ke Backend aplikasi. dan kemudian Backend aplikasi akan memberikan data data tersebut. Selanjutnya, Sistem akan menampilkan Data User dan Sekolah di HomeFragment<br/> 

&nbsp; &nbsp; &nbsp; Apabila User belum Login maka akan dimunculkan Dialog yang meminta User untuk memasukan Email beserta Password yang terdaftar sebagai Akun di aplikasi Geotag Paud. setelah memasukan Email dan Password maka Email dan Password tersebut akan dicek. Namun, sebelumnya perlu dilakukan pengecekan
Koneksi Internet terlebih dahulu. Apabila tidak ada Koneksi Internet maka akan muncul Error dan Login Dialog<br/>

&nbsp; &nbsp; &nbsp; Apabila terdapat Koneksi Internet, Email dan Password yang dimasukan akan dicek keberadaanya. Apabila Email dan Password salah atau tidak terdaftar maka akan muncul Error dan Login Dialog. Apabila, Email dan Password yang dimasukan benar maka Backend akan memberi Id, Token, beserta Data User dan Sekolah ke Sistem aplikasi untuk kemudian akan ditampilkan Data User dan Sekolahnya di HomeFragment<br/>



## &nbsp; 2. Sequence Diagram Scraping Data

<br/> &nbsp; &nbsp; &nbsp; Scraping atau Web Scraping sendiri berarti adalah Proses ketika Aplikasi mengambil suatu data dari Website tertentu kemudian
data tersebut ditampilkan didalam Aplikasi itu tadi<br/>

&nbsp; &nbsp; &nbsp; Dalam Aplikasi ini, Web Scraping digunakan untuk mengambil Data dari Website Dapodik dan kemudian ditampilkan di dalam Aplikasi di
Data Listview<br/>

Berikut adalah Uraian Proses yang terjadi dalam Web Scraping : <br/><br/><br/>  

<img src="{{site.baseurl}}/assets/image/ScrapSeq.jpeg">

&nbsp; &nbsp; **User :** Pengguna Aplikasi GeoTag Paud yang sedang melihat Data<br/>

&nbsp; &nbsp; **DataFragment :** Activity Data Fragment<br/> 

&nbsp; &nbsp; **System :** Sistem dari Aplikasi<br/>

&nbsp; &nbsp; **Server :** Website Dapodik Paud<br/>

&nbsp; &nbsp; &nbsp; Proses Web Scraping terjadi ketika User membuka DataFragment. Disini DataFragment akan meminta data dari Website Dapodik dan kemudian
Dapodik memberikan kembali datanya kepada sistem untuk kemudian di Parsing<br/> 

&nbsp; &nbsp; &nbsp; Proses Parsing sendiri terjadi dengan mengambil Data dari Dapodik dan dimasukan kedalam Array kemudian disimpan kedalam Preference dengan selanjutnya mengubah Status untuk menandakan bahwa user sudah pernah mengambil data dari Website Dapodik. Kemudian, data yang ada di dalam Preference akan ditampilkan. Apabila data dalam preference kosong maka hanya akan muncul EmptyState. Apabila ada kesalahan ketika memparsing data maka yang akan ditampilkan adalah EmptyState juga<br/>

## &nbsp; 3. Sequence Diagram Geotag

<br/> &nbsp; &nbsp; &nbsp; Geotagging sendiri adalah proses yang memberikan suatu identitas terhadap media video, gambar atau foto maupun website yang kemudian akan disisipkan koordinat suatu tempat secara detail. 
Koordinat dan keterangan posisi yang disisipkan biasanya berupa letak koordinat bujurnya<br/>

&nbsp; &nbsp; &nbsp; Dalam Aplikasi ini sendiri Geotagging digunakan untuk menandai posisi dari TK / PAUD yang terhubung dengan ID Sekolah dari Akun Penggunanya <br/>

Berikut adalah Uraian Proses yang terjadi untuk fitur Geotag : <br/><br/><br/>

<img src="{{site.baseurl}}/assets/image/GeoSeq.png">

&nbsp; &nbsp; **User :** Pengguna Aplikasi GeoTag Paud yang sedang melihat GeoTag<br/>

&nbsp; &nbsp; **GeoTagFragment :** Activity GeoTag Fragment<br/> 

&nbsp; &nbsp; **Maps :** API Google Maps<br/>

&nbsp; &nbsp; **Dialog :** Material Dialog yang muncul untuk Interaksi<br/>

&nbsp; &nbsp; **Storage :** Penyimpanan Lokal Android<br/>

&nbsp; &nbsp; &nbsp; Proses Geo Tagging sendiri terjadi ketika User membuka Fragment Geotag. Disana Geotag Fragment akan mengambil data dari Maps untuk memperlihatkan Peta. Maps juga akan meminta lokasi  User untuk kemudian ditandai di Peta sesuai lokasi yang didapatkan.<br/> 

&nbsp; &nbsp; &nbsp; Dalam prosesnya akan terjadi pengulangan untuk membuat Lokasi menjadi lebih Akurat. Apabila Akurasinya minimal sudah mencapai 6 meter, maka Lokasi saat ini
bisa ditandai<br/>


## &nbsp; 4. Sequence Diagram Send Data<br/> 
&nbsp; &nbsp; &nbsp; Send Data disini adalah Fitur untuk mengirim data yang tersimpan di Media Penyimpanan Android ke dalam Database / Server Aplikasi. Data yang dikirim di Aplikasi ini adalah Foto foto dan juga Lokasi PAUD nya <br/>


Berikut adalah Uraian Proses yang terjadi untuk fitur Send Data : <br/><br/><br/>

<img src="{{site.baseurl}}/assets/image/SendSeq.png">

&nbsp; &nbsp; **User :** Pengguna Aplikasi GeoTag Paud yang sedang mengirim Data<br/>

&nbsp; &nbsp; **Error Dialog :** Dialog yang muncul untuk menunjukan Error<br/>

&nbsp; &nbsp; **System :** Sistem Aplikasi Geotag<br/>

&nbsp; &nbsp; **BackEnd :** Back End dari Aplikasi GeoTag Paud<br/> 

&nbsp; &nbsp; **Server :** Database utama penyimpanan data Aplikasi<br/>

&nbsp; &nbsp; &nbsp; Proses Send Data terjadi ketika user mengklik "Send Data" yang berada di Sidebar Aplikasi. Sebelumnya Aplikasi akan mengecek terlebih dahulu kesediaan Akses ke Internet.<br/> 

&nbsp; &nbsp; &nbsp; Apabila Android terhubung ke Internet maka Aplikasi akan membaca data Foto foto serta Lokasi Paud kemudian dikirimkan.Sebaliknya, apabila Android tidak terhubung ke Internet maka akan muncul pesan Error <br/>



 
