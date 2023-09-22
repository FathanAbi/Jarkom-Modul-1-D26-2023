# Jarkom-Modul-1-D26-2023
Laporan Resmi Praktikum Jaringan Komputer Modul 1

* Fathan Abi Karami (5025211156)
* Alya Putri Salma (5025211174)


# No 1
User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.

## Poin A
Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut? 

Pada soal diketahui protokol yang digunakan adalah ftp. selain itu, diketahui juga bahwa aktivitas yang dilakukan adalah mengunggah file. sehingga filter yang digunakan untuk mendapatkan paket berisi aktivitas tersebut adalah "ftp contains "STOR""

screenshot:

![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/7953be7c-73ac-42a5-ae2b-109f92f28635)

dari paket diatas dapat ditemukan sequence number (raw) nya, yaitu 258040667


## Poin B
Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut? 

dengan cara yang sama dengan poin a, dapat ditemukan acknowledge number (raw) nya, yaitu 1044861039

## Poin C
Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

dengan mengikuti urutan paket yang berhasil dicapture, ditemukan paket yang berisi response untuk aktivitas tersebut

screenshot:
![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/925f3b5a-c2da-4215-afee-436bc90ece00)

dari paket diatas dapat ditemukan sequence number (raw) nya, yaitu 1044861039

## Poin D
Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

dengan cara yang sama dengan poin c, dapat ditemukan acknowledge number (raw) nya, yaitu 258040696

## flag
![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/6c7332c9-2b4d-4c46-b1fa-a2b95919ba85)


# 2

Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!

karena portal praktikum jaringan komputer menggunakn protokol http, gunakan filter http untuk memfilter paket dengan protokol http. kemudian pilih salah satu paket, lalu klik kanan, kemudian pilih follow, pilih http stream. kemudian akan muncul stream http antara client dengan portal praktikum jaringan kompter. pada portal praktikum jaringan komputer terdapat informasi tentang web server yang digunakan, yaitu gunicorn

screenshot:
![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/8a78818c-b8bd-44df-bc94-0278a8a9094a)

## flag
![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/d2d82e15-f913-465d-9b57-81699c9f8b1d)


# 3
Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:
a. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?



menggunakan filter ip.addr == 239.255.255.250 && udp.port == 3702 pada display filter wireshark untuk mengambil paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702.

b. Protokol layer transport apa yang digunakan?
Dapat dilihat pada bagian kolom protocol berdasarkan filter di bagian a, yang digunakan adalah UDP.


# 4
Berapa nilai checksum yang didapat dari header pada paket nomor 130?

pada file pcap, pilih paket dengan nomor 130. didalamnya terdapat informasi tentang nilai checksum paket, yaitu 0x18e5

screenshot:
![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/2d16ccc4-78ab-47bf-ae18-d9a0c5f094bb)

## flag
![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/3842942a-7ca5-49e9-864d-45b7bc5d823b)


# 5
# 6
Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.

Jika dilihat pada soal, ada kejanggalan pada huruf besar di beberapa kata, yaitu:

- Seorang
- Udin
- Berteman
- Slamet
- Teman
- Ia
- Terjadi
- Udin
- Sebuah
- Invalid
Jika diambil huruf kapitalnya saja maka terdapat hint SUBSTITUSI

Kemudian pada kalimat “hasil pencarian hanya menampilkan a1 e5 u21”. Jika dilihat pada bagian “a1 e5 u21”, ini merupakan enkripsi huruf-angka, yaitu
a = 1
e = 5
u = 21

Berdasarkan pernyataan "server SOURCE ADDRESS 7812 is invalid", cari packet nomor 7812 dengan display filter frame.number == 7812 dan jika diperhatikan, tulisan source address ditulis capslock sehingga catat IP source address pada packet nomor 7812, yaitu 104.18.14.101.

104.18.14.101 → 0-18 → 10 4 18 14 10 1 → J D R N J A


# 7 
# 8
# 9 
Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!
Dengan menggunakan display capture ip.src == 10.51.40.1 && ip.dst != 10.39.55.34 sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34.
# 10
