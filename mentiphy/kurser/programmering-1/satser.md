# Satser

För att kunna programmera på en lite högre nivå behöver fler satser användas. På föregående sida nämndes några få satser, som print-satsen och input-satsen. Under denna flik kommer vi lägga till flera nya satser som kommer vara nödvändiga att lära sig för att lösa nya sorters problem.

## Listor
Innan vi börjar med satser ska vi titta på listor, vilket är viktigt att använda när vi vill lagra mycket information i samma variabel. Nedan följer ett exempel på när en lista kan vara bra.

```python
namn_lista = ['Emma', 'Hussein', 'Lia', 'Malcolm', 'Ava']
```

I exemplet ovan skapar vi en lista för att hålla redan på namnen, exempelvis i en klass som läser programmering. Om vi nu vill redigera den här listan finns det inbggda funktioner och metoder som gör att man kan ändra listan utan att behöva deklarera en ny.

Säg till exempel att det tillkommer en till person vi behöver lägga till på listan. Då använder vi en inbyggd metod i listorna som lägger till det namnet.

```python
namn_lista = ['Emma', 'Hussein', 'Lia', 'Malcolm', 'Ava']
namn_lista.append('Linus')

print(namn_lista)
```
```{admonition} Tips
:class: Hint
Kopiera koden, kör den och se resultatet!
```
Metoden `.append()` lägger alltså till ett nytt element i listan. I andra situationer kanske det blir relevant att en person ska tas bort från listan, då kan det göras på lite olika sätt. Säg att vi vill ta bort Lia, då hade det varit bäst att göra det på följande sätt.

```python
namn_lista = ['Emma', 'Hussein', 'Lia', 'Malcolm', 'Ava', 'Linus']
namn_lista.remove('Lia')
```
```{admonition} Tips
:class: Hint
Kopiera koden, kör den och se resultatet!
```

### Hantera element i listor
Det finns en hel del olika sätt att hantera olika element i listor. Nedan följer lite simpla sätt att få åtkomst till olika element i en lista samt skapa dellistor. Mer information om det kommer lite längre ner. 

För att nå ett specifikt element i listan skrivs det på följande sätt.

```python
namn_lista = ['Emma', 'Hussein', 'Lia', 'Malcolm', 'Ava', 'Linus']

print(namn_lista[0])
print(namn_lista[5])
print(namn_lista[-1])
```
```{admonition} Tips
:class: Hint
Kopiera koden, kör den och se resultatet!
```

Listor i Python är nollindexerade vilket betyder att det första elementet i listan befinner sig på plats 0 i listan, det andra elementet på plats 1, osv.

I vissa situationer vill man dela upp listan i dellistor, då kan det vara smidigt att använda *skivningsoperatorer*. En skivningsoperator fungerar på följande sätt:

```python
[start:stop:steg]
```
Start indikerar var man vill börja med att dela upp listan, stop betyder var man vill sluta med att dela upp listan och steg innebär hur många steg som ska hoppas över per element när dellistan ska skapas. Vi återvänder till exemplet med `namn_lista` för att skapa några olika dellistor.

```python
namn_lista = ['Emma', 'Hussein', 'Lia', 'Malcolm', 'Ava', 'Linus']

print(namn_lista[0:2])
print(namn_lista[0:5:2])
print(namn_lista[0:5:3])
```

```{admonition} Tips
:class: Hint
Kopiera koden, kör den och se resultatet!
```

### Fler metoder och funktioner med listor
Det finns en hel rad olika metoder och funktioner som är inbyggt i Python rörande listor, nedan listas en hel rad olika metoder och funktioner.

```{list-table}
:header-rows: 1

* - Metod
  - Betydelse
* - `append`
  - Lägger till ett element sist.
* - `clear`
  - Tar bort alla element ut listan.
* - `copy`
  - Skapar en kopia av listan dvs ett nytt objekt med samma innehåll.
* - `count`
  - Räknar antalet förekomster visst element.  
* - `extend`
  - Lägger till alla element från en annan lista.
* - `index`
  - Returnerar index för första förekomst av ett element.
* - `insert`
  - Stoppar in ett nytt element på angivet index.
* - `pop`
  - Tar bort och returnerar sista elementet.
* - `remove`
  - Tar bort första förekomst av angivet element.
* - `reverse`
  - Vänder på listan.
* - `sort`
  - Sorterar listan.
```

