# pertemuan 1

ini merupakan dokumentasi IT CLUB Cyber Harbas pada pertemuan 1

pada kesempatan kali ini saya ingin membuat sebuah dokumentasi untuk kalian yang tidak hadir agar bisa mencoba lab yang sudah saya buat ini

disini saya merekomendasikan kalian menggunakan termux jika memang tidak memiliki laptop.
disini saya ingin membuat cara setup termux agar bisa digunakan

## install termux
disini kalian perlu mendownload sebuah apk termux dan disini saya merekomendasikan kalian untuk mendownloadnya melalui githuub saja

- [termux-releas](https://github.com/termux/termux-app/releases)
atau gunakan link ini agar langsung mendownload apknya
- [github_arm64-v8a.apk](https://github.com/termux/termux-app/releases/download/v0.119.0-beta.1/termux-app_v0.119.0-beta.1+apt-android-7-github-debug_arm64-v8a.apk)

[![alt text](docs/images/image.png)](https://github.com/termux/termux-app/releases)

## setup termux
untuk melakukan setup termux kalian bisa cek [github saya](hattps://github.com/ariafatah0711/termux_aria) dan lakukan setup, hanya saja karena setupnya itu agak ribet disini saya sudah menyiapkan setup untuk kalian agar tidak perlu lama lama menyalinya

```
termux-setup-storage && termux-change-repo && pkg update -y && pkg upgrade -y && pkg install -y git wget zip unzip nano python python2 python3 file tar
```

setelah kalian menyalin ini kalian sudah bisa mencoba bermain main dengan perintah linux

## download lab
```
wget https://github.com/ariafatah0711/itclub/raw/refs/heads/main/P1/pertemuan_1.tar.gz ;tar -xzf pertemuan_1.tar.gz; rm -rf pertemuan_1.tar.gz
```