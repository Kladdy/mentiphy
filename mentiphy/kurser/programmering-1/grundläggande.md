# Grundläggande programmering i Python

För att börja att programmera i Python finns det vissa grundläggande kod och färdigheter som är bra att börja med.

## Kommentarer
Vi ska börja med någonting som är mycket viktigt, men inte påverkar utfallet av koden, nämligen kommentarer. Kommentarer används för att kommunicera med sig själv eller andra vad koden gör. För att skapa en kommentar i Python lägger man ett # framför sin text.

```python
# Det här är en kommentar!
```

Kommentarer underlättar processen att planera, strukturera och kommunicera sin kod med sig själv eller andra, vilket i slutändan gör det lättare att skriva och förstå kod.

När man blir tilldelad en programmeringsuppgift är det ett bra hjälpmedel att kommentera hur man vill göra sin kod innan man börjar skriva den "riktiga" koden som faktiskt påverkar programmet.

Nedan visas ett exempel på hur pseudokoden kan användas för att underlätta processen av att lösa ett problem. 

```python
# Deklarera variabeln
x = 5
# Skapa loopen och låt programmet skriva ut resultatet av loopen
for i in range(5):
    print(i*x)
```
```{admonition} Notera
:class: attention
Du behöver inte förstå koden ovan, utan det är hur koden kommenteras som är det viktiga.
```
# print-satsen
När vi vill se resultatet utskrivet av en kod behöver vi använda print-satsen. När vi skriver ett program i en fil och sedan vill köra den behövs det för att se resultatet, så är inte fallet om man skriver koden direkt i en terminal.

Skapa en fil, ange vilket programmeringsspråk, skriv in koden nedan, spara filen, kör sedan koden och se resultatet!

```python
print('Hello world')
```

För att skriva text i python (som kallas för strängar) behöver man ha ett ' eller " mellan texten man skriver. Vi kommer till olika datatyper senare på den här sidan.

# Variabler och tilldelningar

En *variabel* är en en namnigven storhet  som kan ha ett värde. För att skapa en variabel så skriver vi först ett variabelnamn, sedan tilldelar vi variabeln ett värde.

```python
variabel = uttryck
```
Variabeln kan sedan användas istället för värdet. 

```python
# Deklarera variabeln och tilldela värdet
x = 5
# Visa vad värdet är
print(x)
```
I exemplet ovan har variabeln `x` först "deklarerats" och sedan "tilldelats" värdet 5. Resultatet av koden kommer då vara 5 och inte `x`. 

Det finns en rad olika fördelar med att använda variabler över att bara beräkna med olika värden direkt för det första ger det en tydligare struktur. Nedan finns det två exemplel på en kod som räknar ut hur många sekunder det går på ett år, jämför hur koden ser ut mellan de två exemplen.

### Exempel 1
```python
dagar = 365
timmar = 24
minuter = 60
sekunder = 60
print(dagar*timmar*minuter*sekunder)
```

### Exempel 2
```python
print(60*60*24*365)
```

Det som skiljer är att det första exemplet är tydligare och mer välstrukturerat. Exempel 2 kommer ge rätt svar när programmet körs, men vid större programmeringsprojekt och längre kod kommer variabler bli betydligt lättare att hålla koll på än värden som man inte riktigt vet var dem kommer från.

En annan fördel med att använda variabler är att variablers värden kan ändras.

```python
x = 5
x = x+2
x = x-1
x = x/2
print(x)
```

Svaret av körningen ovan kommer vara att `x` tilldelas värdet `5`, sen `5+2=7`, sen `7-1=6` och till sist `6/2 = 3`.

_____________________________________________

#### Fråga: Vad hade körningen visat för svar?

```python
y = 3
y = 9
y = y-4
y = y*2
print(y)
```

```{admonition} Visa svar
:class: caution dropdown
10
```

#### Fråga: Vad hade körningen visat för svar?

```python
x = 3
y = 9
print(x*y) 
```

```{admonition} Visa svar
:class: caution dropdown
27
```

## Datatyper och typkonverteringar
Beroende på vilken sorts information som ska lagras i en variabel finns det olika datatyper. Inledningsvis ska vi titta på några få datatyper, men under kursens gång kommer vi fylla på med olika datatyper som är relevanta för kursen.

