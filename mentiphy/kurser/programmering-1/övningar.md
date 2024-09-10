# Övningar till kursen

Under den här fliken samlas samtliga övningar till kursen. Istället för att navigera bland de andra flikarna är samtliga övningar samlade här. 

Tabellen nedan visar var övningar till de olika avsnitten finns.

```{list-table}
:header-rows: 1

* - Avsnitt
  - Innehåll
  - Nummer
* - Grundläggande programmering
  - print-satsen, variabler och tilldelningar, datatyper och typkonverteringar, input-satsen.
  - *1.1-1.6*
* - Satser
  - Listor, if- och else-satsen, elif-satsen, logiska uttryck.
  - *2.1-2.10*
* - Loopar
  - for-loopen, range-funktionen, listor och for-loopar, while-loopen.
  - *3.1-3.5*
```

## 1. Grundläggande programmering

### Övning 1.1
Skriv ett program som hälsar på användaren. Exempelvis med orden "Hej på dig!"

```{admonition} Tips
:class: Hint dropdown
Använd print-satsen.
```
### Övning 1.2
Skriv ett program som utför additionen 5+7 och skriver ut svaret av additionen. 

```{admonition} Tips
:class: Hint dropdown
Använd additionstecknet och print-satsen.
```
### Övning 1.3
Skriv ett program som frågar efter din ålder och skriver ut hur gammal du kommer vara om 5 år.

```{admonition} Tips
:class: Hint dropdown
Använd input-satsen.
```
### Övning 1.4
Skapa en simpel miniräknare som frågar efter två nummer och sedan skriver ut vad summan, skillnaden, produkten och kvoten är mellan dessa tal.

```{admonition} Tips
:class: Hint dropdown
Börja med att använda input-satsen, deklarera variabler och tilldela värdena genom att utföra beräkningarna, använd till sist en print-sats.
```
### Övning 1.5
Skapa ett program som frågar efter en temperatur i enheten i grader Celsius och sedan skriver ut vad den temperaturen korresponderar i grader Fahrenheit. Tips formeln för konverteringen från grader Celsius till grader Fahrenheit är: 

$F= \frac{9}{5} \cdot C + 32 $

```{admonition} Tips
:class: Hint dropdown
Börja med att använda input-satsen, deklarera variabeln och tilldela värdet genom att utföra beräkningarna enligt formeln ovan, använd till sist en print-sats.
```
### Övning 1.6
Skapa ett program där programmet frågar efter en summa pengar, efter en räntesats och ett antal år. Beräkna summan av ränta på ränta på det insatta kapitalet med hjälp av en exponentialfunktion och skriv ut resultatet till användaren.

$y = C \cdot a^x $

```{admonition} Tips
:class: Hint dropdown
Börja med att använda input-satsen, deklarera variablerna och tilldela värdena genom att utföra beräkningarna enligt formeln ovan, använd till sist en print-sats.
```

## 2. Satser
### Övning 2.1
Skapa ett program där en lista med dina fyra favoritfrukter är inkluderade i en lista. Skriv sedan ut den första och den sista frukten i listan.
```{admonition} Tips
:class: Hint dropdown
Använd `[]` efter listan för att få åtkomst till olika element inom listan, `[-1]` indikerar det sista elementet i listan.
```
### Övning 2.2
Skapa ett program som frågar efter två listor som input och som sen skriver ut båda listorna tillsammans i en lista. 
```{admonition} Tips
:class: Hint dropdown
Använd +-operatorn för att lägga ihop två listor.
```
### Övning 2.3
Skapa ett program som innehåller 12 siffror. Skriv sedan ut varannat element i listan, var tredje element i listan och var fjärde element i listan.

```{admonition} Tips
:class: Hint dropdown
Använd skivningsoperatorerna.
```
### Övning 2.4
Skapa ett program som frågar användaren efter ett lösenord. Om användaren anger rätt lösenord så skrivs ett meddelande att lösenordet är korrekt, annars skrivs ett meddelande att lösenordet var felaktigt.
```{admonition} Tips
:class: Hint dropdown
Börja med att deklarera det korrekta lösenordet, använd sen en if- och else-sats.
```
### Övning 2.5
Skapa ett program där användaren anger hur många poäng hen fick på provet. Listan nedan visar hur många poäng som ger ett särskilt betyg.

