[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/aRvIU2lf)
| Name           | NRP        | Kelas     |
| ---            | ---        | ----------|
| Joaquin Fairuz Nawfal Ismono | 5025241106 | A |



## Put your topology config image here!

![Topology](images/Topology.png)

## Put your GNS3 Project file here!

[Gns3Project](FP.gns3project)

<br>

## Soal 1

> Menggunakan metode VLSM, buatlah pembagian subnet untuk masing-masing gedung dengan cara yang seefisien mungkin!

> _Using the VLSM method, create subnets for each building as efficiently as possible!_

**Answer:**

- Screenshot

![Topology](images/1/VLSM.png)

- Explanation

  `Penjelasan dan tabel pembagian ada di` [sini](https://docs.google.com/spreadsheets/d/1VKQlQxHWKOhOAsVP7lnIODnBlSu_BdD-mPrsS4rLdhM/edit?gid=0#gid=0) `dan saya juga meminta bantuan` [Google](https://subnettingpractice.com/vlsm.html) `untuk membagi subnet ke semua node.`

<br>

## Soal 2

> Konfigurasi semua router agar bisa terhubung ke semua jaringan. Gunakan static routing dan uji dengan melakukan ping dari **Budapest** ke **Alekhine** dan dari **Ponziani** ke **Sicilian**!

> _Configure all routers to connect to all networks. Use static routing and perform testing by pinging from **Budapest** to **Alekhine** and from **Ponziani** to **Sicilian**!_

**Answer:**

- Screenshot

1. Hasil `ip r` dari node Smith-Morra

![Ping](images/2/SmithMorra.png)

2. Hasil `ip r` dari node Fianchetto

![Ping](images/2/Fianchetto.png)

3. Hasil `ip r` dari node Lucena

![Ping](images/2/Lucena.png)

4. Hasil `ip r` dari node Zwischenzug

![Ping](images/2/Zwischenzug.png)

5. Hasil `ip r` dari node Zugzwang

![Ping](images/2/Zugzwang.png)

6. Hasil `ping` dari node Budapest (10.28.32.3) ke Alekhine (10.28.41.195)

![Ping](images/2/Budapest.png)

7. Hasil `ping` dari node Ponziani (10.28.41.130) ke Sicilian (10.28.41.2)

![Ping](images/2/Ponziani.png)

- Explanation

  `Semua langkah-langkah kurang lebih sudah ada di dokumen catatan ` [tertera](FP%20Jarkom.pdf)

<br>

## Soal 3

> Berikan seluruh client (**Blackmar-Diemer, Budapest,** dan **Stafford**) IP secara dinamis dari DHCP. Range IP dibebaskan, namun tunjukkan bahwa mereka mendapatkan IP secara dinamis!

> _Assign all clients (**Blackmar-Diemer, Budapest,** and **Stafford**) dynamic IP addresses via DHCP. You may use any IP range you would like, but prove that they receive IP addresses dynamically!_

**Answer:**

- Screenshot

1. IP dari node Blackmar-Diemer

![Ping](images/3/BlackmarDiemer.png)

2. IP dari node Budapest

![Ping](images/3/Budapest.png)

3. IP dari node Stafford

![Ping](images/3/Stafford.png)

- Explanation

  `Semua langkah-langkah kurang lebih sudah ada di dokumen catatan ` [tertera](FP%20Jarkom.pdf)

<br>

## Soal 4

> Berikan web server **Slav** dan **Sicilian** IP address yang tetap/fixed dari DHCP. 

> _Assign **Slav** and **Sicilian** web servers fixed IP addresses via DHCP._

**Answer:**

- Screenshot

1. IP dari node Slav

![Ping](images/4/Slav.png)

2. IP dari node Sicilian

![Ping](images/4/Sicilian.png)

- Explanation

  `Sudah sekalian dengan nomor 3. Jangan lupa tambahkan ` **hwaddress** **ether** **[hwaddress_milik_Node]** ` di config Node Slav dan Sicilian. Semua langkah-langkah kurang lebih sudah ada di dokumen catatan ` [tertera](FP%20Jarkom.pdf)

<br>

## Soal 5

> Buatlah konfigurasi untuk domain:  
**parkov.com** → IP Node **Slav**  
**paskarov.com** → IP Node **Sicilian** 
Pada **DNS Master Caro-Kann.** Tambahkan juga subdomain www untuk kedua domain tersebut.

> _Configure the domains:  
**parkov.com** → **Slav** Node IP  
**paskarov.com** → **Sicilian** Node IP  
On the **Caro-Kann DNS Master,** then add the www subdomain for both domains._

**Answer:**

- Screenshot

1. Hasil `ping` dari node Stafford ke semua Domain dan Subdomain

![Ping](images/5/Ping.png)

- Explanation

  `Semua langkah-langkah kurang lebih sudah ada di dokumen catatan ` [tertera](FP%20Jarkom.pdf)

<br>

## Soal 6

> Konfigurasikan juga **Alekhine** sebagai **DNS Slave** yang bekerja untuk membantu **Caro-Kann.** Lakukan pengujian dengan **mematikan Caro-Kann** lalu coba ping ke domain dan subdomain tersebut (pilih salah satu saja).

> _Configure **Alekhine** as a **DNS Slave** to assist **Caro-Kann**. Perform testing by **disabling Caro-Kann** and then pinging the domain and subdomain (choose only one)._

**Answer:**

- Screenshot

1. Keadaan server DNS Caro-Kann dimatikan

![Ping](images/6/Caro-Kann.png)

2. Hasil `ping` dari node Stafford ke Domain dan Subdomain paskarov.com

![Ping](images/6/Ping.png)

- Explanation

  `Sudah sekalian dengan nomor 5. Semua langkah-langkah kurang lebih sudah ada di dokumen catatan ` [tertera](FP%20Jarkom.pdf)

<br>

## Soal 7

> Konfigurasikan **Sicilian** agar berfungsi sebagai **web server nginx** yang akan menyajikan [halaman berikut](https://drive.google.com/file/d/1eX0ZjRKprx8T34XFAssrpc7ZE1j6Jv0j/view). Konfigurasikan juga agar **Sicilian** bisa menyimpan custom access log ke file **/tmp/access.log** dan error log ke file **/tmp/error.log.**

> _Configure **Sicilian** to function as an **nginx web server**that will serve [this page](https://drive.google.com/file/d/1eX0ZjRKprx8T34XFAssrpc7ZE1j6Jv0j/view). Also, configure **Sicilian** to save custom access logs to **/tmp/access.log** and error logs to **/tmp/error.log.**_

**Answer:**

- Screenshot

1. Isi webpage

![Ping](images/7/Chromium.png)

2. Hasil `curl -vL 10.28.41.2` dari node Stafford

![Ping](images/7/Curl.png)

- Explanation

  `Semua langkah-langkah kurang lebih sudah ada di dokumen catatan ` [tertera](FP%20Jarkom.pdf)

<br>

## Soal 8

> Buatlah custom access log ke file **/tmp/access.log.** Untuk keperluan logging, gunakan format log seperti di bawah:
> - Tanggal dan waktu akses dalam format standar log.
> - Nama node yang sedang diakses.
> - Alamat IP klien yang mengakses website.
> - Metode HTTP dan URI yang diakses oleh klien.
> - Status respons HTTP yang diberikan oleh server.
> - Jumlah byte yang dikirimkan dalam respons.
> - Waktu yang dihabiskan oleh server untuk menangani permintaan.> 
> - Contoh format log yang sesuai:  
[01/Oct/2024:11:30:45 +0000] Jarkom Node Sicilian Access from 192.168.1.15 using method "GET /resep/bayam HTTP/1.1" returned status 200 with 2567 bytes sent in 0.038 seconds

> _Webserver: Create a custom access log to the file **/tmp/access.log.** For logging purposes, use the log format shown below:_
> - _The date and time of access in standard log format._
> - _The name of the node being accessed._
> - _The IP address of the client accessing the website._
> - _The HTTP method and URI accessed by the client._
> - _The HTTP response status returned by the server._
> - _The number of bytes sent in the response._
> - _The time spent by the server processing the request._
> - _Example of appropriate log format:  
[01/Oct/2024:11:30:45 +0000] Jarkom Node Sicilian Access from 192.168.1.15 using method "GET /resep/bayam HTTP/1.1" returned status 200 with 2567 bytes sent in 0.038 seconds_

**Answer:**

- Screenshot

 1. Isi dari /tmp/access/log di node Sicilian ketika melakukan curl dan membuka webpage (melakukan nomor 7)

![Ping](images/8/Log.png)

- Explanation

  `Semua langkah-langkah kurang lebih sudah ada di dokumen catatan ` [tertera](FP%20Jarkom.pdf)

<br>

## Soal 9

> Konfigurasikan juga **Slav** agar berfungsi sebagai **web server nginx** yang menyajikan [halaman berikut](https://drive.google.com/file/d/1h8ik1Zcubntp0dvHt9NHYqSZLSTG6FuZ/view) dan **hanya** bisa diakses melalui port **8000** dan **8888.**

> _Configure **Slav** to function as an **nginx web server** that serves [this page](https://drive.google.com/file/d/1h8ik1Zcubntp0dvHt9NHYqSZLSTG6FuZ/view?usp=drive_link) and is **only** accessible via ports **8000** and **8888.**_

**Answer:**

- Screenshot

1. Isi webpage

![Ping](images/9/Chromium.gif)

2. Hasil `curl -vL 10.28.40.2` dari node Stafford

![Ping](images/9/Portless.png)

3. Hasil `curl -vL 10.28.40.2:8000` dari node Stafford

![Ping](images/9/8000.png)

4. Hasil `curl -vL 10.28.40.2:8888` dari node Stafford

![Ping](images/9/8888.png)

- Explanation

  `Semua langkah-langkah kurang lebih sudah ada di dokumen catatan ` [tertera](FP%20Jarkom.pdf)

<br>

## Soal 10

> Untuk memudahkan akses, buatlah satu domain lagi dengan nama **openings.com** yang mengarah ke **Petrov.** Lalu, konfigurasikan juga **Petrov** sebagai **Reverse Proxy** yang akan melakukan forward request ke server yang sesuai berdasarkan URL profile yang diminta oleh klien dengan ketentuan sebagai berikut:
> - Request untuk “openings.com/**sicilian**” harus dialihkan ke web server **Sicilian.**
> - Request untuk “openings.com/**slav**” harus dialihkan ke web server **Slav.**

> _To facilitate access, create another domain with the name **openings.com** that points to **Petrov.** Then, configure **Petrov** as a **Reverse Proxy** that will forward requests to the appropriate server based on the profile URL requested by the client with the following conditions:_
> - _Requests for “openings.com/**sicilian**” must be forwarded to web server **Sicilian.**_
> - _Request for “openings.com/**slav**” must be forwarded to web server **Slav.**_

**Answer:**

- Screenshot

1. Isi webpage /sicilian

![Ping](images/10/Sicilian.png)

2. Isi webpage /slav

![Ping](images/10/Slav.png)

- Explanation

  `Semua langkah-langkah kurang lebih sudah ada di dokumen catatan ` [tertera](FP%20Jarkom.pdf)

<br>

## Soal 11

> Tambahkan juga konfigurasi agar request untuk “openings.com/**random**” akan mengalihkan request ke webserver **Sicilian** dan **Slav** dengan algoritma _round-robin_.

> _Additionally, configure requests for "openings.com/**random**" to be redirected to the **Sicilian** and **Slav** web servers using a round-robin algorithm._

**Answer:**

- Screenshot

1. Isi webpage

![Ping](images/11/Random.gif)

- Explanation

  `Sudah sekalian dengan nomor 10. Semua langkah-langkah kurang lebih sudah ada di dokumen catatan ` [tertera](FP%20Jarkom.pdf)

<br>

## Soal 12

> Anatoly Parkov berencana untuk melakukan ekspansi secara besar-besaran. Maka dari itu, hapus seluruh konfigurasi Static Routing dan ubah agar seluruh router menggunakan Dynamic Routing. Gunakan protokol RIP!

> _Anatoly Parkov plans to perform a great expansion. Therefore, remove all Static Routing configurations and configure all routers to use Dynamic Routing. Use the RIP protocol!_

**Answer:**

- Screenshot

1. Hasil `ping` dari node Budapest ke Alekhine

![Ping](images/12/Budapest.png)

2. Hasil `ping` dari node Ponziani ke Sicilian

![Ping](images/12/Ponziani.png)

- Explanation

  `Semua langkah-langkah kurang lebih sudah ada di dokumen catatan ` [tertera](FP%20Jarkom.pdf)

<br>

## Soal 13

> Untuk meningkatkan keamanan, konfigurasikan firewall **Smith-Morra** untuk melakukan pembatasan koneksi SSH ke server DNS. Drop semua packet SSH yang berasal dari seluruh client yang memiliki tujuan ke **Caro-Kann** atau **Alekhine.**

> _To increase security, configure the **Smith-Morra** firewall to restrict SSH connections to the **DNS server.** Drop all SSH packets from all clients destined for **Caro-Kann** or **Alekhine.**_

**Answer:**

- Screenshot

1. Hasil `nc 10.28.41.194 22` dari node Stafford ke Caro-Kann (`nc nc -l -p 22`)

![Ping](images/13/Caro-Kann.gif)

2. Hasil `nc 10.28.41.195 22` dari node Blackmar-Diemer ke Alekhine (`nc nc -l -p 22`)

![Ping](images/13/Alekhine.gif)

- Explanation

  `Semua langkah-langkah kurang lebih sudah ada di dokumen catatan ` [tertera](FP%20Jarkom.pdf)

<br>

## Soal 14

> Nampaknya, web server juga manusia sehingga hanya ingin bekerja di hari kerja. Maka dari itu, semua client hanya bisa mengakses **Sicilian** dan **Slav** pada hari Senin-Jumat pada pukul 09:00-17:00.

> _Apparently, web servers are humans too, so they only want to work on weekdays. Therefore, all clients can only access **Sicilian** and **Slav** on Monday through Friday, 9:00 AM to 5:00 PM._

**Answer:**

- Screenshot

1. Yang terjadi dari node Client-Group-3 (docker netics-pc-desktop) jika membuka domain webserver di waktu yang diperbolehkan

![Ping](images/14/Benar.gif)

2. Yang terjadi dari node Client-Group-3 (docker netics-pc-desktop) jika membuka domain webserver di waktu yang tidak diperbolehkan

![Ping](images/14/Salah.gif)

3. Yang terjadi dari node Client-Group-3 (docker netics-pc-desktop) jika melakukan `curl -vL 10.28.41.2` di waktu yang tidak diperbolehkan

![Ping](images/14/Salah.png)

- Explanation

  `Semua langkah-langkah kurang lebih sudah ada di dokumen catatan ` [tertera](FP%20Jarkom.pdf)

<br>

## Soal 15

> Terakhir, Gerry Paskarov berpesan untuk selalu melakukan logging, sehingga konfigurasikan fitur logging untuk melakukan log terhadap seluruh paket yang di-DROP pada firewall **Smith-Morra.**
> _Finally, Gerry Paskarov advises to always perform logging, so configure a logging feature to log all packets dropped on the **Smith-Morra** firewall._

**Answer:**

- Screenshot

1. Yang dilakukan di node Stafford untuk mengetest (`ssh` ke arah DNS Server)

![Ping](images/15/Stafford.png)

2. Isi dari log di node Smith-Morra

![Ping](images/15/Log.png)

- Explanation

  `Semua langkah-langkah kurang lebih sudah ada di dokumen catatan ` [tertera](FP%20Jarkom.pdf)

<br>
  
## Problems

1. Hehe tiba2 size VM GNS3 ku mbludak. GNS S-nya stress. Jadi harus install ulang dan makan banyak waktu damn.

![Ping](images/GNS.png)

2. Uhm... yeah.

![Ping](images/Awikwok.gif)

## Revisions (if any)
