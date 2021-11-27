# Jaringan Komputer C-09 (2021)
Laporan Resmi Jaringan Komputer Modul 4 - Subnetting and Routing

NRP              | Nama
-----------------|-----------
05111940000014   | Ega Prabu Pamungkas
05111940000178   | Muhammad Rizqullah Akbar
05111940000227   | Rayhan Daffa Alhafish


# VLSM (Variable Length Subnet Masking) - CPT
## Penentuan Subnet pada Topologi 

Sebelum melakukan perhitungan Subnetting dan melakukan labelling kita perlu melakukan penentuan subnet pada topologi. Untuk dapat menentukannya kita perlu melakukan labelling pada topologi. <br> 

![img](https://github.com/rayhandaffa/Jarkom-Modul-4-C09-2021/blob/main/img/VLSM_Gambar.jpeg)

## Perhitungan Subnet

Langkah pertama yang perlu kita lakukan adalah melakukan penentuan jumlah alamat IP yang dibutuhkan untuk setiap subnet dan lakukakan labelling netmask berdasarkan jumlah IP yang dibutuhkan. <br> 

![img](https://github.com/rayhandaffa/Jarkom-Modul-4-C09-2021/blob/main/img/vlsm%20table.jpg) <br>

Berdasarkan total IP dan netmask yang dibutuhkan, kita dapat menggunakan netmask /19 untuk memberikan pengalamatan IP pada subnet. Selanjutnya, kita perlu melakukan pembagian IP berdasarkan NID dan netmask yang telah dihitung sebelumnya dan melakukan subnetting. Untuk hasil tree pun akan menjadi seperti di bawah ini : <br> 

![img](https://github.com/rayhandaffa/Jarkom-Modul-4-C09-2021/blob/main/img/vlsm_tree.jpeg) <br>

Setelah mendapatkan hasil dari tree, selanjutnya kita melakukan pembagian IP sehingga di dapatkan tabel di bawah ini: <br> 

![img](https://github.com/rayhandaffa/Jarkom-Modul-4-C09-2021/blob/main/img/vlsm_pembagian_ip.jpg) <br> 

## Konfigurasi Routing
Untuk melakukan konfigurasi pada routing hal pertama kita perlu membuat sebuah topologi di CPT. <br> 

![img](https://github.com/rayhandaffa/Jarkom-Modul-4-C09-2021/blob/main/img/topolog-cpt.jpeg) <br>

Setelah membuat topologi di CPT, selanjutnya perlu kita mengatur IP untuk masing-masing interface yang ada di setiap device sesuai dengan pembagian subnet pada pohon VLSM.

1. Foosha <br> 
    ![img](https://github.com/rayhandaffa/Jarkom-Modul-4-C09-2021/blob/main/img/vlsm-routing-foosha-1.jpeg) <br>
    ![img](https://github.com/rayhandaffa/Jarkom-Modul-4-C09-2021/blob/main/img/vlsm-routing-foosha-2.jpeg) <br>
2. Guanhao <br> 
    ![img](https://github.com/rayhandaffa/Jarkom-Modul-4-C09-2021/blob/main/img/vlsm-routing-guanhao.jpeg) <br>
3. OIMO<br>
    ![img](https://github.com/rayhandaffa/Jarkom-Modul-4-C09-2021/blob/main/img/vlsm-routing-oimo.jpeg)<br>
4. Seastone<br>
    ![img](https://github.com/rayhandaffa/Jarkom-Modul-4-C09-2021/blob/main/img/vlsm-routing-seastone.jpeg)<br>
5. Alabasta<br>
    ![img](https://github.com/rayhandaffa/Jarkom-Modul-4-C09-2021/blob/main/img/vlsm-routing-alabasta.jpeg)<br>
6. Water7 <br>
    ![Img](https://github.com/rayhandaffa/Jarkom-Modul-4-C09-2021/blob/main/img/vlsm-routing-water7.jpeg)<br>
7. PUCCI<br>
    ![img](https://github.com/rayhandaffa/Jarkom-Modul-4-C09-2021/blob/main/img/vlsm-routing-pucci.jpeg)<br>
 
## Testing
Jika sudah melakukan routing maka semua node dalam topologi yang telah dibuat bisa melakukan ping satu sama lain dan ping ke internet. Untuk contoh kami menggunakan ping `cispher` ke `EnniesLobby` dapat di bawah ini : <br> 

![img](https://github.com/rayhandaffa/Jarkom-Modul-4-C09-2021/blob/main/img/vlsm-ping-cipher-ke-enieslobby.jpeg)<br> 

Gambar di atas menunjukan bahwa ping dari `EnniesLobby` yang memiliki subnet 250 HOST ke `cipher` yang memiliki subnet 700 HOST dan menandakan routing yang dilakukan berhasil. 

# CIDR (Classless Inter Domain Routing) - GNS3

## Perhitungan Subnet

## Konfigurasi Routing

## Testing
