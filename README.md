# Lapres Modul 1 Jarkom 2020 - T1  
`"Repository dibuat untuk memenuhi tugas praktikum mata kuliah komunikasi data dan jaringan komputer tahun 2020."`  
  
Anggota:  
**Adeela Nurul Fadhila** `[05311840000001]` [@Rinnabel](https://github.com/Rinnabel)  
**Muhammad Ilya Asha Soegondo** `[05311840000010]` [@ilyaasha24](https://github.com/ilyaasha24/)  

Asisten:  
**Arino Jenynof** `[05111740000096]`  

Penguji:  
**Nur Muhammad Husnul Habib Yahya** `[05111740000094]`  

## Daftar Isi  
- [Lapres Modul 1 Jarkom 2020 - T1](#lapres-modul-1-jarkom-2020---t1)
  - [Daftar Isi](#daftar-isi)
  - [Pendahuluan](#pendahuluan)
    - [Terdapat tiga buah file *.pcapng yang mendukung soal-soal display filter, yaitu:](#terdapat-tiga-buah-file-pcapng-yang-mendukung-soal-soal-display-filter-yaitu)
  - [A. Display Filter](#a-display-filter)
    - [1. Sebutkan webserver yang digunakan pada "testing.mekanis.me"!](#1-sebutkan-webserver-yang-digunakan-pada-testingmekanisme)
    - [2. Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!](#2-simpan-gambar-tim_kunjungan_kerja_bakn_dpr_ri_ke_sukabumi141436jpg)
    - [3. Cari username dan password ketika login di "ppid.dpr.go.id"!](#3-cari-username-dan-password-ketika-login-di-ppiddprgoid)
    - [4. Temukan paket dari web-web yang menggunakan basic authentication method!](#4-temukan-paket-dari-web-web-yang-menggunakan-basic-authentication-method)
    - [5. Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!](#5-ikuti-perintah-di-akupengenpw-username-dan-password-bisa-didapatkan-dari-file-pcapng)
    - [6. Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).](#6-seseorang-menyimpan-file-zip-melalui-ftp-dengan-nama-answerzip-simpan-dan-buka-file-open-thispdf-di-answerzip-untuk-mendapatkan-password-zipnya-temukan-dalam-file-zipkeytxt-passwordnya-adalah-isi-dari-file-txt-tersebut)
    - [7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut. `Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"`](#7-ada-500-file-zip-yang-disimpan-ke-ftp-server-dengan-nama-1zip-2zip--500zip-salah-satunya-berisi-pdf-yang-berisi-puisi-simpan-dan-buka-file-pdf-tersebut-your-super-mega-ultra-rare-hint--nama-pdf-nya-yespdf)
    - [8. Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!](#8-cari-objek-apa-saja-yang-didownload-retr-dari-koneksi-ftp-dengan-microsoft-ftp-service)
    - [9. Cari username dan password ketika login FTP pada localhost!](#9-cari-username-dan-password-ketika-login-ftp-pada-localhost)
    - [10. Cari file .pdf di wireshark lalu download dan buka file tersebut! `clue: "25 50 44 46"`](#10-cari-file-pdf-di-wireshark-lalu-download-dan-buka-file-tersebut-clue-25-50-44-46)
  - [B. Capture Filter](#b-capture-filter)

## Pendahuluan  
### Terdapat tiga buah file *.pcapng yang mendukung soal-soal display filter, yaitu:  
1. [File pertama](.//file/soal_jarkom_modul1_no1-5,10.pcapng) untuk menjawab soal nomor 1-5 dan nomor 10.  
2. [File kedua](.//file/soal_jarkom_modul1_no6,7,9.pcapng) untuk menjawab soal nomor 6, 7, dan 9.  
3. [File ketiga](.//file/soal_jarkom_modul1_no8.pcapng) untuk menjawab soal nomor 8.  

## A. Display Filter  
### 1. Sebutkan webserver yang digunakan pada "testing.mekanis.me"!  
Filter: `ip.src == 157.245.50.224` untuk mencari berdasarkan IP atau  
Filter: `http.host == "testing.mekanis.me"` untuk mencari berdasarkan host  
Mencari IP dari testing.mekanis.me menggunakan ping  
![1a](.//media/image1.png)  
Klik salah satu paket dan cari bagian server  
![1b](.//media/image2.png)  
Webserver yang digunakan: nginx/1.14.0 (Ubuntu)  

### 2. Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!  
Klik `File` > `Export objects` > `HTTP`  
Filter sesuai nama file lalu `Save`  
![2a](.//media/image3.png)  
![2b](.//media/image4.jpeg)  
Image: [Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg](.//file/Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg)  

### 3. Cari username dan password ketika login di "ppid.dpr.go.id"!  
Filter: `http.host == ppid.dpr.go.id` untuk mencari berdasarkan host  
Cari paket dengan method POST kemudian lihat isi HTML Form  
![3](.//media/image6.png)  

### 4. Temukan paket dari web-web yang menggunakan basic authentication method!  
Filter: `http.authbasic`  
![4](.//media/image7.png)  

### 5. Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!  
Filter: `http.host == aku.pengen.pw`  
Klik salah satu paket lalu lihat `Credentials` pada `Authorization` untuk mendapatkan Username dan Password  
![5a](.//media/image8.png)  
Masukkan Username dan Password ketika diminta, lalu ikuti perintah pada website  
![5b](.//media/image9.png)  

### 6. Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).  
Filter: `ftp-data`  
`Follow Stream` - `Save as` - `Raw` paket yang mentransfer [Answer.zip](.//file/Answer.zip)  
![6a](.//media/image10.png)  
`Follow Stream` - `Save as` - `Raw` paket yang mentransfer [zipkey.txt](.//file/zipkey.txt)  
![6b](.//media/image11.png)  
Buka [pdf](.//file/Open%20This.pdf) dalam [zip](.//file/Answer.zip) tersebut  
![6c](.//media/image12.png)  
Image: [Open This.pdf](.//file/Open%20This.pdf)  

### 7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut. `Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"`  
Filter: `ftp-data`  
Ubah "Yes.pdf" ke format Hexadecimal menjadi "59 65 73 2e 70 64 66"  
Klik `Edit` > `Find (Ctrl + F)` Kemudian input "59 65 73 2e 70 64 66" dan pilih tipe `Hex value`  
`Follow stream` paket tersebut, `Save as` dengan tipe `Raw`  
![7a](.//media/image13.png)  
Buka file [pdf](.//file/Yes.pdf) dalam [zip](.//file/473.zip) tersebut  
![7b](.//media/image14.png)  
Image: [Yes.pdf](.//file/Yes.pdf)  

### 8. Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!  
Filter: `ftp.request && ip.addr == 198.246.117.106`  
"198.246.117.106" merupakan IP dari Microsoft FTP Service  
![8](.//media/image15.png)  
Objek yang didownload berupa Readme  
``167 37.018072 192.168.0.128 198.246.117.106 FTP 67 Request: RETR Readme``  

### 9. Cari username dan password ketika login FTP pada localhost!  
Filter: `ftp` pastikan IPnya "127.0.0.1"  
Cari USER dan PASS  
![9](.//media/image16.png)  

### 10. Cari file .pdf di wireshark lalu download dan buka file tersebut! `clue: "25 50 44 46"`  
Klik `Edit` > `Find (Ctrl + F)` Kemudian input "25 50 44 46" dan pilih tipe `Hex value`  
"25 50 44 46" merupakan header file berformat pdf  
![10a](.//media/image17.png)  
Follow Stream (TCP atau HTTP) paket tersebut kemudian `Save as` dengan tipe `Raw`  
![10b](.//media/image18.png)  
Buka file [pdf](.//file/1759.pdf) yang telah didownload  
![10c](.//media/image19.png)  
Image: [1759.pdf](.//file/1759.pdf)  

## B. Capture Filter  
### 11. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
`dst port 21 || src port 21`
![11](.//media-ela/image_11.jpg)
`dst port 21` digunakan untuk menangkap paket menuju ke port 21
`src port 21` digunakan untuk menangkap paket yang berasal dari port 21
Untuk mmenangkap paket yang mengandung port 21, sebelumnya kami melakukan koneksi dari FileZilla client menuju ke server.

### 12. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
***src port 80***
![12](.//media-ela/image_12.jpg)


### 13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
### 14. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
### 15. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!
