# Historia poleceń
* ## _**history**_ - manipulowanie listą historii poleceń
        $ history <opcje>

        -n                  //wyświetla n ostatnich polecen wprowadzonych do terminala
        -d <numer_linii>    //usuwa wpis z historii pod numerem wpisu numer_linii


        !n                  //wykonuje polecenie znajdujące się pod n numerem linii
    ### Przykłady:
    #### *`$ history 10 `*
    ##### *//wynik: Wyswietla 10 ostatnich polecen wprowadzonych do terminala*
    #### *`$ history -d 40 `*
    ##### *//wynik: usuwa wpis w historii pod numerem wpisu 40*
    #### *`$ !8 `*
    ##### *//wynik: wykonuje polecenie z historii pod numerem wpisu 8*
---
* ## _**fc**_
        $ fc {x..y}

    ##### *//wynik: wyświetla zakres wpisów w historii od x do y*
---
* ## _**bash_history**_ - plik przechowujący historię poleceń
    >Tylko wtedy kiedy powłoką jest bash

    >historia jest przechowywana do poprzedniej sesji

        $ cd $HOME && more .bash_history

    ##### *//wynik: Przechodzi do katalogu domowego a następnie wyświetla zawartość pliku .bash_history.*
---