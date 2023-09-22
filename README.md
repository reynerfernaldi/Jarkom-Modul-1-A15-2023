# Jarkom-Modul-1-A15-2023

### Kelompok A15

| **No** | **Nama**                   | **NRP**    |
| ------ | -------------------------- | ---------- |
| 1      | Frederick Hidayat          | 5025211152 |
| 2      | Reyner Fernaldi            | 5025201094 |


# PEMBAHASAN

## 1. User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.

### a. Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut?
- Buka file ```soal1.pcapng```
- `STOR` merupakan perinta untuk Meng-upload file ke FTP server, oleh karena itu kita mencari pada protocol FTP yang memiliki perintah `STOR`. Packet ini berada pada baris ke 147
    ![Alt text](img/1a.png?raw=true "Title")
- Melihat ke bagian detail Transmission Control Protocol
- Mendapatkan nilai Sequence Number (raw): 258040667

### b. Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut? 

- Melihat detail Transmission Control Protocol
    ![Alt text](img/1aa.png?raw=true "1a")
- Mendapatkan nilai Acknowledgment number (raw): 1044861039

### c. Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

-  Mencari Response dengan nama file yang sama dengan nama file kirim, yaitu c75-GrabThePhisher.zip
    ![Alt text](img/1c.png?raw=true "1a")
-  Melihat ke bagian detail Transmission Control Protocol
- Mendapatkan nilai Sequence Number (raw): 1044861039

### d. Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

-  Melihat ke bagian detail Transmission Control Protocol
- Mendapatkan nilai Acknowledgment number (raw): 258040696

## 2. Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!
- Buka file ```soal2.pcapng```
- Praktiikum Jarkom dijalankan pada IP Address 10.21.78.111
- Mencari paket yang berasal dari IP Address 10.21.78.111 dengan protocol HTTP karena praktikum jarkom dijalankan dalam web
![Alt text](img/2.png?raw=true "1a")
- Melihat detail pada HTTP dan server dijalankan dengan Server: gunicorn

## 3.Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:

### a. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?
- Kueri untuk memfilternya adalah 
`ip.src == 239.255.255.250 || ip.dst == 239.255.255.250 && udp.port == 3702`
![Alt text](img/3.png?raw=true "1a")
- Terdapat 21 paket

### b. Protokol layer transport apa yang digunakan?
- Protokol yang digunakan adalah User Datagram Protocol (UDP)

## 4.Berapa nilai checksum yang didapat dari header pada paket nomor 130?
![Alt text](img/4.png?raw=true "1a")
- Checksum yang didapat adalah 0x18e5
## 5. Elshe menemukan suatu file packet capture yang menarik. Bantulah Elshe untuk menganalisis file packet capture tersebut.

- Buka file ```soal5.pcap```
- ![Alt text](img/5a.png?raw=true "1a")
- Menemukan e-mail yang menarik. Kami menemukan email yang berisi password zip file. Ketika didecode dengan base64, maka menghasilkan password 5implePas5word
### a. Berapa banyak packet yang berhasil di capture dari file pcap tersebut?

- Terdapat 60 paket yang berhasil tercapture

### b. Port berapakah pada server yang digunakan untuk service SMTP?

- SMTP menggunakan port 25. SMTP berfungsi memastikan pengiriman email melalui jaringan dikomunikasikan dengan aman antara sesama SMTP server

### c. Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public 

- Yang merupakan ip public adalah 74.53.140.153

## 6. Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.

- Didapatkan tulisan SUBSTITUSI SOURCE ADDRESS 7812 kemudian melihat bagian source
  ![image](https://github.com/reynerfernaldi/Jarkom-Modul-1-A15-2023/assets/90272678/d01d8fb4-26d4-46f9-85ea-6926311ba943)
- Didapatkan 108.18.14.101
- 10 8 18 14 10 1 sebagai bahan dekripsi
- a1 e5 u21. sebagai dasar cipher nya
- Kemudian didapatkan JDRNJA
![image](https://github.com/reynerfernaldi/Jarkom-Modul-1-A15-2023/assets/90272678/1595a8a0-a11b-4584-b1fb-851ebb8d7c12)



## 7. Berapa jumlah packet yang menuju IP 184.87.193.88?
![Alt text](img/7.png?raw=true "1a")
- Terdapat 6 paket yang menuju IP 184.87.193.88

## 8. Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)
- Kuerinya adalah tcp.dstport == 80 || udp.dstport == 80

## 9.Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!

- kureinya adalah ip.src == 10.51.40.1 && ip.dst != 10.39.55.34
    ![Alt text](img/9.png?raw=true "1a")


## 10.Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet
![Alt text](img/10.png?raw=true "1a")
- kredensialnya adalah dhafin:kesayangannyak0k0






