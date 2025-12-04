# Loopar
Under det här fliken kommer vi djupdyka i problem där kod behöver upprepas många gånger efter varandra. För att upprepa kod på ett effektivt sätt är det perfekt att göra med hjälp av loopar, som vi ska kolla på under det här avsnittet.

## for-loopen
För program som genomför liknande uppgifter flera gånger i rad, samt att när man vet hur många gånger man vill upprepa kodeb är en for-loop perfekt att använda för att inte behöva skriva onödigt många rader kod. Titta på de två exempel nedan och se hur mycket mindre kod som behöver användas när en for-loop används.

### Exempel 1
```python
print(1)
print(2)
print(3)
print(4)
print(5)
print(6)
```
### Exempel 2
```python
for siffror in range(1, 7):
    print(siffror)
```
Resultatet av exempel 1 och 2 är faktiskt samma, även om antalet rader kod är begränsad till två rader istället för sex rader som exempel 1 har. 

Koden i Exempel 2 börjar med en `for` (vilket översätts till svenskans för) vilket följs up av siffror. Det betyder alltså till att börja med, "för alla siffror", sedan kommer ett `in` vilket då betyder i. Till sist kommer `range(1, 7)` vilket betyder en siffra i intervallet 1-6. Om vi ska tänka hur koden fungerar i termer av ord så blir det: "för alla siffror i intervallet 1-6". Kolonet betyder sedan att för det här intervallet ska koden nedan upprepas för.

## range-funktionen
När man vill skapa en loop som uppdateras ett visst antal gånger baserat på ett antal siffror är range-funkionen perfekt för det ändamålet. Range-funktionen generar en sekvens med heltal. Vilket skapas på följande sätt:

```python
range(start, slut, steg)
```

Vilket liknar skivningsoperatorerna för listorna vi gjorde i föregående avsnitt. Som ni kanske såg i exempel 2 angavs bara två värden, vilket händer ganska ofta när man använder funktioner. Om inte allting anges antar range-funktionen vissa standardvärden, i det här fallet är följande inputs densamma.

```python
range(5)
range(0, 5, 1)
```

Om inget värde skrivs ut för start eller slut kommer range-funktionen starta med 0. Om inget värde skrivs ut för steg kommer range-funktionen vara 1. För att bli bekväm med hur range-funktionen fungerar kommer några frågor nedan för att vänja er med hur range-funktionen fungerar. 

## Listor och for-  loopar

Loopar är mycket lätta och användbara tillsammans med listor. Exempelvis om vi vill skriva ut alla värden av alla element i listan kan det lätt genomföras med hjälp av en for-loop.

```python
nummerlista = [1, 2, 3, 4, 5]
for element in nummerlista:
  print(element)
```

```{admonition} Tips
:class: Hint
Kopiera koden, kör den och se resultatet!
```

Först deklareras listan `nummerlista` sen i for-loopen betyder `element` ett element i listan `nummerlista` och för varje element ska for-loopen skriva ut vad värdet av elementet är.

for-loopen är mycket viktig för att effektivsera arbetet att skriva kod, särskilt när det är liknande saker som ska genomföras många gånger i rad och när man vet hur många gånger man vill upprepa koden.

## while-loopen
En annan typ av loop som kallas för `while-loop` är en loop som när man vill upprepa kod flera gånger så länge ett att ett villkor uppfylls. När villkoret inte längre stämmer avslutas loopen. Ordet `while` betyder `medan` och det är precis så loopen fungerar, medan ett visst villkor är uppfyllt ska koden upprepas. Nedan kommer ett exempel på hur en while-loop kan användas.

```python
i = 1
while i < 7:
  print(i)
  i = i + 1

```

```{admonition} Tips
:class: Hint
Kopiera koden, kör den och se resultatet!
```
Det finns två ytterligare viktiga sätt att använda while-loopar på, vilket är med hjälp av en `break`-sats och med hjälp av en `continue`-sats. Nedan kommer ett exempel på hur en `break`-sats fungerar.

```python
i = 1
while i < 7:
  print(i)
  i = i + 1
  if i == 5:
    break

```

```{admonition} Tips
:class: Hint
Kopiera koden, kör den och se resultatet!
```

Det vi ser som resultat av koden är att även om villkoret fortfarande är uppfyllt kan man kringå det och avsluta loopen ändå, vilket i visa situationer kan vara mycket användbart. Nedan kommer ett exempel på en `continue`-sats.

```python
i = 1
while i < 7:
  i = i + 1
  if i == 5:
    print('Hoppa över!')
    continue
  print(i)

```

