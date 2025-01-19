# pertemuan 1

Selamat datang di pertemuan kedua IT CLUB Cyber! Pada sesi ini, kita akan menjelajahi dunia Capture The Flag (CTF) dengan fokus pada platform OverTheWire. \
Tujuan utama dari pertemuan ini adalah memperkenalkan konsep CTF dan memberikan panduan praktis agar kalian dapat mencoba sendiri tantangan-tantangan yang tersedia di OverTheWire. \
Bagi kalian yang tidak dapat hadir secara langsung, dokumentasi ini akan memandu langkah demi langkah untuk memulai dan menyelesaikan tantangan awal di OverTheWire. \
Jika kalian belum memiliki laptop, jangan khawatir! Kalian dapat menggunakan Termux sebagai alternatif.

untuk teori dari ppt sebelumnya bisa dilihat disini [introduce ctf](./introduce.md)

bagi yang tidak memiliki laptop disarankan menggunakan termux ntuk installasinya ikuti tutorial ini [di langkah 1-2 disini](../P1)

## 1. install ssh
### termux
```bash
pkg install openssh
```

### debian/ubuntu
```bash
apt install openssh
```

### redhat
```bash
yum install openssh
```

## 2. Memulai Tantangan OverTheWire
1. Buka Situs OverTheWire:Navigasikan ke https://overthewire.org/wargames/ untuk memilih tantangan.
2. Pilih Tantangan "Bandit":
   - Bandit adalah tantangan pemula yang sempurna untuk memahami dasar-dasar CTF.
   - Klik pada "Bandit" untuk mendapatkan detail level awal.
3. Dapatkan Informasi Level 0:
   - Server: bandit.labs.overthewire.org
   - Port: 2220
   - Username: bandit0
   - Password: bandit0
4. Masuk ke Server dengan SSH:Gunakan perintah berikut untuk terhubung:
   ```bash
   ssh bandit0@bandit.labs.overthewire.org -p 2220
   ```
   Saat diminta, masukkan password: bandit0.
5. Jika Muncul Pertanyaan tentang Fingerprint:
   - Ketikkan: yes.
   - Pertanyaan ini muncul karena server SSH belum pernah diakses sebelumnya dari perangkat Anda. Dengan mengetik "yes," Anda menyetujui untuk menambahkan fingerprint server ke daftar known_hosts.
6. Mulai Tantangan:
   - Ikuti instruksi di layar untuk menyelesaikan level pertama.
   - Gunakan perintah dasar Linux seperti ls, cd, cat, dan lainnya.

## 3. solve the overthewire bandit
[bandit level 01](./bandit/level%2001.html) \
[bandit level 02](./bandit/level%2002.html) \
[bandit level 03](./bandit/level%2003.html) \
[bandit level 04](./bandit/level%2004.html) \
[bandit level 05](./bandit/level%2005.html) \
[bandit level 06](./bandit/level%2006.html) \
[bandit level 07](./bandit/level%2007.html) \
[bandit level 08](./bandit/level%2008.html) \
[bandit level 09](./bandit/level%2009.html) \
[bandit level 10](./bandit/level%2010.html) \
[bandit level 11](./bandit/level%2011.html) \
[bandit level 12](./bandit/level%2012.html)

## 4. data for pass

| Password |                                  |
|:--------:|----------------------------------|
|  bandit0 |              bandit0             |
|  bandit1 | ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If |
|  bandit2 | 263JGJPfgU6LtdEvgfWU1XP5yac29mFx |
|  bandit3 | MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx |
|  bandit4 | 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ |
|  bandit5 | 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw |
|  bandit6 | HWasnPhtq9AVKe0dmk45nxy20cvUa6EG |
|  bandit7 | morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj |
|  bandit8 | dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc |
|  bandit9 | 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM |
| bandit10 | FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey |
| bandit11 | dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr |
| bandit12 | 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4 |