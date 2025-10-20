# Praktikum 7 - Haakimine # 

### Miks uued andmekandjad vajavad lähtestamist? ###
Uued andmekandjad vajavad lähtestamist, sest neil puudub partitsioonitabel, mis on andmestruktuur, mis määrab, kuidas kettal asuvad andmed jaotatakse loogilisteks draivideks. Lähtestamise käigus luuakse see tabel (nt GPT või MBR), mille abil operatsioonisüsteem saab aru, kus partitsioonid algavad ja lõppevad ning kuidas neid adresseerida. Ilma lähtestamiseta ei oska süsteem kettal olevaid sektoreid korralikult lugeda ega sinna faile salvestada, kuna puudub vajalik metainfo ketta loogiliseks struktuuriks.

### Tooge välja vähemalt 4 erinevat tehnilist eelist GPT kasutamiseks võrreldes MBRiga? ###
- Toetus suurtele ketastele – GPT kasutab 64-bitist LBA aadressimist, mis võimaldab hallata üle 2 TB suuruseid kettaid (MBR piir on 2 TB).
- Rohkem partitsioone – GPT võimaldab luua kuni 128 primaarset partitsiooni ilma loogiliste või laiendatud jaotusteta (MBR lubab vaid 4).
- Redundantsus ja taastatavus – GPT salvestab partitsioonitabeli koopiad nii ketta alguses kui lõpus, võimaldades neid vigastuse korral taastada.
- Andmete terviklikkuse kontroll (CRC32) – GPT kasutab kontrollsummasid partitsioonitabelite vigade tuvastamiseks, mis suurendab töökindlust ja kaitseb korruptsiooni eest.

### 3. Lisage link https://kodu.ut.ee/~kasutajatunnus/opsys/hdd.png praktikumi aruandesse tõestuseks, et olete käesoleva ülesande edukalt lahendanud. ###
https://kodu.ut.ee/~eliasmikael/opsys/hdd.png

<img width="1123" height="1129" alt="7prax-3" src="https://github.com/user-attachments/assets/52fb9803-55b6-4905-a245-44e15bbb4f26" />

### 4. Lisage käsu ls -la /mnt/ut/public_html/opsys/ väljundi pilt aruandesse. ###
<img width="673" height="152" alt="prax7-pilt4" src="https://github.com/user-attachments/assets/04e30f4d-a6d7-45ab-a1d8-1e678c725751" />

### 4. task ###
<img width="1078" height="761" alt="prax4-pilttttt" src="https://github.com/user-attachments/assets/b5daa66e-621a-48ca-b3f6-a76dfc350e84" />

