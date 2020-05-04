# Uzyskiwanie informacji o użytkownikach

* finger
`$ finger <nazwa_uzytkownika>`
np. `$ finger user` 
//  wynik: imię i nazwisko, ścieżka katalogu domowego, powłoka, login, itd.

* who
`$ who -u `
//  wynik: lista zalogowanych użytkowników, terminale użytkowników.

* id
`$ id <nazwa_uzytkownika>`
np. `$ id user`
// wynik: wyświetla id użytkownika, jego grupy rzeczywiste i aktywne wraz z id.

* groups
`$ groups <nazwa_uzytkownika>`
np. `$ groups user`
// wynik: lista grup do których należy użytkownik

* getent
`$ getent passwd <nazwa_uzytkownika>`
np. `$ getent passwd user`
// wynik: Informacje o użytkowniku z bazy danych passwd.

* grep
`$ grep -i <nazwa_uzytkownika> /etc/passwd`
np. `$ grep -i user /etc/passwd`
// wynik: Linie zawierające nazwę użytkownika w pliku passwd.

* lslogins
`$ lslogins -u <nazwa_uzytkownika>`
np. `$ lslogins -u user`
// wynik: Szczegółowe informacje o użytkowniku.

* users
`$ users`
// wynik: użytkownicy połączeni z systemem

* w
`$ w`
// wynik: zalogowani użytkownicy, czynność którą wykonują w momencie wpisania komendy.

* lastlog
`$ lastlog -u <nazwa użytkownika>`
	`-a` // wyświetla wszystkie rekordy 
np. `$ lastlog -u user`
// wynik: informacje o ostatnim logowaniu użytkownika

* last
`$ last`
// wynik: informacje o czasie połączenia użytkowników.
* whoami
`$ whoami`
// wynik: wyświetla nazwę użytkownika, na którym jesteśmy zalogowani