```python
# Datatypen int
x = 5

# Datatypen float
y = 5.4

# Datatypen sträng
namn = 'Sigfrid'

# Datatypen list
namn_lista = ['Emil', 'Ava']
```
Variabeln `x` som deklarerades ovan och blev tilldelad värdet `5` blir av datatypen int eftersom `5` endast består av ett *heltal*. Variabeln `y` är ett så kallat *flyttal* som både har en decimaldel och den heltalsdel. Efter det ser vi en datatyp som heter "sträng" som innehåller bokstäver, ord eller meningar. Till sist har vi en lista som har många viktiga funktioner som kommer behandlas senare.

I vissa situationer kan det krävas att man går från en datatyp till en annan, detta kallas för en *typkonvertering*. Nedan listas några exempel på viktiga typkonverteringar. 

```python
# Gör från int till sträng
int_till_sträng = str(12)

# Gör från sträng till int
sträng_till_int = int('12')

# Gör från sträng till lista
sträng_till_lista = list('abc')
```

_____________________________________________
## Input-satsen
Ibland vill man inte tilldela ett statiskt värde till en variabel, utan istället kan det ibland vara bättre att fråga användaren om ett värde till variabeln (en input). Då använder vi input-satsen. Vi ska se ett exempel på hur inputsatsen kan användas.

```python
namn = input('Ange ditt namn')
print('Hej', namn, 'trevligt att träffas!')
```

Programmet ovan börjar med att fråga om en input, i det här fallet användarens namn. Efter det tilldelas variabeln värdet (namnet) och till sist anropas det i print-satsen på raden under. Det här är bara ett av många exempel på när det blir intressant att använda input för att göra sitt program mer interaktivt.

Vi ska titta på ett till exempel här nedan.

```python
sida = int(input('Ange kvadratens sidlängd'))
print(sida*sida, 'är kvadratens area')
```

Prorammet ovan frågar användaren efter en sida av en kvadrat, och svarar med en area av kvadraten. Eftersom datatypen för sidan är av typen *int* behöver koden förtydliga att inputen kommer vara av typen int. Om datatypen int inte explicit anges kommer python tolka inputen av typen sträng.

## Övningar till avsnittet
Här nedan listas flera övningar kopplad till innehållet av den här sidan, skriv din kod och se om du kan få svaret som programmet efterfrågar.

Tänk på att kommentera din kod. Tänk även på att deklarera och namnge på ett korrekt sätt för relevanta variabler för din kod.  
<!-- start-övningar -->
### Övning 1.1
Skriv ett program som hälsar på användaren. Exempelvis med orden "Hej på dig!"

```{admonition} Tips
:class: Hint dropdown
Använd print-satsen.
```

### Övning 1.2
Skriv ett program som utför additionen 5+7 och skriver ut svaret av additionen. 

```{admonition} Tips
:class: Hint dropdown
Använd additionstecknet och print-satsen.
```

### Övning 1.3
Skriv ett program som frågar efter din ålder och skriver ut hur gammal du kommer vara om 5 år.

```{admonition} Tips
:class: Hint dropdown
Använd input-satsen.
```

### Övning 1.4
Skapa en simpel miniräknare som frågar efter två nummer och sedan skriver ut vad summan, skillnaden, produkten och kvoten är mellan dessa tal.

```{admonition} Tips
:class: Hint dropdown
Börja med att använda input-satsen, deklarera variabler och tilldela värdena genom att utföra beräkningarna, använd till sist en print-sats.
```

### Övning 1.5
Skapa ett program som frågar efter en temperatur i enheten i grader Celsius och sedan skriver ut vad den temperaturen korresponderar i grader Fahrenheit. Tips formeln för konverteringen från grader Celsius till grader Fahrenheit är: 

$F= \frac{9}{5} \cdot C + 32 $

```{admonition} Tips
:class: Hint dropdown
Börja med att använda input-satsen, deklarera variabeln och tilldela värdet genom att utföra beräkningarna enligt formeln ovan, använd till sist en print-sats.
```

### Övning 1.6
Skapa ett program där programmet frågar efter en summa pengar, efter en räntesats och ett antal år. Beräkna summan av ränta på ränta på det insatta kapitalet med hjälp av en exponentialfunktion och skriv ut resultatet till användaren.

$y = C \cdot a^x $

```{admonition} Tips
:class: Hint dropdown
Börja med att använda input-satsen, deklarera variablerna och tilldela värdena genom att utföra beräkningarna enligt formeln ovan, använd till sist en print-sats.
```
<!-- end-övningar -->