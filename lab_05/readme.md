# Metody wstępnego przetwarzania danych, semestr 2026L

## Lab 05, zadania

**Zadanie 1**

Korzystając ze zbioru danych titanic (https://raw.githubusercontent.com/datasciencedojo/datasets/refs/heads/master/titanic.csv) wykonaj:

**1.1**
* sprawdź czy w zbiorze są wartości brakujące i policz jaki % tych wartości występuje dla każdej z cech
* w kolumnie `Embarked` zastąp wartości brakujące wartością `U` (co będzie oznaczało `Unknown`, jako nowa wartość cechy)


**1.2**
* stwórz kopię ramki danych
* enkodowanie cechy `Sex` metodą One-Hot Encoding bez omijania pułapki zmiennych zero-jedynkowych
* enkodowanie cechy `Embarked` metodą One-Hot Encoding bez omijania pułapki zmiennych zero-jedynkowych

**1.3**
* wylicz i wyświetl teraz zgodnie z przykładem z wykładu wartość VIF dla cech numerycznych tego zbioru


**1.4**
* ponownie stwórz kopię oryginalnej ramki danych,
* ponownie enkoduj cechy `Sex` oraz `Embarked` metodą One-Hot Encoding, ale tym razem z ominięciem pułapki zmiennych zero-jedynkowych
* wylicz i wyświetl teraz zgodnie z przykładem z wykładu wartość VIF dla cech numerycznych tego zbioru


**Zadanie 2**

Pracując na zbiorze danych `adult.csv` wykonaj:

**2.1**
* zakoduj cechę `workclass` metodą One hot encoding z omijaniem pułapki,
* dla cechy `native-country` wykonaj następujące czynności:
    * stwórz nową kolumnę o nazwie `region`
    * zmapuj kraje na regiony (pokrywające się z kontynentami: Europa, Azja, Ameryka Północna itd.)
    * zakoduj cechę `region` metodą One hot encoding z omijaniem pułapki

**2.2**
* dla cechy `occupation` wykonaj kodowanie metodą Binary encoding i dołącz te nowe kolumny do ramki danych

**2.3**
* zakoduj metodą one hot encoding cechy `race` oraz `sex`.
