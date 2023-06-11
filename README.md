# UAP-Administrasi-Sistem

<div align="center">
<strong><p>Ujian Akhir Praktikum MK Administrasi Sistem - Hanifah Rahmajati - 215150700111049</p></strong>
</div>

1. Buat direktori dengan nama UAP-Adsis, isi dengan file txt dengan format penamaan catatannya-<nama kamu>.txt, kemudian isi file txt tersebut dengan nama dan NIM kamu. Kemudian atur permission view-only pada file tersebut untuk user biasa. 
Tunjukkan bukti berupa screenshot yang menunjukkan bahwa file tersebut berhasil diatur permissionnya menjadi view-only untuk user biasa.  
a. Membuat direktori UAP-Adsis dengan perintah mkdir UAP-Adsis.  
    <img src="https://i.imgur.com/ACIPPip.png" alt= "image">  
b. Membuat file catatannya-hana.txt menggunakan perintah touch catatannya-hana.txt. Masuk ke file tersebut menggunakan perintah nano catatannya-hana.txt  
    <img src="https://i.imgur.com/UUbBY46.png" alt= "image">  
c. Edit file txt dengan memasukkan nama dan NIM.  
    <img src="https://i.imgur.com/ENvefAD.png" alt= "image">  
d. Atur permission sebagai view-only untuk user biasa menggunakan perintah sudo chmod 644 catatannya-hana.txt.  
    <img src="https://i.imgur.com/w3UmnZH.png" alt= "image">  
e. Cek menggunakan perintah ls -l.  
    <img src="https://i.imgur.com/hFyYPyM.png" alt= "image">  
  
2. Lakukan konfigurasi alamat IP address sementara pada sistem dan default gateway. (petunjuk 192.168.56.x | x adalah nomor absen).  
a. Konfigurasi IP Address sementara menggunakan perintah sudo ifconfig ens33 192.168.56.6 netmask 255.255.255.0. Saya
memasukkan IP Address 192.168.56.6 sesuai dengan nomor absen saya di MK Administrasi Sistem, yaitu 6.  
    <img src="https://i.imgur.com/1hFY4cq.png" alt= "image">  
b. Verifikasi untuk memastikan alamat IP yang telah dikonfigurasi telah terdaftar dengan menjalankan perintah sudo ifconfig ens33.  
    <img src="https://i.imgur.com/Yg6MVxI.png" alt= "image">  
c. Konfigurasi IP Addres Default Gateway menggunakan perintah sudo route add default gw 192.168.56.6 ens33. Digunakan IP Address yang sama dengan perintah sebelumnya.  
    <img src="https://i.imgur.com/dhcy3iq.png" alt= "image">  
d. Jalankan perintah sudo route -n untuk memastikan bahwa alamat IP Default Gateway sudah terdaftar.  
    <img src="https://i.imgur.com/3RcW6PG.png" alt= "image">  
  
3. Lakukan Instalasi Webmin lalu buatlah user bernama nama anda, lalu buat group Adsis_(kelas masing-masing) dan masukkan nama anda di group.  
a. Masuk ke direktori file /etc/apt/sources.list menggunakan sudo nano /etc/apt/sources.list. Tambahkan deb http://download.webmin.com/download/repository sarge contrib pada akhir baris.  
    <img src="https://i.imgur.com/DwpfKiM.png" alt= "image">  
    <img src="https://i.imgur.com/EW8TsaG.png" alt= "image">  
b. Menambahkan kunci PGP Webmin agar sistem dapat mempercayai repository baru dengan perintah:  
    wget http://www.webmin.com/jcameron-key.asc  
    <img src="https://i.imgur.com/YwvNZCf.png" alt= "image">  
    sudo apt-key add jcameron-key.asc  
    <img src="https://i.imgur.com/sKXWN8B.png" alt= "image">  
c. Menjalankan perintah sudo apt get install webmin untuk menginstall webmin.  
    <img src="https://i.imgur.com/iQ0RSfA.png" alt= "image">  
d. Untuk mengakses halaman webmin dapat dilakukan menggunakan web browser. Akses halaman Webmin dengan alamat IP dari server Webmin dan port 10000 dengan perintah https://alamatipwebmin:10000. Akses melalui https://192.168.76.128:10000  
    <img src="https://i.imgur.com/7mwBmt6.png" alt= "image">  
e. Setelah itu login dengan username dan password dari akun server yang telah dimiliki. Login menggunakan username dan password Ubuntu.  
    <img src="https://i.imgur.com/7mwBmt6.png" alt= "image">  
f. Mengakses Users and Group pada webmin untuk membuat user baru.  
    <img src="https://i.imgur.com/fXJU2EO.png" alt= "image">  
g. Membuat user baru dengan nama hanifahr.  
    <img src="https://i.imgur.com/P15BRN6.png" alt= "image">  
    User hanifahr berhasil dibuat.  
    <img src="https://i.imgur.com/Vo7U4cY.png" alt= "image">  
h. Membuat group baru dengan nama Adsis_E sesuai dengan kelas MK Administrasi Sistem saya.  
    <img src="https://i.imgur.com/7cTcHgg.png" alt= "image">  
    Grup Adsis_E berhasil dibuat.  
    <img src="https://i.imgur.com/QvzFfGE.png" alt= "image">  
i. Tambahkan user hanifahr yang baru dibuat pada perintah sebelumnya ke dalam group Adsis_E.  
    <img src="https://i.imgur.com/rD4UrRz.png" alt= "image">  
    User hanifahr berhasil ditambahkan ke grup Adsis_E.  
    <img src="https://i.imgur.com/DOF63ab.png" alt= "image">  

4. Lakukan ping ke alamat ip anda dan coba lakukan reject dan drop di webmin, lalu analisis apa yang terjadi?  
    a. Ping alamat IP saya menggunakan perintah ping 192.168.76.128 -t.  
    <img src="https://i.imgur.com/sfDA0YL.png" alt= "image">  
    b. Akses Networking -> Linux Firewall pada Webmin. Pada bagian Incoming Packets (INPUT) pilih Add rule dan atur rule atas Incoming Packets (INPUT) untuk me-reject ping. Apply configuration.  
    <img src="https://i.imgur.com/MV0coko.png" alt= "image">  
    <img src="https://i.imgur.com/l9Uw1NV.png" alt= "image">  
    c. Ping berubah menjadi Destination net unreachable karena setting INPUT sudah diubah menjadi reject.  
    <img src="https://i.imgur.com/w2HLmpR.png" alt= "image">  
    d. Atur juga konfigurasi untuk drop Incoming Packets (INPUT). Ping berubah menjadi Request timed out karena setting INPUT sudah diubah menjadi drop.  
    <img src="https://i.imgur.com/Y8NlgeX.png" alt= "image">  
  
5. Buatlah perintah otomatis yang berfungsi untuk ping www.filkom.ub.ac.id  
