# Polecenia do zarządzania plikami
* ## _**cp**_ - kopiowanie plików i katalogów
        $ cp <opcje> <zrodlo> <cel>

        *zrodlo, cel - katalog lub plik

        -i | --interactive          // pyta przed nadpisywaniem
        -u | --update               // kopiuje tylko jeśli ZRODLO jest nowsze niż CEL
        -v | --verbose              // wypisuje bieżące działania
        -f | --force                // usuwa istniejące pliki docelowe (nadpisuje je)
        -p                          // zachowuje właściciela pliku, tryb pliku, znaczniki czasu.
        -R | --recurisve            // kopiuje katalogi rekurencyjnie(z podkatalogami i plikami wewnątrz)
        -T | --no-target-directory  // traktuje cel jako zwykły plik

        -s | --symbolic-link        //wiązanie symboliczne
        -l | --link                 //wiązanie twarde

        Kopiowanie kilku plików na raz jest możliwe tylko gdy kopiujemy je do katalogu, a nie jako nowy plik.    
        
Przykłady:

`$ cp plik0 /home/user/desktop/plik0_kopia`

*//wynik: kopiuje plik0 z biezacego katalogu do miejsca docelowego jako plik0_kopia*

`$ cp -i plik0.txt plik0_kopia.txt `

*//wynik: kopiuje plik0 jako plik0_kopia i pyta o potwierdzenie*

`$ cp -u plik0.txt plik0_kopiaZapasowa.txt`

*//wynik: kopiuje tylko jeśli plik0 jest nowszy od plik0_kopiaZapasowa*

`$ cp -p plik.txt plik_kopia.txt`

*//wynik: kopiuje zachowując tryb pliku, właściciela i znaczniki czasu.*

`$ cp -v plik.txt plik_kopia.txt`

*//wynik: po skopiowaniu wypisuje bieżące działania.*

`$ cp -R Obrazy Obrazy_kopia`

*//wynik: kopiuje katalogi wraz z jego zawartością*

`$ cp -RT Obrazy Obrazy_kopia`

*//wynik: kopiuje folder rekurencyjnie, jeśli Obrazy_kopia istnieje, kopiuje do niego zawartość Obrazy*

`$ cp plik.txt /home/folder2 plik0.txt /home/folder1`

*//wynik: kopiuje dwa pliki jednoczesnie do wskazanych miejsc*

---
* ## _**rm**_ - usuwanie plików lub katalogów
        $ rm <opcje> <nazwa_pliku | nazwa_katalogu>

        -d      // usuwa katalogi, nie wymaga by były puste.
        -f      // ignoruje nieistniejące pliki, nie pyta użytkownika o zgodę na usunięcie pliku.
        -i      // dla każdego pliku wymaga potwierdzenai usunięcia.
        -r      // usuwanie rekurencyjne, usuwa także katalogi z całą zawartością
        -v      // wypisuje nazwę pliku przed usunięciem

    ### Przykłady:
    #### *`$ rm -d obrazy `*
    ##### //wynik: *Usuwa katalog obrazy*
    #### *`$ rm -f system32.txt `*
    ##### //wynik: *Usuwa plik system32.txt bez ostrzezenia.*
    #### *`$ rm -i *`*
    ##### //wynik: *Prosi o potwierdzenie usuniecia wszystkich plików z obecnego katalogu*
    #### *`$ rm -dr Gothic `*
    ##### //wynik: *Usuwa katalog Gothic z cała jego zawartością*
    #### *`$ rm -fv *`*
    ##### //wynik: *Usuwa zawartość bieżącego katalogu wyświetlajac które pliki zostały usunięte, nie pyta uzytkownika o zgode na usuniecie.*
