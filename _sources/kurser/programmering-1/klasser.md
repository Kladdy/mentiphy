# Klasser

I Python kan vi använda klasser och objekt för att organisera vår kod och göra den mer överskådlig. En klass fungerar som en mall för att skapa objekt, alltså egna typer av variabler med specifika egenskaper och funktioner. En klass är som en ritning för att skapa objekt. Vi definierar en klass med nyckelordet `class` följt av klassens namn.


## Exempel: En tärning
Vi ska börja med ett exempel där vi skapar en mall för en tärning. En mall på en tärning hade då inkluderat två viktiga egenskaper för en tärning. Den första viktiga egenskapen hos en tärning är att den har ett antal sidor. Antalet sidor varierar, det kan vi låta användaren välja. Dessutom har den andra egenskapen att vi kan slå den, som ger oss ett slumpmässigt värde mellan 1 och antalet sidor (det här ska vi lägga till senare).


### Skapa en klass

Vi börjar med att skapa en klass genom att skriva `class`, därefter ger vi klassen ett namn `Tärning`. Då har vi skapat klassen. Därefter skapar vi en *konstruktor* som är en funktion där vi lägger till vilka egenskaper som tärningen har. I det här fallet i varje mall för en tärning så finns det ett antal sidor.

```python
class Tärning:
    def __init__(self, sidor):
        """Den här metoden körs när vi skapar ett objekt av klassen. 
        Vi sparar hur många sidor tärningen har."""
        self.sidor = sidor
    
min_tärning = Tärning(6)
```

Vi skriver sedan `self.sidor = sidor` som betyder att objektet (tärningen) har en egenskap som heter `sidor`. Antalet sidor ska vara en inputparameter som vi skickar in vid skapandet av objektet.

Om vi vill skapa ett objekt (en tärning i vårt fall) med hjälp av klassen kan vi deklarera en variabel `min_tärning` som har klassen `Tärning` som typ av objekt och vi använder `6` som input då vi vill skapa en tärning med sex sidor.

### Metoder i klasser
Klasser kan ha metoder, vilket är funktioner som hör till ett objekt och beskriver vad objektet kan göra. Exempelvis kan vi lägga till en metod som gör att tärningen kan kastas och returnera ett slumpmässigt värde.

```python
import random

class Tärning:
    def __init__(self, sidor):
        """Den här metoden körs när vi skapar ett objekt av klassen. 
        Vi sparar hur många sidor tärningen har."""
        self.sidor = sidor
    
    def slå(self):
        """Returnerar ett slumpmässigt värde mellan 1 och antal sidor."""
        return random.randint(1, self.sidor)

min_tärning = Tärning(6)
print(min_tärning.slå())
```

Ovan i exemplet ser vi en annan metod `def slå(self):` där objektet (tärningen) kan utföra saker, i det här fallet kastas och ge tillbaka ett värde. `self` lägger vi alltid till för att vara tydliga med att det är objektet som ska påverkas av metoden.

## Exempel: Ett djur

Nu kan vi skapa en klass `Djur` för att beskriva djur.

```python
class Djur:
    def __init__(self, namn, art):
        """Den här metoden skapar objekt med ett namn och en art."""
        self.namn = namn
        self.art = art
```

Här skapar vi en klass `Djur` med en metod som kallas `__init__`. Den här metoden kallas automatiskt när vi skapar ett nytt objekt och används för att ge objektet sina startvärden.

### Skapa objekt

För att skapa ett objekt av klassen använder vi klassnamnet som en funktion:

```python
mitt_djur = Djur("Bella", "Hund")
print(mitt_djur.namn)  # Output: Bella
```

### Metoder i klasser

I det här exemplet kan vi lägga till en metod som gör att djuret låter:

```python
class Djur:
    def __init__(self, namn, art):
        self.namn = namn
        self.art = art
    
    def låt(self):
        print(f"{self.namn} gör ett ljud!")

mitt_djur = Djur("Bella", "Hund")
mitt_djur.låt()  # Output: Bella gör ett ljud!
```

### Ärva från en annan klass

Python stöder arv, vilket betyder att vi kan skapa en ny klass som bygger på en befintlig klass. Detta gör att vi kan återanvända kod från en annan klass.

```python
class Hund(Djur):
    def __init__(self, namn, ras):
        super().__init__(namn, "Hund")
        self.ras = ras
    
    def skäll(self):
        print(f"{self.namn} skäller!")

min_hund = Hund("Bella", "Labrador")
min_hund.skäll()  # Output: Bella skäller!
```