```{list-table}
:header-rows: 1

* - Betyg
  - Poäng
* - A
  - 100 poäng eller mer.
* - C
  - 50-100 poäng.
* - E
  - 30-50 poäng.
* - F
  - 30 eller mindre
```
Låt sedan programmet skriva ut vilket betyg som användaren fick.

```{admonition} Tips
:class: Hint dropdown
Använd sen en if-, elif- och else-sats.
```
### Övning 2.6
Skapa ett program som avgör om talet du anger är jämt eller udda. Om svaret är udda eller jämt ska programmet svara att talet är udda respektive jämt. 
```{admonition} Tips
:class: Hint dropdown
Använd en if- och else-sats samt operatorn % som ger resten vid heltalsdivision.
```

### Övning 2.7
Kopiera listan nedan.

```python
namn_lista = ['Ali', 'Adrian', 'Assar', 'Assad', 'Ali']
```
Skriv ett program som skriver ut hur många gånger namnet `'Ali'` förekommer i listan.
```{admonition} Tips
:class: Hint dropdown
Använd en inbyggd metod för listor som heter count().
```

### Övning 2.8
Skapa ett program som sorterar och skriver ut listan nedan i storleksordning.

```python
nummer_lista = [5, 2, 7, 1, -1]
```
```{admonition} Tips
:class: Hint dropdown
Använd en inbyggd metod för listor som heter sort().
```

### Övning 2.9
Skapa ett program som hittar och skriver ut det största och det minsta elementet i listan nedan.

```python
numb_list = [11, 23, 140, -54, -55, 43, 90]
```
```{admonition} Tips
:class: Hint dropdown
Använd en inbyggd metod för listor som heter min() respektive max().
```

### Övning 2.10
Skapa ett program som beräknar och skriver ut hur många element det är i listan nedan.
```python
char_list = ['a', 'b', 'd', 'e'. 'f']
```
```{admonition} Tips
:class: Hint dropdown
Använd en inbyggd metod för listor som heter len().
```

## 3. Loopar

### Övning 3.1
Skapa ett program som med hjälp av en for-loop skriver ut dina favoritluncher från en lista. 

```{admonition} Tips
:class: Hint dropdown
Börja med att deklarera en lista med dina favoritluncher, sedan använd en for-loop för att skriva ut samtliga element ur listan.
```
### Övning 3.2
Skapa ett program som räknar upp till ett angiet tal från 0, koden avslutas sedan med att skriva ut att räkningen är avslutad.
```{admonition} Tips
:class: Hint dropdown
Använd en for-loop och använd range() funktionen.
```
### Övning 3.3
Skapa en lista med alla jämna tal mellan 1-50. Listan ska skapas utan skriva in talen själv.
```{admonition} Tips
:class: Hint dropdown
I den här övningen behövs faktiskt bara en range-funktion. Den kan även göras med en for-loop. Försök att få till en med både en for-loop och en utan.
```
### Övning 3.4
Skriv ett program som frågar användaren efter en siffra och sedan skriver ut multiplikationstabellen för siffran från 1-10.
```{admonition} Tips
:class: Hint dropdown
Använd en for-loop och använd range() funktionen.
```
### Övning 3.5
Skriv ett program som frågar användaren efter en siffra och sedan skriver ut vad talet är i fakultet. Definitionen av fakultet är enligt formeln nedan:

$$n! = n \cdot (n-1) \cdot (n-2) \cdot \ldots \cdot 2 \cdot 1 $$

Där 1 i fakultet definieras som: 

$$1!=1$$
```{admonition} Tips
:class: Hint dropdown
Använd en for-loop och använd range() funktionen.
```

```{include} satser.md
:start-after: <!-- start-testövning -->
:end-before: <!-- end-testövning -->
```


