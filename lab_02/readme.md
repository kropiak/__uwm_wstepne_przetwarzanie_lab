# Metody wstępnego przetwarzania danych, semestr 2026L

## Lab 02, zadania

Bazując na wykładzie numer 2 wykonaj poniższe zadania i dostarcz rozwiązania w postaci notatnika Jupyter udostępnionego prowadzącemu poprzez repozytorium git.

**Termin: 23.03.2026 godzina 11:29.**

**Zadanie 1**

Wykorzystując zbiór danych https://www.kaggle.com/datasets/amrahhasanov23/otodom-pl-flat-prices-in-poland dokonaj sprawdzenia poprawności danych według wytycznych:
* kompletność dla wszystkich cech,
* czy dane dla kolumny `price` są > 0.

Wylicz również na tej podstawie zbiorczą metrykę jakości danych zgodnie z przykładami z wykładu.

**Zadanie 2**

Dla tego samego zbioru danych wyświetl histogram prezentujący cechę `price`, ale pomiń w tym zbiorze rekoredy, w których tej wartości brakuje.

**Zadanie 3**

Wyświetl wykres pudełkowy dla cechy `price`. Czy w danych dla tej cechy mamy widoczne wartości odstające? Jeżeli tak, to odfiltruj je ze zbioru i zapisz tę część danych (zapewne ramka pandas) do zmiennej `outlier_data`.

**Zadanie 4**

Dodaj nową cechę do zbioru `price_per_m2` i wylicz (tam gdzie to możliwe) cenę z ceceh `price` oraz `surface`. Wyświetl histogram z naniesioną linią reprezentującą wartość funkcji rozkładu dla tej cechy.

Oblicz również wartości kwartyli dla tej cechy i je wyświetl.

Czy wykres ma cechy rozkładu normalnego?

**Zadanie 5**

Jakie jest teoretyczne (wynikające z danych rozkładu, a nie eksperymentu) prawdopodobieństwo wypadnięcia 7 orłów przy 20 rzutach uczciwą monetą? Wykorzystaj przykład z wykładu, zaprezentuj również histogram dla tego rozkładu. Oblicz i wypisz to prawdopodobieństwo.


**Zadanie 6**

Napisz funkcję, która będzie wykonywała symulację rzutu sześciennymi kostkami. W funkcji możemy podać parametr określający liczbę eksperymentów oraz liczbę kostek w każdym rzucie. Funkcja zwraca listę wyników.

Wykonaj kilka symulacji z różnymi parametrami i wyświetl wyniki na wykresie typu histogram wraz z funkcją rozkładu prawdopodobieństwa.