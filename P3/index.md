# pertemuan 3
Selamat datang di pertemuan ketiga IT CLUB Cyber! Pada sesi ini, kita akan mendalami salah satu tahap penting dalam keamanan siber, yaitu Information Gathering & Vulnerability Analysis. \
Materi ini merupakan langkah awal yang penting dalam memahami cara menemukan dan menganalisis potensi kerentanan pada target sistem.

Sebelum kita memulai materi hari ini, saya ingin menjelaskan tentang tahapan penetration testing (pentest). \
Hal ini belum sempat dibahas pada pertemuan sebelumnya, jadi penjelasan ini bisa menjadi tambahan wawasan untuk kalian.

Proses pentest umumnya terdiri dari beberapa tahapan utama, yaitu:
1. Information Gathering (Reconnaissance):
2. Vulnerability Analysis:
3. Exploitation:
4. Post-Exploitation:
5. Reporting:

## A. Information Gathering
- information gathering merupakan Pengumpulan informasi sebanyak-banyak nya ke target dengan tujuan menemukan salah satu atau lebih kerentananan yang ada di dalam target.
- Teknik information gathering disebut juga dengan **reconnaissance** atau pengintaian. 

## jenis jenis Information Gathering
### 1. Information Gathering Pasif
- Proses pengumpulan informasi tentang target tanpa berinteraksi langsung dengan sistem atau jaringan target.
- Tidak menyentuh atau berinteraksi langsung dengan sistem target.
- contoh:
  - Anda mengunjungi halaman Facebook/situs Web perusahaan target
    
### 2. Information Gathering Active
- Pengumpulan informasi di mana alat yang digunakan benar-benar mengirimkan probe ke jaringan atau sistem target untuk mendapatkan respons yang kemudian digunakan untuk menentukan postur jaringan atau sistem.
- Melibatkan interaksi langsung dengan sistem target
- contoh:
  - Anda melakukan ping ke alamat IP server web perusahaan untuk memeriksa apakah lalu lintas ICMP diblokir
  - Anda bertemu dengan administrator TI perusahaan target di sebuah pesta undangan. Anda mencoba menggunakan rekayasa sosial untuk mendapatkan lebih banyak informasi tentang sistem dan infrastruktur jaringan mereka.

## Teknik Teknik Information Gathering
### Network-Based Information Gathering
- **Footprinting Jaringan**: Mengidentifikasi IP Address, rentang jaringan, dan layanan terbuka.
- Tools yang digunakan:
  - **Nmap**: untuk scanning port dan jaringan.
  - **Netcat (nc)**: untuk komunikasi langsung atau troubleshooting jaringan.
  - **Wireshark**: untuk menganalisis lalu lintas jaringan.

### Website-Based Information Gathering
- Mencari informasi sensitif pada website:
  - Direktori tersembunyi melalui **Dirb** atau **Gobuster**.
  - Melihat metadata file dengan **ExifTool**.
  - Mengecek kerentanan spesifik dengan Nikto atau **Wapiti**.

### DNS Enumeration
- Mengidentifikasi subdomain atau informasi DNS menggunakan:
  - **dnsenum**.
  - **Sublist3r**.

### Social Engineering Information Gathering
- Mengumpulkan informasi melalui manusia, seperti mempelajari akun media sosial, phishing, atau survei.

## Tujuan Information Gathering
- Memahami Struktur Target
- Mengidentifikasi Kelemahan Potensial
- Menyusun Strategi Penetrasi

---
# B. Vulnerability Analysis
- Vulnerability Analysis merupakan Menganalisis informasi yang telah dikumpulkan untuk mengidentifikasi kelemahan atau kerentanan pada sistem, jaringan, aplikasi, atau infrastruktur yang dapat dieksploitasi oleh penyerang.
- ini merupakan tahap selanjutnya setelah Information Gathering.

## Jenis Vulnerability Analysis
### 1. Manual Vulnerability Analysis
- Dilakukan oleh manusia menggunakan pengalaman, logika, dan inspeksi manual terhadap kode, konfigurasi, atau sistem.
- Misalnya:
  - Menginspeksi konfigurasi file seperti /etc/passwd di Linux.
  - Meninjau kode sumber aplikasi secara manual untuk mencari kelemahan.

### 2. Automated Vulnerability Analysis
- Menggunakan tools otomatis untuk memindai sistem dan mengidentifikasi kelemahan.
- Misalnya:
  - Memindai kerentanan pada port terbuka menggunakan Nmap.
  - Menggunakan Nessus atau OpenVAS untuk memeriksa daftar CVE yang dikenal.

## Tujuan Vulnerability Analysis
### 1. Mengidentifikasi Kerentanan
- Mencari konfigurasi yang salah, software usang, atau kelemahan yang diketahui (CVE - Common Vulnerabilities and Exposures).

### 2. Memprioritaskan Risiko
- Menilai tingkat keparahan (severity) dari kerentanan berdasarkan dampaknya pada keamanan.

### 3. Membantu Perencanaan Mitigasi
- Memberikan rekomendasi langkah perbaikan untuk mencegah eksploitasi kerentanan.

## Langkah-langkah Vulnerability Analysis
### 1. Identifikasi Target
- Tentukan komponen mana yang akan dianalisis, seperti server, aplikasi, perangkat IoT, atau jaringan.

### 2. Pemindaian Kerentanan
- Gunakan tools untuk mendeteksi kelemahan seperti:
  - Software usang.
  - Port terbuka yang tidak perlu.
  - Konfigurasi sistem yang salah.

