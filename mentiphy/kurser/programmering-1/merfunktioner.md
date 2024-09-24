# Mer om funktioner

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

### Steg 1 - Rektangel
För att börja projektet behöver vi en funktion som skapar en rektangel.

Skapa en funktion `def rektangel(x, y, bredd, höjd, färg)` som skapar en en rektangel vid position `(x, y)` med bredd och höjd `bredd` och `höjd` och färgen `färg`. Funktionen returnerar rektangeln.

```{admonition} Tips
:class: Hint dropdown
Börja med att deklarera funktionen med parametrarna `x`, `y`, `bredd`, `höjd` och `färg`. I funktionskroppen anropas först `t = skapa_turtle(x, y)` funktionen. Ändra sedan färgen till parametern `färg`, därefter skapa rektangeln.
```

### Steg 2 - Pentagram
Vi behöver även en funktion som skapar ett pentagram.

Skapa en funktion `def pentagram(x, y, sida)` som skapar ett pentagram vid position `(x, y)` med sidan `sida`. Funktionen bygger pentagrammet.

```{admonition} Tips
:class: Hint dropdown
Börja med att deklarera funktionen med parametrarna `x`, `y` och `sida`. I funktionskroppen anropas funktionen `t = skapa_turtle(x, y)`, sedan skapar vi pentagrammet genom att skapa fem sidor, där vinkeln mellan varje sida är 36 grader.
```

### Steg 3 - Vietnamnamesiska flaggan

Skapa en funktion `def vietnamesiska_flaggan(x, y, höjd)` som ritar den vietnamesiska flaggan med nedre hörnet i punkten `(x, y)` och med höjden `höjd`. Funktionen ritar flaggan. Flaggans proportioner är 3:2, alltså bredden är 3 och höjden 2. Pentagrammet ska vara centrerad i flaggan. Se bilden nedan för inspiration.

```{image} img/vietnam.png
:alt: en Flagga
```
```admonition} Tips
:class: Hint dropdown
Börja med att deklarera funktionen med parametrarna `x`, `y` och `höjd`. I funktionskroppen ritar vi flaggan genom att anropa `def rektangel(x, y, bredd, höjd, färg)`. Skapa sedan pentagrammet genom att anropa funktionen `def pentagram(x, y, sida)` du behöver dock skriva om det programmet så den fyller i färgen korrekt.
```

### Steg 4

#### 1
Skapa en ny fil som heter `randomTurtles.py`

#### 2
Längst upp i filen lägg till:

```python	
import turtle
import random
```

#### 3
Lägg sedan till funktionerna `hoppa`, `skapa_turtle` och `rektangel` längst upp i filen.

#### 4
Skapa funktionen `move_random(t)` som flyttar skölpaddan i en slumpmässig riktning och sträcka. Riktningen ska ändras i intervallet `[-45, 45]` och längden som skölpaddan ska gå är i intervallet `[0, 25]`. För att skapa slumpmässiga värden använd `random` modulen. Ett slumpmässigt tal skapas genom att anropa funktionen `random.randint(a, b)` där `a` och `b` är mellan vilka tal som talet ska slumpas. 