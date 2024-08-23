# Grundläggande programmering i Python

För att börja att programmera i Python finns det vissa grundläggande kod och färdigheter som är bra att börja med.

## Kommentarer
Vi ska börja med någonting som är mycket viktigt, men inte påverkar utfallet av koden, nämligen kommentarer ibland kallat psuedokod. Kommentarer underlättar  m många också säger används för att kommunicera med sig själv eller andra vad koden gör. För att skapa en kommentar i Python lägger man ett # framför sin text.

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
```{admonition} Programmering 1
:class: attention
Du behöver inte förstå koden ovan, utan det är hur koden kommenteras som är det viktiga.
```
# print-satsen
När vi vill se resultatet utskrivet av en kod behöver vi använda print-satsen. När vi skriver ett program i en fil och sedan vill köra den behövs det för att se resultatet, så är inte fallet om man skriver koden direkt i en terminal.

Skapa en fil, ange vilket programmeringsspråk, skriv in koden nedan, spara filen, kör sedan koden och se resultatet!

```python
print('Hello world')
```
