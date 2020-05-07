# Uzyskiwanie informacji o użytkownikach

* ## _**whoami**_ - nazwa uzytkownika wprowadzajacego to polecenie 
		$ whoami
	##### *//wynik: wyświetla nazwę użytkownika, na którym jesteśmy zalogowani*
---
* ## _**id**_ - wyświetlanie identyfikatora użytkownika
		$ id <nazwa_uzytkownika>
	##### *//wynik: wyświetla id użytkownika, jego grupy rzeczywiste i aktywne wraz z id*
---
* ## _**users**_ - lista obecnie zalogowanych użytkowników
		$ users
	##### *//wynik: lista użytkowników połączonych z systemem*
---
* ## _**groups**_ - wyświetlanie grup użytkownika 
		$ groups <nazwa_uzytkownika>
	##### *//wynik: lista grup do których należy użytkownik*
---
* ## _**who**_ - kto jest zalogowany?
 		$ who -u
	##### *//wynik: lista zalogowanych użytkowników, terminale użytkowników*
---
* ## _**w**_ - kto jest zalogowany i co robi?
		$ w
	##### *//wynik: lista zalogowanych użytkowników oraz czynność którą wykonują w momencie wpisania komendy*
---
* ## _**lslogins**_ - wyświetla informacje o znanych użytkownikach w systemie
		$ lslogins -u <nazwa_uzytkownika>
	#### *//wynik: szczegółowe informacje o użytkowniku*
---
* ## _**finger**_ - sprawdzanie informacji o użytkowniku
		$ finger <nazwa_uzytkownika>
	#####   *//wynik: imię i nazwisko, scieżka katalogu domowego, powłoka, login itd.* imię i nazwisko, scieżka katalogu domowego, powłoka, login itd.*
---
* ## _**lastlog**_ - ostatnie logowanie
		$ lastlog -u <nazwa_uzytkownika>


		-u 	//Wyświetla ostatni rejestr określonego użytkownika
		-a 	//wyświetla wszystkie rekordy

	### Przykład:
	#### *`$ lastlog -u user`*
	##### *//wynik: informacje o ostatnim logowaniu uzytkownika*
---
* ## _**last**_ - lista ostatnio zalogowanych użytkowników
		$ last
	##### *//wynik: informacje o czasie połączenia użytkowników*
---
* ## _**getent**_ - wpisy z biblioteki passwd
		$ getent passwd <nazwa_uzytkownika>
	##### *//wynik: informacje o uzytkowniku z bazy danych passwd*
---
* ## _**grep**_ - lista wierszy zawierająca nazwę użytkownika
		$ grep -i <nazwa_uzytkownika> /etc/passwd
	##### *//wynik: linie zawierające <nazwa_uzytkownika> w pliku passwd*
---


	


	






