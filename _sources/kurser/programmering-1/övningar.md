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
  - *3.1-3.12*
* - Turtles
  - Rita simpel grafik med hjälp av turtle-modulen.
  - *4.1-4.8*
* - Funktioner
  - Deklarera och använda funktioner.
  - *5.1-5.11*
* - Lexikon
  - Deklarera och använda lexikon.
  - *6.1-6.4*
* - Projekt i programmering
  - Lösa diverse projekt i programmering
  - Onumrerade
* - Repetition inför klasser
  - Repetitionsuppgifter anpassade för att förbereda inför att lära sig klasser.
  - *1-11*
- Klasser
  - Deklarera och använda klasser, metoder, arv av klasser.
  - *8.1-8.10*
```

## 1. Grundläggande programmering
```{include} grundläggande.md
:start-after: <!-- start-övningar -->
:end-before: <!-- end-övningar -->
```

## 2. Satser
```{include} satser.md
:start-after: <!-- start-övningar -->
:end-before: <!-- end-övningar -->
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

```{include} loopar.md
:start-after: <!-- start-övningar -->
:end-before: <!-- end-övningar -->
```

### Övning 3.9
Skriv ett program som multiplicerar alla tal i en lista och returnerar produkten. Om listan är tom, returnera 1.

```{admonition} Tips
:class: Hint dropdown
Använd en inbyggd metod för listor som heter len().
```

### Övning 3.10
Skapa ett program som tar en lista med heltal och returnerar summan av alla jämna tal i listan.
```{admonition} Tips
:class: Hint dropdown

Använd en `for`-loop för att iterera genom listan och kontrollera om ett tal är jämnt med hjälp av `if num % 2 == 0`.
```

### Övning 3.11
Skapa ett program som räknar hur många negativa tal som finns i en lista.

```{admonition} Tips
:class: Hint dropdown

Du kan använda en variabel för att hålla koll på antalet negativa tal och en `for`-loop tillsammans med en `if`-sats för att jämföra varje tal med 0.
```
### Övning 3.12
Skapa ett program som tar en lista och ett gränsvärde, och returnerar en ny lista med alla tal som är större än gränsvärdet
```{admonition} Tips
:class: Hint dropdown

Använd en `for`-loop för att iterera genom listan och en `if`-sats för att kontrollera om varje tal är större än gränsvärdet.
```

## 4. Turtles

```{include} turtle.md
:start-after: <!-- start-övningar -->
:end-before: <!-- end-övningar -->
```

## 5. Funktioner

```{include} funktioner.md
:start-after: <!-- start-övningar -->
:end-before: <!-- end-övningar -->
```

## 6. Lexikon

```{include} lexikon.md
:start-after: <!-- start-övningar -->
:end-before: <!-- end-övningar -->
```

## 7. Projekt i programmering

```{include} merfunktioner.md
:start-after: <!-- start-projekt -->
:end-before: <!-- end-projekt -->
```
 	
```{include} datahantering.md
:start-after: <!-- start-projekt -->
:end-before: <!-- end-projekt -->
```

```{include} lexikon.md
:start-after: <!-- start-projekt -->
:end-before: <!-- end-projekt -->
```

## 8. Repetition inför klasser

### Övning 1
Skriv en funktion factorial(n) som returnerar fakulteten av n.

```{admonition} Tips	
:class: Hint dropdown

Använd en `for`-loop.
```

### Övning 2
Skriv en funktion remove_duplicates(lst) som tar en lista och returnerar en ny lista utan dubbletter.

```{admonition} Tips
:class: Hint dropdown

Använd en `for`-loop, samt `set` funktionen
```

### Övning 3
Skriv ett program som frågar användaren efter en temperatur i Celsius och skriver ut om det är "Varmt", "Lagom" eller "Kallt" beroende på värdet.

```{admonition} Tips
:class: Hint dropdown

Använd en `if`-sats.
```

### Övning 4
Skriv en funktion word_count(sentence) som räknar antalet ord i en given mening.

```{admonition} Tips
:class: Hint dropdown

Använd först `.split(' ') och sedan en `for`-loop.
```

### Övning 5
Skriv en funktion find_longest_word(words) som tar en lista med ord och returnerar det längsta ordet.

```{admonition} Tips
:class: Hint dropdown

Använd först `.split(' ') och sedan `len()`
```

### Övning 6
Skriv en funktion is_perfect_square(n) som returnerar True om n är ett perfekt kvadrat, annars False.

```{admonition} Tips
:class: Hint dropdown

Använd typkonverteringar.
```

### Övning 7
Skapa en dictionary där nycklarna är ämnen (t.ex. "Matematik", "Historia") och värdena är betyg (t.ex. 5, 4). Skriv ut alla ämnen med betyg över 3.

```{admonition} Tips
:class: Hint dropdown

Gå till lexikonfliken på mentiphy och använd tipsen!
```

### Övning 8
Importera modulen random och generera ett slumpmässigt tal mellan 1 och 100.

```{admonition} Tips
:class: Hint dropdown

Använd `random.randint(a, b)`.
```


### Övning 9
Importera modulen random, skapa en funktion som tar ett antal element som input. Funktionen returnerar medelvärdet av de 100 slumpmässiga talen.

```{admonition} Tips
:class: Hint dropdown

Använd `random.randint(a, b)`, samt en `for`-loop.
```

### Övning 10
Skapa en dictionary med fem olika länder som nycklar och deras huvudstäder som värden. Skriv ut huvudstaden för ett specifikt land.

```{admonition} Tips
:class: Hint dropdown

Gå till lexikonfliken på mentiphy och använd tipsen!
```

### Övning 11
Skapa ett spel där användaren anger en gissning mellan 0-100. Om gissningen är under det rätta svaret svarar programmet "Lägre!" och om gissningen är under det rätta svaret svarar programmet "Större!". När gissningen är korrekt avslutas spelet. Låt det korrekta svaret genereras av en funktion, en gissning används av en funktion och allting ska sedan skrivas i en main(funktion).

```{admonition} Tips
:class: Hint dropdown

Uppgiften liknar en av projekten, lös problemet och rådfråga på vägen!
```

## 8. Klasser

```{include} klasser.md
:start-after: <!-- start-övningar -->
:end-before: <!-- end-övningar -->
```