# Jarkom-Modul-1-B10-2022

## Kelompok B10
| Name                      | NRP        | 
| ------------------------- | ---------- |
| Frederick Wijayadi Susilo | 5025201111 |
| Doanda Dresta Rahma       | 5025201049 |
| Zunia Aswaroh             | 5025201058 |

## 1
> Sebutkan web server yang digunakan pada "monta.if.its.ac.id"! 

Pertama, akses terlebih dahulu website http://monta.if.its.ac.id, kemudian lakukan display filter menggunakan `tcp contains "monta.if.its.ac.id"`

![image](https://user-images.githubusercontent.com/67154280/191028336-49bb3a43-4e3c-4b14-b3ed-ed307957eced.png)
Setelah itu, lakukan `Follow > TCP Stream`

![image](https://user-images.githubusercontent.com/67154280/191028414-aa5d941a-a1a2-4ce4-ade8-45463fe8bdc4.png)
Diperoleh webserver yang digunakan pada "monta.if.its.ac.id" dari informasi yang didapatkan yaitu `nginx/1.10.3`

## 2
> Ishaq sedang bingung mencari topik ta untuk semester ini , lalu ia datang ke website monta dan menemukan detail topik pada website “monta.if.its.ac.id” , judul TA apa yang dibuka oleh ishaq ?

## 3
> Filter sehingga wireshark hanya menampilkan paket yang menuju port 80!

Kasus soal ini, kita lakukan dengan capture filter `tcp.dstport == 80` dan akan mendapatkan hasil sebagai berikut

![image](https://user-images.githubusercontent.com/67154280/191031218-18699a9f-1798-4935-b4a8-ec212a29cbfb.png)

## 4
> Filter sehingga wireshark hanya mengambil paket yang berasal dari port 21!

Kasus soal ini, kita lakukan dengan display filter `tcp.srcport == 21` dan akan mendapatkan hasil sebagai berikut

![image](https://user-images.githubusercontent.com/67154280/191030656-a4fa7858-c8c8-4d4a-a0ad-36d5b0181df7.png)

## 5
> Filter sehingga wireshark hanya mengambil paket yang berasal dari port 443!

pertama, buka file paket yang tersedia, lakukan `tcp.port == 443`
![image](https://github.com/WantToBePro31/Jarkom-Modul-1-B10-2022/blob/main/No.5%20Jarkom.png)

## 6
> Filter sehingga wireshark hanya menampilkan paket yang menuju ke lipi.go.id !


## 7
> Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

### Cerita soal 8-10
Untuk soal 8-10, silahkan baca cerita di bawah ini!

Di sebuah planet bernama Viltrumite, terdapat Kementerian Komunikasi dan Informatika yang baru saja menetapkan kebijakan baru. Dalam kebijakan baru tersebut, pemerintah dapat mengakses data pribadi masyarakat secara bebas jika memang dibutuhkan, baik dengan maupun tanpa persetujuan pihak yang bersangkutan. Sebagai mahasiswa yang sedang melaksanakan program magang di kementerian tersebut, kalian mendapat tugas berupa penyadapan percakapan mahasiswa yang diduga melakukan tindak kecurangan dalam kegiatan Praktikum Komunikasi Data dan Jaringan Komputer 2022. Selain itu, terdapat sebuah password rahasia (flag) yang diduga merupakan milik sebuah organisasi bawah tanah yang selama ini tidak sejalan dengan pemerintahan Planet Viltrumite. Tunggu apa lagi, segera kerjakan tugas magang tersebut agar kalian bisa mendapatkan pujian serta kenaikan jabatan di kementerian tersebut!


## 8
> Telusuri aliran paket dalam file .pcap yang diberikan, cari informasi berguna berupa percakapan antara dua mahasiswa terkait tindakan kecurangan pada kegiatan praktikum. Percakapan tersebut dilaporkan menggunakan protokol jaringan dengan tingkat keandalan yang tinggi dalam pertukaran datanya sehingga kalian perlu menerapkan filter dengan protokol yang tersebut.

Pertama yang dilakukan adalah memilah paket dengan protokol TCP (Transfer Control Protocol)

![image](https://user-images.githubusercontent.com/66405353/191034048-7a849aaf-1c3e-4d9e-854f-e9d4825b7ddd.png)

Dari paket-paket yang ditampilkan, ditemukan adanya paket-paket yang suspicious antara ip address 127.0.0.1 melalui port 60236 dan ip address 127.0.1.1 melalui port 65432

![image](https://user-images.githubusercontent.com/66405353/191034174-c7da38ef-0c29-495a-8a42-1f12928af47a.png)

Kemudian ditampilkan hanya paket yang ditransfer antara kedua port tersebut

![image](https://user-images.githubusercontent.com/66405353/191035982-df74f548-98ea-44e0-a09b-abe30ccdb705.png)

Sehingga didapatkan percakapan penuh antara kedua oknum

![bukti](https://user-images.githubusercontent.com/66405353/191038482-0e3a4621-831d-4740-96b4-686d5622abe9.png)

## 9
> 

## 10
> 
