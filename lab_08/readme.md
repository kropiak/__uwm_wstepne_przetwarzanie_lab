# Metody wstępnego przetwarzania danych, semestr 2026L

## Lab 8: Redukcja wymiarowości poprzez PCA


Bazując na przykładzie implementacji algorytmu PCA z pakietu `sklearn` w materiałach z wykładu numer 6 wykonaj poniższe zadania.

> Dokumentacja pakietu: https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html

**Zbiór danych 1:** https://archive-beta.ics.uci.edu/dataset/186/wine+quality (wybierz tylko wine quality white)

**Zadanie 1**

Bazując na przykładowym kodzie implementacji PCA dla zbioru `iris` z wykładu, przygotuj implementację dla zbioru numer 1 (white wine powyżej) redukując liczbę cech tego zbioru o 2.
Ile wariancji originalnego zbioru wyjaśnia nowy, zredukowany zbiór?

**Zadanie 2**

Sprawdź w dokumentacji pakietu (link powyżej) w jaki sposób dobierając wartość parametru `n_components` można ustawić próg wariancji, poniżej którego nie chcemy zejść przygotowując nowy, zredukowany zbiór danych. Ustaw ten próg na 95% i sprawdź ile cech pozostało w finalnym zbiorze danych.

**Zadanie 3**

Przygotuj kod, którym sprawdzisz teraz jaki wpływ na model klasyfikacji ma zastosowana redukcja wymiarowości w zadaniu 1 oraz 2.
Wykorzystaj kod z labu poprzedniego (czyli sekcja 1.1 w wykładzie 6 z KNNClassifier).

**Ogólny pipeline:**
* wczytanie danych,
* skalowanie (trzeba przed użyciema PCA) - pamiętaj o podziale danych i ochronie przed ich wyciekiem,
* redukcja wymiarowości (eksperyment 1 - o 2 cechy, eksperyment 2 - z progiem wariancji),
* trening modelu, walidacja i zebranie metryk

**Mile widziane:**

1. Podobnie jak przy wcześniejszych eksperymentach, warto je powtórzyć na różnych podzbiorach danych (losowy podział). Zastanów się jak i gdzie wpleść pętlę, w której można określić liczbę eksperymentów i zbierać wyniki dla każdego z nich.
2. Wygenerowanie wykresów pudełkowych dla wielu wyników eksperymentów może ukazać charakterystykę każdego podejścia, np. mniejszy rozrzut wyników, czyli większą stabilność modelu (węższy przedział ufności co do wartości oczekiwanej danej metryki modelu).
  

