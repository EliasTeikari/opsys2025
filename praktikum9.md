# Praktikum 9 - Teenused ja optimeerimine #

### Ülesanne 1 ###

Käsk:
sudo su
echo $PWD

Väljund:
/home/elias

### Ülesanne 2 ###
<img width="905" height="707" alt="image" src="https://github.com/user-attachments/assets/4baae07d-b95e-4d4e-889e-00bcc95ebd36" />

### Ülesanne 3 ###
Valisin tarkvaraks Thunderbirdi. Thunderbird on Mozilla loodud e-posti ja uudiste klient. Kasutan veebipõhist e-posti (nt Gmail) ja ei vaja eraldi meiliklienti. Tarkvara võtab kettaruumi ja töötab taustal ilma vajaduseta. Vabastatud kettamaht: 211 kB  

<img width="957" height="688" alt="image" src="https://github.com/user-attachments/assets/e014e6be-eaf7-4422-ab07-798e2252dad5" />

<img width="880" height="484" alt="image" src="https://github.com/user-attachments/assets/b33baca3-5e6c-4190-bd63-86b0185db1ac" />

<img width="872" height="115" alt="image" src="https://github.com/user-attachments/assets/9c668fb9-5515-4121-a9a5-db9471da8e0d" />

### Ülesanne 4 ###
<img width="1277" height="1045" alt="image" src="https://github.com/user-attachments/assets/8fb2e6bb-91d0-4813-986d-b5ff5119a4fd" />

### Ülesanne 5 ###
Kui sama nimega EXE-fail on olemas nii kasutaja kui süsteemi %Path% kaustades,
siis Windows käivitab selle, mis leitakse esimesena otsingujärjekorras.
Tavaliselt tähendab see, et jooksvasse kausta või kasutaja PATH-i kuuluv fail on prioriteetsem kui süsteemikausta oma.

Linuxis toimub otsing $PATH muutujas vasakult paremale.
Turvalisuse poolest on Linuxi lähenemine tugevam, sest tavakasutaja ei saa süsteemseid faile üle kirjutada ega samanimelisi programme süsteemikaustadesse lisada.

### Ülesanne 6 ###
<img width="646" height="663" alt="image" src="https://github.com/user-attachments/assets/d9941a8b-411b-4d7f-b74f-a1642d518fa3" />
Valisin teenuse Themes. Service name: Themes
Path to executable: C:\Windows\System32\svchost.exe -k netsvcs -p
Startup type: Automatic
Service status: Running

Themes-teenus haldab kasutajaliidese välimust ja kujundusi Windowsis (nt tumerežiim, värviteemad, akna efektid ja taustad). See võimaldab süsteemil kuvada graafilise liidese (GUI) elemente kaasaegses stiilis ning hallata kasutaja poolt valitud kujundusi.
Teenuse töötamine on vajalik kui soovid kasutada kaasaegset Windowsi välimust ja teemasid.
Kui teenus peatada või määrata „Disabled“, siis süsteem kasutab klassikalist halli Windows 2000 stiili ja graafilised efektid kaovad.
Teenuse keelamine ei kahjusta süsteemi toimimist, kuid muudab välimuse visuaalselt ebameeldivaks ja vähem kasutajasõbralikuks.

Themes-teenus on vajalik esteetilise kasutajaliidese jaoks. Seda ei soovitata keelata, kui soovid säilitada Windowsi tänapäevase välimuse.
