# Datahantering
Under det här avsnittet ska vi gå igenom hur man kan läsa av data från textfiler, fokuset för den här kursen kommer vara att läsa av från excelfiler.

## Installera pandas
Vi ska börja med att ladda ner vissa funktioner som vi behöver för att kunna hantera textfiler och kunna göra analyser av textfiler. Vi behöver installera både `pandas` och `openpyxl` i terminalen. `pandas` är ett bibliotek av olika funktioner som används för datahantering. `openpyxl` är en inbyggd modul som är kopplad till `pandas` för att kunna läsa av specifikt excelfiler.

Börja med att skriva följande i terminalen för att få `pandas` och `openpyxl` nedladdat:

```bash
pip install pandas openpyxl
```

## Läsa av filer
För att läsa av information från en excelfil i python är det viktigt att man **skapar excelfilen i samma map som programmet**. Då kan man låta python hitta den excelfilen genom att skriva in filnamnet. Annars hittar inte python den filen. 

Skapa nu en fil i excel som du fyller i vilka kurser du läser och vilket betygspoäng som du har eller som din påhittade person har.

```{list-table}
:header-rows: 1

* - Kurs
  - Betygspoäng
* - Svenska 1
  - 12,5
* - Matematik 1c
  - 15
* - Engelska 5
  - 20
* - Fysik 1
  - 12,5
```

--- 

Om man vill räkna om ett betyg till motsvarande betyg kan man följa tabellen nedan.

```{list-table}
:header-rows: 1

* - Betyg
  - Betygspoäng
* - A
  - 20
* - B
  - 17,5
* - C
  - 15
* - D
  - 12,5
* - E
  - 10
* - F
  - 0
```

Efter att en fil är skapad är det viktigt att man vet namnet på filen, det är dessutom väldigt viktigt att man **sparar och stänger filen innan man vill köra programmet**.

För att läsa av en textfil börjar man först med att importera pandas längst upp i programmet.

```python
import pandas as pd
```

Därefter om man vill läsa av en textfil kan man den inbyggda funktionen `read_excel`.

```python
df = pd.read_excel("data.xlsx")
```

Variabeln `df` lagrar nu datan från excel i en så kallad *DataFrame*. I variabeln `df` har alla kolumner lagrats i flera olika listor. Om vi vill få åtkomst till en specifik kolumn kan vi skriva:

```python
list_kolumn = df["Kolumnnamn"]
```
Nu är all data från kolumnen `"Kolumnnamn"`nu lagrats i listan `list_kolumn`. Då kan nu hantera all data från denna kolumn genom att använda inbyggda listfunktioner.

## Projektuppgift med datahantering - Betygsprogram
Uppgiften är att bygga ett program som räknar ut ditt meritvärde på gymnasiet. Vi ska räkna ut det genom att läsa av en excelfil med betygen och sedan räkna ut meritvärdet.

#### Steg 1
Skapa excelfilen och fyll i tabellen som vi gjorde tidigare. Spara filen i samma mapp som programmet.

#### Steg 2
Importera pandas och openpyxl längst upp i programmet.

#### Steg 3
Läs av filen och spara informationen i ett DataFrame som heter `df`.

#### Steg 4
Skapa funktionen `def poäng(betyg):` som tar en lista med betyg som bokstav och räknar om det från en bokstav till ett poäng enligt tabellen som beskrevs längre upp. Returnerar poängen.

#### Steg 5
Skapa funktionen `def merit(betygspoäng, meritpoäng):` som tar alla betyg samt meritpoängen och returnerar eritvärdet.

#### Steg 6
Testa att ändra betygen och se om du kan räkna ut meritvärdet genom att anropa funktionen `merit`. 

