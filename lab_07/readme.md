# Metody wstępnego przetwarzania danych, semestr 2026L

## Lab 7: Skalowanie cech.

**Zbiór danych 1:** https://archive-beta.ics.uci.edu/dataset/186/wine+quality (wybierz tylko wine quality white)

> **UWAGA!!!**
> Zbiór podlinkowany powyżej zawiera o wiele więcej obserwacji niż zbiór wine quality wczytywany bezpośrednio poprzez bibliotekę sklearn (chociażby z przykładu z zajęć).
> Nie można więc używać ich w tym zadaniu zamiennie.

**Zadanie 1**

Wybierz 4 cechy ze zbioru numer 1 o najwyższej wariancji i wyświetl ich rozkłady korzystając z przykładu w sekcji 1 wykładu numer 6.


**Zadanie 2**

Napisz funkcję, która będzie służyła do wykrywania czy dana cecha ramki danych posiada wartości odstające wyliczane metodą rozstępu międzyćwiartowego.
Możesz zaimplementować wyliczanie ćwiartek na piechotę lub wykorzystać do tego bibliotekę pandas i/lub numpy, scikit-learn.
Funkcja przyjmuje ramkę danych jako parametr wejściowy, a zwraca listę cech (kolumn), które zawierają wartości odstające.

**Zadanie 3**

Wykorzystaj zbiór danych 1 i stwórz model klasyfikacji wykorzystując kod z sekcji 1.1 wykładu numer 6. Wykorzystaj wszystkie 4 podejścia (brak skalowania, standaryzacja, skalowanie min-max, skalowanie robust) i wyświetl wyniki dla metryki accuracy (jak w przykładzie).

Wytyczne:
* skalujemy wszystkie cechy
* pamiętaj o ochronie przed wyciekiem danych

**Zadanie 4**

Wykorzystaj funkcję z zadania numer 2 do wskazania cech, które ze względu na występujące (lub może nie) wartości odstające, kwalifikują się do poddania ich skalowaniu. Przeskaluj tylko te cechy i wytrenuj model zgodnie z kodem z zadania 3 (de facto odfiltrowujemy tylko cechy przed uruchomieniem całego pipeline-u).

Porównaj wyniki z uzyskanymi w zadaniu numer 3.
Odpowiedz:
* Czy sam fakt występowania wartości odstających jest wskazówką do przeprowadzenia skalowania danych?
* Czy obecność wartości odstających może być czynnikiem decyzyjnym w kontekście zastosowania konkretnej metody skalowania danych?
* Jaki inny czynnik wsytępujący w danych może kwalifikować cechę do poddania jej skalowaniu?
