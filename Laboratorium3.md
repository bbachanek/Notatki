1\. Wyświetl plik /etc/passwd z podziałem na strony przyjmując, że strona na 5 linii tekstu. (raczej more niż less)
```sh
 more -5 /etc/passwd
 ```
2\. Korzystając z polecenia cat utwórz plik tekst3.txt, który będzie składał się z zawartości pliku tekst1.txt, ciągu znaków podanego ze standardowego wejścia (klawiatury) i pliku tekst2.txt.
```sh
touch tekst1.txt
touch tekst2.txt
cat tekst1.txt tekst2.txt > tekst3.txt
```

4\. Wyświetl linie o numerach 3, 4 i 5 z pliku /etc/passwd.
```sh
sed -n '3,5p' /etc/passwd
```

5\. Wyświetl linie o numerach 7, 6 i 5 od końca pliku /etc/passwd.
```sh
tail -n 7 /etc/passwd | head -n 1
tail -n 6 /etc/passwd | head -n 1
tail -n 5 /etc/passwd | head -n 1
```

6\. Wyświetl zawartość pliku /etc/passwd w jednej linii.
```sh
cat /etc/passwd | tr '\n' ' '
```
7\. Za pomocą filtru tr wykonaj modyfikację pliku plik.txt, polegającą na wypisaniu każdego słowa w osobnej linii.
```sh
cat /etc/passwd | tr ' ' '\n'
```
8\. Zlicz wszystkie pliki znajdujące się w katalogu /var i jego podkatalogach.
```sh
ls -1 /var | wc -l
```
9\. Napisać polecenie zliczające ilość znaków z pierwszych trzech linii pliku /etc/passwd.
```sh
cat /etc/passwd |head -n 3 |wc -c
