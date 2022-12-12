# BAB 2 DHCP Server

## 2.1 Tujuan Praktikum

- Mahasiswa dapat memahami konsep DHCP Server
- Mahasiswa dapat kelebihan dan kekurangan Ip Static dan Ip Dinamis
- Mahasiswa dapat mengkonfigurasi DHCP Server pada Linux Ubuntu dan konfigurasi DHCP Client pada Windows

## Dasar Teori

### 2.2.1 Pengertian DHCP

Dynamic Host Configuration Protocol (DHCP) adalah protokol yang digunakan untuk mengalokasikan alamat IP secara dinamis pada jaringan komputer. DHCP memungkinkan komputer untuk mendapatkan alamat IP secara otomatis dari server DHCP tanpa harus mengkonfigurasi secara manual. DHCP juga dapat mengalokasikan konfigurasi lainnya seperti subnet mask, default gateway, dan DNS server.

### 2.2.2 Manfaat DHCP

beberapa manfaat dalam menggunakan DHCP adalah sebagai berikut:

- DHCP menyediakan alamat IP secara dinamis, sehingga tidak perlu lagi mengatur alamat IP secara manual.
- Menghemat waktu dan tenaga administrator dalam mengkonfigurasi IP Address secara manual
- DHCP dapat melayani jaringan yang besar, karena DHCP dapat melayani banyak client secara bersamaan.
- DHCP memungkinakan client menggunakan alamat ip reusable, sehingga tidak perlu lagi mengatur alamat ip secara manual setiap kali client dihidupkan.
- DHCP dapat mengatur waktu penggunaan alamat ip, sehingga client dapat menggunakan alamat ip tersebut selama waktu yang telah ditentukan.

### 2.2.3 Metode DHCP

Ada 3 metode dalam pengalokasian alamat ip menggunakan DHCP yaitu :

a. Alokasi Secara Automatic

Metode digunakan agar DHCP clint mendapatkan IP Dari DHCP Server yang bersifat tetap/permanent, sehingga client selalu menggunakan ip tersebut sampai terputus dari jaringan, jika client terhubung kembali kemungkinan akan mendapatkan alamat ip yang sama seperti sebelumnya.

b. Alokasi Secara Dinamis

pada metode ini administrator dapat melakukan pembatasan waktu penyewaan kepada client. jadi ketika client menyewa ip kepada DHCP Server akan ada batasan waktu untuk bisa menggunakan alamat ip tersebut. jika waktunya sudah habis client dapat menyewa ip kembali dan mendpat ip yang berbeda jika ip yang sebelumnya telah digunakan client yang lain.

c. Alokasi Secara Reservation

Alokasi ini memungkinkan client melakukan pemesanan IP kepada DHCP Server. Dalam hal ini dibutuhkan MAC Address dari interface client. MAC Address (Media Access Control) adalah alamat fisik suatu interface jaringan (seperti lan card pada computer, interface/port pada router dan node pada jaringan lain) yang bersifat unik dan berfungsi sebagai identitas perangkat tersebut.

### 2.2.4 Cara Kerja DHCP

Dalam DHCP terdapat 2 komponen utama yaitu :

1. DHCP Server

DHCP Server adalah komputer yang berfungsi untuk menyediakan/menyewakan alamat IP kepada client dan informasi TCP/IP lainnya pada setiap client yang meminta. DHCP Server dapat berjalan pada sistem operasi seperti Windows NT Server, Windows 2000 Server, Ubuntu Server dan Sistem operasi lain yang mendukung DHCP Server.

2. DHCP Client

DHCP Client adalah komputer yang berfungsi untuk meminta alamat IP dari DHCP Server, dan berkomunikasi dengan DHCP Server untuk mendapatkan alamat IP. DHCP Client dapat berjalan pada sistem operasi seperti Windows 98, Windows 2000, Windows XP, Windows Vista, Windows 7, Windows 8, Windows 10, Ubuntu, dan Sistem operasi lain yang mendukung DHCP Client.