---
* ## _**mv**_ - przenosi pliki lub zmienia ich nazwę
        $ mv <opcje> <plikZrodlowy | katalogZrodlowy> <plikDocelowy | katalogDocelowy>
        -b | --backup                               //tworzy kopie zapasowe plików, które mają zostać nadpisane
        -S przyrostek_kopii | --suffix=przyr_kopii  //dodaje przyrostek_kopii do nazwy pliku kopii zapasowej.
        -f | --force                                //usuwa istniejące pliki, nie wymaga potwierdzenia
        -n                                          //zabezpiecza przed nadpisaniem pliku
        -i | --interactive                          //wymaga potwierdzenia przy nadpisywaniu plików
   
    ### Przykłady:
    #### *`$ mv plik1 /tmp`*
    ##### //wynik: *przenosi plik1 z biezącego katalogu do katalogu /tmp*
    #### *`$ mv file1 file2`*
    ##### //wynik: *zmienia nazwę pliku file1 na file2*
    #### *`$ mv dir1 dir2 `*
    ##### //wynik: *jeśli katalog dir2 istnieje, dir1 zostanie do niego przeniesiony. Jesli nie istnieje, zmienia nazwę dir1 na dir2.*
    #### *`$ mv file1 file2 dir1 `*
    ##### //wynik: *przenosic pliki file1, file2 do katalogu dir1*
    #### *`$ mv *.pdf ~/Documents`*
    ##### //wynik: *przenosi wszystkie pliki PDF do folderu ~/Documents*
    #### *`$ mv -i file1 dir1 `*
    ##### //wynik: *jesli taki plik już istnieje w tym katalogu, pyta czy nadpisac plik.*
    #### *`$ mv -n file1 dir1 `*
    ##### //wynik: *jesli taki plik juz istnieje, nie robi nic.*
    #### *`$ mv -f file1 dir1 `*
    ##### //wynik: *jesli przenoszony plik znajduje sie w miejscu docelowym, nadpisuje go bez zapytania o potwierdzneie.*
    #### *`$ mv -b -S kopia_ file1 ~/Documents`*
    ##### //wynik: *tworzy kopie zapasową pliku file1 z sufixem kopia_*

---
* ## _**find**_ - szukanie plików w hierarchii katalogowej
        $ find <opcje> <sciezka> <nazwaPliku>

        -L // podąża za wiązaniami symbolicznymi
        -name <szukany_wzorzec> // szuka podanego wzorca
        -iname <szukany_wzorzec> // szuka podanego wzorca, nie zwracajac uwagi na wielkość liter.
        -type //pliki, których typ jest określony jako:
		    d // katalog
		    f // plik normalny
		    b // plik blokowy
		    c // plik znakowy
            s // gniazdo
		    l // dowiązania symboliczne
        -path ‘wzorzec’         //pliki, których ścieżka dostępu pasuje do wzorca.
        -links                  //pliki, z liczbą N dowiązań do plików
        -size                   //pliki, które mają wielkość N oktetów(1 oktet= 8 bit)
            b // 512 bitów
            c // bajty
            w // dwu bajtowe słowa
            k // kilobajty
            M // megabajty
            G // gigabajty
        -user                   //pliki, które należą do użytkownika
        -perm nnn               //pliki, które mają prawa dostępu określone jako tryb
        -atime n                //pliki, które były otwierane w N dniach
        -mtime n               //pliki, które zostały zmodyfikowane w N dniach
        -print                  //wyświetla nazwę odnalezionego pliku oraz jego ścieżkę
        -exec polecenie{}\;     //uruchamia polecenie dla odnalezionego pliku, zamiast tego można stosować potok (pipe ‘|’)
        -ok. polecenie ()\;     //wymaga potwierdzenia przed uruchomieniem polecenia dla odnalezionego pliku.

    ### Przykłady:
    #### *`$ find /home -type f -iname "document.pdf" `*
    ##### //wynik: *Szuka plików o nazwie 'document.pdf' w katalogu /home. Ignoruje roznice w wielkosci liter.*
    #### *`$ find /home/user -type f -name *.pdf`*
    ##### //wynik: *Szuka plików pdf w wskazanym katalogu*
    #### *`$ find /home -type d -exec chmod 0777 {} \;`*
    ##### //wynik: *Zmienia uprawnienia wszystkich folderów w katalogu /home na 777*
    #### *`$ find . -type f -size 1024c `*
    ##### //wynik: *znajduje wszystkie pliki ważące 1024 B w bieżącym katalogu.*
    #### *`$ find . -type f -size +1M`*
    ##### //wynik: *szuka plików wiekszych niz 1 MB w bieżącym katalogu*
    #### *`$ find . -name "*.conf" ` -mtime 5*
    ##### //wynik: *Wyswietla pliki w bieżącym katalogu które były edytowane w ciągu ostatnich 5 dni*
    #### *`$ find . -perm 761`*
    ##### //wynik: *wyświetla wszystkie pliki z uprawnieniami 761*
    #### *`$ find / -user uzytkownik `*
    ##### //wynik: *wszystkie pliki uzytkownika uzytkownik*    
