# termux

## Installation
install termux menggunakan salah satu metode ini \
[playstore](https://play.google.com/store/apps/details?id=com.termux) \
[F-Droid](https://f-droid.org/id/packages/com.termux/) \
[github](https://github.com/termux/termux-app/releases) (recomended) \

## github
install in termux [arm64](https://objects.githubusercontent.com/github-production-release-asset-2e65be/44804216/b80ab2fa-2cf5-442b-9245-a105f9ae7604?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=releaseassetproduction%2F20241218%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20241218T074152Z&X-Amz-Expires=300&X-Amz-Signature=056d1fbd9620b5d6f810a03030968cc2222c3721d9de08113f39abcfcdfb72b4&X-Amz-SignedHeaders=host&response-content-disposition=attachment%3B%20filename%3Dtermux-app_v0.118.1%2Bgithub-debug_arm64-v8a.apk&response-content-type=application%2Fvnd.android.package-archive)

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