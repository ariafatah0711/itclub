# termux

## Installation
install termux menggunakan salah satu metode ini \
[playstore](https://play.google.com/store/apps/details?id=com.termux) \
[F-Droid](https://f-droid.org/id/packages/com.termux/) \
[github](https://github.com/termux/termux-app/releases) (recomended)

## github
install in github, pilih yang arm64
![alt text](docs/images/image-8.png)

lalu install aplikasinya \
![alt text](docs/images/image.png)

setelah aplikasi terinstall jalankan perintah ini untuk mensetup storage dan repo
```bash
termux-setup-storage # akses storage
termux-change-repo # change repository
```

pilih ok jika terdapat pilihan

![alt text](docs/images/image-1.png)
![alt text](docs/images/image-2.png)

jika sudah kita bisa lakukan update
```bash
pkg update && pkg upgrade
```

jika terdapat pertanyaan kita jawab aja y

![alt text](docs/images/image-3.png)

jika sudah selesai kita bisa lakukan installasi package (opsional)
```bash
pkg install git wget zip unzip nano
pkg install python python2 python3 ruby
pkg install nodejs clang php # opsional
```