## Övningar

<!-- start-övningar -->

### Övning 8.1
Skapa en klass `Bil` med attributen `märke` och `modell`.

```{admonition} Tips
:class: Hint 
Definiera en klass `Bil` och använd `__init__` för att spara märke och modell.
```

### Övning 8.2
Lägg till en metod `beskriv` i `Bil` som skriver ut bilens märke och modell.

```{admonition} Tips
:class: Hint dropdown
Skapa en metod i klassen som använder `print()` för att skriva ut bilens information.
```

### Övning 8.3
Skapa en subklass `Elbil` som ärver från `Bil` och lägg till ett attribut `batterikapacitet`.

```{admonition} Tips
:class: Hint dropdown
Använd `super().__init__()` för att återanvända koden från `Bil`.
```

### Övning 8.4
Skapa en metod i `Elbil` som skriver ut batterikapaciteten.

```{admonition} Tips
:class: Hint dropdown
Skapa en metod som skriver ut `batterikapacitet` med `print()`.
```

### Övning 8.5
Skapa en klass `Person` med namn och ålder, samt en metod `hälsa` som skriver ut en hälsning.

```{admonition} Tips
:class: Hint dropdown
Metoden kan skriva ut något som "Hej, jag heter [namn] och är [ålder] år gammal!"
```

### Övning 8.6
Skapa en klass `Rektangel` med attributen `bredd` och `höjd`, och en metod som räknar ut arean.

```{admonition} Tips
:class: Hint dropdown
Arean beräknas med `bredd * höjd`.
```

### Övning 8.7
Skapa en klass `Cirkel` med en metod för att räkna ut omkretsen (använd `math.pi`).

```{admonition} Tips
:class: Hint dropdown
Omkretsen beräknas med `2 * math.pi * radie`.
```

### Övning 8.8
Skapa en klass `Bibliotek` där vi kan lägga till och ta bort böcker i en lista.

```{admonition} Tips
:class: Hint dropdown
Använd en lista för att lagra böcker och metoder för att hantera dem.
```

### Övning 8.9
Skapa en klass `Bankkonto` där vi kan sätta in och ta ut pengar.

```{admonition} Tips
:class: Hint dropdown
Håll koll på saldot och uppdatera det vid insättning och uttag.
```

### Övning 8.10
Skapa en klass `Spelkaraktär` med hälsa och attackkraft, samt en metod för att attackera en annan karaktär.

```{admonition} Tips
:class: Hint dropdown
Använd en metod som minskar hälsan på den attackerade karaktären.
```

### Övning 8.11

Skapa en klass Student med attributen namn, ålder och kurser. Lägg till metoder för att lägga till och ta bort kurser.

```{admonition} Tips
:class: Hint dropdown
Använd en lista för att lagra kurser och skapa metoder för att ändra den.
```

### Övning 8.12

Skapa en klass Bok med attributen titel, författare och antal_sidor. Lägg till metoder för att visa information och ändra antal sidor.

```{admonition} Tips
:class: Hint dropdown
Metoderna ska kunna visa bokens information och ändra antalet sidor vid en ny upplaga.
```

### Övning 8.13

Skapa en klass Restaurang med namn, meny och öppettider. Lägg till metoder för att lägga till rätter och ändra öppettider.

```{admonition} Tips
:class: Hint dropdown
Använd en lista för menyn och en sträng för öppettiderna.
```

### Övning 8.14

Skapa en klass Smartphone med märke, modell och batterinivå. Lägg till metoder för att ladda batteriet och använda telefonen.

```{admonition} Tips	
:class: Hint dropdown
Se till att batterinivån inte överstiger 100% eller sjunker under 0%.
```

### Övning 8.15

Skapa en klass Spel med titel, genre och betyg. Lägg till metoder för att ändra betyget och visa information om spelet.

```{admonition} Tips
:class: Hint dropdown
Betyget ska vara mellan 1 och 10.
```

### Övning 8.16

Skapa en klass Flygplan med modell, kapacitet och aktuella_passagerare. Lägg till metoder för att lägga till och ta bort passagerare.

```{admonition} Tips	
:class: Hint dropdown
Se till att flygplanet inte tar fler passagerare än sin kapacitet.
```


### Övning 8.17

Skapa en klass Musikspelare med låtar och nuvarande_låt. Lägg till metoder för att spela, pausa och byta låt.

