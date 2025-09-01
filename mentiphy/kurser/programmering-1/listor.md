# Listor
En svaghet för de variablerna vi än så länge har introducerat är att vi endast kan lagra ett värde per variabel, vilket inte alltid är det vi vill. En listor kan laga fler värden i samma variabel. Nedan följer ett exempel på när en lista kan användas för att lösa helt nya sorters problem.

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

## Videogenomgång

Genomgången på listor är i början av videon fram till ungefär 11:30, sedan kommer nästa genomgång.

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

<!-- start-övningar -->
### Övning 3.1
Skapa ett program där en lista med dina fyra favoritfrukter är inkluderade i en lista. Skriv sedan ut den första och den sista frukten i listan.
```{admonition} Tips
:class: Hint dropdown
Använd `[]` efter listan för att få åtkomst till olika element inom listan, `[-1]` indikerar det sista elementet i listan.
```

### Övning 3.2
Skapa ett program som frågar efter två listor som input och som sen skriver ut båda listorna tillsammans i en lista. 
```{admonition} Tips
:class: Hint dropdown
Använd +-operatorn för att lägga ihop två listor.
```

### Övning 3.3
Skapa ett program som innehåller 12 siffror. Skriv sedan ut varannat element i listan, var tredje element i listan och var fjärde element i listan.

```{admonition} Tips
:class: Hint dropdown
Använd skivningsoperatorerna.
```

### Övning 3.4
Skriv ett program som tar en mening från användaren, exempelvis: 

```
Det här är en mening.
```

Dela upp meningen i en lista där varje ord är ett element. Skriv sedan ut listan.

```{admonition} Tips
:class: Hint dropdown
Använd metoden `split()` för att dela upp en text i ord.
```

### Övning 3.5
Skapa ett program som innehåller en lista med minst 10 heltal. Låt programmet sortera listan i:
- Stigande ordning
- Fallande ordning

Skriv ut resultaten.

```{admonition} Tips
:class: Hint dropdown
Metoden `sort()`, om du vill ha den i andra ordningen använd `sort(reverse=True)`.
```

### Övning 3.6
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

### Övning 3.7
Låt användaren skriva in en mening. Skriv ett program som:
- Räknar antalet ord i meningen
- Hittar det längsta ordet
- Hittar det kortaste ordet

Skriv ut resultaten.

```{admonition} Tips
:class: Hint dropdown
Du kan använda metoder som `split()` och funktioner som `max()` och `min()`.
```

### Övning 3.8
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

### Övning 3.9

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

## Lösningar till övningar
Uppdaterad video kommer!