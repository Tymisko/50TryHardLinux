# Przetwarzanie danych tekstowych

## `awk` - filtrowanie danych na podstawie wzorców

    $ awk 'pattern {akcja}' plik_wejsciowy

    -F fs | --field-separator fs    // Ustawia znak rozdzielajacy pola w tekscie

**Przykłady:**

    $ awk '{print;}' plik
*wynik: wyświetla zawartość pliku*

    $ awk -F ',' '{print $2,$3}' plik
*wynik: wyświetla drugą i trzecią kolumnę danych z pliku, w którym kolumny są oddzielone `,`*

    $ awk '/aa|bb/' plik
*wynik: wyświetla linijki w których występuje ciąg znaków `aa` lub `bb`*

---