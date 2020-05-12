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
        
    ## Przykłady:
    #### *`$ cp plik0 /home/user/desktop/plik0_kopia`*
    #### *//wynik: kopiuje plik0 z biezacego katalogu do miejsca docelowego jako plik0_kopia*
    #### *`$ cp -i plik0.txt plik0_kopia.txt `*
    #### *//wynik: kopiuje plik0 jako plik0_kopia i pyta o potwierdzenie*
    #### *`$ cp -u plik0.txt plik0_kopiaZapasowa.txt `*
    #### *//wynik: kopiuje tylko jeśli plik0 jest nowszy od plik0_kopiaZapasowa*
    #### *`$ cp -p plik.txt plik_kopia.txt`*
    #### *//wynik: kopiuje zachowując tryb pliku, właściciela i znaczniki czasu.*
    #### *`$ cp -v plik.txt plik_kopia.txt`*
    #### *//wynik: po skopiowaniu wypisuje bieżące działania.*
    #### *`$ cp -R Obrazy Obrazy_kopia`*
    #### *//wynik: kopiuje katalogi wraz z jego zawartością*
    #### *`$ cp -RT Obrazy Obrazy_kopia`*
    #### *//wynik: kopiuje folder rekurencyjnie, jeśli Obrazy_kopia istnieje, kopiuje do niego zawartość Obrazy*
    #### *`$ cp plik.txt /home/folder2 plik0.txt /home/folder1`*
    #### *//wynik: kopiuje dwa pliki jednoczesnie do wskazanych miejsc*
---
* ## _**rm**_ - usuwanie plików
        $ polecenie <opcje>


        -v | --verbose //wynik   
    ### Przykłady:
    #### *`$ polecnie `*
    ##### *//wynik: wynik*
---
* ## _**mv**_ - przenoszenie lub zmiana nazwy
        $ polecenie <opcje>


        -v | --verbose //wynik   
    ### Przykłady:
    #### *`$ polecnie `*
    ##### *//wynik: wynik*
---
* ## _**find**_ - szukanie
        $ polecenie <opcje>


        -v | --verbose //wynik   
    ### Przykłady:
    #### *`$ polecnie `*
    ##### *//wynik: wynik*
---
* ## _**diff**_ - opis
        $ polecenie <opcje>


        -v | --verbose //wynik   
    ### Przykłady:
    #### *`$ polecnie `*
    ##### *//wynik: wynik*
---
* ## _**cmp**_ - opis
        $ polecenie <opcje>


        -v | --verbose //wynik   
    ### Przykłady:
    #### *`$ polecnie `*
    ##### *//wynik: wynik*
---
* ## _**comm**_ - opis
        $ polecenie <opcje>


        -v | --verbose //wynik   
    ### Przykłady:
    #### *`$ polecnie `*
    ##### *//wynik: wynik*
---