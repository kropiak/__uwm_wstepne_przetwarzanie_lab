# Metody wstępnego przetwarzania danych, semestr 2026L

## Lab 01, zadania

Bazując na wykładzie numer 1 wykonaj poniższe zadania i dostarcz rozwiązania w postaci notatnika Jupyter udostępnionego prowadzącemu poprzez repozytorium git.

**Termin: 16.03.2026 godzina 11:29.**

**Zadanie 1**

Stwórz moduł o nazwie `mystats` i zaimplementuj w nim metodę `median`, która będzie wyliczała medianę z przekazanej listy wartości numerycznych (możesz dodać odpowiednie warunki sprawdzające). W głównym skrypcie dodaj kod testujący jej działanie, możesz użyć poniższego szablonu.

```python
def main():
    """ tu uruchamiaj kod testowy """
    pass

if __name__ == '__main__':
    main()
```

**Zadanie 2**

W module `mystats` zaimplementuj metodę obliczającą średnią ucinaną z parametrem `p` (patrz materiały z wykładu). Przetestuj jej działanie w głównym skrypcie.

**Zadanie 3**

Na zbiorze danych `iris` (https://archive.ics.uci.edu/dataset/53/iris) policz (wszystkie cechy - cechy bez typu irysa czyli etykiety):
* globalną wartość średnią dla wszystkich cech,
* globalną medianę dla wszystkich cech,
* globalne odchylenie standardowe dla wszystkich cech, 
* wszystkie powyższe wartości dla każdego typu irysów oddzielnie.

**Zadanie 4**

Dla zbioru danych `wine quality` (https://archive.ics.uci.edu/dataset/186/wine+quality) policz:
* wariancję dla każdej cechy z wyjątkiem target (`quality`) oraz `color`,
* uszereguj i wyświetl cechy ze zbioru sortując rosnąco po wyliczonej wariancji (Odpowiadamy na pytanie: Które cechy charakteryzują się najmniejszym rozrzutem danych?),
* wariancję dla każdej cechy oraz dla każdej unikalnej wartości dla cechy `quality`,
* uśrednioną wariancję ze wszystkich cech dla każdej wartości `quality` (czyli średnią z wariancji wyliczonych w poprzednim podpunkcie),
* wylicz odchylenie standardowe dla każdej cechy oprócz `quality`, ale z podziałem na kolor wina (tę cechę też musisz odrzucić z wyliczeń). Czy różnią się one znacząco dla poszczególnych kolorów wina?

**Zadanie 5**

Znajdź wartości przedziałów kwartyli dla wszystkich cech zbioru `wine quality` (oprócz `quality` oraz `color`).

**Zadanie 6**

Wyświetl pozycje ze zbioru `wine quality`, które znajdują się powyżej 95-go percentyla wartości dla cechy `residual_sugar`.
