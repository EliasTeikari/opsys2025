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
