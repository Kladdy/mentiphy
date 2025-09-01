# Satser

För att kunna programmera på en lite högre nivå behöver fler satser användas. På föregående sida nämndes några få satser, som print-satsen och input-satsen. Under denna flik kommer vi lägga till flera nya satser som kommer vara nödvändiga att lära sig för att lösa nya sorters problem.

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

Genomgången på if- och else-satsen börjar 11:30 i videon.

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

### Övning 2.1
Skapa ett program som tittar om ett namn som du anger med en input är samma som ditt namn. Skriv ut `Ja!` om det gäller, annars skriv ut `Nej!`.

```{admonition} Tips
:class: Hint dropdown
Börja med att avända en input, jämför sedan namnet med ditt namn i if-satsen och gör därefter en else-sats.
```


### Övning 2.2
Skapa ett program som frågar användaren efter ett tal. Efter svarar programmet om talet är mindre eller större än 50.
Om talet var mindre skrivs ett meddelande att talet var mindre, annars skrivs ett meddelande att talet var större.

```{admonition} Tips
:class: Hint dropdown
Börja med att använda en input som lagrar ett tal, därefter skapa en if och else-sats med hjälp av logista uttryck som `<` och `>`. 
```


### Övning 2.3
Skapa ett program som frågar användaren efter ett lösenord. Om användaren anger rätt lösenord så skrivs ett meddelande att lösenordet är korrekt, annars skrivs ett meddelande att lösenordet var felaktigt.

```{admonition} Tips
:class: Hint dropdown
Börja med att deklarera det korrekta lösenordet, använd sen en if- och else-sats.
```

### Övning 2.4
Skapa ett program som frågar efter en given frukt. Om de skriver äpple ska programmet skriva ut 5 kr, om det är ett päron ska programmet skriva ut 10 kr. Om användaren anger någonting annat än en frukt ska programmet svara "Det finns inga priser för den här frukten".

```{admonition} Tips
:class: Hint dropdown
Skapa en if-sats för äpplet med ett svar, sedan en elif för päron med ett svar, sedan en else-sats med ett svar.
```

### Övning 2.5
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

### Övning 2.6
Skapa ett program som avgör om talet du anger är jämt eller udda. Om svaret är udda eller jämt ska programmet svara att talet är udda respektive jämt. 
```{admonition} Tips
:class: Hint dropdown
Använd en if- och else-sats samt operatorn % som ger resten vid heltalsdivision.
```

### Övning 2.7
Fråga användaren efter tre tal, programmet ska sedan rangordna vilket tal som är störst och skriva ut den korrekta ordningen på storleksordningen av talen.

```{admonition} Tips
:class: Hint dropdown
Använd flera villkor i if-satsen med hjälp av `and`.
```
<!-- end-övningar -->

## Lösningar till övningar
Uppdaterad video kommer!
