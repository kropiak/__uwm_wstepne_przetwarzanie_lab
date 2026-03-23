# Metody wstępnego przetwarzania danych, semestr 2026L

## Lab 03, zadania

**Zadanie 1**

Poniżej przygotowany jest pojedynczy eksperyment oparty na klasyfikacji metodą KNN. Dane z datasetu `wine` zostały podzielone na zbiór treningowy i testowy w proporcji 0.8 i 0.2 odpowiednio.

```python
from sklearn.neighbors import KNeighborsClassifier
from sklearn.datasets import load_wine
from sklearn.model_selection import train_test_split


data = load_wine()

X_train, X_test, y_train, y_test = train_test_split(
    data.data, data.target, test_size=0.2)


knn = KNeighborsClassifier(n_neighbors=5)
knn = knn.fit(X_train, y_train)

results = knn.score(X_test, y_test)
results
```

Twoim zadaniem jest napisać kod, który zmieni przebieg tego pojedynczego eksperymentu w eksperyment oparty o próby bootstrapowe.

**Poniżej wytyczne:**
* dodaj parametr umożliwiający wskazanie liczby prób bootstrapowych,
* zapisuj metrykę `accuracy` dla każdego modelu na danych testowych,
* po wykonaniu wszystkich eksperymentów wyświetl histogram oraz boxplot dla tej metryki,
* znajdź 95% przedział ufności dla wartości metryki `accuracy`.

**Zadanie 2**

Bazując na tym samym zbiorze danych (`wine`) wyświetl wykres funkcji rozkładu dla jego cech (ale bez atrybutu decyzyjnego), aby sprawdzić czy mają one cechy rozkładu normalnego. Możesz wygenerować kilka wykresów, jeżeli jeden jest zbyt nieczytelny. Oceniając intuicyjnie normalność danych dla danej cechy podziel je na dwie listy (chodzi tylko o nazwy cech do późniejszego wykorzystania): jedna zawiera nazwy cech, które Twoim zdaniem wykazują cechy normalności, a pozostałe nazwy cech umieść w drugiej liście.

**Zadanie 3**

Wylicz teraz korelację Pearsona dla wszystkich cech (oprócz atrybutu decyzyjnego). Wyświetl macierz korelacji w postaci wykresu typu mapa cieplna (patrz wykład) z naniesionymi wartościami korelacji.

**Zadanie 4**

Wylicz korelację Spearmana oraz tau Kendalla dla tych samych cech co w zadaniu 3 i zapisz wyniki w postaci macierzy. Wylicz teraz różnicę między macierzą korelacji Pearsona i Spearmana oraz Pearsona i Kendalla (pracujesz na tablicach numpy) i wyświetl te różnice w postaci mapy cieplnej.

Czy można stwierdzić, że największe różnice w wartości korelacji wyliczonej metodą Pearsona, a pozostałymi dwiema wystąpują dla cech, które nie wykazują cech normalności? Czy nie widać tutaj takiej zależności (pamiętaj o tych dwóch listach z zadania 2)?


**Zadanie 5**

Wylicz korelację Spearmana dla wszystkich cech w odniesieniu do atrybutu decyzyjnego. Wyświetl nazwy cech i wartość korelacji do atrybutu `Class` sortując malejąco po wartości korelacji. Odetnij ze zbioru danych 3 cechy o najniższej korelacji i bazując na próbie bootstrapowej z zadania 1 przeprowadź kolejny eksperyment z wykorzystaniem zredukowanego zbioru cech. Porównaj wyniki i opisz swoje wnioski.