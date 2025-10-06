# Praktikum 5 - Linux failiõigused #


## Lahendused ##
### Ülesanne 5-1 ###
<img width="804" height="189" alt="yl-5-1-b" src="https://github.com/user-attachments/assets/c098973a-cc75-44f8-857e-343b04f26562" />

<img width="591" height="165" alt="yl-5-1" src="https://github.com/user-attachments/assets/0d9d828b-590f-400f-96f1-e78c0bb507db" />

Faili minufail.txt lugemiseks peab kasutajal olema kataloogil /tmp/kaust vähemalt x (execute) õigus, et ta saaks kausta siseneda, ning failil endal r (read) õigus, et faili sisu oleks loetav. Faili kustutamiseks peab kasutajal olema kataloogil /tmp/kaust õigused w (write) ja x (execute), sest kustutamine toimub kausta tasemel, mitte faili sees, ning failil endal ei pea seejuures olema ühtegi õigust.

### Ülesanne 5-2 ###

Shelli skripti käivitamiseks ei piisa ainult käivitusõigusest, sest shell peab saama faili sisu lugeda, et seda tõlgendada.
Seega on vaja lisaks täitmisõigusele ka lugemisõigust (r).

### Ülesanne 5-3 ### 

Igal kasutajal on oma nimega grupp, et tagada failisüsteemi turvalisus ja eraldatus. Nii ei pääse teised kasutajad tema failidele ligi.
See võimaldab ka hiljem paindlikult lisada kasutajaid ühiskasutusega gruppidesse ilma isiklike õigusi rikkumata.

### Ülesanne 5-4 ### 

<img width="1012" height="254" alt="yl 5-4" src="https://github.com/user-attachments/assets/cdf43445-e89f-44d6-838a-557e08d4dcc0" />

### Ülesanne 5-5 ###

<img width="919" height="332" alt="yl 5-5" src="https://github.com/user-attachments/assets/5c9c3b9d-e695-4a2d-bb93-591e14bdfd4e" />
Setuid õigus võimaldab programmil käivituda faili omaniku õigustes. Antud juhul saab kasutaja jukuisa lugeda faili hinded.txt, mis on tegelikult ainult kasutajale opetaja loetav. Programm tötab opetaja õigustes, seega saab ta faili avada ja kuvada Juku hinded.

### Ülesanne 5-6 ###

Setuid võib vähendada turvalisust, näiteks kui programm on vigane, saab ründaja selle kaudu õigusi muuta. kasuta ainult lihtsaid, auditeeritud programme ja anna minimaalsed õigused.

### Ülesanne 5-7 ###

<img width="770" height="207" alt="5-7-esimene" src="https://github.com/user-attachments/assets/4b116df3-9ab6-4564-b867-914641ada0a3" />
<img width="938" height="172" alt="5-7_teine" src="https://github.com/user-attachments/assets/17ab82f2-8897-4014-bca5-17af27418492" />

Kustutada saavad ainult faili omanik (peeter), kataloogi omanik (opetaja) ja root. Seega saavad kasutaja peeter loodud faile kustutada ainult:
1. peeter, 2. opetaja, 3. root.

### Ülesanne 5-8 ###

<img width="824" height="324" alt="5-8_ülesanne" src="https://github.com/user-attachments/assets/f4a502f5-7665-4fb8-aa2b-4076bec6c1fa" />

### Ülesanne 5-9 ### 

<img width="689" height="191" alt="5-9 lahenndus" src="https://github.com/user-attachments/assets/8fc7cd7f-d3fc-431f-bb3d-5cae86caf3ce" />

Ainult root-kasutaja saab muuta või eemaldada +i atribuudi.Faili ei saa kirjutada, muuta ega kustutada isegi omanik.
Faili saab kustutada ainult pärast atribuudi eemaldamist käsuga sudo chattr -i testfail-2 ja seejärel sudo rm testfail-2.
