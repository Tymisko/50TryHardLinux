# Edycja plików tekstowych

* ## ***Nano*** - edytor tekstu oparty na terminalu
        $ nano <plik>

        ^	        //symbolizuje klawisz „ctrl” w menu.
        M	        //symbolizuje klawisz „alt” w menu.

        ^ + W	    //szukanie łańcucha znaków
 
    ### **Przykłady**:
    #### `Ctrl + W` - szukanie wzorca
        Jednoczesne kliknięcie obu klawiszy, powoduje rozpoczęcie wprowadzania szukanego wzorca.
        
        Kliknięcie klawisza Enter, wskaze pierwszy wynik, aby zobaczyć następny należy kliknąć [ALT+W]

    #### `$ Ctrl + \` - szukanie wzorca i zmienianie go
        Szukanie wprowadzonego wzorca i zamienianie go.

        Należy wpisac szukany wzorzec, kliknięcie klawisza enter spowoduje przejście do pierwszego znalezionego wzorca.
        
        Kliknięcie klawisza Y spowoduje rozpoczęcie zamiany tego słowa.Kliknięcie klaiwsza N spowoduje pomija ten wynik.
        
        Wciśnięcie klawisza A powoduje zamianę wszystkich znalezionych wzorców.*

    #### `Alt + a ` - zaznaczanie tekstu
        Rozpoczyna zaznaczanie tekstu, przenieś kursor na koniec tekstu który chcesz zaznaczyć. 
        
        Aby anulować zaznaczenie kliknij Ctrl + 6

    #### `Alt + 6` - kopiowanie
        Kopiuje zaznaczony tekst
    #### `Ctrl + k` - wycinanie
        wycina zaznaczony tekst
    #### `Ctrl + u` - wklejanie 
        wkleja tekst ze schowka
    #### `Ctrl + o` - zapisywanie
        zapisuje zmiany w pliku, jeśli nie istnieje - tworzy go
---
* ## ***Gedit*** - łatwy w użyciu edytor tekstu w wersji GUI 
        $ gedit <nazwaPliku>
---
* ## ***Vim*** - rozbudowany Vi, edytor tekstu dla programisty 
        $ vim <opcje> <plik | lista plików>

        -y                          //uruchamia VIM w łatwym trybie
        -g                          //Vim zostanie uruchomiony GUI jeśli Vim został skompilowany ze sparciem dla GUI

        -m | -R                     //blokuje nadpisywanie pliku

        -s {skrypt}                 //zostanie uruchomiony plik {skrypt}, znaki zostaną zinterpretowane jakby były wpisywane.

        -t {znacznik}               //początkowa pozycja kursora znajduje się przy „znacznik”
        +n                          //umieszcza na starcie kursor w n wierszu

        -e                          //zaczyna w trybie Ex, aby wrócić do trybu normalnego należy wprowadzić polecenie :vi
        -E                          //uruchamia Vima w ulepszym trybie Exview

        -c {polecenie}              //zostanie wykonane po wczytaniu się pierwszego pliku
        --cmd {polecenie}           //zostanie wykonane tuż przed interpretacja jakiegokolwiek pliku vimrc

        -b                          //tryb binarny, ustawia się opcje które umożliwiają edycję plików binarnych lub wykonywalnych
        -D                          //Debugowanie, tryb debugowania wykonuje pierwsze polecenie ze skryptu
        -r {plik}                   //Tryb odzyskiwanie danych. Plik wymiany zostanie wykorzystany do odzyskania gwałtownie przerwanej sesji
        -w {plik}                   //Wszystkie wciśnięcia klawiszy, aż do zakończenia działania programu są zapisywane w {plik}
        -x                          //Używa szyfrowania podczas zapisywania plików. Zostaniesz poproszony o podanie klucza.
---
* ## ***Pico*** - prosty edytor tekstu 
        $ pico <opcje> <plik>

        -v		    //tylko przegląda plik, wyłączenie edycji
        -z		    //włącza możliwość zawieszania pracy przez Ctrl+Z (^+Z)
        -o katalog 	//Ustawia katalog pracy. Dostępnie wyłącznie pliki z podanego katalogu.
        +n		    //umieszcza na starcie kursor w n wierszu
        -b		    //wlacza opcje zastepowania tekstu dopasowaniami znalezionymi przy pomocy polecenia „Where is”
---
* ## ***Vi*** - edytor tekstu
        $ vi <nazwaPliku>

		:w                  //zapisz i nie wychodź
		:w nowa_nazwa       //zapisz plik pod inną nazwą
		:wq                 //Zapisz i wyjdź
		:q!                 //Wyjdź bez zapisywania
---
* ## ***Emacs*** - edytor tekstu w wersji GUI.
>wymaga zainstalowania

        $ emacs <nazwaPliku>
---