```{admonition} Tips
:class: Hint
Kopiera koden, kör den och se resultatet!
```

Här ser vi en `continue`-sats, vilket betyder att om villkoret uppfylls ska koden hoppa över det och fortsätta i while-loopen.

## Listbyggare

Det finns en sätt att skapa listor på ett mer kompakt sätt, vilket exemplifieras genom att titta på två exempel som löser samma problem.

### Exempel 1

```python
frukt_lista = ['äpple', 'banan', 'ananas', 'apelsin', 'kiwi']
ny_frukt_lista = []
for frukt in frukt_lista:
    if a in frukt:
        ny_frukt_lista.append(frukt)
    
print(ny_frukt_lista)
```

### Exempel 2

```python
frukt_lista = ['äpple', 'banan', 'ananas', 'apelsin', 'kiwi']
ny_frukt_lista = [frukt for frukt in frukt_lista if 'a' in frukt]

print(ny_frukt_lista)
```

Om du kopierar både exempel 1 och och exempel 2 och kör koden kommer det visa sig att det blir samma resultat, båda exemplen skapar en ny lista med alla frukter som innehåller bokstaven `a`, om bokstaven inte finns med exkluderas de frukterna genom villkoret som är angivet i if-satsen. Vi kan se ett annat exempel på hur vi kan bygga en lista med 10 siffror på ett kompakt sätt.

```python

siffror = [i for i in range(1,11)]

print(siffror)

```
Eller om vi exempelvis vill skapa en lista med alla tal fast upphöjt med 2 mellan 10 och 20.

```python

siffror = [i**2 for i in range(10,21)]

print(siffror)

```

Listbyggare är ett utmärkt sätt att utmana sig själv från att skapa listor utan att använda for-loopar vilket skapar en mer kompakt kod med färre onödiga rader.

## Videogenomgång

<iframe
    width="100%"
    max-width="800"
    height="450"
    src= https://youtube.com/embed/MF2EmjPFqNE
    frameborder="0"
    allow="autoplay; encrypted-media"
    allowfullscreen
>
</iframe>

## Övningar till avsnittet


<!-- start-övningar -->
### Övning 4.1
Skapa ett program som med hjälp av en for-loop skriver ut dina favoritluncher från en lista. 

```{admonition} Tips
:class: Hint dropdown
Börja med att deklarera en lista med dina favoritluncher, sedan använd en for-loop för att skriva ut samtliga element ur listan.
```

### Övning 4.2
Skriv ett program som använder en while-loop för att bygga en lista med de första 20 jämna talen.
```{admonition} Tips
:class: Hint dropdown
Börja med att deklarera en tom lista, sedan använd en while-loop.
```

### Övning 4.3
Bygg en lista med potenser av 2 (dvs 2, 4, 8, 16, ...) tills värdet är större än 1000.
```{admonition} Tips
:class: Hint dropdown
Använd en while-loop med villkoret att värdet ska vara mindre än 1000.
```

### Övning 4.4
Skriv ett program som frågar användaren om hur många stjärnor man vill ha i en trappa. Programmet ska sedan med en for-loop skapar en trappa av stjärnor. Kolla nedan på ett exempel.

```
*
**
***
****
*****
```

```{admonition} Tips
:class: Hint dropdown
Använd en input-sats, en for-loop och använd range() funktionen.
```


### Övning 4.5 
Skapa ett program som frågar användaren om ett tal. Talet ska sedan skriva ut samtliga tal från 0 till det angivna talet. Koden avslutas sedan med att skriva ut att "Uppräkningen är avslutad!".
```{admonition} Tips
:class: Hint dropdown
Använd en input-sats, en for-loop och använd range() funktionen.
```

### Övning 4.6
Skapa ett program som fyller en lista med alla tal från 0-10 upphöjt med 2.
```{admonition} Tips
:class: Hint dropdown
Börja med att skapa en tom lista, skapa sedan en for-loop som fyller på med talen i kvadrat. Använd metoden .append() för att lägga till listan.
```

### Övning 4.7
Skriv ett program som frågar användaren efter en siffra och sedan skriver ut multiplikationstabellen i en lista för siffran från 1-10.
```{admonition} Tips
:class: Hint dropdown
Använd en for-loop och använd range() funktionen.
```

### Övning 4.8
Skapa en lista med alla jämna tal mellan 1-50. Uppgiften ska lösas med hjälp av en for-loop, en while-loop och en listbyggare. Listan ska skapas utan skriva in talen själv.
```{admonition} Tips
:class: Hint dropdown
Använd en for-loop, en while-loop och en listbyggare. Använd dessutom operatorn `%` och en if-sats.
```