```{admonition} Tips
:class: Hint dropdown
Använd en lista för låtar och en metod för att hoppa mellan dem.
```

### Övning 8.18

Skapa en klass Butik med namn, varor och priser. Lägg till metoder för att lägga till nya varor och ändra priser.

```{admonition} Tips
:class: Hint dropdown
Använd en ordbok där nyckeln är varans namn och värdet är priset.
```

### Övning 8.19

Skapa en klass Bibliotekskort med kortnummer, ägare och lånade_böcker. Lägg till metoder för att låna och lämna tillbaka böcker.

```{admonition} Tips
:class: Hint dropdown
Se till att kortet inte kan låna fler än ett visst antal böcker.
```

### Övning 8.20

Skapa en klass Sportlag med namn, spelare och vinster. Lägg till metoder för att lägga till spelare och registrera vinster.

```{admonition} Tips
:class: Hint dropdown
Använd en lista för spelare och en räknare för vinster.
```

## Spelövning
Här kommer en större övning som innefattar att bygga ett spel med hjälp av flera klasser.

#### Steg 1
Skapa en klass `Karaktär` med attribut som `namn`, `level`, `hälsa` och `styrka`. 

- Sätt den initiala hälsan till 100 och styrkan till 10. 

Skapa ett specialattribut `element` som representerar åtminstone elementen, exempelvis `Eld`, `Vatten` och `Jord`, som har unika attribut. 

- En karaktär med elementen `Vatten` har 50% mer styrka mot en karaktär med elementen `Eld`. 

- En karaktär med elementen `Jord` gör 50% mer styrka mot en karaktär med elementen `Vatten`. 

- En karaktär med elementen `Eld` gör 50% mer styrka mot en karaktär med elementen `Jord`.


#### Steg 2
Lägg till en metod `lever` som returnerar hälsan hos en karaktär.

#### Steg 3
Skapa en metod `beskriv` som skriver ut karaktärens `level`, `hälsa` och `styrka`.

#### Steg 4
Skapa subklassen `Fiende` som ärver attribut och metoder från `Karaktär`. Subklassen `Fiende` har en `level`, `hälsa`, `styrka` och `element`. Se till att den första fienden har en hälsa som är slumpad mellan 50 och 75 och skadan mellan 5-10. Attributet ska vara slumpmässiga.

#### Steg 5
Skapa en metod `beskriv` som skriver ut fiendens `level`, `hälsa` och `styrka`. Printa även en rad med bindestreck längst ner!

#### Steg 6
Lägg till en metod `attackera` som låter en karaktär attackera en annan karaktär och minska dess hälsa.

Spelet fungerar så att skadan du gör mot motståndaren slumpas mellan styrkan/2 - styrkan som din karaktär, och skadan mot dig slumpas mellan styrkan/2 - styrkan av fienden. Sedan låter man fienden attackera dig varannan gång och du attackera fienden den andra.Använd `import random`.

Viktigt att göra om skadan och hälsan till datatypen int!

#### Steg 7
Skapa en def combat(spelare, fiende, level) funktion. Använd en loop för att låta spelet möta en fiende tills en karaktär har 0 i hälsa. 

- Om din karaktär har 0 i hälsa så har du förlorat och programmet avslutas. 

- Om du vinner ökar din level med 1 och du får två val: Antingen får du 50 % mer styrka, eller så får du öka din nuvaranda hälsa med 100.

Viktigt att göra om skadan och hälsan till datatypen int!

Anropa main(level) funktionen i slutet av if-satsen om du vinner. Main-funktionen bygger vi i steg 9.

#### Steg 8
När du har vunnit mot en fiende ska dessutom den nya fiendens level öka. När fiendens level ökar ska styrkan och hälsan ökas med 25%. Återigen ska nästa monster skapas, men inom den nya intervallet där hälsan och styrkan har ökat med 25%. 

Viktigt att göra om skadan och hälsan till datatypen int!

#### Steg 9
Skapa en main() funktion där input från spelaren i form av `1` eller `2` används. 

- Varje monster ska beskrivas med hjälp av metoden `beskriv`. Alla fiender ska beskrivas innan man möter dem. 

- När ett monster är besegrat ska valet mellan att öka hälsan eller öka styrkan göras med en input. Beskriv de nya attributerna hos karaktären.

#### Steg 10
Se över att spelet är balanserat, det betyder att spelet inte ska vara för lätt men inte heller för svårt! Det borde vara svårt att nå level 10.

<!-- end-övningar -->

