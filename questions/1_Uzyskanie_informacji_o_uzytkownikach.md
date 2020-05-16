# Uzyskiwanie informacji o użytkownikach

## `whoami` - nazwa uzytkownika wprowadzajacego to polecenie 
*wynik: wyświetla nazwę użytkownika, na którym jesteśmy zalogowani*

---

## `id` - wyświetlanie identyfikatora użytkownika
	$ id <nazwa_uzytkownika>
*wynik: wyświetla id użytkownika, jego grupy rzeczywiste i aktywne wraz z id*

---

## `users` - lista obecnie zalogowanych użytkowników
	$ users
*wynik: lista użytkowników połączonych z systemem*

---

## `groups` - wyświetlanie grup użytkownika 
	$ groups <nazwa_uzytkownika>
*wynik: lista grup do których należy użytkownik*

---

## `who` - kto jest zalogowany?
	$ who -u
*wynik: lista zalogowanych użytkowników, terminale użytkowników*

---

## `w` - kto jest zalogowany i co robi?
	$ w
*wynik: lista zalogowanych użytkowników oraz czynność którą wykonują w momencie wpisania komendy*

---

## `lslogins` - wyświetla informacje o znanych użytkownikach w systemie
	$ lslogins -u <nazwa_uzytkownika>
*wynik: szczegółowe informacje o użytkowniku*

---

## `finger` - sprawdzanie informacji o użytkowniku
	$ finger <nazwa_uzytkownika>
*wynik: imię i nazwisko, scieżka katalogu domowego, powłoka, login itd.*

---

## `lastlog` - ostatnie logowanie
		$ lastlog -u <nazwa_uzytkownika>

		-u 	// Wyświetla ostatni rejest określonego użytkownika
		-a 	// Wyświetla wszystkie rekordy

**Przykład:**

	$ lastlog -u user
*wynik: informacje o ostatnim logowaniu uzytkownika*

---

## `last` - lista ostatnio zalogowanych użytkowników
	$ last
*wynik: informacje o czasie połączenia użytkowników*

---

## `getent` - wpisy z biblioteki passwd
	$ getent passwd <nazwa_uzytkownika>
*wynik: informacje o uzytkowniku z bazy danych passwd*

---

## `grep` - lista wierszy zawierająca nazwę użytkownika
	$ grep -i <nazwa_uzytkownika> /etc/passwd
*wynik: linie zawierające <nazwa_uzytkownika> w pliku passwd*

---


	


	






