WSTĘP : 
Miałam za zadanie zrobić projekt, który pobiera dane kątowe z pierwszych dwóch kolumn - pitch i roll - z pliku "outputCatapult01". Funckcja odpowiedzialna za pobranie danych :
![image](https://user-images.githubusercontent.com/84075025/122968267-a5c50700-d38b-11eb-8e26-95e822a3b375.png)

Przedstawić te dane na wykresie w stworzonej przeze mnie aplikacji w Win Api w języku programowania cpp. Program pokazuje również kompas.
![image](https://user-images.githubusercontent.com/84075025/122967958-51ba2280-d38b-11eb-93c2-36dcac725cb1.png)

Pobrane dane zapisuje i podstawia do wzoru matematycznego, który określa położenie wskazówki na kompasie.
 ![image](https://user-images.githubusercontent.com/84075025/122968128-7f9f6700-d38b-11eb-9468-ac333ec65049.png)
 
Funckja, która oblicza położenie kątowe wskazówki:
![image](https://user-images.githubusercontent.com/84075025/122968486-e15fd100-d38b-11eb-8964-2671f4285bf5.png)

Oraz funckja, która rysuje wykres i kompas:
![image](https://user-images.githubusercontent.com/84075025/122968625-07857100-d38c-11eb-90bb-05a525b70c73.png)

JAK KORZYSTAĆ Z PROGRAMU?
Program pozwala na ominięcie pierwszych możliwie błędnych linijek danych kątowych z pliku "outputCatapult01". Zatem musimy wpisać, ile linijek chcemy odrzucić wpisując to w białą przestrzeń oraz nacisnąć przycisk "WYGENERUJ" (jeśli uważamy, że wszystkie linijki są poprawne, możemy jedynie wcisnąć guzik bez wcześniejszego wpisywania liczb).
![image](https://user-images.githubusercontent.com/84075025/122969258-bb86fc00-d38c-11eb-8ab8-2ab68b1e89c8.png)

Po wciśnięciu przycisku generuje się powoli wykres. W danym czasie jak pokazane są dane na wykresie, takie dane wykorzystuje program do obliczania, w jakim położeniu powinna być wskazówka na kompasie.
Jest równiez możliwość skalowania wykresu na bieżąco w osi X i Y. Wystarczy nacisnąć których z przycisków "+" bądź "-". 
![image](https://user-images.githubusercontent.com/84075025/122969835-68fa0f80-d38d-11eb-8f7f-e243e815cc43.png)

NAJWAŻNIESZE CZĘŚCI KODU:
Tekst edit jest odpowiedzialny za wczytanie liczb wpisanych przez użytkownika. Po naciśnięciu przycisku "WYGENERUJ" tekst jest przekazywany do zmiennej char "hile".
![image](https://user-images.githubusercontent.com/84075025/122970216-e9b90b80-d38d-11eb-98dc-db3ab4977b3b.png)

W tym momencie program pobiera tekst i przerabia go z "chara" na "inta", by móc odjąć go od pierwszych linijek pobranych z pliku. Również odpalany jest timer zaczynający rysowanie kompasu i wykresów.
![image](https://user-images.githubusercontent.com/84075025/122970471-461c2b00-d38e-11eb-806d-1779f9161c61.png)

Moją wisienką na torcie jest funckja, która odpala się po odpaleniu timera. Wczytuje ona funkcje rysowania:
![image](https://user-images.githubusercontent.com/84075025/122970765-95625b80-d38e-11eb-86ac-370ccdfc10f6.png)

Ważnym elementem jest też druga funckja rysująca. Jej zadaniem jest wymazywanie pierwszego narysowanego wykresu, by móc do woli skalować nowo postałe
![image](https://user-images.githubusercontent.com/84075025/122971016-d9556080-d38e-11eb-9ad7-3f74819a38db.png)
