# Grupowanie poleceń
* ## **`;` - separacja poleceń średnikami**
        $ polecenie1 ; polecenie2 ; polecenie3
   
    ### Przykłady:
    #### *`$ ls ; pwd ; date `*
    ##### *//Wynik: Wykonuje kolejno polecenie `ls, pwd, date`. Jeśli zostały wykonane poprawnie wyświetlane są ich wyniki na ekranie w kolejności w jakiej zostały podane komendy.*
---
* ## **`&&` - operator logiczny AND**
    > Wykonanie nastepnego polecenia, jeśli poprzednie zostało wykonane **bezbłędnie**

        $ polecenie1 && polecenie2   
    ### Przykłady:
    #### *`$ mkdir folder && cd folder `*
    ##### *//Wynik: Tworzy katalog "folder", jeśli został pomyślnie utworzony, przechodzimy do katalogu podrzędnego "folder".*
---
* ## _**`||` - operator logiczny OR**_
    >//Wykonanie następnego polecenia, jeśli poprzednie zostało wykonane z **błędem**.

        $ polecenie-1 || polecenie
    ### Przykłady:
    #### *`$ cd folder || mkdir folder`*
    ##### *//Wynik: Przechodzimy do katalogu „folder”, jeśli nie istnieje, tworzymy go.*
---
* ## _**`|` - potok poleceń (ang. Pipe)**_
    >Wykonanie następnego polecenia uwzględniając wynik poprzedniego

        $ polecenie-1 | polecenie-2
  
    ### Przykłady:
    #### *`$ ls -l | grep -i ”wzorzec”`*
    ##### //wynik: Wyświetla wynik będący sumą poleceń. W tym przypadku informacje o plikach w bieżącym katalogu zawierające "wzorzec".
---