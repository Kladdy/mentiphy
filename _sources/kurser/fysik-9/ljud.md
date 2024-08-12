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

# Ljud

## Vad är ljud?

Vad är egentligen ljud? Jo, ljud är vibrationer. Tänk på en gitarrsträng, när du slår den så vibrerar den - och låter! Svårare än så är det inte.

```{admonition} Kom ihåg
:class: attention
Ljund är *vibrationer*.
```

För att de här vibrationerna ska nå våra öron krävs någonting för ljudet att färdas i. Vanligtvis är det luften, där de här vibrationerna sprider sig på samma vis som om du skulle slänga en sten i en blank sjö. 

<iframe
    width="100%"
    max-width="800"
    height="450"
    src="https://www.youtube.com/embed/Bl5HH31U6v0"
    frameborder="0"
    allow="autoplay; encrypted-media"
    allowfullscreen
>
</iframe>

Ljudet kan också färdas i andra ämnen, som exempelvis vatten eller metall. Beroende på hur tätt ämnet är så färdas ljudet olika fort. 

```{admonition} Tips
:class: hint
Jämför ljudhastigheten med dominobrickor! Om du ställer dem tätt (har ett tätt ämne som metall) kommer de falla snabbare (ljudet färdas fortare) jämfört med om du sätller dem med så långt avstånd som möjligt mellan varandra (ett ämne med låg täthet, som luft).
```

Ljudhastigheten i luft kan uppskattas till ungefär 340 m/s, medan ljudhastigheten i vatten är ungefär 1500 m/s och i metall är den över 5000 m/s! 

```{admonition} Tips
:class: hint
Eftersom vi vet att ljudet färdas ungefär 1 km på 3 sekunder ($340 m/s \cdot 3 s \approx 1 km$) så vet vi att blixten är ungefär 1 km längre bort för varje gång vi kan räkna till 3 från att vi ser blixten tills att vi hör den.
```

_____________________________________________

## Frekvens och amplitud

### Frekvens

Ovan står det att ljud är vibrationer. Ljudet kan vibrera olika fort - vilket vi kan mäta! Det gör vi genom att mäta antalet svängningar per sekund.

Det här måttet är centralt inom fysiken, och kallas för **frekvens**. Frekvens är en *storhet* (precis som massa eller längd) och har därför en enhet - *hertz* som förkortas *Hz* (precis som att kg är enheter för massa eller m är enheten för längd).

```{admonition} Kom ihåg
:class: attention
Frekvens betyder antalet svängningar per sekund och mäts i hertz (Hz).
```

Om en gitarrsträng vibrerar med frekvensen 440 Hz så vibrerar strängen fram och tillbaka 440 gånger på en sekund.

<iframe
    width="100%"
    max-width="800"
    height="450"
    src="https://www.youtube.com/embed/Q5WdMT2Jf2I"
    frameborder="0"
    allow="autoplay; encrypted-media"
    allowfullscreen
>
</iframe>

Det finns vissa ljud vi inte hör, som exempelvis ultra- eller infraljud. Det berättar vi mer om klicka <a href='https://mentiphy.se/kurser/fysik-9/ljud.html#infraljud-och-ultraljud>här</a>. 

_____________________________________________

### Amplitud

ye

_____________________________________________

### Toner

ye

_____________________________________________

## Resonans

ye

_____________________________________________

## Vår hörsel

Ljudet består som tidigare nämnt av vibrationer, som kan färdas genom luften. När vibrationerna når fram till våra inneröron orsakas tryckförändringar. Dessa registreras av hårcellerna vi har i örat och omvandlas till signaler som skickas upp till hjärnan för att tolkas. På så vis kan hjärnan få de mest spännande vibrationerna att låta som en konsert med David Bowie.

_____________________________________________

### Infraljud och ultraljud

Människan kan (som bäst) höra ljud med frekvensen 20 - 20 000 Hz. Men, det finns ändå ljud som har lägre frekvenser än 20 Hz eller högre än 20 000 Hz.

*Infraljud* har frekvenser under 20 Hz. Vi kan inte höra infraljud men vi kan påverkas av det, exempelvis genom att vi blir trötta. Vissa djur kan höra infraljud, som duvor.

*Ultraljud* har frekvenser över 20 000 Hz. Vi kan inte höra ultraljud heller men vi kan använda oss av det i sjukvården. Vissa djur kan höra ultraljud, som hundar eller fladdermöss.

```{admonition} Fördjupning
:class: seealso
Både fladdermöss och hundar kan "använda" ultraljud. Till hundar finns det speciella visselpipor som skickar ut ultraljud så att hunden ska höra utan att omgivningen störs. Fladdermöss använder ultraljud för att navigera - de skickar ut ljudsignaler och noterar sedan hur lång tid det tog för ljudet att eka (ljud som studsar kallas eko) tillbaka. Precis som ett ekolod fungerar!
```

```{admonition} Kom ihåg
:class: attention
*Infraljud* har frekvenser under 20 Hz och *ultraljud* har frekvenser över 20 000 Hz.
```

Ultraljud är användbart i sjukvården. Det ljudet har frekvensen 3-7 miljoner hertz och det finns ännu inte några hittade nackdelar. Det kan användas för att undersöka foster och andra mjuka organ, men också till att krossa njursten utan att behöva använda kirurgi.

_____________________________________________

### Ljudnivå

```{list-table}
:header-rows: 1

* - Exempel
  - Ljudnivå i decibel (dB)
* - Fågelkvitter
  - 20 dB
* - Samtal
  - 60 dB
* - Skolmatsal
  - 80 dB
* - Nattklubb
  - 110 dB
* - Konsert
  - 120 dB
* - Gevärsskott
  - 150 dB
```

ye
decibelskala + hörselskador

_____________________________________________

## Quiz

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
display_quiz("quiz/ljud.json", shuffle_answers=True, shuffle_questions=True)
```