## if- och else-satsen
I vissa situationer efterfrågar ett program att någonting ska hända, förutsatt att ett visst villkor uppfylls.

if-satsen används i dessa situationer, nedan exemplifieras användingsområdet av if-satsen.

```python
x = int(input('Ange det första talet: '))
y = int(input('Ange det andra talet: '))

if x > y:
    print('Det första talet är störst')
else:
    print('Det andra talet är störst, eller så är dem lika stora')
```
Testa att kopiera programmet ovan, spara det, kör det och ange två siffror. Poängen med if-satsen är alltså att koden som är skriven i satsen endast körs om villkoret uppfylls. I det här fallet `x > y`. Den andra delen av koden finns nästa sats, vilket kallas else. 

Om villkoret hos if-satsen inte uppfylls kommer koden inte att läsa av koden innanför if-satsen utan snarare hoppa vidare till else-satsen längre ner i koden. 

Som många förmodligen tänkte på är koden ovan inte perfekt, det beror framför allt på anledningen att det finns tre olika situationer. När `x` är större än `y`, när `x` är lika med `y` och när `x` är mindre än `y`. För att lösa detta problem är det bäst att faktiskt introducera en ny sats.

## elif-satsen

För att förbättra koden ovan kan vi introducera en elif-sats. Koden förbättras på följande sätt om elif introduceras.

```python
x = int(input('Ange det första talet: '))
y = int(input('Ange det andra talet: '))

if x > y:
    print('Det första talet är störst')
elif x == y:
    print('Det första talet och det andra talet är lika stora')
else:
    print('Det andra talet är störst')
```

Nu med elif-satsen introducerad tar den satsen hand om fallet när båda talen är lika stora. Betydelsen av elif är helt enkelt "else if" eller "annars om"på svenska ska det tolkas som. Alltså, om det första villkoret inte är uppfyllt då tittar programmet om nästa villkor som anges i elif-satsen är uppfyllt, om detta villkor inte heller är uppfyllt avslutar programmet med att köra koden som står angivet i else-satsen.

## Logiska uttryck

I situationer där satser som if-satsen, elif-satsen och else-satsen används kan det vara bra att förstå vad olika logiska uttryck betyder och hur de används.

```python
# x är lika med y
x == y

# x är inte lika med y
x != y

# x är större än y
x > y

# x är mindre än y
x < y

# x är större eller lika med y
x >= y

# x är mindre eller lika med y
x <= y
```

Det är viktigt att operanderna är jämförbara, dvs `x` och `y` ska kunna jämföras på ett lätt sätt. Till exempel när både `x`och `y` är av typen sträng, int eller float.

Det finns även andra logiska uttryck som `and`, `or` och `not`. Exempel om hur det kan användas visas nedan.

```python
dag = 'Måndag'

if dag== 'Måndag' or dag=='Tisdag' or dag=='Onsdag':
    print('Vi är i starten av veckan!')
else:
    print('Vi är i slutet av veckan!')
```

Med `or` operanden kan vi addera fler villkor inom samma if-sats, vilket i många fall kan vara smidigare än att upprepa fler if-satser efter varandra. 

När vi har ett intervall kan det vara smidigt att använda en `and` operand.

```python
ålder = int(input('Ange din ålder: '))

if ålder > 12 and ålder < 20:
    print('Du är tonåring')
elif ålder < 12:
    print('Du är inte tonåringen ännu')
else:
    print('Du har redan varit tonåring')
```
elif-satsen underlättar för addera fler villkor om det behövs för att programmet ska fungera korrekt.

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
De första tre uppgifterna syftar till att öva på listor, de 4-6 på if-, elif- och else-satser.

<!-- start-övningar -->
### Övning 2.1
Skapa ett program där en lista med dina fyra favoritfrukter är inkluderade i en lista. Skriv sedan ut den första och den sista frukten i listan.
```{admonition} Tips
:class: Hint dropdown
Använd `[]` efter listan för att få åtkomst till olika element inom listan, `[-1]` indikerar det sista elementet i listan.
```

