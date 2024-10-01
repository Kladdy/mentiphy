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
* - Turtles
  - Rita simpel grafik med hjälp av turtle-modulen.
  - *4.1-4.8*
* - Funktioner
  - Deklarera och använda funktioner.
  - *5.1-5.5*
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
Skriv en funktion som tar en lista med heltal och returnerar summan av alla jämna tal i listan.
```{admonition} Tips
:class: Hint dropdown

Använd en `for`-loop för att iterera genom listan och kontrollera om ett tal är jämnt med hjälp av `if num % 2 == 0`.
```

### Övning 3.11
Skriv en funktion som räknar hur många negativa tal som finns i en lista.

```{admonition} Tips
:class: Hint dropdown

Du kan använda en variabel för att hålla koll på antalet negativa tal och en `for`-loop tillsammans med en `if`-sats för att jämföra varje tal med 0.
```
### Övning 3.12
Skriv en funktion som tar en lista och ett gränsvärde, och returnerar en ny lista med alla tal som är större än gränsvärdet
```{admonition} Tips
:class: Hint dropdown

Använd en `for`-loop för att iterera genom listan och en `if`-sats för att kontrollera om varje tal är större än gränsvärdet.
```
### Övning 3.13
Skriv en funktion som tar en lista av tal och returnerar det största talet. (Använd inte `max()`)

```{admonition} Tips
:class: Hint dropdown

Du kan använda en variabel som börjar med det första talet i listan och sedan jämföra varje efterföljande tal med denna variabel.
```
### Övning 3.14
Skriv en funktion som vänder på en lista utan att använda inbyggda funktioner som reverse().
```{admonition} Tips
:class: Hint dropdown

Du kan skapa en tom lista och lägga till elementen från original-listan baklänges genom att använda en `for`-loop.
```
### Övning 3.15
Skriv en funktion som kontrollerar om ett tal är ett primtal.
```{admonition} Tips
:class: Hint dropdown

Använd en `for`-loop för att kontrollera om talet är delbart med något tal mellan 2 och talet själv. Om det är delbart med något av dessa tal är det inte ett primtal.
```
### Övning 3.16
Skriv en funktion som tar en lista av tal och returnerar skillnaden mellan det största och det minsta talet.
```{admonition} Tips
:class: Hint dropdown

Du kan använda `max()` och `min()` för att hitta det största och minsta talet i listan och sedan beräkna skillnaden mellan dessa.
```

### Övning 3.17
Skriv en funktion som tar en lista med tal och returnerar två listor: en med alla udda tal och en med alla jämna tal.

```{admonition} Tips
:class: Hint dropdown

Skapa två tomma listor och använd en `for`-loop tillsammans med en `if-else`-sats för att skilja på jämna och udda tal med hjälp av `%`-operatorn.
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