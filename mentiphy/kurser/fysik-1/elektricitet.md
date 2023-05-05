# Elektricitet

## Laddningar

*Elektrisk laddning* är en fysikalisk storhet som betecknas $Q$ och har enheten *coulomb* (C). 

Laddningar är helt enkelt laddade partiklar. De kan antingen vara positiva eller negativa, vilka är varandras motsatser. För varje partikel som finns i vår natur finns det, så viss vi vet, en *antipartikel* som har motsatt laddning.

_____________________________________________

Atomen är uppbyggd av laddade partiklar. En atom består av en kärna med positiva laddningar och kring kärnan rör sig negativa laddningar. De positivt laddade partiklarna kallas *protoner* och de negativt laddade kallas *elektroner*. En video om atomens uppbyggnad finns i avsnittet om <a href='https://mentiphy.se/kurser/fysik-9/materia.html#atomer-och-molekyler'>atomer och molekyler</a> för fysik i årskurs 9.

Atomer är i sin grundform neutralt laddade (de har lika många protoner som elektroner). Laddade atomer beror på ett *överskott* (negativt laddade) eller *underskott* (positivt laddade) av elektroner. En elektrons laddning kallas *elementarladdningen* och har storleken $1,602\cdot10^{-19}C$.

```{admonition} Kom ihåg
:class: attention
* Laddning betecknas $Q$ och har enheten coulomb (C).
* Elektroner är negativt laddade och protoner är positivt laddade.
* Elektrisk laddning beror på ett överskott eller underskott av elektroner.
* En elektrons laddning kallas för elementarladdningen.
```

_____________________________________________

Om två partiklar har lika laddning *repellerar* de (stöter bort) varandra. Om två partiklar har olika laddning *attraherar* de (dras mot) varandra.

Videon visar det:

<iframe
    width="100%"
    max-width="800"
    height="450"
    src="https://www.youtube.com/embed/yeSEiQTNxybdM"
    frameborder="0"
    allow="autoplay; encrypted-media"
    allowfullscreen
>
</iframe>

Om ett föremål är negativt laddat (överskott av elektroner) kommer överskottselektronerna repellera varandra så mycket de kan (lika laddningar repellerar) och därför spridas jämnt över föremålets yta. På så vis blir ett föremål lika laddat överallt, vilket kallas **elektrostatisk jämvikt**. På samma vis kommer en positiv laddning spridas jämnt.

<!-- _____________________________________________

ye influens? -->

_____________________________________________

### Coulombs lag

För att de här laddningarna ska kunna repellera och attrahera varandra krävs det en *kraft*. Båda laddningarna kommer påverka varandra med en lika stor kraft fast i motsatt riktning. De är varandras *motkrafter*, vilket vi kommer ihåg stämmer väl ihop med Newtons tredje lag. Eftersom de två krafterna antingen är riktade mot varandra eller från varandra så behöver vi bara veta storleken på kraften, och den kan vi få från Coulombs lag:

$$ F = k \cdot \frac{|Q_1 \cdot Q_2|}{r^2} $$

där $k$ är en konstant, ($k = \frac{1}{4\pi \epsilon_0} = 8,99 \cdot 10^9 Nm^2/C^2$), $Q_1$ och $Q_2$ är laddningarnas storlek i coulomb (C) och $r$ är avståndet mellan laddningarna.

_____________________________________________

### Experiment

Ta en ballong och gnid den i håret ett tag innan du släpper. Ballongen kommer då sitta kvar i håret! Varför det?

```{admonition} Visa svar
:class: caution dropdown
Det beror på att elektroner skrapas av från håret när du gnider ballongen mot det, vilket gör att håret blir positivt laddat (underskott på elektroner) och ballongen blir negativt laddad (överskott på elektroner). Därför attraherar de varandra!
```

_____________________________________________

### Uppgifter

1. Vad innebär det att två laddningar repellerar eller attraherar varandra? För vilka laddningar gäller det?

```{admonition} Visa svar
:class: caution dropdown
Två lika laddningar kommer repellera varandra, alltså stöta bort varandra, medan två olika laddningar kommer attrahera varandra, alltså dras mot varandra.
```

2. Vad innebär det att någonting har ett "överskott av elektroner"?

```{admonition} Visa svar
:class: caution dropdown
Det "någonting" är då negativt laddat eftersom det finns fler elektroner än protoner.
```

3. Vad är elementarladdningen?

```{admonition} Visa svar
:class: caution dropdown
Den laddning en elektron har, alltså $1,602\cdot10^{-19}C$.
```

4. Två laddningar, $Q_1$ och $Q_2$ befinner sig 20 cm ifrån varandra. $Q_1$ har laddningen +8,0 nC och $Q_2$ har laddningen -10,0 nC. Åt vilket håll är krafterna som de verkar på varandra med riktade? Hur stora är de?

```{admonition} Visa svar
:class: caution dropdown
Eftersom $Q_1$ är en positiv laddning och $Q_2$ är en negativ laddning kommer de attrahera varandra. Krafterna är alltså riktade mot varandra. 

Storleken ges sedan av Coulombs lag. Vi räknar först om alla värden från uppgiften till rätt enheter:

* $Q_1 = 8,0 nC = 8,0 \cdot 10^{-9} C$
* $Q_2 = -10,0 nC = -10,0 \cdot 10^{-9} C$
* $r = 20 cm = 0,2 m$
* $k = 8,99 \cdot 10^9 Nm^2/C^2$

Sätter vi in det i Coulombs lag får vi svaret för båda krafterna (eftersom de är lika stora!):

$$ F = k \cdot \frac{|Q_1 \cdot Q_2|}{r^2} = 8,99 \cdot 10^9 \cdot \frac{|8,0 \cdot 10^{-9} \cdot (-10,0 \cdot 10^{-9})|}{0,2^2} \approx 1,8 \cdot 10^{-5} N = 18 \mu N$$ 

Krafterna har ungefär storlekarna $18\mu N$.
```

