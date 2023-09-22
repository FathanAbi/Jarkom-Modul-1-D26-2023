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

# 4
Berapa nilai checksum yang didapat dari header pada paket nomor 130?

pada file pcap, pilih paket dengan nomor 130. didalamnya terdapat informasi tentang nilai checksum paket, yaitu 0x18e5

screenshot:
![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/2d16ccc4-78ab-47bf-ae18-d9a0c5f094bb)

## flag
![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/3842942a-7ca5-49e9-864d-45b7bc5d823b)


# 5 (REVISI)
Elshe menemukan suatu file packet capture yang menarik. Bantulah Elshe untuk menganalisis file packet capture tersebut.

sebelum mengerjakan soal, perlu dicari command nc agar dapat menjawab soal. pertama buka file pcap dan follow tcp stream. pada hasil follow ditemukan password yang ter-encode dalam base64. lakukan decoding untuk mendapat password sebenarmya. kemudian gunakan password untuk membuka file secret.txt untuk mendapatkan command nc

screenshot password:
![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/baf35c98-bf55-48cb-98ae-56aa94212bee)

screenshot hasil encoding:
![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/c5ba2303-6c89-4e92-a250-8ac64446c2c6)

screenshot isi file secret.txt
![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/cb75ec3d-b7cb-4072-b60b-b983f32e184b)


## Poin A
Berapa banyak packet yang berhasil di capture dari file pcap tersebut?

pada file pcap, dapat dilihat terdapat 60 paket yang dicapture
screenshot:
![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/5395bbc8-7d4f-4dd8-8248-dc9cdfdc601f)

## Poin B
Port berapakah pada server yang digunakan untuk service SMTP?

dengan menggunakan filter “SMTP”. lalu pilih paket didapat port yang digunakan adalah port 25

screenshot:
![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/e29fa8e4-0af7-4571-95bc-2305b7f4508a)


## Poin C
Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?

berdasarkan informasi pada (https://www.avast.com/c-ip-address-public-vs-private) didapet private ip adalah ip yang berada di range:
*	Class A: 10.0.0.0 — 10.255.255.255
*	Class B: 172.16.0.0 — 172.31.255.255 
*	Class C: 192.168.0.0 — 192.168.255.255

dari file pcap diatas didapat yang merupakan public ip adalah 74.53.140.153

screenshot:
![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/6b3b5954-f38e-4de1-9988-917eef8518b9)

## flag
![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/11bbe41e-be3e-4b29-a6d2-6e533fcaa7e6)

# 6

# 7

# 8 (REVISI)
Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)

menggunakan tcp.dstport == 80, untuk menampilkan paket dengan protokol tcp yang menuju port 80, menggunakan udp.dtsport == 80 untuk menampilkan paket dengan protokol udp yang menuju port 80. menggunakan konjugasi or (||) untuk menggabungkan keduanya

## flag
![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/4ce8d775-73fd-49e4-8e9d-b23fef780450)

# 9 (REVISI)
Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!

menngunakan ip.src == 10.51.40.1 untuk menampilkan paket yang berasal dari alamat 10.51.40.1. kemudian menngunakan ip.dst == 10.39.55.34 untuk membuat pengecualian dari paket yang berasal dari alamat 10.39.55.34

## flag
![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/862cc287-9d99-4370-b925-10dc783c8a6e)


# 10 (REVISI)
Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet

gunakan filter “telnet” untuk mencari paket dengan protokol telnet. lalu cari paket yang terdapat Login: dan Password: . kemudian follow tcp stream. didapat Login:dhafin dan Password:kesayangannyak0k0. sehinnga kredensialnya adalah dhafin:kesayangannyak0k0

screenshot:
![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/a01c3d74-4a6b-4f2a-9e9d-e0533ce2ab04)

## flag
![image](https://github.com/FathanAbi/Jarkom-Modul-1-D26-2023/assets/90834092/ca9007db-2aa7-4cd5-9f06-0d1fc8a8261b)
