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
  
4. Lakukan ping ke alamat ip anda dan coba lakukan reject dan drop di webmin, lalu analisis apa yang terjadi?  
  
5. Buatlah perintah otomatis yang berfungsi untuk ping www.filkom.ub.ac.id  
