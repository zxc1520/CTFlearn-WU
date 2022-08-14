# PikesPeak
## Forensic

### Skor:
20 Points

### Deskripsi:
Pay attention to those strings!

### Author:
kcbowhunter

### Solusi
#### langkah-langkah
- Lihat kategori dari soal yang diberikan
- Pahami clue dari soal yang diberikan

Diberikan soal dengan "pay attention to those string" yang berarti cermati kembali strings-strings yang diberikan.
```sh
strings PikesPeak.jpg | grep -i CTF
```

```sh
┌──(afifgh21㉿AFIFGHULAM-PC)-[~/Documents/forensic/ctflearn/PiksPeak]
└─$ strings PikesPeak.jpg | grep -i CTF
CTFLEARN{PikesPeak}
CTFLearn{Colorado}
%ctflearn{MountainMountainMountain}
#cTfLeArN{CTFMountainCTFmOUNTAIN}
CTF{AsPEN.Vail}
CTFlearn{Gandalf}
ctflearning{AUCKLAND}
ctfLEARN{MtDoom}
6ctflearninglearning{Mordor.TongariroAlpineCrossing}
+CTFLEARN{MountGedePangrangoNationalPark}
$ctflearncTfLeARN{MountKosciuszko}
```
terlihat banyak sekali string yang ditampilkan, sesuai clue dari deskripsi problem setter diatas bahwa perhatikan kembali strings tersebut, hanya ada 1 string yang benar sesuai format CTFlearn, yakni
```sh
CTFlearn{h4ck3d}
```
dengan mencocokan format tersebut, maka dapat disimpulkan flag yang benar adalah string `CTFlearn{Gandalf}`
## Flag
```sh
CTFlearn{Gandalf}
```