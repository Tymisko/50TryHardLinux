# Wyświetlanie zawartości katalogów i woluminów (pełna informacja o plikach w polecenaich ls.)

* ## ***ls*** - wypisuje zawartość katalogu
        $ ls <opcje> <plik | katalog>

        -a		//wyświetla wszystkie pliki, nawet ukryte
        -d		//wyświetla tylko katalogi
        -s		//wyświetla rozmiar plików

        -l 		//tryb dużego formatu, wyświetla prawa do plików,   skrót do tego to komenda ll.

        -S 		//sortuje według rozmiaru
        -t 		//sortuje według czasu i daty modyfikacji
        -r 	    //odwraca stosowany sposób sortowania

        -R 		//wyświetla również podkatalogi

|zona| 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
|---|---|---|---|---|---|---|---|---|
|znaczenie|TYP PLIKU|PRAWA|LICZBA HARD LINK|WŁAŚCICIEL|GRUPA|OBJĘTOŚĆ|DATA I GODZINA OSTATNIEJ MODYFIKACJI PLIKU|NAZWA PLIKU|
|przyklad|-|rwxr-x---|1|user|nauka|265|01.05.2017 14:45|file|

|TYPY PLIKÓW||
|---|---|
|-|pliki zwykłe|
|d|katalogi|
|c|pliki specjalne|
|b|pliki specjalne przypisane|
|l|łącza symboliczne|
  
   ### **Przykłady**:
   #### `$ ls`
   ##### //wynik: *lista plików w obecnym katalogu*
   #### `$ ll ` lub `$ ls -l `
   ##### //wynik: *wyświetla w formacie długim formacie listownia*
   #### `$ ls -la`
   ##### //wynik: *Wyswietla wszystkie pliki w długim formacie*
   #### `$ ls -ltr`
   ##### //wynik: *Wyswietla posortowane w odwrotnej kolejnosci pliki*
   #### `$ ls -R`
   ##### //wynik: *Uwzględnia podkatalogi.*
---
* ## ***df*** - informacje o użyciu przestrzeni dyskowej systemu plików
        $ polecenie <opcje> <plik>

        -i                          //wyświetla informacje o użyciu miejsca przez węzły systemu plików
        --total                     //wyświetla dodatkowy wiersz z podsumowaniem wszystkich systemów plików.

        -T                          //wyświetla informacje o systemie plików
        -x                          //ignoruje podany system plików

        -h | --human-readable       //wyświetla w czytelniejszym formacie dodając literowe przyrostki określające potęgi 1024
        -H | --si                   //podobnie jak -h, jednak posługuje się potęgami 1000 zamiast 1024

   ### **Przykłady**:
   #### `$ df / `
   ##### //wynik: *informacje o systemie plików, ilości 1KB bloków, uzywanego i wolnego miejsca. Uzycie zasobów dysku w %. Miejsce zamontowania.*

   #### `$ df -h`
   ##### //wynik: *Wyswietla w czytelniejszym formacie*

   #### `$ df -T ext4`
   ##### //wynik: *wyświetla informacje o podanym systemie plików*

   #### `$ df -x ext4 `
   ##### //wynik: *Wyswietla systemy plików po za ext4*

   #### `$ df -ih / `
   ##### //wynik: *wyświetla informacje o uzyciu inodes(węzłów) systemu Linux*

   #### `$ df -hT ext4 --output=source,size,pcent`
   ##### //wynik: *Wyswietla systemy plików typu ext4, rozmiar i zuzycie w %*



   
    
---
