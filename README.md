# Jarkom-Modul-1-D03-2022

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



