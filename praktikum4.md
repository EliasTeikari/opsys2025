# Praktikum 4 - Windowsi seadistamine ja turvalisus #

Praktikumis õppisin Windows 11 turvalisuse põhitõdesid: paigaldasin uuendusi, testisin viirusetõrjet ja tulemüüri, seadistasin kasutajaõigusi, privaatsussätteid ning uurisin turbelogisid ja registri muutmist.

## Minu lahendused ##

### Ülesanne 4-1 ###
<img width="1411" height="1150" alt="4-1_4praktikum_lahendus_teikari" src="https://github.com/user-attachments/assets/cda77580-cb3d-4c1b-acb3-fc69ce30b430" />

### Ülesanne 4-2 ###
<img width="2048" height="1325" alt="4-2_4praktikum_lahendus_teikari" src="https://github.com/user-attachments/assets/2d79b130-9b6d-4bb2-beaf-c27edec7c383" />

### Ülesanne 4-3 ###
<img width="2048" height="1337" alt="4-3_4praktikum_lahendus_teikari" src="https://github.com/user-attachments/assets/2fc7d603-17e8-4966-9d79-51a9239975c8" />

### Ülesanne 4-4 ###
<img width="2065" height="1361" alt="4-4_4praktikum_lahendus_teikari_1" src="https://github.com/user-attachments/assets/ee5c9dce-4d3e-4890-9829-80b908503bcb" />

Kohalik Administrator omab laialdasi haldusõigusi (failide, kasutajate, teenuste jms haldamine), kuid tegutseb ikkagi kasutajakonto tasemel piirangutega. SYSTEM (LocalSystem) on Windowsi enda sisekonto, millel on madala taseme tuuma- ja token-privileegid — selliseid õigusi tavaline administraator ei oma.

Näide tegevusest, mis nõuab SYSTEM-õigusi: seadme draiveri laadimine või mahalaadimine (SeLoadDriverPrivilege).

Mida see võimaldab: see privileeg lubab protsessil laadida kernel-tasemel draiveri (.sys faili) otse operatsioonisüsteemi tuuma-ruumi — st lisada koodi, mis töötab kõrgema õigustasemega kui tavarakendused.

Miks admin ei piisa: admin saab tavatingimustes draivereid paigaldada läbi signeeritud installiprogrammide või Windowsi haldustööriistade, kuid otsene kernelitaseme draiveri laadimine nõuab süsteemi tokeni ja madala taseme juurdepääsu (nt võimalust kutsuda kernel-API-sid), mida SeLoadDriverPrivilege annab. Ilma SYSTEM-taseme privileegita ei saa lihtsalt protsessiga kernelisse koodi injectida ega manuaalselt laetud kaitstud draivereid asendada.

### Ülesanne 4-5 ###
<img width="1265" height="1109" alt="4-5_4praktikum_lahendus_teikari_tootaja1" src="https://github.com/user-attachments/assets/792a7c7e-94e5-4d88-8ebb-d92972380d03" />

<img width="1266" height="1107" alt="4-5_4praktikum_lahendus_teikari_tootaja2" src="https://github.com/user-attachments/assets/012e1573-5e8a-48e5-bf7f-497a9dcfcf57" />


<img width="1122" height="1130" alt="lahendu4-5" src="https://github.com/user-attachments/assets/0a4c465a-9523-4c15-9e58-b5ce484315eb" />

<img width="1135" height="1131" alt="4-5555" src="https://github.com/user-attachments/assets/52358cd4-72b6-401c-a248-bfdd956e17be" />

### Ülesanne 4-6 ###
Microsofti arvates peaksin Seadme turbe alamsätetes aktiveerima funktsiooni „Mälu terviklus“ ehk hüperviisoriga kaitstud kooditervikluse (HVCI). Selle sisselülitamine muudab süsteemi turvalisemaks, kuna blokeerib pahatahtlike draiverite käivitamise ja vähendab riski, et arvutit saaks kasutada pahavara levitamiseks või süsteemi kompromiteerimiseks.

### Ülesanne 4-7 ###
<img width="1129" height="1128" alt="4-7_4praktikum_lahendus_teikari" src="https://github.com/user-attachments/assets/4888831a-bd73-402c-9dff-7ecfd88cac38" />

### Ülesanne 4-8 ###
<img width="1129" height="1128" alt="4-8_4praktikum_lahendus_teikari" src="https://github.com/user-attachments/assets/e73f3820-ea9d-4787-bf6f-46fa15d6d7ce" />

### Ülesanne 4-9 ###
<img width="1127" height="1132" alt="4-9_4praktikum_lahendus_teikari" src="https://github.com/user-attachments/assets/ea17db22-846a-404c-9493-230d3959089b" />

### Ülesanne 4-10 ###
<img width="1122" height="1128" alt="zpiergnöa" src="https://github.com/user-attachments/assets/a496e617-4fa3-49b2-a1a1-9e4e129afe33" />



