# Metody wstępnego przetwarzania danych, semestr 2026L

## Lab 04, zadania

**Zadanie 1**

Dla zbioru danych `zamowienia.csv` wykonaj:
* 1.1 Wczytaj dane i sprawdź czy są w nim wartości brakujące.
* 1.2 Zbiór z wartościami brakującymi zapisz do oddzielnej zmiennej.
* 1.3 W kolumnie `Sprzedawca` zastąp losowo 10% wartości wartością 'BRAK'. (zobacz funkcje pseudolosowe w bibliotece pandas lub numpy oraz wykorzystaj ćwiczenia z zajęć poprzednich z indeksowaniem danych w ramkach/seriach)
* 1.4 W kolumnie `idZamowienia` zastąp 5% wartości wartością `np.nan`.
* 1.5 W kolumnie `Data zamówienia` zastąp 20% wartości wartością `np.nan`.
* 1.6 W kolumnie `Utarg` zastąp 15% wartości wartością `np.nan`.

**Zadanie 2**

Dla nowego zbioru (z wartościami brakującymi) z zadania 1 wykonaj:
* 2.1 Zastąp wartości brakujące w kolumnie `idZamowienia` wartością 0.
* 2.2 Zastąp wartości brakujące w kolumnie `Data zamówienia` wartościami w przód (`ffill()`).
* 2.3 Zastąp wartości brakujące w kolumnie `Utarg` wartością średnią dla danego kraju.

**Zadanie 3**

Wyświetl na wykresach typu histogram wraz z funkcją rozkładu (dokładnie tak jak w przykładach z wykładu) rozkłady cechy `Utarg` dla zbioru oryginalnego oraz tego po wykonaniu poleceń z zadania 2.

**Zadanie 4**

Wykorzystując zbiór danych https://github.com/YBI-Foundation/Dataset/blob/main/Diabetes%20Missing%20Data.csv wykonaj imputację danych metodą KNN (przykład w materiałach z wykładu), ale stosując technikę `group imputing` czyli wyszukiwanie najbliższych sąsiadów odbywa się w danej grupie obiektów, a nie w całej populacji. Pamiętaj, że wykonujemy to dla cech numerycznych, więc pozostałe możesz póki co pomijać.

**Przetestuj to rozwiązanie dla grup utworzonych dla cech:**
* `Class` - tu będą dwie grupy
* `Age` - tutaj podział na grupy odbywa się na grupy: `<18`, `18_29`, `30_49` i `50+` (możesz je utworzyć jako dodatkową kolumnę pomocniczą).
  
Po każdej imputacji porównaj rozkład zbioru oryginalnego i uzupełnionego jak w przykładach na wykładzie.

**Wskazówki:**
* grupy można stworzyć za pomocą wbudowanej funkcji `groupby` biblioteki pandas i zaaplikować imputer na każdej grupie,
* możesz wytrenować i zaaplikować imputer jednocześnie dla danej grupy (metoda `fit_transform` w większości przypadków wykorzystania biblioteki scikit-learn).

Pamiętaj o tym, że jest to tylko ćwiczenie, a w realnym scenariuszu najpierw dokonamy podziału na abiory train i test jeżeli jest to operacja mająca na celu przygotowanie danych do treningu modelu ML!