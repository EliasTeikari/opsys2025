# Praktikum 7 - Haakimine # 

### 1. ülesanne ###
Uued andmekandjad vajavad lähtestamist, sest neil puudub partitsioonitabel, mis on andmestruktuur, mis määrab, kuidas kettal asuvad andmed jaotatakse loogilisteks draivideks. Lähtestamise käigus luuakse see tabel (nt GPT või MBR), mille abil operatsioonisüsteem saab aru, kus partitsioonid algavad ja lõppevad ning kuidas neid adresseerida. Ilma lähtestamiseta ei oska süsteem kettal olevaid sektoreid korralikult lugeda ega sinna faile salvestada, kuna puudub vajalik metainfo ketta loogiliseks struktuuriks.

### 2. ülesanne ###
- Toetus suurtele ketastele – GPT kasutab 64-bitist LBA aadressimist, mis võimaldab hallata üle 2 TB suuruseid kettaid (MBR piir on 2 TB).
- Rohkem partitsioone – GPT võimaldab luua kuni 128 primaarset partitsiooni ilma loogiliste või laiendatud jaotusteta (MBR lubab vaid 4).
- Redundantsus ja taastatavus – GPT salvestab partitsioonitabeli koopiad nii ketta alguses kui lõpus, võimaldades neid vigastuse korral taastada.
- Andmete terviklikkuse kontroll (CRC32) – GPT kasutab kontrollsummasid partitsioonitabelite vigade tuvastamiseks, mis suurendab töökindlust ja kaitseb korruptsiooni eest.

### 3. ülesanne ###
https://kodu.ut.ee/~eliasmikael/opsys/hdd.png

<img width="1123" height="1129" alt="7prax-3" src="https://github.com/user-attachments/assets/52fb9803-55b6-4905-a245-44e15bbb4f26" />

### 4. ülesanne ###
<img width="673" height="152" alt="prax7-pilt4" src="https://github.com/user-attachments/assets/04e30f4d-a6d7-45ab-a1d8-1e678c725751" />

### 5. ülesanne ###
<img width="1078" height="761" alt="prax4-pilttttt" src="https://github.com/user-attachments/assets/b5daa66e-621a-48ca-b3f6-a76dfc350e84" />

### 6. ülesanne ###
Käsk sudo mount -t auto -o ro /dev/sdc2 /media/usb ühendas seadme /dev/sdc2 kausta /media/usb.
Parameeter -o ro määras seadme ainult lugemiseks (read-only) ja -t auto lasi Ubuntu-l automaatselt tuvastada failisüsteemi.
Ubuntu asendas auto väärtusega fuseblk, mis näitab, et tegemist oli NTFS-failisüsteemiga.
Seade eemaldati käsuga sudo umount /media/usb, mille järel seda enam mount väljundis ei olnud.

### 7. ülesanne ###
<img width="1333" height="357" alt="fstabnb" src="https://github.com/user-attachments/assets/caa10ff5-9859-4467-bcb7-1f6839d47e4a" />
Faili /etc/fstab lõppu lisasin rea:
UUID=60C0EA74C0EA4FB8  /mnt/bigdata  ntfs  defaults  0  0

See rida tagab, et 4TB NTFS-ketas ühendatakse automaatselt Ubuntu käivitamisel kataloogi /mnt/bigdata.
Testisin käsuga sudo mount -a, mis ei andnud vigu, ja kontrollisin lsblk väljundist, et seade /dev/sdc2 oli edukalt ühendatud.


