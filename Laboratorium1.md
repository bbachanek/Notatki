1\. Używając lini poleceń stwórz strukturę katalogów:
```sh
mkdir {dom,nauka/{c,logo,pascal},praca/{dokumenty,zlecenia/{zrealizowane,niezrealizowane}}} -p
```
2\. Przejdź do katalogu dom i utwórz katalog wazne-sprawy.
```sh
cd dom; mkdir wazne-sprawy
```
3\. Wejdź do katalogu wazne-sprawy i utwórz tam pusty plik rachunki.txt.
```sh
cd wazne-sprawy; touch rachunki.txt
```
4\. Będąc w katalogu wazne-sprawy skopiuj plik rachunki.txt do katalogu zrealizowane.
```sh
cp rachunki.txt ../../praca/zlecenia/zrealizowane/
```
5\. Przejdź do katalogu zrealizowane i zmień nazwę pliku rachunki.txt na wykonano.txt.
```sh
cd ../../praca/zlecenia/zrealizowane/
mv rachunki.txt wykonano.txt
```
6\. Utwórz plik wykonano.txt wielkości 11 bajtów, następnie podziel go pliki wielkości 5 bajtów. W ten sposób otrzymasz 3 pliki. (split)
```sh
split --bytes=5 wykonano.txt
```
7\. Będąc w katalogu logo skopiuj powyżej otrzymane 3 pliki do katalogu dokumenty.
```sh
cp ../../praca/zlecenia/zrealizowane/x* ../../praca/dokumenty
```
8\. Będąc w katalogu dokumenty połącz skopiowane 3 pliki w plik odtworzono.txt, tak aby otrzymać plik o zawartości identycznej z wykonano.txt. Następnie plik odtworzono.txt skopiuj do katalogu wazne-sprawy.
```sh
cat x* >> odtworzono.txt
cp odtworzono.txt ../../dom/wazne-sprawy
```
9\. Będąc w katalogu wazne-sprawy sprawdź, czy są jakieś różnice w zawartości plików wykonano.txt i odtworzono.txt.
```sh
diff -s odtworzono.txt ../../praca/zlecenia/zrealizowane/wykonano.txty
```
