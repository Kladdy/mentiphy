# Mer om funktioner
Under den här fliken fördjupar vi våra kunskaper om funktioner, vi kombinerar våra kunskaper om turtle-modulen med våra kunskaper om funktioner.

## Funktionsprojekt 1
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
* - `t.setheading(angle)`
  - Sätter skölpaddans riktning. `0` är x-axeln och `90` är y-axeln.
``` 
---
### Funktioner och turtles

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


<!-- start-projekt -->

### Projekt - Turtles
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
```{admonition} Tips
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

---
#### Steg 9
Skapa en till skölpadda som slumpas på samma sätt som föregående skölpadda. När avståndet mellan skölpaddorna är inom 20 enheter ska skölpaddan skriva ut meddelandet "nära". Metoden `write(sträng)` skriver ut strängen i fönstret intill skölpaddan. Låt också programmet räkna och sedan skriva ut hur många gånger det var nära mellan skölpaddorna.

---

## Projekt 2 - Bibliotek
Nästa funktionsprojekt innefattar att bygga ett simpelt system för ett bibliotek. Biblioteket ska kunna lägga till böcker till systemet. En bok ska kunna lånas och lämnas tillbaka och man ska även kunna se alla böcker som är tillängliga.

#### Steg 1
Skapa en ny fil med namnet `bookShelf.py`

#### Steg 2
Kopiera följande kod och lägg längst ner.

```python
def main_program():
    available_books = []
    borrowed_books = []

    while True:
        main_menu()
        choice = input("Enter your choice: ")

        if choice == '1':
            add_book(available_books)
        elif choice == '2':
            borrow_book(available_books, borrowed_books)
        elif choice == '3':
            return_book(available_books, borrowed_books)
        elif choice == '4':
            view_books(available_books)
        elif choice == '5':
            print("Exiting the system.")
            break
        else:
            print("Invalid choice. Please try again.")
```

#### Steg 3
Skapa en funktion `add_book(available_books)` som lägger till en bok i listan `available_books`.

#### Steg 4
Skapa en funktion `borrow_book(available_books, borrowed_books)` som tillåter användaren låna en bok, då försvinner den från listan `available_books` och läggs till på listan `borrowed_books`.

#### Steg 5
Skapa en funktion `return_book(available_books, borrowed_books)` som tillåter boken att lämnas tillbaka på listan `available_books` och boken försvinner på listan `borrowed_books`.

#### Steg 6
Skapa en funktion `view_books(available_books)` som skriver ut alla boken i listan `available_books`.

#### Steg 7
Lägg till koden nedanför längst ner och kör programmet!

```python
if __name__ == "__main__":
    main_program()
```

## Projekt 3 - Miniräknare

#### Steg 1
Skapa en funktion `addera(tal1, tal2)` som tillåter användaren att addera två tal och returnerar summan.

#### Steg 2
Skapa en funktion `subtrahera(tal1, tal2)` som tillåter användaren att subtrahera två tal och returnerar differensen.

#### Steg 3
Skapa en funktion `multiplikera(tal1, tal2)` som tillåter användaren att multiplikera två tal och returnerar produkten.

#### Steg 4
Skapa en funktion `dividera(tal1, tal2)` som tillåter användaren att dividera två tal och returnerar kvoten.

#### Steg 5
Skapa en funktion `main()` som frågar användaren efter två tal, därefter skriver den ut olika alternativ. Om användaren klickar `1` adderas talen, `2` subtraheras talen, `3` multiplikeras talen och `4` divideras talen.

När programmmet är klart ska programmet köras om och fråga användaren om den vill använda miniräknaren igen. Om `5` anges så stängs programmet ned.

#### Steg 6
Redigera `main()` funktionen så att den frågar användaren om den vill spara svaret av uträkningen. Användaren kan nu välja att använda det sparade värdet som en del av sin uträkning och då lägga till en nytt tal för att göra en ny uträkning.

Exempel: Du anger talen `2` och `3`, du väljer addition och får summan `5`. Då frågar programmet dig om du vill spara summan `5` för att använda den senare. Då frågar programmet dig på nytt vilken operator du vill välja, då kanske du väljer subtraktion, då blir `5` det första talet som inputparameter till funktionerna.

## Projekt 4 - Hänga gubbe

#### Steg 1: Förberedelser

1. **Skapa en ny fil**:
    - Skapa en ny fil med namnet `hangagubbe.py`


2. **Importera nödvändiga bibliotek**:
    - Lägg till följande kod högst upp i filen:

      ```python
      import turtle
      import random
      ```
3. **Definiera ordlistan**:
    - Skapa en lista med ord som spelarna ska gissa:

      ```python
      ordlista = ["ord1", "ord2", "ord3", "ord4", "ord5"]
      ```
    Programmet kommer sedan slumpa ett av orden ovan för dig att gissa.

#### Steg 2: Spelets logik
1. **Välj ett slumpmässigt ord**:
    - Lägg till följande kod för att slumpa ett ord från listan och skapa variabler för spelets tillstånd:

      ```python
      hemligt_ord = random.choice(words)
      gissade_ord = []
      försök = 6  # Antal försök innan gubben hängs
      ```
2. **Skapa huvudloopen**:
    - Skapa en while-loop som fortsätter till det spelaren gubben hängs:
    - Skapa en lista med varje tecken i ordet.
    - Skapa en annan lista som är lika lång som `hemligt_ord` och fyller med "_".
    - Fråga användaren om en gissning, om gissningen stämmer ska programmet skriva ut att gissningen var korrekt, samt  visa på vilken position som tecknet fyllde. Om gissningen är fel ska programmet skriva ut att gissningen var fel. Vi ska börja med att rita gubben vid senare skede, just nu fokuserar vi bara på att programmet ska fungera någorlunda.
    - Om antalet gissnar överskrider `försök` ska programmet skriva ut att vi har förlorat, samt avsluta koden.
    - Om vi har gissat rätt, ska programmet också avslutas.

#### Steg 3: Spelets grafik
1. **Rita platsen där gubben ska hängas**:
    - Skapa en funktion som ritar ut platsen där gubben kommer hängas, anropa funktionen längst ner i koden.
    - Titta på bilden nedan som inspiration för hur den kan se ut.

```{image} img/hangman_1.png
:alt: En plats.
:align: center
:width: 50%
```

2. **Rita gubben**:
    - Skapa en funktion där gubben ritas ut med hjälp av turtlegrafik.
    - Dela upp ritningen av gubben i olika delar. 
    - Anropa rita gubben-funktionen vid en fel gissning ska en viss del av gubben ritas ut. 

#### Steg 4: Utvärdera programmet

7. **Utvärdera programmet**:
- Kör programmet och testa spelet.
- Fundera på hur du kan förbättra det:
  - Lägg till fler ord i listan.
  - Visa en vinst- eller förlustskärm med Turtle.
  - Gör spelet snyggare med färger eller animationer.


<!-- end-projekt -->