# Modul 2 - Media Transmisi Berkabel

## Tujuan Pembelajaran :

- Mahasiswa dapat memahami konsep dasar media transmisi berbentuk kabel dan dapat mengidentifikasi jenis-jenis kabel yang digunakan pada jaringan komputer.
- Mahasiswa mampu membuat kabel jaringan dengan susunan straight dan crossover.
- Mahsiswa mampu mengecek sambungan kabel straight dan crossover dengan menggunakan tester kabel.

## Persiapan

- Berdoa agar lancar dalam belajar, bagi yang membawa hp harap hp nya di _silence_ atau sekalian dimatikan

## Materi

## 2.1 Pengertian Media Transmisi Berkabel

Media transmisi adalah media yang dapat digunakan untuk mengirimkan informasi dari suatu tempat ke tempat yang lain. Media transmisi dibedakan menjadi dua, yaitu:

a. Media transmisi berkabel, yaitu media transmisi yang menghubungkan pengirim dan penerima secara fisik berupa kabel.

Media transmisi berkabel ini dibedakan menjadi:

- Twisted Pair
- Coaxial
- Fiber Optik

b. Media transmisi tanpa kabel/nirkabel ini dibedakan menjadi:

Media transmisi tanpa kabel/nirkabel ini dibedakan menjadi:

- Gelombang Mikro
- System Satelit
- Infra Merah
- Sinar Laser

## 2.2 Kabel Twisted Pair

### Twisted Pair

