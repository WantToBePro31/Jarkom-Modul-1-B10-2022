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

Kasus soal ini, kita lakukan display filter menggunakan `tcp contains "monta.if.its.ac.id"` dan kita dapatkan halaman untuk **detail topik**
![image](https://user-images.githubusercontent.com/67154280/191036247-7edf2c5c-1ce3-44d9-92a2-942dd0b6aefa.png)

Setelah itu, lakukan `Follow > TCP Stream` dan didapatkan
![image](https://user-images.githubusercontent.com/67154280/191036389-b346e1b9-4b62-4ee7-b41d-89f8fdbfed1a.png)

Lalu, kita mengganti `Show data as` dari `ASCII` menjadi `Raw` dan kita `Save as` dengan nama file `detailTopik.zip`
![image](https://user-images.githubusercontent.com/67154280/191036889-f29ea5d3-3303-4c30-b8a9-e5298d47ec0d.png)

![image](https://user-images.githubusercontent.com/67154280/191037592-34ab95be-d4ca-4b19-ad87-0f5719f063d3.png)

Selanjutnya, kita extract file `detailTopik.zip` dan kita mendapatkan file `detailTopik`, kemudian tambahkan extension `.html` dan akan diperoleh hasil berikut
![image](https://user-images.githubusercontent.com/67154280/191037987-bd42ac49-0358-48f5-9657-08e4cf7beef6.png)

Dengan menekan nama mahasiswa yang dicari oleh ishaq, kita mendapatkan judul TA yaitu **Perancangan Sistem Pengendali Panas Otomatis pada Mesin Sangrai Kopi dengan Logika Fuzzy**
![image](https://user-images.githubusercontent.com/67154280/191040588-519a20e4-e726-4f8f-b2e8-a52080146737.png)

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

pertama masuk pada file paket yang tersedia , lakukan `tcp.srcport == 443` pada display filter.
![image](https://github.com/WantToBePro31/Jarkom-Modul-1-B10-2022/blob/main/No.5%20Jarkom.png)

## 6
> Filter sehingga wireshark hanya menampilkan paket yang menuju ke lipi.go.id !
pertama , lakukan ping terlebih dahulu pada cmd `ping lipi.go.id`
![image](https://github.com/WantToBePro31/Jarkom-Modul-1-B10-2022/blob/main/CMD.png)

kemudian , langsung masukin `tcp contains "lipi.go.id"`
![image](https://github.com/WantToBePro31/Jarkom-Modul-1-B10-2022/blob/main/No.6%20Jarkom.png)

## 7
> Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

pertama cek ip dulu `ipconfig` pada cmd 
![image](https://github.com/WantToBePro31/Jarkom-Modul-1-B10-2022/blob/main/CMD2.png)

kemudian, masukin di wifi pada wireshark lakukan `ip.src == 10.8.108.239` pada display filter.
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

## 9
> 

## 10
> 
