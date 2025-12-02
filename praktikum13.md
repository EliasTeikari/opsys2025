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


## Ülesanne 4

```bash
#!/bin/bash
valjund=$(ls)
for i in $valjund
do
        if [ ${i##*.} = txt ]; then
                uus_fail="${i/.txt/.csv}"
                mv "$i" "$uus_fail"
                echo "Nimetasin: $i -> $uus_fail"
        fi
done
```

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