### Övning 2.2
Skapa ett program som frågar efter två listor som input och som sen skriver ut båda listorna tillsammans i en lista. 
```{admonition} Tips
:class: Hint dropdown
Använd +-operatorn för att lägga ihop två listor.
```

### Övning 2.3
Skapa ett program som innehåller 12 siffror. Skriv sedan ut varannat element i listan, var tredje element i listan och var fjärde element i listan.

```{admonition} Tips
:class: Hint dropdown
Använd skivningsoperatorerna.
```

### Övning 2.4
Skriv ett program som tar en mening från användaren, exempelvis: 

```
Det här är en mening.
```

Dela upp meningen i en lista där varje ord är ett element. Skriv sedan ut listan.

```{admonition} Tips
:class: Hint dropdown
Använd metoden `split()` för att dela upp en text i ord.
```

### Övning 2.5
Skapa ett program som innehåller en lista med minst 10 heltal. Låt programmet sortera listan i:
- Stigande ordning
- Fallande ordning

Skriv ut resultaten.

```{admonition} Tips
:class: Hint dropdown
Metoden `sort()`, om du vill ha den i andra ordningen använd `sort(reverse=True)`.
```

### Övning 2.6
Skapa två listor med heltal, t.ex.:

```python
lista1 = [5, 2, 9]
lista2 = [8, 1, 6]
```

Skriv ett program som:
- Kombinerar de två listorna
- Sorterar den kombinerade listan i stigande ordning
- Tar bort dubbletter från den sorterade listan

Skriv ut den slutgiltiga listan.

```{admonition} Tips
:class: Hint dropdown
Använd `+` för att kombinera listor, och metoden `set()` för att ta bort dubbletter
```

### Övning 2.7
Låt användaren skriva in en mening. Skriv ett program som:
- Räknar antalet ord i meningen
- Hittar det längsta ordet
- Hittar det kortaste ordet

Skriv ut resultaten.

```{admonition} Tips
:class: Hint dropdown
Du kan använda metoder som `split()` och funktioner som `max()` och `min()`.
```

### Övning 2.8
Skapa två listor med heltal.

```python
lista1 = [1, 2, 3, 4, 5]
lista2 = [4, 5, 6, 7, 8]
```

Skriv ett program som:
- Hittar de gemensamma elementen mellan listorna
- Räknar antalet gemensamma element

```{admonition} Tips
:class: Hint dropdown
Använd `set()` och operatorn `&` för att hitta gemensamma element.
```

### Övning 2.9

Skapa en lista med minst 10 element. Skriv ett program som roterar listan ett bestämt antal steg åt höger. Användaren ska kunna ange hur många steg listan ska roteras.

Exempel:

```
Lista: [1, 2, 3, 4, 5]
Steg: 2
Resultat: [4, 5, 1, 2, 3]
```

```{admonition} Tips
:class: Hint dropdown
Använd slicing för att dela upp listan och kombinera delarna igen.
```


### Övning 2.10
Skapa ett program som frågar användaren efter ett lösenord. Om användaren anger rätt lösenord så skrivs ett meddelande att lösenordet är korrekt, annars skrivs ett meddelande att lösenordet var felaktigt.

```{admonition} Tips
:class: Hint dropdown
Börja med att deklarera det korrekta lösenordet, använd sen en if- och else-sats.
```

### Övning 2.11
Skapa ett program där användaren anger hur många poäng hen fick på provet. Listan nedan visar hur många poäng som ger ett särskilt betyg.

```{list-table}
:header-rows: 1

* - Betyg
  - Poäng
* - A
  - 100 poäng eller mer.
* - C
  - 50-100 poäng.
* - E
  - 30-50 poäng.
* - F
  - 30 eller mindre
```
Låt sedan programmet skriva ut vilket betyg som användaren fick.

```{admonition} Tips
:class: Hint dropdown
Använd sen en if-, elif- och else-sats.
```

### Övning 2.12
Skapa ett program som avgör om talet du anger är jämt eller udda. Om svaret är udda eller jämt ska programmet svara att talet är udda respektive jämt. 
```{admonition} Tips
:class: Hint dropdown
Använd en if- och else-sats samt operatorn % som ger resten vid heltalsdivision.
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
