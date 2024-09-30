# Funktioner

För att kunna skapa större och mer komplexa program är funktioner viktigt att använda för tydlighe, struktur och simplicitet. Funktioner kan vara lite svårt att komma igång med men de är helt nödvändiga vid större projekt.

## Skapa funktioner
För att skapa en funktion börjar man likt en variabel med att deklarera den. 

```python
def namn(x, y, z):
    # Fyll på med koden här.
```

Alltid när en ny funktion ska skapas påbörjas det med `def`, sedan kommer namnet av definitionen `namn`. Namnet väljer man helt själv med precis som för variabler så ska funktioner deklareras med rimliga och förklarande namn som passar situationen. 

Exempelvis om man vill skapa en funktion som räknar ut summan mellan två tal så skulle funktionsnamnet kunna vara `summa`. 

Efter funktionens namn kommer *parametrarna* som funktionen behöver använda för att kunna ge tillbaka ett funktionsvärde. I matematiken är vi vana med att en funktion tar ett input-värde (vanligtvis x) och sen får man funktionsvärdet som svar. En funktion i programmering fungerar på liknande sätt, funktionen tar ett antal parametrar och ger tillbaka ett funktionsvärde, i funktionen ovan är parametrarna skrivna med `x`, `y` och `z` samt separerade med ett komma mellan dem.

I exemplet tidigare om funktionen `summa` hade det varit rimligt med två parametrar för att kunna ge ett svar. Vi skulle kunna kalla parametrar för `tal1` och `tal2` inom parentesen.

I slutet kan funktionen även ge en output (alltså ett funktionsvärde) genom att ge tillbaka ett värde. Då behöver funktionen avslutas med en `return`-sats. 

För att exemplifiera hur en hel funktion ser ut ska vi skriva hur hela funktionen `summa` kan se ut.

```python
def summa(tal1, tal2):
    totalt = tal1 + tal2
    return totalt
```

Efter att funktionen är definierade kan man anropa funktionen genom att skriva:

```python
print(summa(5, 7))
```

```{admonition} Tips
:class: Hint
Kopiera både funktionen och print-satsen, kör den och se resultatet!
```

## Flera funktioner

När vi programmerar större program kan vi använda oss av flera olika funktioner för att kunna skapa mer sofistikerade program. Säg att vi vill räkna ut arean på en triangel och en rektangeln som bilden nedan visar.

```{image} img/areaHouse.jpg
:alt: Area av hus
:align: center
:width: 50%
```
Vi delar då upp arean av bilden ovan genom att skapa en funktion för rektangeln och en area för triangeln.

```python
def rek_area(b, h):
    return b * h
```

Samt en funktion för arean av triangeln:

```python
def tri_area(b, h):
    return (b * h)/2
```

För att räkna ut summan av areorna kan vi även använda vår gamla funktion `summa` för att beräkna den totala arean. Ett exempel på hur man skulle kunna använda programmet kommer nedan.

```python
# En funktion för arean av rektangeln
def rek_area(b, h):
    return b * h

# En funktion för arean av triangeln
def tri_area(b, h):
    return (b * h)/2

# En funktion för summan
def summa(tal1, tal2):
    return tal1 + tal2

# Deklarerar basen och höjderna
basen = 30
höjden_rek = 20
höjden_tri = 25

# Beräknar areorna genom att anropa funktionerna
arean_tri = tri_area(basen, höjden_tri)
arean_rek = rek_area(basen, höjden_rek)

# Skriver ut summan av båda areorna
print(summa(arean_tri, arean_rek))
```
Exemplet ovan belyser att vid större programmeringsprojekt blir det för tydlighetens skull viktigt att bryta ner problemet i mindre steg, för att sen lösa de individuella stegen med funktioner.


## Övningar till avsnittet

<!-- start-övningar -->
### Övning 5.1
Skapa en funktion med parametrarna `tal1` och `tal2` som returnerar skillnaden mellan talen.

```{admonition} Tips
:class: Hint dropdown
Börja med att deklarera funktionen med parametrarna `tal1` och `tal2`. I funktionskroppen returneras skillnaden mellan talen.
```

### Övning 5.2
Skapa ett program som tar ett namn som parameter och sedan hälsar på användaren genom att säga *Hej på dig* och sen namnet.

```{admonition} Tips
:class: Hint dropdown
Börja med att deklarera funktionen med parametern `namn`. I funktionskroppen skrivs en print-sats innehållande en hälsningsfras och sen namnet.
```

### Övning 5.3
Skapa en funktion som tar tre parametrar och returnerar talet som är störst

```{admonition} Tips
:class: Hint dropdown
Börja med att deklarera funktionen med parametrarna `a`, `b` och `c`. I funktionskroppen returneras det största värdet genom att använda funktionen den inbyggda funktionen `max()`. 
```

### Övning 5.4

Skapa en funktion som tar en input parameter i grader Celsius `c` och sen skriver ut vad den temperaturen korresponderar i grader Fahrenheit `f`. Formeln för konverteringen från grader Celsius till grader Fahrenheit är: 

$F= \frac{9}{5} \cdot C + 32 $

```{admonition} Tips
:class: Hint dropdown
Börja med att deklarera en funktion, lägg till ett namn på funktionen samt vilka parametrar och returnera värdet genom att utföra beräkningarna enligt formeln ovan, använd till sist en print-sats där du anropas funktionen.
```

### Övning 5.5
Skapa en funktion som tittar om det nämnda året är ett skottår. Om det är skottår, skriv ut `'Skottår!'` om det inte är skottår: skriv ut `'Inte skottår!'`. 

```{admonition} Tips
:class: Hint dropdown
Börja med att deklarera funktionen med parametern `år`. I funktionskroppen skrivs först en if- och else-sats som bestämmer om det är skottår, inom if- och else-satsen skriv en print-sats som anger svaret.
```


<!-- end-övningar -->