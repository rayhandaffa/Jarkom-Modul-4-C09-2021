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

Langkah pertama dalam menggunakan metode CIDR adalah menentukan subnet yang ada dalam topologi dan lakukan labeling netmask terhadap subnet-subnet yang sudah ditentukan. Setelah itu lakukan penggabungan subnet-subnet yang lebih kecil. Dari proses penggabungan yang telah dilakukan, akan didapatkan subnet besarnya dan netmasknya secara keseluruhan.

![Subnetting](/img/CIDR_Gambar.jpeg)

Selanjutnya hitung pembagian IP dengan pohon berdasarkan penggabungan subnet yang telah dilakukan, tidak lupa menggunakan *prefix IP* yang telah ditentukan.

![Tree](/img/cidr_tree.jpg)

Selanjutan berdasarkan perhitungan yang sudah dilakukan, maka dilakukan pembagian IP sebagai berikut

![Table](/img/CIDR_Table.png)

## Konfigurasi Routing

Untuk melakukan konfigurasi routing hal pertama kita perlu membuat topologi pada GNS3 terlebih dahulu.

![Topologi](/img/topologi-gns3.jpeg)

Selanjutnya kita mengatur ip pada masing-masing interface dengan perhitungan yang telah dilakuakan.

1. Foosha

![Foosha](/img/cidr-routing-foosha.jpeg)

2. Guanhao

![Guanho](/img/cidr-routing-guanhao.jpeg)

3. Oimo

![Oimo](/img/cidr-routing-oimo.jpeg)

4. Seastone

![Seastone](/img/cidr-routing-seastone.jpeg)

5. Alabasta

![Alabasta](/img/cidr-routing-alabasta.jpeg)

6. Water7

![Water7](/img/cidr-routing-water7.jpeg)

7. Pucci

![Pucci](/img/cidr-routing-pucci.jpeg)

## Testing

Setelah melakukan konfigurasi pada topologi yang telah dibuat. kita bisa melakukan pengetesan apakah konfigurasi berhasil dengan melakukan ping antar node.

![Test-CIDR](/img/cidr-ping-elena-ke-jipangu.jpeg)

Pada contoh testing ini kita melakukan ping dari Elena ke Jipangu dengan IP Address 192.188.40.2.