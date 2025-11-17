| Nr | Küsimus | Linux | Windows | Kasutatud tööriistad / käsud |
|---|---|---|---|---|
| 1 | Mitu protsessi arvutis käib? | 279 protsessi | 151 protsessi | `ps -ef \| wc -l` • Tegumihaldur |
| 2 | Kõige esimesena käivitatud protsess | `/sbin/init splash` (PID 1) | Registry | `ps -eo pid,cmd,lstart` • Process Explorer |
| 3 | Milliste kasutajate protsesse töötab? | avahi, colord, cups-browsed, elias, root, jne | Elias | `ps -eo user \| sort \| uniq` • Task Manager |
| 4 | Arvuti järjest töötamise aeg | 8 minutit | 00:15:10 | `uptime -p` • Task Manager |
| 5 | Viimati käivitatud protsess | `tail -n 5` väljund | SearchProtocolHost.exe | `ps -eo pid,cmd,lstart --sort=lstart` • Process Explorer |
| 6 | Kõige rohkem CPU kasutav protsess | `/usr/bin/gnome-shell` ~10.9% | System.exe ~7–8% | `ps -eo pcpu,pid,cmd --sort=-pcpu` • Task Manager |
| 7 | Kõige rohkem virtuaalmälu kasutav protsess | `/usr/bin/gnome-shell` (5.3 GB) | MsMpEng.exe (312 MB) | `ps -eo pid,cmd,vsz --sort=-vsz` • Task Manager |
| 8 | Kõige rohkem füüsilist mälu kasutav protsess | `/usr/bin/gnome-shell` (~9.7% MEM) | explorer.exe (~300 MB) | `ps -eo pid,cmd,%mem --sort=-%mem` • Task Manager |
| 9 | Mitu GB RAM on vaba ja hõivatud | 1.3G vaba / 1.3G kasutusel | 72% kasutusel | `free -h` • Task Manager |
| 10 | Kettal vaba ruumi | 8.0G vaba (65% kasutusel) | 52.8G vaba / 79.0G | `df -h /` • File Explorer |
| 11 | Suurim fail ja kaust | `/swap.img` (3.9G) ja `/usr` (5.8G) | pagefile.sys ja Users / Windows | `sudo du -ahx / \| sort -rh \| head` |
| 12 | /dev/zero vs /dev/urandom mõju CPU-le | /dev/zero → madal CPU; /dev/urandom → kõrge CPU | — | `sha1sum /dev/zero`, `sha1sum /dev/urandom`, `top` |
| 13.1 | Suurim kettakirjutaja | System / TiWorker | System / TiWorker | Ressursimonitor (Disk) |
| 13.2 | Fail kuhu kirjutatakse | näha File veerus | näha File veerus | Ressursimonitor |
| 13.3 | Suurim kettaluguja | System / svchost | svchost | Ressursimonitor |
| 13.4 | Fail millest loetakse | näha File veerus | näha File veerus | Ressursimonitor |
| 14 | Suurim võrguliiklus | — | svchost.exe | Ressursimonitor (Network) |
| 15 | Kuidas tuvastada, miks arvuti on aeglane? | CPU/Mälu/Ketas/Network analüüs + logid | Sama nagu Linuxis | `top`, `free`, Task Manager, Resource Monitor |


## 12 ülesanne
<img width="2083" height="2085" alt="image" src="https://github.com/user-attachments/assets/92534509-90e3-4a3a-95a2-4f58d0be91c8" />

## 14 ülesanne
<img width="1070" height="1098" alt="image" src="https://github.com/user-attachments/assets/a7d51aae-0f11-4e46-b726-ac637ad484cf" />
