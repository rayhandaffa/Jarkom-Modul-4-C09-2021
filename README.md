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

## Testing

# CIDR (Classless Inter Domain Routing) - GNS3

## Perhitungan Subnet

## Konfigurasi Routing

## Testing