DHCP menggunakan 4 proses tahapan dalam pengalokasian alamat ip yaitu :

![Proses DHCP!](https://i0.wp.com/study-ccna.com/wp-content/images/dhcp_process_explained.jpg "Proses DHCP")

1. Discover

Pada tahapan ini, client akan mengirimkan permintaan untuk alamat ip kepada server DHCP. Client akan mengirimkan paket broadcast yang berisi informasi MAC Address dan informasi lainnya. Server DHCP akan menerima paket broadcast tersebut dan akan memeriksa apakah ada alamat ip yang tersedia untuk client tersebut. Jika ada, maka server DHCP akan mengirimkan paket unicast kepada client yang berisi informasi alamat ip yang akan diberikan kepada client tersebut.

2. Offer

Pada tahapan ini, server DHCP akan mengirimkan paket unicast kepada client yang berisi informasi alamat ip yang akan diberikan kepada client tersebut. Client akan menerima paket unicast tersebut dan akan memeriksa apakah alamat ip tersebut dapat digunakan oleh client tersebut. Jika alamat ip tersebut dapat digunakan oleh client tersebut, maka client akan mengirimkan paket unicast kepada server DHCP yang berisi informasi alamat ip yang akan digunakan oleh client tersebut.

3. Request

Pada tahapan ini, client akan mengirimkan paket unicast kepada server DHCP yang berisi informasi alamat ip yang akan digunakan oleh client tersebut. Server DHCP akan menerima paket unicast tersebut dan akan memeriksa apakah alamat ip tersebut dapat digunakan oleh client tersebut. Jika alamat ip tersebut dapat digunakan oleh client tersebut, maka server DHCP akan mengirimkan paket unicast kepada client yang berisi informasi alamat ip yang akan digunakan oleh client tersebut.

4. Acknowledge

Pada tahapan ini, server DHCP akan mengirimkan paket unicast kepada client yang berisi informasi alamat ip yang akan digunakan oleh client tersebut. Client akan menerima paket unicast tersebut dan akan memeriksa apakah alamat ip tersebut dapat digunakan oleh client tersebut. Jika alamat ip tersebut dapat digunakan oleh client tersebut, maka client akan mengirimkan paket unicast kepada server DHCP yang berisi informasi alamat ip yang akan digunakan oleh client tersebut.

Empat tahapan diatas hanya akan dilakukan bagi client yang pertama kali mengakses jaringan. Jika client tersebut sudah pernah mengakses jaringan, maka client tersebut akan mengirimkan paket unicast kepada server DHCP yang berisi informasi alamat ip yang akan digunakan oleh client tersebut.

## 2.3 Langkah Praktikum

Pada praktikum kali ini kita akan menggunakan Sistem Operasi Ubuntu Sebagai Server dan Windows sebagai client.

### 2.3.1 Langkah-langkah Konfigurasi DHCP Server

1. langkah pertama yang dilakukan adalah melakukan update repository pada sistem operasi Ubuntu dengan perintah :

```powershell
apt-get update
```

2. langkah kedua yang dilakukan adalah melakukan instalasi DHCP Server pada sistem operasi Ubuntu dengan perintah :

```powershell
apt-get install -y isc-dhcp-server
```

3. Syarat DHCP Server adalah konfigurasi ip statis pada interface eth0 pada sistem operasi Ubuntu dengan perintah :

```powershell
nano /etc/network/interfaces
```

masukkan konfigurasi ip statis pada interface eth0 dengan format sebagai berikut :

```powershell
auto eth0
iface eth0 inet static
address 192.168.10.1
netmask 255.255.255.0
gateway 192.168.10.254
```

keterangan :

- Auto eth0 : berfungsi untuk mengaktifkan interface eth0
- iface eth0 inet static : berfungsi untuk mengkonfigurasi interface eth0 menjadi ip statis
- address : berfungsi untuk mengkonfigurasi ip address pada interface eth0
- netmask : berfungsi untuk mengkonfigurasi netmask pada interface eth0
- gateway : berfungsi untuk mengkonfigurasi gateway pada interface eth0

4. Setelah konfigurasi ip statis pada interface eth0, maka dilakukan restart interface eth0 dengan perintah :

```powershell
ifdown eth0 && ifup eth0
```

atau

```powershell
service networking restart
```

jika tidak bisa laukakn restart komputer

```powershell
reboot
```

5. lakukan pengecekan apakah ip statis pada interface eth0 sudah berubah dengan perintah :

```powershell
ifconfig
```

6. lakukan konfigurasi file isc-dhcp-server pada directory /etc/default/ dengan perintah :

```powershell
nano /etc/default/isc-dhcp-server
```

7. masukkan konfigurasi berikut pada file isc-dhcp-server :

```powershell
INTERFACESv4="eth0"
atau
INTERFACES="eth0"
```

8. konfigurasi pada file dhcpd.conf pada directory /etc/dhcp/ dengan perintah :

```powershell
nano /etc/dhcp/dhcpd.conf
```

9. masukkan konfigurasi berikut pada file dhcpd.conf :

   - alokasi Secara dinamis
     buka file dhcpd.conf dan cari baris dengan awalan "A slightly different configuration for an internal subnet" dan hapus semua baris yang ada di dalamnya, kemudian masukkan konfigurasi berikut :

```powershell
subnet 192.168.1.0 netmask 255.255.255.0 {
 range 192.168.10.100 192.168.10.200;
 option routers 192.168.19.254;
 option domain-name-servers 192.168.10.1;
#option domain-name "mydomain.example";
 option broadcast-address 192.168.10.255;
 default-lease-time 600;
 max-lease-time 7200;
}
```

keterangan :

- subnet : berfungsi untuk mengkonfigurasi subnet pada jaringan
- netmask : berfungsi untuk mengkonfigurasi netmask pada jaringan
- range : berfungsi untuk mengkonfigurasi range ip yang akan diberikan pada client
- option routers : berfungsi untuk mengkonfigurasi gateway pada jaringan
- option domain-name-servers : berfungsi untuk mengkonfigurasi dns server pada jaringan
- option broadcast-address : berfungsi untuk mengkonfigurasi broadcast address pada jaringan
- default-lease-time : berfungsi untuk mengkonfigurasi waktu default lease time pada jaringan
- max-lease-time : berfungsi untuk mengkonfigurasi waktu max lease time pada jaringan

Konfigurasi diatas adalah konfigurasi dhcp untuk alokasi ip secara dinamis, sedangkan untuk konfigurasi dhcp secara automatic beritanda (#) didepan default-lease-time dan max-lease-time.

10. lakukan restart service isc-dhcp-server dengan perintah :

```powershell
service isc-dhcp-server restart
atau
sudo systemctl restart isc-dhcp-server.service
```

11. lakukan pengecekan apakah service isc-dhcp-server sudah berjalan dengan perintah :

```powershell
service isc-dhcp-server status
atau
sudo systemctl status isc-dhcp-server.service
```

- alokasi secara reservation

12. lihat alamat MAC address pada client

    buka file dhcpd.conf dan tambahkan konfigurasi berikut di akhir :

```powershell
host server {
 hardware ethernet 00:0c:29:5a:5a:5a;
 fixed-address 192.168.10.6;
}
```

keterangan :

- host server : pemberi alamat dhcp
- hardware ethernet : berfungsi untuk mengkonfigurasi alamat mac address pada client
- fixed-address : berfungsi untuk mengkonfigurasi ip address pada client

13. lakukan restart service isc-dhcp-server dengan perintah :

```powershell
service isc-dhcp-server restart
atau
sudo systemctl restart isc-dhcp-server.service
```
