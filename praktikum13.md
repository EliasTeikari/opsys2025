# Praktikum 13

## Ülesanne 3
```bash
#!/bin/sh
echo "Sisesta nimi"
read nimi

echo "Sisesta eriala"
read eriala

echo "martiklinumber"
read martiklinumber

echo "Sinu nimi on $nimi!"
echo "Sinu eriala on $eriala!"
echo "Sinu martiklinumber on $martiklinumber!"
```
<img width="632" height="248" alt="image" src="https://github.com/user-attachments/assets/ee07b7cf-dd3c-4d79-950f-ac92a7e5e0ac" />


## Ülesanne 4

```bash
#!/bin/bash

vana=".$1"
uus=".$2"

for fail in *$vana; do
    [ -e "$fail" ] || continue

    uus_fail="${fail/$vana/$uus}"

    mv "$fail" "$uus_fail"
    echo "Nimetasin ümber: $fail -> $uus_fail"
done
```
<img width="733" height="199" alt="image" src="https://github.com/user-attachments/assets/d978cca5-1d7f-417a-b98e-8ecc1035b334" />

## Ülesanne 5

```bash
#!/bin/bash

if [ $# -ne 1 ]; then
        echo "Kasutus: $0 <protsessi_nimi>"
        exit 1
fi

protsess=$1
IFS=$'\n'

for line in $(ps -A)
do
        clean=$(echo " $line" | tr -s ' ')
        pid=$(echo $clean | cut -d ' ' -f2)
        name=$(echo $clean | cut -d ' ' -f5)

        if [ "$name" = "$protsess" ]; then
                echo "PID: $pid Nimi: $name"
        fi
done

```

<img width="657" height="98" alt="image" src="https://github.com/user-attachments/assets/9b572f0d-1868-411f-804b-0db8d9199320" />

## Ülesanne 6
```bash
#!/bin/bash

astenda() {
        t=1
        i=1
        while [ $i -le $2 ]
        do
                t=$(($t * $1))
                i=$(($i + 1))
        done
        echo $t
}

vastus=$(astenda 9 5)
echo "9 astmes 5 = $vastus"
```
<img width="603" height="52" alt="image" src="https://github.com/user-attachments/assets/836409f5-8266-43f8-b7b6-f191140d0e85" />

## Ülesanne 7

<img width="788" height="261" alt="image" src="https://github.com/user-attachments/assets/bc3050d4-7f09-4af9-8d65-dd0326aa6506" />

<img width="1363" height="797" alt="image" src="https://github.com/user-attachments/assets/158c34a1-0246-4f00-96fd-42560081e588" />
