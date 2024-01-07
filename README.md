Zbiór danych używany do analizy sentymentu pochodzi z platformy Kaggle i jest dostępny pod linkiem: (https://www.kaggle.com/datasets/bittlingmayer/amazonreviews). Zawiera on recenzje klientów Amazon, wraz z ocenami w formie gwiazdek, służące do uczenia modeli do analizy sentymentu. W przypadku tego zbioru danych, klasy to __label__1 i __label__2, a każdy wiersz przynależy do dokładnie jednej klasy.

__label__1 odpowiada recenzjom z ocenami 1- i 2-gwiazdkowymi.
__label__2 odpowiada recenzjom z ocenami 4- i 5-gwiazdkowymi.
Recenzje z oceną neutralną (3 gwiazdki) nie zostały uwzględnione w oryginalnym zbiorze danych. Tytuły recenzji są dodawane do tekstu, poprzedzone dwukropkiem i spacją.

Większość recenzji jest w języku angielskim, ale występuje kilka w innych językach, takich jak hiszpański.

Modele: 
LSTM Model
Pierwszy model to sieć rekurencyjna LSTM z warstwami embedding, dwiema warstwami LSTM oraz warstwą gęstą na końcu. Model ten został skompilowany z funkcją straty binary_crossentropy i optymalizatorem 'adam'.

CNN Model
Drugi model to sieć konwolucyjna CNN z warstwą embedding, dwiema warstwami konwolucyjnymi, warstwą poolingową, warstwą gęstą oraz warstwą dropout. Model ten również został skompilowany z funkcją straty binary_crossentropy i optymalizatorem 'adam'.

Pre-trained Word Embedding Model
Trzeci model wykorzystuje wcześniej wytrenowany embedding słów załadowany z pliku glove.6B.100d.txt - adres linku: https://nlp.stanford.edu/data/glove.6B.zip. Embedding ten został użyty w warstwie embedding modelu LSTM. Model ten również został skompilowany z funkcją straty binary_crossentropy i optymalizatorem 'adam'.

W celu uruchomienia, pobierz ze wskazanych powyżej adresów i umieść pliki glove.6B.100d.txt, train.ft.txt i test.ft.txt w głównym katalogu projektu.
