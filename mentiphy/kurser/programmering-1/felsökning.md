# Felsökning
Under det här avsnittet kommer övningar där ni får en kod presenterad och ska försöka förbättra koden eller förklara vad som är fel med koden.

## Uppgiftstyper
Avsnittet erbjuder två olika sorters frågor, som vi kallarresonemangsuppgifter och felsökningsuppgifter. 

### Resonemangsuppgifter
Börja med att endast titta på koden och försök hitta vad problemet är, att kunna se felen utan att behöva skriva någon kod är bra träning. Börja med att titta på tipset innnan du tittar på lösningen.

### Felsökningsuppgifter
Kopiera koden till Visual Studio Code och ändra koden så programmet stämmer. Börja med att titta på tipset innnan du tittar på lösningen.

## Uppgifter
### Kontrollera om ett tal är jämnt (Resonera)
Denna funktion ska kontrollera om ett tal är jämnt, men den ger inte rätt resultat. Vad är felet?

```python
def is_even(number):
    if number % 2 = 0:
        return True
    else:
        return False
```

```{admonition} Tips
:class: Hint dropdown
Titta noga på `if-satsen`.
```

```{admonition} Lösning
:class: Caution dropdown
Felet är att `number % 2 = 0` för att åndra till `number % 2 == 0`.
```

### Summera alla tal i en lista (Resonera) (1)
Koden nedan är tänkt att summera alla tal i en lista, men den fungerar inte som förväntat. Vad är problemet?

```python
def sum_numbers(numbers):
    total = 0
    for i in range(len(numbers)):
        total = total + i
    return total
```

```{admonition} Tips
:class: Hint dropdown

I loopen används indexet `i` i stället för att hämta värdet på varje position i listan.
```

```{admonition} Lösning
:class: Caution dropdown

Felet är att `i` i loopen representerar indexet i listan, inte själva värdet. Du bör istället skriva `total += numbers[i]`.
```

### Summera alla talen i en lista (Resonera) (2)
Den här funktionen ska summera alla tal i en lista, men den fungerar inte som förväntat. Vad är problemet?

```python
def sum_list(numbers):
    total = 0
    for number in numbers:
        total = number
    return total
```

```{admonition} Tips
:class: Hint dropdown
Titta på vad som händer med variabeln `total` i loopen. Hur påverkas summan av att den sätts till ett nytt värde varje gång?
```

```{admonition} Lösning
:class: Caution dropdown
Felet är att `total = number` gör att värdet av `total` alltid skrivs över med det senaste talet i listan, istället för att addera det till den befintliga summan. Ändra till `total += number` för att löpande lägga till varje tal till summan.
```

### Skriv ut alla element i en lista (Felsök)
Koden nedan ska skriva ut varje element i en lista, men den fungerar inte som den ska. Felsök och rätta koden.

```python
def print_list_elements(my_list):
    for i in range(len(my_list)):
        print(my_list[i+1])

print_list_elements([1, 2, 3, 4])
```

```{admonition} Tips
:class: Hint dropdown
Tänk på hur indexering fungerar i listor och att indexet kan hamna utanför gränserna för listan.
```

```{admonition} Lösning
:class: Caution dropdown
Felet är att `i+1` gör att du börjar på andra elementet och slutligen försöker gå utanför listans gränser. Ändra till: `print(my_list[i])`

```

### Returnera det första elementet i en lista (Felsök)
Funktionen nedan ska returnera det första elementet i en lista, men den returnerar inget alls. Vad är felet?

```python
def first_element(my_list):
    my_list[0]
```

```{admonition} Tips
:class: Hint dropdown
Tänk på vad som krävs för att faktiskt returnera ett värde från en funktion.
```

```{admonition} Lösning
:class: Caution dropdown
Felet är att du aldrig använder `return` för att skicka tillbaka resultatet. Lägg till `return` framför `my_list[0]`:
```


---

### Summera alla element i en lista (Felsök)
Denna kod ska summera alla element i en lista, men den ger alltid fel svar. Rätta koden så att den fungerar korrekt.

```python
def sum_list(my_list):
    total = 0
    for i in range(1, len(my_list)):
        total += my_list[i]
    return total

print(sum_list([1, 2, 3, 4]))  # Förväntat resultat: 10
```

```{admonition} Tips
:class: Hint dropdown
Kontrollera från vilket index loopen börjar.
```

```{admonition} Lösning
:class: Caution dropdown
Felet är att loopen börjar vid index 1 istället för 0, vilket gör att det första elementet aldrig inkluderas i summan. Ändra loopen till att börja vid index 0: `for i in range(0, len(my_list))`
```


---

### Kontrollera om ett tal är större än 10 (Felsök)
Koden ska kontrollera om ett tal är större än 10, men den returnerar alltid fel resultat. Felsök och förbättra koden.

```python
def is_greater_than_ten(number):
    if number > 10:
        return False
    else:
        return True
```

```{admonition} Tips
:class: Hint dropdown
Se över vad som returneras i varje fall i `if-else`-satsen.
```

```{admonition} Lösning
:class: Caution dropdown
Logiken i `if-else`-satsen är omvänd. Funktionen returnerar `False` när talet är större än 10, men det borde vara tvärtom. Korrigera returnvärdena så här:
`if number > 10:` `return True` `else:` `return False`.
```




