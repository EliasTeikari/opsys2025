# Praktikum 5 – Failiõigused Linuxis

## Ülesanne 5-1
- a) Lugemiseks minimaalsed õigused:
  - Kaust **/tmp/kaust**: **x**
  - Fail **minufail.txt**: **r**
- b) Kustutamiseks minimaalsed õigused:
  - Kaust **/tmp/kaust**: **w+x**
  - Fail **minufail.txt**: pole nõutud

## Ülesanne 5-2
Selgitus, miks `a=x` ei piisa; vaja ka **r**.

## Ülesanne 5-3
Miks igal kasutajal on oma nimeline grupp (umask 0002 loogika).

## Ülesanne 5-4
- Lühiselgitus: kaustal **g+x**, failil **g+r**.
- Lisa siia **ekraanipildid** või kleebi käskude `id`, `ls -la`, `cat uusfail.txt` väljundid (kui tekstina on lubatud).

## Ülesanne 5-5
- Pilt: `ls -l hinded.txt`, `ls -l hindedJukul`, `jukuisa` käivitus + väljund.
- Lühiselgitus: setuid eesmärk.

## Ülesanne 5-6
Turvariskide arutelu (privilege escalation, env, race).

## Ülesanne 5-7
Sticky bit kustutamisreeglid: **faili omanik**, **kausta omanik**, **root**.

## Ülesanne 5-8
- `ls -l` tähelepanek: režiimil **+**.
- **`getfacl hinded.txt`** täielik väljund (kopeeri siia).

## Ülesanne 5-9
- Kes saab kirjutada: **keegi** enne `chattr -i` eemaldamist.
- Kustutamiseks: `sudo chattr -i testfail-2` → `rm testfail-2`.
