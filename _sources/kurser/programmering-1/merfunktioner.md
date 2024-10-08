# Mer om funktioner
Under den här fliken fördjupar vi våra kunskaper om funktioner, vi kombinerar våra kunskaper om turtle-modulen med våra kunskaper om funktioner.

## Fler metoder för turtles
För att klara av projektet nedan, blir en påfyllning med fler metoder att använda med turtle-modulen nödvändig.

---
```{list-table}
:header-rows: 1

* - Metod
  - Betydelse
* - `t.xcor()`
  - Returnerar skölpaddans x-koordinat.
* - `t.ycor()`
  - Returnerar skölpaddans y-koordinat.
* - `t.heading()`
  - Returnerar skölpaddans riktning `0` är x-axeln och `90` är y-axeln.
* - `t.set_heading(angle)`
  - Sätter skölpaddans riktning. `0` är x-axeln och `90` är y-axeln.
``` 
---
## Funktioner och turtles

För att addera lite mer komplexitet när vi skapar turtle-grafik kan vi även använda funktioner. Till att börja med kan vi börja med att skapa en funktion `def hoppa(t, x, y)`:

```python
def hoppa(t, x, y):
    t.penup()
    t.goto(x, y)
    t.pendown()
```

För att skapa en turtle kan vi även skapa en funktion som heter `def skapa_turtle()`:

```python
def skapa_turtle(x, y):
    t = turtle.Turtle()
    hoppa(t, x, y)
    return t
```

## Funktionsprojekt
Nedan kommer ett funktionsprojekt där vi ska använda funktioner för att bygga turtle-grafik.

Vi ska börja med att använda dessa två funktioner för att göra ett projekt. Gör stegen nedan i ordning eftersom de senare stegen använder kod från de tidigare stegen.

---
### Uppgift 1 - Rektangel
För att börja projektet behöver vi en funktion som skapar en rektangel.

Skapa en funktion `def rektangel(x, y, bredd, höjd, färg)` som skapar en en rektangel vid position `(x, y)` med bredd och höjd `bredd` och `höjd` och färgen `färg`. Funktionen returnerar rektangeln.

```{admonition} Tips
:class: Hint dropdown
Börja med att deklarera funktionen med parametrarna `x`, `y`, `bredd`, `höjd` och `färg`. I funktionskroppen anropas först `t = skapa_turtle(x, y)` funktionen. Ändra sedan färgen till parametern `färg`, därefter skapa rektangeln.
```
---
### Uppgift 2 - Pentagram
Vi behöver även en funktion som skapar ett pentagram.

Skapa en funktion `def pentagram(x, y, sida)` som skapar ett pentagram vid position `(x, y)` med sidan `sida`. Funktionen bygger pentagrammet.

```{admonition} Tips
:class: Hint dropdown
Börja med att deklarera funktionen med parametrarna `x`, `y` och `sida`. I funktionskroppen anropas funktionen `t = skapa_turtle(x, y)`, sedan skapar vi pentagrammet genom att skapa fem sidor, där vinkeln mellan varje sida är 36 grader.
```
---
### Uppgift 3 - Vietnamesiska flaggan

Skapa en funktion `def vietnamesiska_flaggan(x, y, höjd)` som ritar den vietnamesiska flaggan med nedre hörnet i punkten `(x, y)` och med höjden `höjd`. Funktionen ritar flaggan. Flaggans proportioner är 3:2, alltså bredden är 3 och höjden 2. Pentagrammet ska vara centrerad i flaggan. Se bilden nedan för inspiration.

```{image} img/vietnam.png
:alt: en Flagga
:align: center
:width: 50%
```
```admonition} Tips
:class: Hint dropdown
Börja med att deklarera funktionen med parametrarna `x`, `y` och `höjd`. I funktionskroppen ritar vi flaggan genom att anropa `def rektangel(x, y, bredd, höjd, färg)`. Skapa sedan pentagrammet genom att anropa funktionen `def pentagram(x, y, sida)` du behöver dock skriva om det programmet så den fyller i färgen korrekt.
```

### Uppgift 4 - Slumpmässiga skölpaddor
Följ stegen nedan för att lösa ett problem med turtle-modulen som använder sig av funktioner, random och turtle-modulen.

---
#### Steg 1
Skapa en ny fil som heter `randomTurtles.py`

---
#### Steg 2
Längst upp i filen lägg till:

```python	
import turtle
import random
```
---
#### Steg 3
Lägg sedan till funktionerna `hoppa`, `skapa_turtle` och `rektangel` längst upp i filen.

---
#### Steg 4
Skapa funktionen `move_random(t)` som flyttar skölpaddan i en slumpmässig riktning och sträcka. Riktningen ska ändras i intervallet `[-45, 45]` och längden som skölpaddan ska gå är i intervallet `[0, 25]`. För att skapa slumpmässiga värden använd `random` modulen. Ett slumpmässigt tal skapas genom att anropa funktionen `random.randint(a, b)` där `a` och `b` är mellan vilka tal som talet ska slumpas. 

---
#### Steg 5
Skriv nu en kod som skapar en skölpadda, ritar en centrerad kvadrat med metoden `rectangle`. Kvadraten ska ha sidan 500 och fyllas med en ljus färg, exempelvis `'lightblue'`. 

---
#### Steg 6
Flytta skölpaddan till en slumpmässig position inom kvadraten. Nu ser koden ut någonting så här:

```{image} img/turtleSquare.PNG
:alt: En kvadrat.
:align: center
:width: 50%
```

---
#### Steg 7
Skriv nu kod som med hjälp av for-satsen gör anrop till `move_random` Nu kan det se ut så här:

```{image} img/turtleRandomStart.PNG
:alt: En slumpmässig turtle.
:align: center
:width: 50%
```

---
#### Steg 8
Lägg nu till kod i `move_random` som går så att om paddan efter förflyttningen befinner sig utanför den blå rutan vänder sig mot origo. Nu kan resultatet se ut så här:

```{image} img/turtleRandomSecond.PNG
:alt: En slumpmässig turtle.
:align: center
:width: 50%
```

