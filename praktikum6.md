# Praktikum 6 - Protsessid ja signaalid #

## 1 Ülesanne ##
<img width="1706" height="1391" alt="esimene" src="https://github.com/user-attachments/assets/2da1a781-51f8-4d3b-8daf-141c3e0c65d0" />

## 2 Ülesanne ##
<img width="825" height="980" alt="teine" src="https://github.com/user-attachments/assets/cded458a-8117-4bc6-8e95-12d83d611c8d" />

## 3 Ülesanne ##
Käsujada: ps -axu | grep daemon | tr -s ' ' | cut -d' ' -f11-
<img width="1708" height="1382" alt="kolmas" src="https://github.com/user-attachments/assets/61d3cc77-e1b0-42a6-aed8-c44b52da991d" />

## 4 Ülesanne ##
Käsujada: ip a | grep 'inet ' | grep -v '127.0.0.1' | tr -s ' ' | cut -d' ' -f3 | cut -d' ' -f3 | cut -d'/' -f1
<img width="1705" height="1392" alt="neljas" src="https://github.com/user-attachments/assets/7228c625-70ef-4988-899a-05cabb459d15" />

## 5 Ülesanne ## 

### 1. WM_MOUSEMOVE ###

Sõnum saadetakse protsessile iga kord, kui kasutaja liigutab hiirt akna kliendiala piires. wParam = 0, näitab, et hiirenuppe ega modifikaatorklahve (nt SHIFT, CTRL) polnud all.
lParam = 327686 sisaldab hiire X- ja Y-koordinaate akna suhtes. Koordinaadid on pakitud 32-bitisesse väärtusesse: madalam sõna = X, kõrgem sõna = Y.
Antud näites:
X = 327686 % 65536 = 6
Y = 327686 // 65536 = 5
See tähendab, et hiirt liigutati akna kliendialal asukohta (X=6, Y=5).
Sõnum saadetakse väga sageli (iga kord, kui hiire positsioon muutub). [https://learn.microsoft.com/en-us/windows/win32/inputdev/wm-mousemove](https://learn.microsoft.com/en-us/windows/win32/inputdev/wm-mousemove)

### 2. WM_KEYDOWN ###

Sõnum saadetakse protsessile siis, kui kasutaja vajutab mõne klahvi alla.
wParam = 65 virtuaalklahvi kood (VK_A), ehk klahv “A”.
lParam = 1 sisaldab kordusloendurit ja muid bitti-infot, kuid siin tähendab see, et klahv vajutati esimest korda. See sõnum annab protsessile teada, et klahv on alla vajutatud (enne kui see vabastatakse, saadetakse hiljem WM_KEYUP). Windows saadab selle protsessile iga kord, kui kasutaja vajutab klaviatuuril mõne klahvi, millel on fookus vastavas aknas. [https://learn.microsoft.com/en-us/windows/win32/inputdev/wm-keydown](https://learn.microsoft.com/en-us/windows/win32/inputdev/wm-keydown)


Sain ka mõned “???” sõnumid, mille ID väärtused olid alla 45000.
Ühe neist õnnestus kindlaks teha:

22:51:03.422,274,"???",0,0

See vastab sõnumile WM_SYSCOMMAND (ID 274), mida Windows saadab siis, kui kasutaja klikib akna tiitliriba nupul (nt minimeerimine, maksimeerimine või sulgemine). Antud sõnum ei olnud tõlketabelis (konst.csv), seetõttu kuvatigi nime asemel “???”.
Infoallikas:
[https://learn.microsoft.com/en-us/windows/win32/winmsg/wm-syscommand](https://learn.microsoft.com/en-us/windows/win32/winmsg/wm-syscommand)


Kas soovid, et ma vormindan selle sulle markdown-tabeli kujul (nagu mõnel teisel praktikumi osal), et saad sama stiili hoida kogu failis?