![Twisted Pair!](https://idmanajemen.com/wp-content/uploads/2017/10/pengertian-kabel-utp.jpeg "Twisted Pair Cable")

Kabel twisted pair (pasangan berpilin) merupakan sebuah bentuk kabel dimana dua konduktor digabungkan yang bertujuan untuk mengurangi atau meniadakan interferensi elektromagnetik dari luar seperti radiasi elektromagnetik dari kabel unshielded twisted pair (UTP), dan crosstalk (cakap silang) diantara pasangan kabel yang berdekatan. Kabel twisted pair lebih tipis, lebih mudah putus, dan mengalami gangguan lain sewaktu kabel kusut. Akan tetapi, keunggulan kabel twisted pair ini terhadap jaringan secara keseluruhan yaitru apabila sebagian kabel twisted pair rusak, maka tidak semua jaringan akan terhenti seperti yang mungkin terjadi pada kabel coaxial. Contoh dari twisted pair ini adalah Unshielded Twisted Pair (UTP) dan Shielded Twisted Pair (STP).

a. Unshielded Twisted Pair (UTP)

Unshielded Twisted Pair atau disingkat UTP adalah salah satu jenis kabel jaringan yang menggunakan bahan dasar tembaga yang tidak dilengkapi dengan shield/pelindung internal. UTP merupakan jenis kabel yang paling umum dan sering digunakan di dalam jaringan lokal (LAN) karena harganya yang cukup murah, fleksibel dan memiliki kinerja yang relatif bagus. Dalam kabel UTP ini terdapat insulasi satu lapis yang melindungi kabel dari ketegangan fisik atau kerusakan tapi tidak melindungi kabel dari interferensi elektromagnetik. Kabel UTP memiliki impendansi kira-kira 100 Ohm dan tersedia dalam beberapa kategori yang ditentukan dari kemampuan transmisi data yang dimilikinya seperti tertulis dalam tabel berikut:
![Twisted Pair!](https://static.javatpoint.com/tutorial/computer-network/images/utp-vs-stp2.png "STwisted Pair Cable")

### Tabel 1. Kategori Kabel UTP

| KATEGORI                    | KEGUNAAN                                                                                        |
| --------------------------- | ----------------------------------------------------------------------------------------------- |
| Category 1 (Cat1)           | Komunikasi suara analog, hanya cocok untuk suara saja.                                          |
| Category 2 (Cat2)           | Transmisi suara maupun data digital hingga 4 megabit per detik                                  |
| Category 3 (Cat3)           | Transmisi data digital hingga 10 megabit per detik                                              |
| Category 4 (Cat4)           | Transmisi data digital hingga 16 megabit per detik                                              |
| Category 5 (Cat5)           | Transmisi data digital hingga 100 megabit per detik                                             |
| Enhanced Category 5 (Cat5e) | Transmisi data digital hingga 250 megabit per detik                                             |
| Category 6 (Cat6)           | Transmisi data hingga diatas 1000 megabit per detik. Digunakan untuk mendukung Gigabit Ethernet |

Diantara semua kabel di atas, kabel Enhanced Category 5 (Cat5e) dan Category 5 (Cat5) merupakan kabel UTP yang paling populer yang banyak digunakan dalam jaringan berbasis teknologi Ethernet. Konektor yang biasa digunakan adalah RJ45.

b. Shielded Twisted Pair (STP)

Shielded Twisted Pair (STP) adalah kabel pasangan berpilin yang memiliki perlindungan dari logam untuk melindungi kabel dari interferensi elektromagnetik luar. Keunggulan kabel STP yaitu jaminan proteksi jaringan dari interferensi-interferensi eksternal, namun harga kabel STP ini lebih mahal dibandingkan kabel UTP.
Lapisan kabel STP bukan bagian dari sirkuit data, maka dari itu perlu di ground pada setiap ujungnya. Kabel STP tidak dapat dipakai untuk jarak jauh tanpa bantuan device penguat. Kabel shielded twisted pair (STP) memiliki kecepatan dan keluaran 10 – 100 Mbps, biaya rata-rata per node agak mahal dibandingkan UTP dan coaxial, media dan ukuran konektor medium, panjang kabel maksimum yang diizinkan hanya 100m
![Twisted Pair!](https://static.javatpoint.com/tutorial/computer-network/images/utp-vs-stp3.png "Twisted Pair Cable")
![Twisted Pair!](https://412292.smushcdn.com/560079/wp-content/uploads/sites/37/2017/03/b.-UTP-vs-STP-Cable-300x189.jpg?lossy=1&strip=1&webp=1 "Twisted Pair Cable")

## 2.3 Pengkabelan Straight Through dan Cross Over

Kabel Ethernet dapat disambungkan sebagai straight through atau crossover. Straight through adalah jenis yang paling umum dan digunakan untuk jaringan komputer.

### 2.3.1 T568A Dan T568B Wiring Standard Basis

Konektor RJ45 adalah konektor 8 posisi, 8 pin modular yang digunakan untuk mengakhiri kabel patch Cat5e atau kabel Cat6 . Pinout adalah susunan kabel khusus yang menentukan bagaimana konektor dipasang. Ada dua standar yang diakui oleh ANSI (American National Standards Institute), TIA (Telecommunication Industry Association) dan EIA (Electronic Industries Alliance), yang merupakan standarisasi internasional stuktur kabel telekomunikasi untuk pemasangan kabel Ethernet. Yang pertama adalah kabel standar T568A dan yang kedua adalah T568B. T568B telah melampaui 568A dan dipandang sebagai skema pengkabelan default untuk pemasangan kabel terstruktur twisted pair. Jika Anda tidak yakin mana yang akan digunakan, pilih 568B.
![T568A Dan T568B Wiring Standard!](https://www.cables-solutions.com/wp-content/uploads/2016/12/T568A-T568B-Wiring-Standard.png "T568A Dan T568B Wiring Standard")

### 2.3.2 Kabel Straight

Kabel straight merupakan jenis kabel yang memiliki cara pemasangan yang sama antara ujung satu dengan ujung lainnya. Kabel straight menggunakan satu standar pengkabelan, kedua ujungnya menggunakan standar pengkabelan T568A atau kedua ujungnya menggunakan standar pengkabelan T568B. Gambar berikut menunjukkan kabel straight yang kedua ujungnya disambungkan sebagai standar T568B.
![T568A Dan T568B Wiring Standard!](https://www.cables-solutions.com/wp-content/uploads/2016/12/Straight-Through-Cable.png "T568B Wiring Standard")
Fungsi kabel straight ini biasanya digunakan untuk pemasangan device yang berbeda. Kabel tipe straight ini paling banyak digunakan sampai saat ini karena fungsinya.

### Contoh penggunaan kabel straight

- Menghubungkan komputer dengan switch jaringan
- Menghubungkan komputer dengan hub jaringan
- Menghubungkan komputer dengan router jaringan
- Menghubungkan komputer dengan LAN
- Menghubungkan switch dengan hub jaringan
- Menghubungkan switch dengan router jaringan

### Susunan Warna Kabel Straight

Untuk susunan warna kabel straight ujung satu dengan ujung lainnya sama menggunakan standar T568B. Urutannya seperti berikut:

1. Putih Orange
2. Orange
3. Putih Hijau
4. Biru
5. Putih Biru
6. Hijau
7. Putih Coklat
8. Coklat

### 2.3.3 Kabel Crossover

Kabel crossover merupakan jenis kabel yang memiliki cara pemasangan yang berbeda antara ujung satu dengan ujung lainnya. Tidak seperti kabel straight through, kabel crossover menggunakan dua standar kabel yang berbeda: satu ujung menggunakan standar kabel T568A, dan ujung lainnya menggunakan standar kabel T568B. Pengkabelan internal kabel crossover Ethernet membalikkan sinyal pengiriman dan penerimaan. Ini paling sering digunakan untuk menghubungkan dua perangkat dengan jenis yang sama.
![T568A Dan T568B Wiring Standard!](https://www.cables-solutions.com/wp-content/uploads/2016/12/crossover-cable-.png "T568B Wiring Standard")

Contoh penggunaan kabel crossover

- Menghubungkan komputer dengan komputer
- Menghubungkan switch dengan switch
- Menghubungkan hub dengan hub
- Menghubungkan router dengan router

### Susuan Warna Kabel Crossover

Untuk susunan warna kabel crossover ujung satu dengan ujung lainnya berbeda menggunakan standar T568A dan T568B. Urutannya seperti berikut:

Ujung 1

1. Putih Orange
2. Orange
3. Putih Hijau
4. Biru
5. Putih Biru
6. Hijau
7. Putih Coklat
8. Coklat

Ujung 2

1. putih hijau
2. hijau
3. putih orange
4. biru
5. putih biru
6. orange
7. putih coklat
8. coklat

## 2.4 Praktikum

### Alat dan Bahan

1. Kabel UTP
2. Konektor RJ45
3. Crimping Tool
4. Tester Kabel

Setelah mempersiapkan alat dan bahan diatas, berikut adalah langkah-langkah dalam pembuatan kabel straight dan kabel crossover:

### Langkah pembuatan kabel straight :

1. Potong kabel tersebut menjadi 2 bagian dengan menggunakan crimping tool;
2. Ambil potongan pertama, kemudian masing-masing ujungnya dikupas/lepaskan pembungkus karetnya kira-kira panjangnya 4 cm sehingga terlihat bagian dalam kabel, dimana terdapat 4 pasang kabel yang terpilin;
3. Luruskan keempat pasang kabel yang berpilin tersebut pada kedua ujungnya;
4. Ambil salah satu ujung kabel yang telah lurus tersebut, kemudian buat urutan kabel dari kiri ke kanan sebagai berikut:
5. putih orange-orange-putih hijau-biru-putih biru-hijau-putih cokelatcokelat.
6. Pegang erat-erat kabel tersebut agar posisinya tidak berubah, kemudian potong rata kabel tersebut sehingga sisanya kurang lebih 1,25 cm. Pastikan ujung-ujung kabel tersebut rata dengan urutan yang benar;
7. Setelah itu masukkan kabel tersebut ke dalam RJ-45, dimana posisi kabel dari kiri ke kanan tetap sama dan posisi tonjolan RJ-45 ada di bawah. Kabel dimasukkan sampai ujung-ujung tembaga pada masing-masing kabel kelihatan dari ujung RJ-45;
8. Setelah yakin bahwa kabel sudah masuk sepenuhnya ke dalam RJ-45, crimping kabel tersebut dengan menggunakan tang crimping;
9. Lakukan langkah no 4-7 pada ujung kabel berikutnya;
10. Setelah kedua ujung kabel terpasang RJ-45, tes kabel tersebut dengan menggunakan tester. Perhatikan nyala lampu pada tester, jika lampu 1-8 pada kedua bagian tester menyala maka kabel yang dibuat telah berfungsi dengan baik. Tetapi jika salah satu atau semua lampu tidak menyala berarti terdapat kesalahan pada pemasangan RJ-45 nya.

### Langkah pembuatan kabel crossover :

1. Potong kabel tersebut menjadi 2 bagian dengan menggunakan crimping tool;
2. Ambil potongan pertama, kemudian masing-masing ujungnya dikupas/lepaskan pembungkus karetnya kira-kira panjangnya 4 cm sehingga terlihat bagian dalam kabel, dimana terdapat 4 pasang kabel yang terpilin;
3. Lakukan langkah no 3-7 pada langkah pembuatan kabel straight sebelumnya;
4. Setelah selesai dengan ujung kabel tersebut, sekarang ambil ujung kabel berikutnya yang telah diluruskan, kemudian buat urutan kabel dari kiri ke kanan sebagai berikut:
5. putih hijau-hijau-putih orange-biru-putih biru-orange-putih cokelatcokelat.
6. Pegang erat-erat kabel tersebut agar posisinya tidak berubah, kemudian potong rata kabel tersebut sehingga sisanya kurang lebih 1,25 cm. Pastikan ujung-ujung kabel tersebut rata dengan urutan yang benar;
7. Setelah itu masukkan kabel tersebut ke dalam RJ-45, dimana posisi kabel dari kiri ke kanan tetap sama dan posisi tonjolan RJ-45 ada di bawah. Kabel dimasukkan sampai ujung-ujung tembaga pada masing-masing kabel terlihat dari ujung RJ-45;
8. Setelah yakin bahwa kabel sudah masuk sepenuhnya ke dalam RJ-45, crimping kabel tersebut dengan menggunakan tang crimping;
9. Setelah kedua ujung kabel terpasang RJ-45, tes kabel tersebut dengan menggunakan tester. Perhatikan nyala lampu pada tester, jika urutan nyala lampu adalah 1-3, 2-6, 3-1, 4-4, 5-5, 6-2, 7-7, 8-8 maka kabel yang dibuat telah berfungsi dengan baik. Tetapi jika salah satu atau semua lampu tidak menyala berarti terdapat kesalahan pada pemasangan RJ-45 nya.

## Tugas

1. Buatlah sebuah kabel straight dengan menggunakan susunan standar T568B. (putih orange, orange, putih hijau, biru, putih biru, hijau, putih cokelat, cokelat)!
2. Buat dan jelaskan hasil pengukuran kabel menggunakan tester kabel!
3. Jelaskan perbedaan antara kabel straight dan crossover ditinjau dari susunan kabelnya dan penggunaannya dalam membangun sebuah jaringan komputer!