#### Steg 7
Gå till [studera.nu](https://studera.nu) och titta upp några utbildningar som du vill läsa. Skapa två nya kolumner i excelfilen "Program" och "Meritvärde". I kolumnen program fyller du i vilka program som du vill läsa. I kolumnen meritvärde fyller du i meritvärdet som krävs för att komma in på utbildningen. 

Titta i tabellen nedan som inspiration för hur ni ska fylla i excelfilen.

```{list-table}
:header-rows: 1

* - Program
  - Meritvärde
* - Läkarprogrammet
  - 20
* - Sjuksköterskaprogrammet
  - 12,5
* - Ämneslärarprogrammet
  - 10
* - Veterinärprogrammet
  - 21,5
* - Socionomprogrammet
  - 15
* - Ekonomprogrammet
  - 16
```

#### Steg 8
Skapa en funktion `def antagen(betyg, krav)` som tar ditt meritvärde och en lisa över betygskraven. Funktionen returnerar vilka utbildningar som du kommer in på.

## Projektuppgift med datahantering - Matkort
Uppgiften är att göra ett program som håller koll på hur mycket du kan spendera på ditt matkort.

#### Steg 1
Skapa filen `maktort.py` i din lokala map på skrivbordet.

#### Steg 2
Skapa ett exceldokument som kallas `matkort.xlsx`. Fyll i kolumnerna med `Dag` och `Kronor`. Fyll i alla dagar du har varit i skolan den här månaden, fyll i datumen. Fyll sedan i andra kolumnen hur mycket som du spenderade den dagen på ditt matkort. Titta på exemplet nedan. Spara filen i samma mapp som programmet.

```{list-table}
:header-rows: 1

* - Dag
  - Kronor
* - Måndag 4/11
  - 70
* - Tisdag 5/11
  - 85
* - Torsdag 7/11
  - 65
* - Fredag 8/11
  - 50
* - Måndag 11/11
  - 70
* - Tisdag 12/11
  - 80
```

#### Steg 3
Importera pandas och openpyxl längst upp i programmet.

#### Steg 4
Läs av filen och spara informationen i ett DataFrame som heter `df`.

#### Steg 5
Skapa funktionen `def saldo(dagar, kronor):` som tar en lista med alla kronor som du har spenderat den månaden. Den tar även mot en ett värde på hur många skoldagar det är den månaden. Funktionen ska returnera hur mycket pengar du har kvar på ditt matkort. Följ formeln nedan för att veta vad saldot är.

$saldo= 70 \cdot antalskoldagar - spenderat$

Saldo betyder hur mycket som finns kvar på kortet, antal dagar betyder hur många skoldagar som månaden består av, spenderat betyder summan av alla kostnader som finns i listan över kronor.

För att anropa den här funktionen behöver du skapa två variabler längst ner i programmet, nämligen en variabel som heter `skoldagar` som är antalet skoldagar, samt en variabel som heter `kronor_lista` som är en lista över alla tal i kronorkolumnen i excelfilen.

#### Steg 6
Skapa en funktion `def spendera(kronor, pengar_kvar)` som tar listan över alla kronor, samt vad saldot är. Funktionen ska returnera hur mycket du ska spendera i snitt varje dag till starten av nästa månad.

För att anropa den här funktionen behöver du ge funktionen listan `kronor_lista`samt saldot i form av en lokal variabel där du anropar `saldo`-funktionen.

#### Steg 7
Testa att ändra i excelfilen och se om allting stämmer.

#### Steg 8
Skapa en funktion `def main()`. Mainfunktionen ska vi göra för att det blir med pedagogiskt och enklare att använda programmet. Börja med att skapa funktionen och kopiera följande kod:

```python
def main():
  print("Klicka 1 om du vill kolla saldot")
  print("Klicka 2 om du vill kolla hur mycket du ska spendera i snitt varje dag resten av månaden")
  print("Klicka 3 om du vill avsluta programmet")
```

#### Steg 9
Fyll sedan på funktionen så att om användaren anger `1` som input ska programmet visa saldot.

#### Steg 10
Om användaren anger `2` ska programmet visa hur mycket du ska spendera i snitt varje dag resten av månaden.

#### Steg 11
När du anger `3` ska programmet avsluta programmet. Använd då bara att om `3` anges så returneras ingenting.

#### Steg 12
När du får ett svar från `main` funktionen, kör om mainfunktionen så du kan fortsätta programmet.

#### Steg 13
Anropa mainfunktionen längst ner i programmet.
