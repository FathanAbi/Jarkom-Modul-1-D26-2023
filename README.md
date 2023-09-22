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

# 2

Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!

karena portal praktikum jaringan komputer menggunakn protokol http, gunakan filter http untuk memfilter paket dengan protokol http. kemudian pilih salah satu paket, lalu klik kanan, kemudian pilih follow, pilih http stream. kemudian akan muncul stream http antara client dengan portal praktikum jaringan kompter. pada portal praktikum jaringan komputer terdapat informasi tentang web server yang digunakan, yaitu gunicorn

screenshot:
![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/8a78818c-b8bd-44df-bc94-0278a8a9094a)

# 3

# 4
Berapa nilai checksum yang didapat dari header pada paket nomor 130?

pada file pcap, pilih paket dengan nomor 130. didalamnya terdapat informasi tentang nilai checksum paket.

screenshot:
![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/2d16ccc4-78ab-47bf-ae18-d9a0c5f094bb)

# 5
# 6
# 7 
# 8
# 9 
# 10
