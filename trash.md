# minggu 1: Dasar Command Linux

## Persiapan
- Termux (Android)
  - install: playstore, F-droid, Github (recomended)
- Windows Subsystem Linux (windows)
  - install: microsoft store
- Linux Virtual (VM)
  - install: virtual box, vmware

## materi 1: command linux dasar
### syntax
```bash
whoami  # Menampilkan nama user yang sedang login
ls      # Melihat isi direktori
pwd     # Menampilkan lokasi direktori saat ini
cd      # Berpindah direktori
mkdir   # Membuat direktori baru
touch   # Membuat file kosong
nano    # Editor teks dasar
rm      # Menghapus file/direktori
cp      # Menyalin file/direktori
mv      # Memindahkan atau mengganti nama file/direktori
```

### example
```bash
mkdir CyberSec
cd CyberSec
touch tools.txt
```

## materi 2: penggunaan tanda &&, ;, |
- ```&&``` → Menjalankan perintah kedua jika perintah pertama sukses.
  ```bash
  mkdir Project && cd Project
  ```
- ```;``` → Menjalankan beberapa perintah secara berurutan (terlepas sukses/gagal)
  ```bash
  mkdir Test; touch Test/file.txt; ls Test
  ```
- ```|``` (Pipe) → Mengoper output perintah pertama sebagai input ke perintah kedua
  ```bash
  ls | grep file.txt
  ```

## materi 3: penggunaan >, >>, <<
- ```>``` → Mengarahkan output ke file (menimpa isi file)
  ```bash
  echo "Hello, World!" > message.txt
  ```
- ```>>``` → Mengarahkan output ke file (menambahkan tanpa menimpa isi file)
  ```bash
  echo "New Line" >> message.txt
  ```
- ```<<``` → Membuat heredoc untuk input berkelanjutan.
  ```bash
  cat << EOF > config.txt
  This is a sample config file
  EOF
  ```

## materi 4: command tambahan 
### syntax
```bash
grep     # Mencari teks tertentu dalam file
find     # Mencari file/direktori berdasarkan nama
curl     # Mengunduh atau mengirim data dari/ke URL
wget     # Mengunduh file dari URL
file     # Menentukan tipe file
tar      # Mengarsipkan file/direktori
unzip    # Mengekstrak file ZIP
strings  # Menampilkan string teks yang bisa dibaca dari file binary
xxd      # Menampilkan file dalam format heksadesimal
base64   # Encode/decode data dalam format Base64
tr       # Mengganti atau menghapus karakter dalam teks
```

### example
- ```grep```: Cari teks tertentu dalam file
  ```bash
  grep -i "password" config.txt
  grep -v "# " /etc/nginx/nginx.conf
  ```
- ```find```: Mencari file atau direktori
  ```bash
  find . -name "secret.txt"
  find /path/to/dir -type f -name "*.log"
  ```
- ```wget```: Mengunduh file dari URL
  ```bash
  wget https://example.com/file.zip
  ```
- ```curl```: Melihat dan mengunduh konten dari URL
  ```bash
  curl https://example.com
  curl -o output.html https://example.com
  ```
- ```file```: Menentukan tipe file
  ```bash
  file document.pdf
  ```
- ```tar``` dan ```unzip```: Mengarsipkan dan Mengekstrak File
  ```bash
  # create archive
  tar -cvf archive.tar file1 file2

  # extract arvhive
  tar -xvf archive.tar

  # unzip file
  unzip file.zip
  ```
- ```strings``` dan ```xxd```: Analisis File
  - Tampilkan teks yang bisa dibaca dari file biner:
    ```bash
    strings binaryfile.bin
    ```
  - Tampilkan file dalam format heksadesimal
    ```bash
    xxd binaryfile.bin
    ```
- ```base64```: Encode/Decode Data
  ```
  echo "halo" | base64
  echo "SGVsbG8gV29ybGQh" | base64 -d
  ```
- ```tr```: Mengganti atau Menghapus Karakter
  ```bash
  echo "hello world" | tr a-z A-Z   # Ganti huruf kecil menjadi huruf besar 
  echo "abc123xyz" | tr -d 0-9      # Hapus angka dari teks:
  echo "hi aria" | tr "hi" "halo"   # Ganti karakter spesifik:
  ```

# minggu 2: belum tau

# minggu 3: ctf

# minggu 4: ctf