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

### Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut? 
### Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
### Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?


