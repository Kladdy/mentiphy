# Loopar
Under det här fliken kommer vi djupdyka i problem där kod behöver upprepas många gånger efter varandra. För att upprepa kod på ett effektivt sätt är det perfekt att göra med hjälp av loopar, som vi ska kolla på under det här avsnittet.

## for-loopen
För program som genomför liknande uppgifter flera gånger i rad är en for-loop perfekt att använda för att inte behöva skriva onödigt många rader kod. Titta på de två exempel nedan och se hur mycket mindre kod som behöver användas när en for-loop används.

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
for siffror in range(6):
    print(siffror)
```
Resultatet av exempel 1 och 2 är faktiskt samma, även om antalet rader kod är begränsad till två rader istället för sex rader som exempel 1 har. 

Koden i Exempel 2 börjar med en `for` (vilket översätts till svenskans för) vilket följs up av siffror. Det betyder alltså till att börja med, "för alla siffror", sedan kommer ett `in` vilket då betyder i. Till sist kommer `range(6)` vilket betyder en siffra i intervallet 0-5. Om vi ska tänka hur koden fungerar i termer av ord så blir det: "för alla siffror i intervallet 0-5". Kolonet betyder sedan att för det här intervallet ska koden nedan upprepas för hela intervallet.

## range-funktionen
När man vill skapa en loop som uppdateras ett visst antal gånger baserat på ett antal siffror är range-funkionen perfekt för det ändamålet. Range-funktionen generar en sekvens med heltal. Vilket skapas på följande sätt:

```python
range(start, slut, steg)
```

Vilket liknar skivningsoperatorerna för listorna vi gjorde i föregående avsnitt. Som ni kanske såg i exempel 2 angavs bara ett värde, vilket händer ganska ofta när man använder funktioner. Om inte allting anges antar range-funktionen vissa standardvärden, i det här fallet är följande inputs densamma.

```python
range(5)
range(0, 5, 1)
```

För att bli bekväm med hur range-funktionen fungerar kommer några frågor nedan för att vänja er med hur range-funktionen fungerar.

## Listor och for-  loopar

Anledningen att listor blev introducerade ordentligt i början på den här sidan är också för att for-loopar kan appliceras väldigt väl på listor. Exempelvis om vi vill skriva ut alla värden av alla element i listan kan det lätt genomföras med hjälp av en for-loop.

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

for-loopen är mycket viktig för att effektivsera arbetet att skriva kod, särskilt när det är liknande saker som ska genomföras många gånger i rad.

## while-loopen
Ett annat sätt när man vill upprepa kod flera gånger är med hjälp av en `while-loop`. Ordet `while` på svenska blir medan och det är precis så loopen fungerar, medan ett visst villkor är uppfyllt upprepa koden. Nedan kommer ett exempel på hur en while-loop kan användas.

```python
print('Beräkning av n!')
n = int(input('Ange n: '))
prod = 1
i = 1

while i <= n:
    prod += i
    i += 1
print(n, '=', prod)
```
## Videogenomgång

<iframe
    width="100%"
    max-width="800"
    height="450"
    src= https://youtube.com/embed/PebJzdRhnyQ
    frameborder="0"
    allow="autoplay; encrypted-media"
    allowfullscreen
>
</iframe>

## Övningar till avsnittet
Här kommer fliken för övningar, de första tre övningarna är bra för att träna på for-loopar, sedan kommer övningar för while-loopen.


<!-- start-övningar -->
### Övning 3.1
Skapa ett program som med hjälp av en for-loop skriver ut dina favoritluncher från en lista. 

```{admonition} Tips
:class: Hint dropdown
Börja med att deklarera en lista med dina favoritluncher, sedan använd en for-loop för att skriva ut samtliga element ur listan.
```

### Övning 3.2 
Skapa ett program som räknar upp till ett angivet tal från 0, koden avslutas sedan med att skriva ut att räkningen är avslutad.
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
Skapa en lista med minst 15 heltal. Skriv ett program som:
- Filtrerar ut alla jämna tal och skapar en ny lista
- Filtrerar ut alla udda tal och skapar en annan ny lista

Skriv ut de två nya listorna.

```{admonition} Tips
:class: Hint dropdown
Använd `if`- och `else`-satsen.
```

### Övning 3.5
Skapa ett program som räknar ut och skriver ut summan av alla nummer 1-100. 
```{admonition} Tips
:class: Hint dropdown
Börja med att deklarera en summan som noll, skapa sedan en for-lopp som innehåller en range som går upp hela vägen till 100, sedan för varje tal i addera den till variabeln summan.
```

### Övning 3.6
Skapa ett program som fyller en lista med alla tal från 0-10 upphöjt med 2.
```{admonition} Tips
:class: Hint dropdown
Börja med att skapa en tom lista, skapa sedan en for-loop som fyller på med talen i kvadrat. Använd metoden .append() för att lägga till listan.
```

### Övning 3.7
Skriv ett program som frågar användaren efter en siffra och sedan skriver ut multiplikationstabellen för siffran från 1-10.
```{admonition} Tips
:class: Hint dropdown
Använd en for-loop och använd range() funktionen.
```

### Övning 3.8
Skriv ett program som frågar användaren efter en siffra och sedan skriver ut vad talet är i fakultet. Definitionen av fakultet är enligt formeln nedan:

$$n! = n \cdot (n-1) \cdot (n-2) \cdot \ldots \cdot 2 \cdot 1 $$

Där 1 i fakultet definieras som: 

$$1!=1$$
```{admonition} Tips
:class: Hint dropdown
Använd en for-loop och använd range() funktionen.
```

### Övning 3.9
Skapa ett program som frågar användaren efter en sträng, sedan svarar programmet hur många vokaler som det finns i det givna ordet. 

```{admonition} Tips
:class: Hint dropdown
Börja med att skapa en sträng över alla vokaler, deklarera sen en variabel som håller räkningen på hur många vokaler som finns i ordet. Därefter skapar du en for-loop som går igenom strängen bokstav för bokstav, som tittar om bokstaven finns i variabeln som håller koll på alla vokaler. Bokstaven är en vokal, lägg till +1 på variabeln som håller räkningen på antalet vokaler. 
```

### Övning 3.10
Skriv ett program som multiplicerar alla tal i en lista och returnerar produkten. Om listan är tom, returnera 1.

```{admonition} Tips
:class: Hint dropdown
Använd en inbyggd metod för listor som heter len().
```

### Övning 3.11
Skapa ett program som tar en lista med heltal och returnerar summan av alla jämna tal i listan.
```{admonition} Tips
:class: Hint dropdown

Använd en `for`-loop för att iterera genom listan och kontrollera om ett tal är jämnt med hjälp av `if num % 2 == 0`.
```

### Övning 3.12
Skapa ett program som räknar hur många negativa tal som finns i en lista.

```{admonition} Tips
:class: Hint dropdown

Du kan använda en variabel för att hålla koll på antalet negativa tal och en `for`-loop tillsammans med en `if`-sats för att jämföra varje tal med 0.
```
### Övning 3.13
Skapa ett program som tar en lista och ett gränsvärde, och returnerar en ny lista med alla tal som är större än gränsvärdet
```{admonition} Tips
:class: Hint dropdown

Använd en `for`-loop för att iterera genom listan och en `if`-sats för att kontrollera om varje tal är större än gränsvärdet.
```
<!-- end-övningar -->

## Lösningar till övningar

<iframe
    width="100%"
    max-width="800"
    height="450"
    src= https://youtube.com/embed/UFCUIO5UfJU
    frameborder="0"
    allow="autoplay; encrypted-media"
    allowfullscreen
>
</iframe>