---
* ## _**diff**_ - porównywanie plików wiersz po wierszu
        $ diff <opcje> <plik1 | katalog1> <plik2 | katalog2>

        -c                              //wypisuje 3 wiersze kopiownego kontekstu
        -C n | --contexts n             //wypisuje n wierszy kopiowanego kontekstu
        -u                              //wypisuje 3 wiersze zunifikowanego kontekstu
        -U n | --unified n              //wypisuje n wierszy zunifikowanego kontekstu


        -i | --ignore-case              //ignoruje różnice wielkości znaków
        -b | --ignore-space-change   //ignoruje zmiany w ilości białych znaków
        -w | --ignore-all-space         //ignoruje wszystkie białe znaki
        -a | --text                     //traktuj wszystkie pliki jako tekst
        -q | --brief                    //informuje jedynie czy pliki się różnią.
        -s | --report-identical-files   //informuje gdy piki są identyczne
        -y | --side-by-side             //wyświetla dane wyjściowe w dwóch kolumnach.
        --suppress-common-lines         // nie wypisuje wspólnych wierszy
   
    ### Przykłady:
    #### *`$ diff file1 file2 `*
    ##### //wynik: *wyświetla różnice miedzy plikami*
    #### *`$ diff -c file1 file2 `*
    ##### //wynik: *wyświetla różnicę w formacie context*
    #### *`$ diff -C 1 file1 file2 `*
    ##### //wynik: *wyswietla liczbę lini 1 w formacie context*
    #### *`$ diff -u file1 file2`*
    ##### //wynik: *wyswietla wynik w formacie unified*
    #### *`$ diff -ui file1 file2`*
    ##### //wynik: *ignoruje wielkosc znaków przy porównywaniu*
    #### *`$ diff -s file1 file2`*
    ##### //wynik: *informuje, jesli pliki są identyczne.*
    #### *`$ diff -b file1 file2`*
    ##### //wynik: *ignoruje zmiane ilości spacji*
    #### *`$ diff -w file1 file2`*
    ##### //wynik: *ignoruje wszystkie białe znaki*
    #### *`$ diff -y file1 file2 `*
    ##### //wynik: *porównanie wyswietlone w dwóch kolumnach*
---
* ## _**cmp**_ - porównuje pliki bajt po bajcie

>sprawdza czy pliki różnią się


        $ cmp <opcje> <plik1> <plik2>


    -c                      //wypisuje różniące się znaki
    -l                      //dla każdej różnicy wypisuje numer bajtu (DEC) wartości różniących się bajtów (OCT)
    -s | --silent           //zwraca tylko kod zakończenia wskazujący czy pliki się różnią.

    
### Przykłady:
   #### *`$ cmp file1 file2`*
   ##### //wynik: *wyswietla informacje czy pliki sie roznia*
   #### *`$ cmp -c file1 file2`*
   ##### //wynik: *roznica znaków plików file1 file2*
---
* ## _**comm**_ - opis
        $ polecenie <opcje> <plik1> <plik2>

        -1                  //pomija wiersze unikalne dla pliku 1 (tylko unikalne dla 2, i wspólne)
        -2                  //pomija wiersze unikalne dla pliku 2 (tylko unikalne dla 1, i wspólne)
        -3                  //pomija linie które pojawiają się w obu plikach (tylko unikalne)
        --check-order       //sprawdza czy dane wejściowe są poprawnie posortowane
        --nocheck-order     //nie sprawdza czy dane wejściowe są poprawnie posortowane
  
    ### Przykłady:
    #### *`$ comm -1 -2 file1 file2 `*
    ##### //wynik: *wyswietla tylko wspolne linie obu plikow*
    #### *`$ comm -3 file1 file2`*
    ##### //wynik: *wyświetla tylko unikalne linie*
    #### *`$ comm --check-order file1 file2`*
    ##### //wynik: *sprawdza, czy dane wejściowe są poprawnie posortowane.*
---