5. En kula med massan 0,3 gram svävar i luften på grund av att den attraheras uppåt av ett stort metallklot med laddningen $2,0\mu C$ och nedåt av jordens dragningskraft. Kulan är 0,20 meter från metallklotet. Vad är kulans laddning?

```{admonition} Visa svar
:class: caution dropdown
Den elektriska kraften, $F_E$, måste vara lika stor som dragningskraften, $F_g$, eftersom kulan är stilla. Detta ger $F_E=F_g$, vilket enligt Newtons andra lag ($F=ma$) och Coulombs lag är samma sak som

$$k \frac{|Q_1\cdot Q_2|}{r^2}=mg$$

Vi söker kulans laddning. Vi väljer kulans laddning till $Q_1$ och klotets till $Q_2$, och bryter sedan ut $Q_1$ eftersom det är denne vi söker. Detta ger 
       
$$Q_1 = \frac{mgr^2}{kQ_2}$$
      
Vi sätter sedan in värdena från uppgiften med deras omvandlade enheter:

* $m = 0,3g=0,3 \cdot 10^{-3}kg$
* $g = 9,82 m/s^2$
* $r=0,2 m$
* $k = 8,99 \cdot 10^9 Nm^2/C^2$
* $Q_1 = 2,0\mu C = 2,0 \cdot 10^{-6} C$

och beräknar $Q_1$

$$Q_1 = \frac{0,3 \cdot 10^{-3} \cdot 9,82 \cdot 0,20^2}{8,99 \cdot 10^9 \cdot 2,0 \cdot 10^{-6}} \approx 6,6 \cdot 10^{-9} C $$

Svaret blir alltså att kulans laddning är $6,6nC$
```

6. Förklara både matematiskt (utifrån Coulombs lag) och fysikaliskt varför kraften som $Q_1$ verkar på $Q_2$ med är lika stor som kraften som $Q_2$ verkar på $Q_1$ med är.

```{admonition} Visa svar
:class: caution dropdown
Matematiskt: 

Enligt Coulombs lag kan vi säga att ena kraften beräknas med hjälp av $ F_1 = k \cdot \frac{|Q_1 \cdot Q_2|}{r^2} $ och att den andra kraften beräknas med hjälp av $ F_2 = k \cdot \frac{|Q_2 \cdot Q_1|}{r^2} $. Eftersom $Q_1 \cdot Q_2 = Q_2 \cdot Q_1|$ (multiplikation är kommutativt) så kommer storleken på krafterna att bli samma (även om riktningarna är olika). 

Fysikaliskt:

Newtons tredje lag säger att för varje kraft som verkar på en kropp, finns det en lika stor och motriktad kraft som verkar tillbaka på den kroppen. När två laddningar interagerar med varandra genom elektrostatisk kraft så är den kraft som den ena laddningen verkar på den andra med alltså precis lika stor som den kraft som den andra laddningen verkar på den första med, men riktad i motsatt riktning.
```

_____________________________________________

### Spel

Här nedan finns ett spel från PhET Interactive Simulations (som ges ut av University of Colorado). Välj "Macro Scale" i första läget. Prova att ändra storleken på laddningarna och avståndet mellan dem. Vad händer med krafterna? 

<div>
   <iframe src="https://phet.colorado.edu/sims/html/coulombs-law/latest/coulombs-law_en.html"
        width="100%"
        max-width="800"
        height="450"
        allowfullscreen>
    </iframe>
</div>

_____________________________________________

## Ledare och isolatorer

Saker som leder ström bra kallas **ledare**. De flesta metaller är bra ledare, exempelvis koppar, silver, guld, aluminium och järn. Det beror på att de har fria elektroner som kan förflytta sig, vilket gör att de leder elektrisk ström. 

Kablar kan exempelvis vara av koppar.

_____________________________________________

Motsatsen till ledare kallas **isolatorer**, vilket är saker som (nästan) inte leder någon ström alls. Exempel på isolatorer är plast, glas, gummi och keramik. De är bra isolatorer eftersom de har inga, eller nästan inga, fria elektroner. Molekylerna håller hårt i alla elektroner, vilket gör att de inte leder elektrisk ström. 

Som tidigare nämnt kan kablar vara av koppar. Den elektriska ledaren i en kabel är omsluten av en isolator, så som gummi, vilket gör att vi kan hålla i kabeln även om det finns ström i den.

_____________________________________________

En **halvledare** är som namnet antyder någonting vars ledningsförmåga är mellan en ledares och en isolators. Det beror på att halvledarens molekylers valensskal är halvfyllda. Halvledare leder elektricitet när de är uppvärmda till en viss temperatur, men är annars isolatorer. Två exempel är kisel och germanium som används mycket i datorteknik.

_____________________________________________

**Supraledare** är material som tillåter att strömmen passerar utan någon resistans (motstånd). Två exempel på supraledare är bly och tenn (vid mycket låga temperaturer). Supraledare är användbara för att exempelvis skapa mycket starka elektromagneter som används i magnetkameror och partikelacceleratorer.

_____________________________________________

## Elektriska fält

happy guy