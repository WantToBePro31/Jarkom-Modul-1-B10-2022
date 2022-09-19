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

Pertama , buka file paket yang tersedia pada drive , kemudian lakukan `tcp.srcport == 443`
![image](https://drive.google.com/drive/u/0/folders/14f85-_uVA-HfheDwLzWHqmfgGv0bwvgr)
## 6
> Filter sehingga wireshark hanya menampilkan paket yang menuju ke lipi.go.id !


## 7
> Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!


## 8
> 

## 9
> 

## 10
> 
