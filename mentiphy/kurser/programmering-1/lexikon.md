# Lexikon

Under den här fliken kommer vi fördjupa oss i en ny datatyp som heter lexikon. Lexikon används för att lagra mer sofistikerad information än en lista. Exempelvis kan vi ha ett särskilt objekt i en lista (kallad nyckel) och för den nyckeln tilldelar vi olika värden.

## Defininera ett lexikon

Exempelvis om vi skulle göra ett lexikon över en inköpslista så skrivs det på följande sätt.

```python

inköpslista = {'äpplen': 15, 'apelsin': 10, 'banan': 10, 'paprika': 25} 
    
```

I exemplet ovan skapar vi ett lexikon och tilldelar nyckel och värde. Det finns även andra situationer där vi har olika nycklar som vi vill tilldela fler än ett värde.

Nedan visas ett exempel på hur man kan använda ett lexikon för att hålla reda på olika böcker under olika kategorier.

```python
bibliotek = {'Skräck': ['It', 'Dracula'], 'Drama': ['Frankenstein', 'The Shining'], 'Fantasy': ['The Lord of the Rings', 'The Hobbit']}
```

I exemplet ovan skapar vi ett lexikon som innehåller olika nycklar, i det här fallet kategorier. Under kategorierna blir det i det här fallet en lista som är värdet som är tilldelat till listan. 

Vi vet från tidigare att listor är smidiga att använda för att de är lätta att redigera. Exempelvis att lägga till fler värden, att ta bort ett värde, eller att hitta ett specfikt värde i listan.

## Användning av lexikon

För att exemplifiera hur ett ett lexikon kan användas och varför det är smidigt ska vi ska återkomma till exemplet med vår `inköpslista`.

#### Översikt av lexikonet

Vi börjar med att vilja se alla nycklar vi har i vårt lexikon, då skriver vi följande:

```python

print(inköpslista.keys())

```

Om vi vill se alla värden för alla nycklar i lexikonet skriver vi:

```python

print(inköpslista.values())

```

#### Åtkomst till nycklar och värden

Säg att vi vill veta se värdet av en nyckel i ett lexikon, då skriver vi på följande sätt:

```python

print(inköpslista['apelsin'])

```

#### Ändra värden på nycklar
Det ger oss `apelsin`-nyckelns nuvarande värde, vilket är 10. Säg att vi skulle vilja redigera det värdet. Då skriver vi:

```python

inköpslista['apelsin'] = 25
print(inköpslista['apelsin'])

```

Nu har vi tilldelat värdet på `apelsin` till 25. 

#### Lägg till fler nycklar

Vi kan nu välja att vilja lägga till en till nyckel till vårt lexikon. Då skriver vi:

```python

inköpslista['anannas'] = 20
print(inköpslista)

```

#### Ta bort nycklar

Vi kan nu välja att vilja ta bort ett nyckel från lexikonet. Då skriver vi:

```python

inköpslista.pop('banan')
print(inköpslista)
```

#### Loopar och lexikon

Vi kan nu återkomma till exempelvis att vi vill loopa igenom alla nycklar i lexikonet. Då skriver vi:

```python

for nyckel in inköpslista.keys():
    print(nyckel)

```

Om vi vill loopa igenom alla värden i lexikonet skriver vi:

```python

for värde in inköpslista.values():
    print(värde)

```

## Övningar till avsnittet

<!-- start-övningar -->
### Övning 6.1

Skapa ett program som tar in ett lexikon med matvaror och deras kostnad, programmet skriver ut alla priser.

```{admonition} Tips
:class: Hint dropdown

Använd en for-loop, ta inspiration längre upp på fliken från "Loopar och lexikon".

```

### Övning 6.2

Använd samma lexikon som från övning 6.1 för att skriva ut alla nycklar (matvaror) i lexikonet.

```{admonition} Tips
:class: Hint dropdown

Använd en for-loop, ta inspiration längre upp på fliken från "Loopar och lexikon".

```

### Övning 6.3

Skapa en funktion som tar en lista med namn som indata och returnerar en dictionary där varje namn är en nyckel och värdet är längden på namnet.

```{admonition} Tips
:class: Hint dropdown  

Tänk på hur du kan iterera över en lista och lägga till nyckel-värde-par i en dictionary. Du kan använda en tom dictionary och fylla på den med `dict[key] = value`.

```

### Övning 6.4

Skapa en funktion som tar en lista med ord och returnerar en dictionary där varje ord är en nyckel och värdet är hur många gånger ordet förekommer i listan.


```{admonition} Tips
:class: Hint dropdown

Använd en dictionary för att hålla reda på antalet förekomster. Du kan använda `if key in dict:` för att kontrollera om nyckeln redan finns.

```
<!-- end-övningar -->

<!-- start-projekt -->

## Projekt med lexikon

I det här projektet ska vi skapa ett program som håller reda på filmer och hur dem betygssätts.

#### Steg 1
Skapa ett exceldokument med följande struktur:

```{list-table}
:header-rows: 1

* - Film
  - Betyg
* - The Shawshank Redemption
  - 9.3
* - The Godfather
  - 9.2
* - The Dark Knight
  - 9
* - Pulp Fiction
  - 8.9
* - Schindler's List
  - 8.9
* - The Lord of the Rings
  - 8.8
```

#### Steg 2
Skapa en funktion som tar en excelfil som input och returnerar en dataframe med informationen.

#### Steg 3
Skapa en funktion som tar ditt dataframe som sedan skapar ett lexikon med filmnamnen som nycklar och betygen som värden. Funktionen returnerar lexikonet.

#### Steg 4
Skapa en funktion som lägger till en ny film till lexikonet.

#### Steg 5
Skapa en funktion som hittar det högsta betyget och returnerar vilken film som har det högsta betyget.

#### Steg 6
Skapa en funktion som hittar det lägsta betyget och returnerar vilken film som har det lägsta betyget.

#### Steg 7
Skapa ett funktion som beräknar medelbetyget och returnerar det.

#### Steg 8
Skapa en mainfunktion som du kan använda för att anropa alla olika funktioner.

<!-- end-projekt -->