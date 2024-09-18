# Funktioner

För att kunna skapa större och mer komplexa program är funktioner viktigt att använda för tydlighe, struktur och simplicitet. Funktioner kan vara lite svårt att komma igång med men de är helt nödvändiga vid större projekt.

## Skapa funktioner
För att skapa en funktion börjar man likt en variabel med att deklarera den.

```python
def namn(x, y, z):
    # Fyll  på med koden här.
```

Alltid när en ny funktion ska skapas påbörjas det med `def`, sedan kommer namnet av definitionen `namn`. Namnet väljer man helt själv med precis som för variabler så ska funktioner deklareras med rimliga och förklarande namn som passar situationen. 

Exempelvis om man vill skapa en funktion som räknar ut summan mellan två tal så skulle funktionsnamnet kunna vara `summa`. 

Efter funktionens namn kommer *parametrarna* som funktionen behöver använda för att kunna ge tillbaka ett funktionsvärde. I matematiken är vi vana med att en funktion tar ett input-värde (vanligtvis x) och sen får man funktionsvärdet som svar. En funktion i programmering fungerar på liknande sätt, funktionen tar ett antal parametrar och ger tillbaka ett funktionsvärde, i funktionen ovan är parametrarna skrivna med `x`, `y` och `z` samt separerade med ett komma mellan dem.

I exemplet tidigare om funktionen `summa` hade det varit rimligt med två parametrar för att kunna ge ett svar. Vi skulle kunna kalla parametrar för `tal1` och `tal2` inom parentesen.

I slutet kan funktionen även ge en output (alltså ett funktionsvärde) genom att ge tillbaka ett värde. Då behöver funktionen avslutas med en `return`-sats. 

För att exemplifiera hur en hel funktion ser ut ska vi skriva hur hela funktionen `summa` kan se ut.

```python
def summa(tal1, tal2):
    totalt = tal1 + tal2
    return totalt
```