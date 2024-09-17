# Turtles
I Python finns en inbyggd modul som heter `turtle` vilket låter användaren skapa en simpel grafik. Skölpaddan kan rita och fylla i figurer med olika färger.

## Skapa en turtle
För att börja med turtle-modulen behöver vi börja med att skriva följande.

```python
import turtle
```

Vi behöver importera turle modulen för att koden ska få åtkomst till alla funktioner och metoder som finns inbyggt i modulen. Efter vi har gjort det kan vi börja med att skapa en turtle. Skriv följande kod:

```python
t = turtle.Turtle()
```

Nu har vi skapat skölpaddan och varje gång vi vill att skölpaddan ska göra någonting så hänvisar vi till skölpaddan genom variabeln `t`. 

## Börja rita

Nu när vi har skapat skölpaddan kan vi beordra den att göra olika saker. En metod är en funktion som är kopplad till ett speciellt objekt (skolpaddan i det här fallet). För att använda en metod använder man *punktnotation*. Precis som när vi använde olika metoder för listor som t.ex `.append()`.

Vi börjar med ett lätt exempel, inkludera koden ovan och kopiera även in detta:

```python
t.forward(100)
t.left(90)
t.forward(100)
t.circle(100)
turtle.exitonclick()
```

Titta vad koden gör och försök klura ut vad de separata metoderna gör för skölpaddan. Genom att titta flera gånger och att försöka förklara för sig själv kan man förstå mycket mer av koden.

Koden `turtle.exitonclick()` gör att fönstret där bilden ritas inte försvinner direkt när skölpaddan är klar, utan försvinner när man stänger ner fönstret.

## Viktiga metoder för att rita med turtles

Nedan listas de viktigaste metoderna när det kommer till turtle-modulen som är bra att använda. 

```{list-table}
:header-rows: 1

* - Metod
  - Betydelse
* - `t.forward(längd)`
  - Skölpaddan rör sig rakt fram lika långt som `längd`.
* - `t.left(antal_grader)`
  - Skölpaddan svänger åt vänster `antal_grader` anger hur många grader som skölpaddan ska svänga med.
* - `t.color(penfärg, fyllnadsfärg)`
  - Ändrar färgen för pennans färg och färgen som man vill fylla i med.
* - `t.begin_fill()`
  - Börjar att fylla i färgen.
* - `t.end_fill()`
  - Avslutar att fylla i färgen.
* - `t.goto(x, y)`
  - Går till x-koordinaten `x` och y-koordinaten `y`.
* - `t.circle(radie)`
  - Skapar en cirkel med radien `radie`.
* - `t.pendown()`
  - Sätter ner pennan och börjar rita.
* - `t.penup()`
  - Tar upp pennan och slutar rita.
* - `t.hideturtle()`
  - Gömmer skölpaddan osynlig.
* - `t.showturtle`
  - Gör skölpaddan synlig.
* - `t.clear()`
  - Tar bort allting som har ritats.
```

## Övningar till avsnittet

<!-- start-övningar -->
### Övning 4.1
Skapa ett program som ritar en kvadrat med sidlängden 100. Gör koden först utan en for-loop och sedan med en for-loop.

```{admonition} Tips
:class: Hint dropdown
Använd metoderna med `t.forward(längd)`, `t.left()` och en for-loop som upprepar koden för varje sida av kvadraten.
```

### Övning 4.2
Använd koden från övning 4.1 och förbättra den så att kvadratens sidor är ritade med färgen `'blue'` och fyll i kvadraten med färgen `'lightblue'`.

```{admonition} Tips
:class: Hint dropdown
Använd metoderna med `t.color(penfärg, fyllnadsfärg)` för att välja färg samt metoderna `t.begin_fill()` och `t.end_fill()` för att fylla i färgerna.
```

### Övning 4.3
Skapa ett program som frågar om en sidlängd och sedan ritar en liksidig triangel med den angivna sidlängden.

```{admonition} Tips
:class: Hint dropdown
Deklarera en variabel som använder input-funktionen för att lagra vilken sidlängd som triangeln ska ha. Använd metoderna med `t.forward(längd)`, `t.left()` och en for-loop som upprepar koden för varje sida av triangeln. Tänk på hur många grader varje vinkel har i en liksidig triangel.
```

### Övning 4.4
Använd koden från övning 4.3 och förbättra den så att triangelns sidor är ritade med en färg som användaren användaren anger, låt även användaren ange med vilken färg som triangeln ska fyllas i med.

```{admonition} Tips
:class: Hint dropdown
Deklarera två variabel som använder input-funktionen för att lagra vilken färg som triangeln ska ritas och fyllas i med. Använd metoderna med `t.color(penfärg, fyllnadsfärg)` för att välja färg samt metoderna `t.begin_fill()` och `t.end_fill()` för att fylla i färgerna.
```

### Övning 4.5
Skapa ett program som ritar en cirkel med radien 20, 40, 60, osv upp till 200. Gör så att cirklarna är placerade innanför den andra. Bilden nedan visar hur resultatet ska se ut.

```{image} img/turtleRings.PNG
:alt: Flera ringar inom varandra.
```

```{admonition} Tips
:class: Hint dropdown
Skapa en for-loop som använder range-funkionen för att skapa alla radier som krävs av cirklarna. I for-loopen ritas cirklarna med hjälp av metoden `t.circle(radie)`. Det är viktigt att for-loopen även inkluderar *var* skölpaddan ska börja med att rita cirkeln. Använd `t.penup()` och `t.pendown()` och ´t.goto(x, y)` i början av for-loopen för att få skölpaddan att börja rita på rätt ställe.
```

### Övning 4.6
Skapa ett program som ritar ett rektangulärt hus med ett triangulärt tak.

```{image} img/turtleHouse.PNG
:alt: Flera ringar inom varandra.
```

### Övning 4.7
Rita 5 cirklar i olika färger bredvid varandra. Bilden nedan visar hur resultatet kan se ut.

```{image} img/turtleColorrings.PNG
:alt: Ringar med färger.
```

```{admonition} Tips
:class: Hint dropdown
Börja med att deklarera en lista med alla färger. Skapa sedan en for-loop som går igenom alla färger, skapa en cirkel för varje gång loppen uppdateras. 
```
<!-- end-övningar -->

### Övning 4.8
Skapa en spiral. Bilden nedan visar hur resultatet kan se ut.

```{image} img/turtleSpiral.PNG
:alt: En spiral.
```
```{admonition} Tips
:class: Hint dropdown
Börja med att deklarera en längd som sprialen ska börja med, gör det här värdet lågt. För varje gång som loopen uppdateras se till att göra sträcket längre. `längd += 1` Skapa en for-loop som använder range-funkionen som upprepar för varje streck som ska ritas. 
```

