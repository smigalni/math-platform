# Visuelle designstandarder

Målet er et ryddig, konsekvent og lettlest uttrykk. Design skal støtte læringen, ikke konkurrere med den.

## Fargekoder og komponenter

| Element | Visuell stil | Bruk |
|---|---|---|
| Viktige regler og formler | Blå ramme og lys blå bakgrunn | Definisjoner, regler og sentrale formler |
| Gjennomarbeidede eksempler | Turkis ramme og lys turkis bakgrunn | Løste eksempler med forklaring |
| Elevoppgaver | Lilla ramme og lys lilla bakgrunn | Oppgaver eleven skal løse |
| Ekstra framheving | Oransje | Brukes sparsomt når noe trenger særskilt oppmerksomhet |

Fargene skal brukes konsekvent på tvers av bøker. Konkrete fargeverdier og CSS-klasser vedlikeholdes i felles designimplementasjon.

## Regelbokser – viktig regel

- Regelbokser skal ha blå visuell utforming: blå kant, lys blå bakgrunn og tydelig tittel.
- **Det skal ikke være svarte rammer rundt formler inne i regelbokser.**
- Ikke bruk LaTeX-kommandoen `\boxed{...}` inne i en regelboks når den gir en ekstra svart ramme rundt formelen. La den blå regelboksen være den eneste rammen.
- Unngå doble rammer og unødvendige dekorative konturer.
- Eksempel: skriv formelen direkte i display-matematikk inne i den blå boksen, uten `\boxed{}`.

## Matematiske uttrykk og svar

- Bruk korrekt MathJax/LaTeX og riktige avgrensere.
- Displayformler skal stå på egne linjer når det gir bedre lesbarhet.
- Bruk `\\dfrac` for brøker når det gir tydeligere lesbarhet.
- Sluttsvar skal ha dobbel understrek: `\\underline{\\underline{...}}`.
- Ikke la rå LaTeX eller Markdown-syntaks vises som vanlig tekst.
- Kontroller at formler faktisk rendres riktig i den publiserte nettsiden.

## Typografi og oppsett

- Eksempler og oppgaver skal visuelt skilles tydelig.
- Unngå lange overskrifter, unødvendig tekst og for mange bokser eller illustrasjoner.
- Bruk figurer når de faktisk forklarer et matematisk poeng.
- Hold navigasjon og innholdsfortegnelse ren. Visuell formatering av oppgaveoverskrifter skal ikke lekke inn i navigasjon/TOC.
- Ikke bruk ikoner som pynt dersom de skaper støy eller forvirring.

## Vanskelighetsfarger

Når et oppgavesett er delt i nivåer, er standardfargene:
- Middels: grønn.
- Vanskelig: oransje/gul.
- Svært vanskelig: rød.

Fargene skal brukes på nivåoverskriftene i selve innholdet, ikke automatisk på navigasjon eller innholdsfortegnelse.
