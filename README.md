# Jarkom-Modul-1-B10-2022

## Kelompok B10
| Name                      | NRP        | 
| ------------------------- | ---------- |
| Frederick Wijayadi Susilo | 5025201111 |
| Doanda Dresta Rahma       | 5025201049 |
| Zunia Aswaroh             | 5025201058 |

## 1
> Sebutkan web server yang digunakan pada "monta.if.its.ac.id"! 

Kasus soal ini, kita lakukan display filter menggunakan `tcp contains "monta.if.its.ac.id"`

![image](https://user-images.githubusercontent.com/67154280/191028336-49bb3a43-4e3c-4b14-b3ed-ed307957eced.png)
Setelah itu, lakukan `Follow > TCP Stream` dan didapatkan

![image](https://user-images.githubusercontent.com/67154280/191028414-aa5d941a-a1a2-4ce4-ade8-45463fe8bdc4.png)
Diperoleh webserver yang digunakan pada "monta.if.its.ac.id" dari informasi yang didapatkan yaitu `nginx/1.10.3`

## 2
> Ishaq sedang bingung mencari topik ta untuk semester ini , lalu ia datang ke website monta dan menemukan detail topik pada website “monta.if.its.ac.id” , judul TA apa yang dibuka oleh ishaq ?

Kasus soal ini, kita lakukan display filter menggunakan `tcp contains "monta.if.its.ac.id"` dan kita dapatkan url untuk **detail topik** yang dibuka oleh ishaq
![image](https://user-images.githubusercontent.com/67154280/191036247-7edf2c5c-1ce3-44d9-92a2-942dd0b6aefa.png)

Selanjutnya, kita buka url `http://monta.if.its.ac.id/index.php/topik/detailTopik/194` dan didapatkan hasil sebagai berikut
![image](https://user-images.githubusercontent.com/67154280/191053491-2eeaa20f-a054-42e8-ad78-b35b5f3e6b13.png)

Dengan demikian, kita mendapatkan judul TA yaitu **Evaluasi unjuk kerja User Space Filesystem (FUSE)**

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

Pertama, masuk ke file paket yang tersedia di drive dan lakukan pada wireshark `tcp.srcport == 443`
![image](https://github.com/WantToBePro31/Jarkom-Modul-1-B10-2022/blob/main/No.5%20Jarkom.png)

## 6
> Filter sehingga wireshark hanya menampilkan paket yang menuju ke lipi.go.id !

Pertama, lakukan ping terlebih dahulu pada cmd `ping lipi.go.id`
![image](https://github.com/WantToBePro31/Jarkom-Modul-1-B10-2022/blob/main/CMD.png)

Kemudian, langsung masukkan display filter `tcp contains "lipi.go.id"`
![image](https://github.com/WantToBePro31/Jarkom-Modul-1-B10-2022/blob/main/No.6%20Jarkom.png)

## 7
> Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

Pertama, cek ip dulu dengan `ipconfig` pada cmd 
![image](https://github.com/WantToBePro31/Jarkom-Modul-1-B10-2022/blob/main/CMD2.png)

Kemudian, masukkan di wifi pada wireshark lakukan `ip.src == 10.8.108.239` pada display filter.
![image](https://github.com/WantToBePro31/Jarkom-Modul-1-B10-2022/blob/main/No.7%20Jarkom.png)


### Cerita soal 8-10
Untuk soal 8-10, silahkan baca cerita di bawah ini!

Di sebuah planet bernama Viltrumite, terdapat Kementerian Komunikasi dan Informatika yang baru saja menetapkan kebijakan baru. Dalam kebijakan baru tersebut, pemerintah dapat mengakses data pribadi masyarakat secara bebas jika memang dibutuhkan, baik dengan maupun tanpa persetujuan pihak yang bersangkutan. Sebagai mahasiswa yang sedang melaksanakan program magang di kementerian tersebut, kalian mendapat tugas berupa penyadapan percakapan mahasiswa yang diduga melakukan tindak kecurangan dalam kegiatan Praktikum Komunikasi Data dan Jaringan Komputer 2022. Selain itu, terdapat sebuah password rahasia (flag) yang diduga merupakan milik sebuah organisasi bawah tanah yang selama ini tidak sejalan dengan pemerintahan Planet Viltrumite. Tunggu apa lagi, segera kerjakan tugas magang tersebut agar kalian bisa mendapatkan pujian serta kenaikan jabatan di kementerian tersebut!


## 8
> Telusuri aliran paket dalam file .pcap yang diberikan, cari informasi berguna berupa percakapan antara dua mahasiswa terkait tindakan kecurangan pada kegiatan praktikum. Percakapan tersebut dilaporkan menggunakan protokol jaringan dengan tingkat keandalan yang tinggi dalam pertukaran datanya sehingga kalian perlu menerapkan filter dengan protokol yang tersebut.

Pertama yang dilakukan adalah memilah paket dengan protokol TCP (Transfer Control Protocol)
> display filter: tcp

![image](https://user-images.githubusercontent.com/66405353/191034048-7a849aaf-1c3e-4d9e-854f-e9d4825b7ddd.png)

Dari paket-paket yang ditampilkan, ditemukan adanya paket-paket yang suspicious antara ip address 127.0.0.1 melalui port 60236 dan ip address 127.0.1.1 melalui port 65432

![image](https://user-images.githubusercontent.com/66405353/191034174-c7da38ef-0c29-495a-8a42-1f12928af47a.png)

Kemudian ditampilkan hanya paket yang ditransfer antara kedua port tersebut
> display filter: (tcp.srcport == 60236 and tcp.dstport == 65432) or (tcp.srcport == 65432 and tcp.dstport == 60236)

![image](https://user-images.githubusercontent.com/66405353/191035982-df74f548-98ea-44e0-a09b-abe30ccdb705.png)

Sehingga didapatkan percakapan penuh antara kedua oknum

![bukti](https://user-images.githubusercontent.com/66405353/191038482-0e3a4621-831d-4740-96b4-686d5622abe9.png)

![image](https://user-images.githubusercontent.com/67154280/191054513-103a26ad-f41a-4c1c-a478-859b36cbea34.png)

## 9
> Terdapat laporan adanya pertukaran file yang dilakukan oleh kedua mahasiswa dalam percakapan yang diperoleh, carilah file yang dimaksud! Untuk memudahkan laporan kepada atasan, beri nama file yang ditemukan dengan format [nama_kelompok].des3 dan simpan output file dengan nama “flag.txt”.

Dalam percakapan disebut pengiriman file melalui port 9002, ditemukan file salt

![image](https://user-images.githubusercontent.com/66405353/191043635-000c2b61-cebe-47f6-89c2-bd3c2036bfc8.png)

Setelah itu, lakukan `Follow > TCP Stream` dan didapatkan
![image](https://user-images.githubusercontent.com/66405353/191046138-1d87d8ff-748f-459e-9a21-77dab998f105.png)

Lalu, kita mengganti `Show data as` dari `ASCII` menjadi `Raw` dan kita `Save as` dengan nama file `b10.des3` dan `flag.txt`
![image](https://user-images.githubusercontent.com/66405353/191046161-e0c3ee96-e0dc-42ee-894a-052dc0e4b5c4.png)
![image](https://user-images.githubusercontent.com/66405353/191046170-eabf3187-d5c0-4c68-ad6d-2e3530652624.png)


## 10
> Temukan password rahasia (flag) dari organisasi bawah tanah yang disebutkan di atas!

Pertama copy file des3 ke dalam direktori wsl

![image](https://user-images.githubusercontent.com/66405353/191055596-4765dade-112f-4180-996d-b4afea081d20.png)

Kemudian jalankan dalam wsl ubuntu command: openssl des3 -d -in b10.des3 -out flag.txt dengan password = 'nakano'

![image](https://user-images.githubusercontent.com/66405353/191055629-53e3275e-8353-45ed-8e25-78c4ebfece9d.png)

Setelah itu didapatkan file flag.txt yang didalamnya terdapat password hasil decrypt

![image](https://user-images.githubusercontent.com/66405353/191055839-d662e67c-a48d-4883-9c43-3abf45bfdd9b.png)

Password adalah **JaRkOm2022{8uK4N_CtF_k0k_h3h3h3}**
