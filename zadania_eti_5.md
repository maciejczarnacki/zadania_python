# Dalej klasy i obiekty

### Zadanie 1.

Stwórz system zarządzania różnymi typami mediów (np. książki, filmy, muzyka).

Zdefiniuj abstrakcyjną klasę bazową Medium, która będzie zawierać:
Abstrakcyjną metodę wyswietl_info(self), która powinna wyświetlać podstawowe informacje o danym medium.
Abstrakcyjną metodę odtwarzaj(self), która symuluje odtwarzanie danego medium (jeśli dotyczy). Jeśli medium nie można odtworzyć (np. książka), metoda powinna wyświetlić odpowiedni komunikat. Zwykły atrybut tytul (string) inicjalizowany w konstruktorze.
Zwykły atrybut data_wydania (obiekt datetime.date) inicjalizowany w konstruktorze.

Stwórz trzy konkretne klasy potomne dziedziczące po Medium:
Ksiazka: Dodatkowo zawiera atrybut autor (string) i implementuje wyswietl_info, wyświetlając tytuł, autora i datę wydania. Metoda odtwarzaj powinna wyświetlić komunikat, że książki nie można odtworzyć w tradycyjny sposób.
Film: Dodatkowo zawiera atrybuty rezyser (string) i dlugosc_w_minutach (int) oraz implementuje wyswietl_info, wyświetlając tytuł, reżysera, długość i datę wydania. Metoda odtwarzaj powinna wyświetlić symulowany komunikat o odtwarzaniu filmu (np. "Odtwarzanie filmu: [tytuł]").
Piosenka: Dodatkowo zawiera atrybuty wykonawca (string) i gatunek (string) oraz implementuje wyswietl_info, wyświetlając tytuł, wykonawcę, gatunek i datę wydania. Metoda odtwarzaj powinna wyświetlić symulowany komunikat o odtwarzaniu piosenki (np. "Odtwarzanie piosenki: [tytuł] wykonawcy [wykonawca]").

### Zadanie 2.

System Konwersji Jednostek - Metody Klasowe i Statyczne

Stwórz klasę KonwerterTemperatur, która będzie służyć do konwersji między różnymi jednostkami temperatury.

Zdefiniuj klasę KonwerterTemperatur.
Stwórz metodę instancji __init__(self, temperatura_celsjusza), która przyjmuje temperaturę w stopniach Celsjusza i przechowuje ją jako atrybut instancji _celsius.
Stwórz metodę instancji do_fahrenheita(self), która zwraca temperaturę w stopniach Fahrenheita.
Stwórz metodę klasy @classmethod o nazwie z_fahrenheita(cls, temperatura_fahrenheita), która przyjmuje temperaturę w stopniach Fahrenheita i zwraca nową instancję klasy KonwerterTemperatur z przeliczoną temperaturą na stopnie Celsjusza.
Stwórz metodę statyczną @staticmethod o nazwie celsjusz_na_kelwin(celsjusz), która przyjmuje temperaturę w stopniach Celsjusza i zwraca jej wartość w Kelwinach.
Przetestuj działanie klasy, tworząc instancje na różne sposoby (bezpośrednio i za pomocą metody klasowej) oraz używając wszystkich metod do konwersji.

### Zadanie 3.

Klasa Prostokat z Kontrolowanym Dostępem do Wymiarów - Właściwości

Stwórz klasę Prostokat, która będzie reprezentować prostokąt z kontrolowanym dostępem do jego szerokości i wysokości.

Zdefiniuj klasę Prostokat z konstruktorem __init__(self, szerokosc, wysokosc), który inicjalizuje chronione atrybuty _szerokosc i _wysokosc.
Zaimplementuj właściwość @property o nazwie szerokosc. Powiąż ją z metodą get_szerokosc(self), która zwraca wartość _szerokosc.
Zaimplementuj setter @szerokosc.setter, który będzie ustawiał nową wartość dla _szerokosc. Setter powinien zawierać walidację, która upewni się, że nowa szerokość jest liczbą dodatnią. Jeśli wartość nie jest poprawna, powinien zostać podniesiony wyjątek ValueError z odpowiednim komunikatem.
Zaimplementuj właściwość @property o nazwie wysokosc z odpowiadającym getterem get_wysokosc(self) i setterem @wysokosc.setter, który również waliduje, czy nowa wysokość jest liczbą dodatnią i w razie potrzeby podnosi ValueError.
Dodaj metodę instancji oblicz_pole(self), która zwraca pole prostokąta na podstawie aktualnej szerokości i wysokości.
Przetestuj działanie klasy, próbując ustawić nieprawidłowe wartości szerokości i wysokości (sprawdź, czy wyjątki są poprawnie podnoszone) oraz oblicz pole prostokąta z poprawnymi wymiarami.
