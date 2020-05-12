# Wyświetlanie komunikatów na ekranie
* ## _**echo/printf**_ - wyświetlanie wiersza tekstu
        $ echo <opcje> <"lancuch znakow">

        -e //włącza interpretacje specjalnych sekwencji
	        \a //dzwonek/alarm
	        \b //backspace
	        \n //znak nowej linii
	        \\ //odwrotny ukośnik
	        \t //tabulator poziomy
	        \v //tabulator pionowy
	        \nnn //znak ASCII o kodzie nnn (OCT)

        -E //wyłącza interpretacje specjalnych sekwencji
        -n //nie wypisuje znaku nowej linii
    ## _printf vs echo_
    >„At a very high level printf is like echo but more formatting can be done.”

    ### Przykłady:
    #### *`$ echo -n "Witaj!"`*
    ##### *//wynik: "Witaj!"*
    #### *`$ printf -n "Witaj!"`*
    ##### *//wynik: "Witaj!"*

---
* ## _**mesg**_ - kontrolowanie dostęp zapisu do terminala
        $ mesg <opcje>

        y //zezwalaj na komunikację 
        n //blokuj komunikację
    ### Przykłady:
    #### *`$ mesg `*
    ##### *//wynik: Wyświetla informację czy komunikacja z innymi użytkownikami jest włączona.*
    #### *`$ mesg y`*
    ##### *//wynik: Zezwala na komunikację z innymi uzytkownikami*
---
* ## _**wall**_ - wysyłanie wiadomości do użytkowników
        $ polecenie <opcje> <"lancuch_znakow" | plik>

        -n                          // tłumi banner
	    -t <x>                      // po x sekundach porzuć próbę zapisu na terminalach.
	    -g <nazwa_grupy | id_grupy>   // Ustawia grupę jako odbiorców wiadomości 

    ### Przykłady:
    #### *`$ wall "Hello World!" `*
    ##### *//wynik: Wyświetla "Hello World" na ekranie wszystkich użytkowników*
---
* ## _**write**_ - wysyłanie komunikatu do innego użytkownika
        $ write <nazwa_uzytkownika> <"lancuch znakow">
    ### Przykłady:
    #### *`$ write user0 "What's up?" `*
    ##### *//wynik: Drukuje "What's up?" w terminalu odbiorcy, jeśli ma włączoną komunikację*
---