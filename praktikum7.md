# Praktikum 7 - Haakimine # 

### 1. Miks uued andmekandjad vajavad lähtestamist? ###

1) Uued andmekandjad vajavad lähtestamist, sest neil puudub partitsioonitabel, mis on andmestruktuur, mis määrab, kuidas kettal asuvad andmed jaotatakse loogilisteks draivideks. Lähtestamise käigus luuakse see tabel (nt GPT või MBR), mille abil operatsioonisüsteem saab aru, kus partitsioonid algavad ja lõppevad ning kuidas neid adresseerida. Ilma lähtestamiseta ei oska süsteem kettal olevaid sektoreid korralikult lugeda ega sinna faile salvestada, kuna puudub vajalik metainfo ketta loogiliseks struktuuriks.

2)
- Toetus suurtele ketastele – GPT kasutab 64-bitist LBA aadressimist, mis võimaldab hallata üle 2 TB suuruseid kettaid (MBR piir on 2 TB).
- Rohkem partitsioone – GPT võimaldab luua kuni 128 primaarset partitsiooni ilma loogiliste või laiendatud jaotusteta (MBR lubab vaid 4).
- Redundantsus ja taastatavus – GPT salvestab partitsioonitabeli koopiad nii ketta alguses kui lõpus, võimaldades neid vigastuse korral taastada.
- Andmete terviklikkuse kontroll (CRC32) – GPT kasutab kontrollsummasid partitsioonitabelite vigade tuvastamiseks, mis suurendab töökindlust ja kaitseb korruptsiooni eest.

