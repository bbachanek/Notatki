1\. Wyświetl na ekran 2 pierwsze wiersze pliku program.c. (head)
```sh
cd ~/temp/nauka/c
atom program.c
head program.c
```
2\. Wyświetl na ekran 4 ostatnie wiersze pliku program.c. (head, tail)
```sh
tail -n 4 program.c
```

3\. W pliku program.c znajdź wszystkie wiersze z wystąpieniem słowa „main”. (grep)
```sh
grep 'main' program.c
```
4\. Plikowi program.c nadaj następujące uprawnienia: właściciel – czytanie, pisanie, grupa – czytanie, pozostali użytkownicy: brak uprawnień. (chmod)
```sh
chmod u=rw,g=r,o=--- program.c
```
5\. Będąc w katalogu temp przenieś katalog wazne-sprawy do katalogu praca.
```sh
cd temp
mv dom/wazne-sprawy praca
```
6\. Zarchiwizuj cały katalog temp. (zip i tar)
```sh
tar -czf archiwum1.tar.gz temp
tar -czf archiwum1.tar.gz temp
```
7\. Usuń katalog temp.
```sh
rm -r temp
```

8\. Odtwórz z archiwum katalog temp. (unzip i tar)
```sh
tar -xzf archiwum1.tar.gz
unzip archiwum2.zip
