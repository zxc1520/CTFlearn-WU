# My Friend John
## Miscellaneous

### Skor:
30 Points

### Deskripsi:
Have you met my friend John?

He's not so scary, even though they call him "The Ripper".

### Author:
Namespace

### Solusi
#### langkah-langkah
- Lihat kategori dari soal yang diberikan
- Pahami clue dari soal yang diberikan

Pada soal, saya cukup merasa curiga dengan si pembuat maksud, yakni teman dari beliau yang bernama "John the Ripper" karena setelah file tersebut didownload dan dibuka maka akan dimitai keterangan password. 

Sepintas saya teringat bahwa Kali Linux telah menyediakan build-in tools password cracker berupa fcrackzip, john the reaper dan juga wordlistnya. langsung saya cek dimana letak wordlist
```
locate wordlist
```

setelah selesai maka langsung saya lakukan password cracking dengan skrip berikut
```sh
fcrackzip -u -D -p /usr/share/wordlist/rockyou.txt use-rockyou.zip
```

`fcrackzip` adalah tool yang digunakan untuk meretas sebuah file zip yang perisikan password, `-u` untuk menyortir password yang terlampau salah, `-d` berarti menggunakan Dictionary dan `-p` untuk menggunakan string sebagai inisial file password.

```sh
ls -la
```
jika sudah selesai maka hasil folder yang terekstrak akan muncul, dan terdapat file wordlist dari folder zip tersebut, maka kita gunakan wordlist yang sudah disediakan ini

```sh
fcrackzip -u -D -p custom-list.txt use-rockyou.zip
```

jika sudah dan berhasil maka akan tedapat satu file lagi berupa zip, kita gunakan cara fcrackzip kembali untuk membuka file zip tersebut, namun untuk kali ini kita menggunakan wordlist rockyou.txt

```sh
ls | grep -i flag && cat flag.txt
```

dan eureka ! flag berhasil ditemukan !

## Flag
```sh
CTFlearn{s0_n0W_y0uv3_M3t_J0hN}
```