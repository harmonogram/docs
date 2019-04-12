# docs
Dokumentacja projektu harmonogramow

## TODO
+ Stworzenie dokumentacji
+ prototyp na python, w edytorze jupyter, aby 
mozna bylo latwo stworzyc i przetestowac prototyp
+ stworzenie prostych scenariuszy testowych
+ stworzenie kolejnych wersji pozwalajacych na latwe kontrolowanie stanu obecnego 
+ wersje z mozliwoscia odtwarzania poprzednich stanow, naprawiania bledow, anulowania przeliczen
+ budowa API
+ budowa frontendu:
 widok kalendarza, listy, tabeli, drzewa
 mozliwosc dodawania, edytowania
 testy
 

## Zasad dzialania

## Interfejs
Aplikacja ma byc prosta do obslugi
poprzez pojedyncze dotkniecie lub przesuniecie palcem po kalendarzu, zarysowanie obszaru kwadratu lub linii na kalendarzu.


## Struktura, Moduly
Frontend, Interfejs
API
Backend, www, desktop


## Baza danych
zawiera 3 podstawowe tabele:
+ projektow
+ wzorcow
+ Input, danych wejsciowych,
+ Output, danych wyjsciowych, przeliczanych w celu wyswietlenia i wykonania dzialan i pokazywania ich w widoku uzytkownika lub raportow.



+ raporty, sumy zbierane co okreslony cykl w celach historycznych i porownawczych
+ mediow, zrodel

https://www.kalendarz-365.pl/ksiezyca/kalendarz-ksiezycowy.html

### Tabela wzorcow do zbierania danych, Pattern
okreslenie jakie dane beda zbierane

### Tabela do zbierania danych, Input
dodawanie danych z formularza lub aktywnych modolow na stronie www/aplikacji

id
name
description
UNIT
SALDO
TYPE
status: modyfikowane, przeniesione, zarchiwizowane, przeliczone, itd

#### Zaleznosci

UNIT:
 + id
 + name 
 + description
 

SALDO:
 + id
 + name 
 + description
 

TYPE:
 + id
 + name 
 + description
 
 
Status:
 + id
 + name 
 + description
 
 
#### EXAMPLE
UNIT
pieniadze: 
 EUR
 PLN
waga 
 kg
 g


SALDO:
 konto bankowe
 rachunki domowe
 pomiar cisnienia
 

TYP:
 assigned, Przypisany
 used, zuzyty


### Tabela projektow, definicja obliczen danych wejsciowych / wyjsciowych
logika obliczen
mozna w ten sposob implementowac logike dla obliczen dzialan, raportow, godzin, itd
Tworzyc nowe wartosci na podstawie juz istniejacych, podejmowac inne dzialania w zaleznosci do wyniku

metody przeliczania jakie SALDO bedzie uzywane
Jednostki beda przeliczane w locie 
Prezentacja wynikow w tabeli output

#### Example

+ projekt_id
+ name: Oszczednosci
+ descriptions: wykonywanie na koniec miesiaca przeliczenia ile zostalo oszczednosci z wydanych pieniedzy, poprzez sprawdzenie salda wydatkow poniesionych/zaplanowanych

+ data_from_in: 1 April 2019 // current month
+ data_from_out: 1 April 2019
+ data_to_in: 30 April 2019
+ data_to_out: 30 April 2019
+ saldo_in: spendings
+ saldo_out: savings
+ type_in: available
+ type_out: expired
+ unit_in: EUR
+ unit_out: PLN
+ value_factor: 4,2 // value_in: 100 -> value_out: 420
+ status_in: aktywne
+ status_out: obliczone



### Tabela wydarzen odnosnie projektow, Events

+ projekt_id
+ name: comiesieczny raport osczednosci
+ descriptions: comiesieczne wykonywanie raportu osczednosci

+ settings - config data for create event
+ type: period_time - jak czesto maja byc wykonywane, czas, period
+ unit: month
+ value: 1

#### Zaleznosci

event_type:
 + id
 + name 
 + description

event_unit
 + id
 + unit_id // parent id
 + name 
 + description
 + factor
 

### Tabela do zbierania danych, Executed, Output Projektow
Kazde wydarzenie oraz wykonanie musi byc rejetsrowane z mozliwoscia odtworzenia stanu poprzedniego danych zaleznych



SALDO:
 konto bankowe
 rachunki domowe
 pomiar cisnienia
 
CALC
 available, pozostaly
 expired, pozostaly niewykorzystany w czasie, roznica +/-
 
 

### Tabela wzorcow, Pattern


 