### 3. Analisis dan Verifikasi
- Tinjau hasil pemindaian dan verifikasi apakah kerentanan benar-benar ada (tidak semua hasil pemindaian adalah valid).
- Pastikan kerentanan tersebut memiliki dampak nyata pada keamanan.

### 4. Klasifikasi dan Prioritas
- Kategorikan kerentanan berdasarkan tingkat risiko:
  - Tinggi (High): Misalnya, kerentanan eksekusi kode jarak jauh (RCE).
  - Sedang (Medium): Misalnya, kerentanan yang membutuhkan autentikasi sebelum eksploitasi.
  - Rendah (Low): Misalnya, kebocoran informasi publik.

### 5. Pelaporan
- Buat laporan terstruktur yang berisi kerentanan yang ditemukan, dampak potensial, dan rekomendasi mitigasi.

# Perbedaan Passive dan Active Reconnaissance
## Passive Reconnaissance: 
- Tidak menyentuh atau berinteraksi langsung dengan sistem target.
- Contohnya adalah mencari informasi di internet. Tools yang digunakan : 
  - google dorking
  - [https://www.exploit-db.com/google-hacking-database](https://www.exploit-db.com/google-hacking-database)
  - Whois
  - Nslookup
  - Dig
  - [https://www.shodan.io/host/](https://www.shodan.io/host/) ip domain/ip host target  

## Active Reconnaissance:
- Melibatkan interaksi langsung dengan sistem target, seperti melakukan scan port atau mencoba mengakses server. 
- Hal ini membutuhkan keterlibatan langsung dengan target. Anggap saja seperti Anda memeriksa kunci pintu dan jendela, di antara titik masuk potensial lainnya.
- Contoh aktivitas pengintaian aktif meliputi:
  - Menghubungkan ke salah satu server perusahaan seperti **HTTP, FTP, dan SMTP**.
  - Menelepon perusahaan untuk mendapatkan informasi (rekayasa sosial).
  - Memasuki lokasi perusahaan dengan berpura-pura menjadi tukang reparasi.
- Mengingat sifat invasif dari pengintaian aktif, seseorang dapat dengan cepat mendapatkan masalah hukum kecuali jika mendapatkan otorisasi hukum yang tepat.
- Tools yang digunakan : 
  - **nmap**
  - **ping**
  - **traceroute**
  - **telnet**
  - **nc**

## Tools-tools recon Pasif
### Whois
- Mengambil informasi publik dari database registrar domain, seperti pendaftar domain, kontak admin, dan tanggal kadaluarsa domain.
  ```bash
  whois vulnweb.com
  ```

### nslookup
- Mirip dengan dig, digunakan untuk query informasi DNS dari domain tertentu.
  ```bash
  nslookup tryhackme.com
  nslookup -type=TXT tryhackme.com
  nslookup -type=A tryhackme.com
  ```
- table dns

  | Query type |       Result       |
  |:----------:|:------------------:|
  | A          | IPv4 Addresses     |
  | AAAA       | IPv6 Addresses     |
  | CNAME      | Canonical Name     |
  | MX         | Mail Servers       |
  | SOA        | Start of Authority |
  | TXT        | TXT Records        |

### dig
- Digunakan untuk memeriksa informasi DNS, seperti alamat IP yang terkait dengan domain, catatan MX (email), atau catatan NS (Name Server).
  ```bash
  dig tryhackme.com
  dig tryhackme.com TXT
  dig @1.1.1.1 tryhackme.com
  ```

## Tools - tools recon aktif
### Nmap
- Nmap diciptakan oleh Gordon Lyon (Fyodor), seorang ahli keamanan jaringan dan pemrogram sumber terbuka. 
- Dirilis pada tahun 1997. Nmap, kependekan dari Network Mapper, adalah perangkat lunak sumber terbuka gratis yang dirilis di bawah lisensi GPL. 
- Nmap adalah alat standar industri untuk memetakan jaringan, mengidentifikasi host langsung, dan menemukan layanan yang berjalan.

## summary recon pasif

|               Purpose               |           Command Line Example          |
|:-----------------------------------:|:---------------------------------------:|
| Lookup WHOIS record                 | whois tryhackme.com                     |
| Lookup DNS A records                | nslookup -type=A tryhackme.com          |
| Lookup DNS MX records at DNS server | nslookup -type=MX tryhackme.com 1.1.1.1 |
| Lookup DNS TXT records              | nslookup -type=TXT tryhackme.com        |
| Lookup DNS A records                | dig tryhackme.com A                     |
| Lookup DNS MX records at DNS server | dig @1.1.1.1 tryhackme.com MX           |
| Lookup DNS TXT records              | dig tryhackme.com TXT                   |

## summary recon aktif

|      Command     |                 Example                 |
|:----------------:|:---------------------------------------:|
| ping             | ping -c 10 MACHINE_IP on Linux or macOS |
| ping             | ping -n 10 MACHINE_IP on MS Windows     |
| traceroute       | traceroute MACHINE_IP on Linux or macOS |
| tracert          | tracert MACHINE_IP on MS Windows        |
| telnet           | telnet MACHINE_IP PORT_NUMBER           |
| netcat as client | nc MACHINE_IP PORT_NUMBER               |
| netcat as server | nc -lvnp PORT_NUMBER                    |

# Challenge / Soal
Pada pertemuan sebelumnya, terdapat beberapa soal yang bisa kalian coba untuk memperdalam pemahaman. Jika kalian tertarik untuk mencobanya, silakan kunjungi tautan berikut:

- [soal](./soal.html)

Setelah menyelesaikan soal-soal tersebut, kalian juga bisa mengecek jawaban di tautan berikut:

- [jawaban](./jawaban.html)