# Zmiana praw dostępu

* ## ***chmod*** - zmienia prawa dostępu do pliku lub katalogu
        $ chmod <opcje> <plik | katalog>

        -R                      //rekurencyjna zmiana uprawnień
        --reference=ZRODLO CEL  //pobiera ustawienia uprawnien z ZRODLO i nadaje je CEL

        Rodzaje klas:
        u - user - właściciel pliku
        g - group - uzytkownicy grupy
        o - other - wszyscy inni uzytkownicy
        a - all - u,g,o = wszyscy uzytkownicy, 
    
|NAZWA UPRAWNIENIA|OPIS                                                                 |I OZNACZENIE| II OZNACZENIE|
|----------------|---------------------------------------------------------------------|--------|----------|
| read           |możesz tylko przeglądać plik, lub pliki w folderze                   | r      | 4        |
| write          |możesz edytować i modyfikować plik, dodawać i usuwać pliki w folderze| w      | 2        |
| execute        |możesz uruchamiać plik                                               | x      | 1        |
  

   ### **Przykłady**:
   #### `$ chmod g=r file`
   ##### //wynik: *Nadaje uprawnienia do czytania pliku członkom grupy*

   #### `$ chmod a-x file`
   ##### //wynik: *Usuwa uprawnienia do wykonywania pliku dla wszystkich uzytkowników*

   #### `$ chmod -R o-w obrazy`
   ##### //wynik: *Usuwa uprawnienia do edycji wszystkim innym uzytkownikom niz user i group folderu obrazy*

   #### `$ chmod u=rwx,g=r,o= file`
   ##### //wynik: *Nadpisuje uprawnienia dla wlasciciela pliku, grupy i usuwa uprawnienia dla pozostałych uzytkowników*

   #### `$ chmod 644 katalog `
   ##### //wynik: *Nadaje uprawnienia read i write dla user, oraz read dla group i other*

   #### `$ chmod 750 katalog `
   ##### //wynik: *nadaje wszystkie uprawnienia wlascicielowi pliku, uprawnienia do czytania i wykonywania dla czlonków grupy oraz brak uprawnień dla pozostałych*

   #### `$ chmod -R 700 folder`
   ##### //wynik: *nadaje pełne uprawnienia do katalogu folder i jego zawartości tylko właścicielowi pliku*

   #### `$ chmod --reference=file1 file2 `
   ##### //wynik: *kopiuje ustawienia uprawnien z file1 do file2*
---
* ## ***chown*** - zmienia właściciela i grupę pliku lub katalogu
        $ chown <opcja> <właściciel> : <grupa> <plik | katalog>

        -R                      //zmienia właściciela | grupę zasobu rekurencyjnie
        -h                      //pozwala zmienić właściciela symbolicznego wiązania.
        --reference=ZRODLO CEL  //pobiera ustawienia uprawnien z ZRODLO i nadaje je CEL

   
    ### **Przykłady**:

    #### `$ chown user file`
    ##### //wynik: *Zmienia właściciela pliku file na user*

    #### `$ chown user file1 folder1 folder2`
    ##### //wynik: *Zmienia wlasciciela kilku zasobów na user*

    #### `$ chown 1000 file`
    ##### //wynik: *zmienia własciciela pliku file na uzytkownika o UID (user id) 1000*

    #### `$ chown jan:users file`
    ##### //wynik: *zmienia wlasciciela i grupe pliku file*

    #### `$ chown :users folder`
    ##### //wynik: *Zmienia tylko grupę katalogu folder*

    #### `$ chown -h user: wiazanie_symboliczne `
    ##### //wynik: *zmienia właściciela wiązania symbolicznego na user*

    #### `$ chown --reference=file1 file2 `
    ##### //wynik: *nadaje ustawienia plikowi file2 takie same jakie ma file1*

    #### `$ polecenie `
    ##### //wynik: *wynik*
---
* ## ***chgrp*** - zmienia grupę właścicieli plików lub katalogów
        $ chgrp <opcja> <plik>

        -R                      //zmienia właściciela | grupę zasobu rekurencyjnie

        -h                      //pozwala zmienić właściciela symbolicznego wiązania.
        -H                      //podąża za ewentualnie istniejącymi wiązaniami symbolicznymi

        -v | --verbose          //wyświetla informacje o przetworzonych danych  
        -c                      //informuje o dokonanych zmianach
    ### **Przykłady**:

    #### `$ chgrp nazwaGrupy file1 folder1 `
    ##### //wynik: *zmienia grupę file1 i folder1 na nazwaGrupy*

    #### `$ chgrp +1000 file1 `
    ##### //wynik: *zmienia grupę pliku file1 na GID(group id) 1000*

    #### `$ chgrp -h nGRUPA wiazanie_symboliczne `
    ##### //wynik: *zmienia grupę wiązania symbolicznego*

    #### `$ chgrp -R nGRUPA obrazy`
    ##### //wynik: *zmienia grupę katalogu obrazy i całej jego zawartości na nGRUPA*
---