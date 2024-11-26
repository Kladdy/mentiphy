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

Skriv en funktion som tar in ett lexikon och returnerar en lista med alla värden i lexikonet.

```{admonition} Tips
:class: Hint dropdown

Du kan skapa en tom lista och loopa igenom alla värden i lexikonet och tilldela dem till listan.

```

### Övning 6.2

Skriv en funktion som tar in ett lexikon och returnerar en lista med alla nycklar i lexikonet.

```{admonition} Tips
:class: Hint dropdown

Du kan skapa en tom lista och loopa igenom alla nycklar i lexikonet och tilldela dem till listan.

```

### Övning 6.3

Skriv en funktion som tar in ett lexikon och en nyckel och returnerar värdena i lexikonet under den nyckeln.

```{admonition} Tips
:class: Hint dropdown

Du kan skapa en tom lista och loopa igenom alla nycklar i lexikonet och tilldela dem till listan.

```

<!-- end-övningar -->