### Övning 4.9
Skapa en lista med minst 15 heltal. Skriv ett program som:
- Filtrerar ut alla jämna tal och skapar en ny lista
- Filtrerar ut alla udda tal och skapar en annan ny lista

Skriv ut de två nya listorna.

```{admonition} Tips
:class: Hint dropdown
Använd `%`-operatorn samt `if`- och `else`-satsen.
```

### Övning 4.10
Skapa ett program som räknar ut och skriver ut summan av alla nummer 1-100. 
```{admonition} Tips
:class: Hint dropdown
Börja med att deklarera en summan som noll, skapa sedan en for-lopp som innehåller en range som går upp hela vägen till 100, sedan för varje tal i addera den till variabeln summan.
```

### Övning 4.11
Skriv ett program som frågar användaren efter en siffra och sedan skriver ut vad talet är i fakultet. Definitionen av fakultet är enligt formeln nedan:

$$n! = n \cdot (n-1) \cdot (n-2) \cdot \ldots \cdot 2 \cdot 1 $$

Där 1 i fakultet definieras som: 

$$1!=1$$
```{admonition} Tips
:class: Hint dropdown
Använd en for-loop och använd range() funktionen.
```

### Övning 4.12
Skriv ett program som multiplicerar alla tal i en lista och returnerar produkten. Om listan är tom, returnera 1.

```{admonition} Tips
:class: Hint dropdown
Använd en inbyggd metod för listor som heter len().
```

### Övning 4.13
Skriv ett program som har ett hemligt korrekt tal mellan 1 och 20 och frågar efter ett tal. Om det angivna inte matchar hemligheten, spara talet i en lista. Om det angivna talet är korrekt, skriv ut "Grattis!" och skriv ut listan över alla gissningar.

```{admonition} Tips
:class: Hint dropdown
Använd en while-loop och en if-sats.
```

### Övning 4.14
Skapa ett program som tar en lista med heltal och returnerar summan av alla jämna tal i listan.
```{admonition} Tips
:class: Hint dropdown

Använd en `for`-loop för att iterera genom listan och kontrollera om ett tal är jämnt med hjälp av `if num % 2 == 0`.
```

### Övning 4.15
Skapa ett program som räknar hur många negativa tal som finns i en lista.

```{admonition} Tips
:class: Hint dropdown

Du kan använda en variabel för att hålla koll på antalet negativa tal och en `for`-loop tillsammans med en `if`-sats för att jämföra varje tal med 0.
```
### Övning 4.16
Skapa ett program som tar en lista och ett gränsvärde, och returnerar en ny lista med alla tal som är större än gränsvärdet
```{admonition} Tips
:class: Hint dropdown

Använd en `for`-loop för att iterera genom listan och en `if`-sats för att kontrollera om varje tal är större än gränsvärdet.
```

### Övning 4.17
Skapa ett program som frågar användaren om ett tal eller "stopp". Om användaren anger ett tal ska talet läggas till en lista och i slutet ska alla tal på listan summeras. Om användaren anger "stopp" ska programmet avslutas och skriva ut summan av alla tal.

Ett exempel på hur körningen skulle kunna se ut hade varit:

```python
Ange ett tal eller "stopp": 2
Ange ett tal eller "stopp": 7
Ange ett tal eller "stopp": 9
Ange ett tal eller "stopp": stopp
Din lista: [2, 7, 9]
Summan av alla tal: 18
```

```{admonition} Tips
:class: Hint dropdown

Använd en `while True:` och en `if`-sats, samt en `else`-sats med en `break`.
```

### Övning 4.18
Skapa ett program som frågar användaren efter en sträng, sedan svarar programmet hur många vokaler som det finns i det givna ordet. 

```{admonition} Tips
:class: Hint dropdown
Börja med att skapa en sträng över alla vokaler, deklarera sen en variabel som håller räkningen på hur många vokaler som finns i ordet. Därefter skapar du en for-loop som går igenom strängen bokstav för bokstav, som tittar om bokstaven finns i variabeln som håller koll på alla vokaler. Bokstaven är en vokal, lägg till +1 på variabeln som håller räkningen på antalet vokaler. 
```
<!-- end-övningar -->

## Lösningar till övningar

*OBS!* I videon står det uppgift 3.X. men det motsvarar numera övning 4.X.

<iframe
    width="100%"
    max-width="800"
    height="450"
    src= https://youtube.com/embed/HKI-NdVOBYU
    frameborder="0"
    allow="autoplay; encrypted-media"
    allowfullscreen
>
</iframe>