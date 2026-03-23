

**Zadanie 1**

Dla zbioru danych `zamowienia.csv` wykonaj:
* 1.1 Wczytaj dane i sprawdź czy są w nim jakieś wartości brakujące.
* 1.2 W kolumnie `Sprzedawca` zastąp losowo 10% wartości wartością 'BRAK'. (zobacz funkcje pseudolosowe w bibliotece pandas lub numpy oraz wykorzystaj ćwiczenia z zajęć poprzednich z indeksowaniem danych w ramkach/seriach)
* 1.3 W kolumnie `idZamowienia` zastąp 5% wartości wartością `np.nan`.
* 1.4 W kolumnie `Data zamówienia` zastąp 20% wartości wartością `np.nan`.
* 1.5 W kolumnie `Utarg` zastąp 15% wartości wartością `np.nan`.
* 1.6 Zbiór z wartościami brakującymi zapisz w oddzielnej zmiennej.

**Zadanie 2**

Dla nowego zbioru (z wartościami brakującymi) z zadania 1 wykonaj:
* 2.1 Zastąp wartości brakujące w kolumnie `idZamowienia` wartością 0.
* 2.2 Zastąp wartości brakujące w kolumnie `Data zamówienia` wartościami w przód (`ffill()`).
* 2.3 Zastąp wartości brakujące w kolumnie `Utarg` wartością średnią dla danego kraju.

**Zadanie 3**

Wyświetl na wykresach typu histogram wraz z funkcją rozkładu (dokładnie tak jak w przykładach powyżej) rozkłady cechy `Utarg` dla zbioru oryginalnego oraz tego po wykonaniu poleceń z zadania 2.