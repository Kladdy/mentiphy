---
jupytext:
    formats: md:myst
    text_representation:
        extension: .md
        format_name: myst
kernelspec:
    display_name: Python 3 (ipykernel)
    language: python
    name: python3
---

# Elektricitet

Man har länge klarat sig utan elektricitet, men idag är samhället beroende av elektriciteten. Bara för att klara vår morgonrutin behövs elektricitet - larmet från mobilen, brödet vi rostar i brödrosten, osten och skinkan vi tar ur kylskåpet, värmen i huset, ja allt det kräver elektricitet. 

_____________________________________________

## Laddningar

### Atomens laddning

Elektricitet finns naturligt, bland annat i atomer. En atom består av mindre partiklar som är *elektriskt laddade*. 

```{image} img/Atomen.png
:alt: En atom med protoner (röda), neutroner (vita) och elektroner (blåa).
```

I figuren här syn en atom. I varje atom finns en *atomkärna* som består av protoner (röda) och neutroner (vita). Atomkärnan är positivt laddad, eftersom protonerna har positiv laddning och neutronerna är oladdade. Runt atomkärnan kretsar elektroner (blåa) som är negativt laddade. 

```{admonition} Varning
:class: danger
Protonerna, elektronerna och neutronerna är inte röda, blåa eller vita i verkligheten, utan det är bara i illustrationssyfte!
```

Atomen är neutral. Antalet protoner, elektroner och neutroner i en atom påverkar vilket ämne det är. I bilden ovanför är det en heliumatom, eftersom den har två protoner och två elektroner. I atomerna finns det lika många protoner som elektroner, och atomens laddning blir därför neutral. 

_____________________________________________

### Statisk elektricitet

Om man gnider en ballong mot håret och sedan lyfter bort den kommer håret vilja följa med. För att förstå *varför* det sker måste vi igen titta på bilden på atomen ovan. Statisk elektricitet kan kanske enklast förklaras med hjälp av att vi gnuggar en ballong mot håret. När vi sedan lyfter bort ballongen kommer håret vilja följa med, och det beror på statisk elektricitet! Videon här förklarar varför det är så:

<iframe
    width="100%"
    max-width="800"
    height="450"
    src="https://www.youtube.com/embed/BxC-Kmf_qAs"
    frameborder="0"
    allow="autoplay; encrypted-media"
    allowfullscreen
>
</iframe>

Elektronerna "hoppar" alltså från håret till ballongen och skapar en laddningsskillnad mellan dem (håret blir positivt laddat eftersom det finns fler protoner än neutroner, ballongen blir negativt laddad eftersom det finns fler elektroner än protoner). 

Olika laddningar dras alltså mot varandra, medan lika laddningar dras ifrån varandra. Vill du veta mer, klicka <a href='https://mentiphy.se/kurser/fysik-1/elektricitet.html#laddningar'>här</a>. 

_____________________________________________

### Åska

yeye

_____________________________________________

### Uppgifter

1. Fråga?

```{admonition} Visa svar
:class: caution dropdown
Svar
```

_____________________________________________

### Spel

Här nedan finns ett spel från PhET Interactive Simulations (som ges ut av University of Colorado). Här kan du prova gnugga en ballong mot en stickad tröja. Vilka är elektronerna? Hur beter de sig när du gnuggar ballongen mot tröjan? Vad händer om du släpper ballongen en bit ifrån tröjan? Vad beror det på?

<div>
   <iframe src="https://phet.colorado.edu/sims/html/balloons-and-static-electricity/latest/balloons-and-static-electricity_en.html"
        width="100%"
        max-width="800"
        height="450"
        allowfullscreen>
    </iframe>
</div>

_____________________________________________

## Quiz

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
display_quiz("quiz/elektricitet.json", shuffle_answers=True, shuffle_questions=True)
```
