# Tworznie katalogów i plików
* ## ***mkdir*** - tworzenie katalogu
        $ mkdir <opcja> <nazwaKatalogu>

        -m | --mode	    //ustawia tryb uprawnień (tak jak w chmod), zamiast domyślnego a=rwx
        -p | --parents	//nie zwraca błędu, jeśli katalog istnieje, tworzy brakujące katalogi nadrzędne
        -v | --verbose	//wyświetla komunikat o każdym utworzonym katalogu
 
    ### **Przykłady**:

    #### `$ mkdir folder1 folder2 folder3 `
    ##### //wynik: *Tworzy kolejno trzy katalogi*

    #### `$ mkdir -m a=rx folder`
    ##### //wynik: *tworzy katalog „folder” i nadpisuje jego tryb uprawnień dla wszystkich, zezwalając na read i execute.*

    #### `$ mkdir -m 777 folder`
    ##### //wynik: *worzy katalog „folder” i zmienia jego uprawnienia dając wszystkim pełną kontrolę*

    #### `$ mkdir -p /home/folder0/folder1`
    ##### //wynik: *tworzy katalog „folder1”, jeśli któryś z katalogów nadrzędnych (/home/folder0) nie istnieje, tworzy go.*

    #### `$ mkdir -p Muzyka/{Rock,Pop,Rap/{Amerykanski,Polski}`
    ##### //wynik: *tworzy katalog Muzyka, wewnątrz niego Katalogi Rock, Pop oraz katalog Rock z katalogami podrzędnymi Amerykanski, Polski.*

    #### `$ mkdir -p Music/{Jazz/Blues,Folk,Disco,Rock/{Gothic,Punk,Progressive},Classical/Baroque/Early}`
    ##### //wynik: *Poniższe drzewo katalogów:*
    ![](../images/mkdir.png)
---
* ## ***touch*** - Zmiana czasu dostępu i modyfikacji pliku na obecny 
        $ touch <opcja> <plik>
    >jeśli plik nie istnieje, tworzy go, chyba, że użyto opcji -c lub -h. 

        -a | --time=atime | --time=access | --time=use  //zmienia tylko czas dostępu
        -m | --time=modify | --time=mtime               //zmienia tylko czas modyfikacji
        -c | --no-create                                //nie tworzy żadnych plików
        -h | --no-dereference                           //działa na dowiązaniach symbolicznych, zamiast na plikach, które one wskazują. Nie tworzy pliku.
        -d | --date=STRING                              //przetwarza STRING i używa go zamiast czasu bieżącego
        -t TIME                                         //używa formatu [[CC]RR]MMDDhhmm[.ss] zamiast czasu bieżącego
        -r | --reference=FILE                           //używa czasów danego FILE, zamiast czasu bieżącego
  

    ### **Przykłady**:
    #### `$ touch -c file`
    ##### //wynik: *jeśli plik „file” istnieje, ustaw jego czas  dostępu i modyfikacji na obecny czas systemowy, jeśli nie istnieje, nie rób nic.*

    #### `$ touch -a file`
    ##### //wynik: *zmienia czas dostępu pliku „file”, jeśli nie istnieje ,tworzy go.*

    #### `$ touch -h file`
    ##### //wynik: *zmienia tylko czas pliku dowiązanego symbolicznie, jeśli nie istnieje, nie robi nic.*

    #### `$ touch -rc file0 file1`
    ##### //wynik: *jeśli file0 istnieje, ustawia jego czas dostępu i modyfikacji na czas pliku file1, jeśli nie istnieje, nie robi nic.*

    #### `$ touch -hc file0 file1`
    ##### //wynik: *jeśli file0 istnieje i file1 jest dowiązaniem symbolicznym, ustawia czas modyfikacji i dostępu file0 na czas symbolicznie dowiązanego file1. Nie narusza pliku referencyjnego.*

    #### `$ touch -t „10310000” file`
    ##### //wynik: *Ustawia czas dostępu i modyfikacji na północ, 31 października.*

    #### `$ touch -d „October 31” file`
    ##### //wynik: *ustawia czas dostępu i modyfikacji na północ, 31 października*

    #### `$ touch -md „Sep 1 1927 23:58:59” file`
    ##### //wynik: *zmienia czas modyfikacji pliku file na 1 września 1927 roku, godzina 23:58:59.*

    >Aby sprawdzić czas dostępu lub modyfikacji należy użyć polecenia stat <nazwaPliku>
---
* ## ***>*** - zapisywanie wyniku polecenia do pliku standardowym strumieniem wyjścia.
        >       //nadpisuje
        >>      //dopisuje

    ### **Przykłady**:

    #### `$ polecenie > <nazwaPliku>`
    ##### //*Jeśli plik istnieje, nadpisuje jego dane wynikiem polecenia, jeśli nie istnieje, tworzy go.*

    #### `$ polecenie >> <nazwaPliku>`
    ##### //*Jeśli plik istnieje, dopisuje do jego danych wynik polecenia, jeśli nie istnieje, tworzy go.*

    #### `$ cat plik0 > plik1`
    ##### //*Kopiuje zawartość i nadpisuje plik1 zawartością plik0, jeśli nie istnieje, tworzy go.*
---

