# docs
Dokumentacja projektu harmonogramow




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
+ Output, danych wyjsciowych, przeliczanych w celu wyswietlenia i wykonania dzialan

+ raporty, sumy zbierane co okreslony cykl w celach historycznych i porownawczych
+ mediow, zrodel

https://www.kalendarz-365.pl/ksiezyca/kalendarz-ksiezycowy.html

### Tabela wzorcow do zbierania danych, Pattern
okreslenie jakie dane beda zbierane

### Tabela do zbierania danych, Input
dodawanie danych z formularza lub aktywnych modolow na stronie www/aplikacji

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


### Tabela projektow, definicja danych wyjsciowych
metody przeliczania jakie SALDO bedzie uzywane
Jednostki beda przeliczane w locie 
Prezentacja wynikow w tabeli output

id
name
description
UNIT
SALDO
TYPE

#### Example

+ name: Osczednosci
+ descriptions: wykonywanie na koniec miesiaca przeliczenia ile zostalo oszczednosci z wydanych pieniedzy, poprzez sprawdzenie salda wydatkow poniesionych/zaplanowanych
+ unit: EUR
+ saldo: savings/spendings
+ type: available/expired


### Tabela do zbierania danych, Output

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
 
CALC
 available, pozostaly
 expired, pozostaly niewykorzystany w czasie, roznica +/-
 
 

### Tabela wzorcow, Pattern


 



