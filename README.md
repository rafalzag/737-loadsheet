# 737-loadsheet

**Zarys funkcjonalności:**

Program 737-loadsheet ma na celu usprawnienie procesu załadunku samolotu.

Obejmuje on swoim zakresem możliwość wyboru załadowania obciążeniem samolotu w dwóch wersjach - wersji Boeing 737-700 (150 pasażerów, gdzie dla każdego przysługuje 20 kg bagażu) i wersji 737-800 (180 pasażerów i 25 kg bagażu na osobę).

Program umożliwi odpowiednie wyliczenie obciążenia ZFW (Zero Fuel Weight) dla wybranego wcześniej typu samolotu w zależności od zadanej liczby pasażerów uwzględniając konstrukcyjną max ZFW.

W programie będzie walidacja ilości pasażerów w zależności od wybranego typu samolotu.

Program załaduje listę pasażerów z inputu zewnętrznego i rozsadzi ich losowo.

Zakres wagowy pasażerów - 40-120 kg.

Następuje sprawdzenie:
a) czy ZFW dla danego typu samolotu nie została przekroczona
b) czy środek ciężkości jest bardziej z przodu, czy z tyłu

Po pomyślnej weryfikacji punktu a) -> umożliwia dalsze procedowanie
Po negatywnej weryfikacji punktu a) -> informuje o przekroczonej ZFW i proponuje usunięcie pasażerów celem spełnienia zadanego warunku do max ZFW
Następnie następuje ponowne sprawdzenie, aż do spełnienia warunku a).

Przy dalszym procedowaniu, dla punktu b) możemy otrzymać 3 odpowiedzi: 1. Środek ciężkości przesunięty do przodu; 2. Środek ciężkości przesunięty do tyłu; 3. Środek ciężkości ok.
Przy opcjach:
1. -> program proponuje zamianę miejscami "cięższych pasażerów" w tylne rzędy, a "lżejszych pasażerów" w przednie rzędy, następnie następuje ponowna weryfikacja, do osiągnięcia punktu 3.
2. -> program proponuje zamianę miejscami "cięższych pasażerów" w przednie rzędy, a "lżejszych pasażerów" w tylne rzędy, następnie następuje ponowna weryfikacja, do osiągnięcia punktu 3.
3. -> program umożliwia zapisanie do pliku outputowego w postaci .txt pełnego loadsheetu.

**GUI:**

Interfejs użytkownika musi umożliwić:
1) Wybranie żądanego typu samolotu
2) Prezentację wybranego typu samolotu
3) Max ZFW dla danego typu samolotu (postać prezentacyjna)
4) Max ilość pasażerów dla danego typu samolotu (postać prezentacyjna)
5) Informacje graficzne nt. przekroczenia ZFW i informacje nt. środka ciężkości
6) Informacje nt. podjęcia stosownych działań celem zoptymalizowania środka ciężkości
7) Zastosowanie przycisku w celem zapisania loadsheetu i exportu do pliku .txt
8) Możliwość wyjścia z programu
