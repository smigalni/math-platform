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
- Mellomregning skal presenteres ryddig over flere linjer. Sett likhetstegnene under hverandre når det er naturlig og gjør utregningen lettere å følge.
- Bruk `\\dfrac` for brøker når det gir tydeligere lesbarhet.
- Sluttsvar skal ha dobbel understrek: `\\underline{\\underline{...}}`.
- Ikke la rå LaTeX eller Markdown-syntaks vises som vanlig tekst.
- Kontroller at formler faktisk rendres riktig i den publiserte nettsiden.

## Typografi og oppsett

- Deloppgaver i samme oppgave skal alltid presenteres som egne punkter i en punktliste. Merkene a), b), c) osv. skal stå på hver sin linje, for eksempel `- a) ...` og `- b) ...`. Ikke skriv flere deloppgaver som ett sammenhengende avsnitt.
- Bruk samme punktstruktur i oppgaveteksten og i tilhørende fasit/løsningsforslag. Hvis en deloppgave har en egen formelblokk eller mellomregning, skal den tydelig høre til riktig punkt.
- Kravet gjelder på mobil, PC og i utskrift.
- Skrifttype og skriftstørrelser styres sentralt av plattformens design, ikke individuelt i hver bok eller regelboks.
- Typografien skal være responsiv og lesbar på mobil, nettbrett og PC.
- Eksempler og oppgaver skal visuelt skilles tydelig.
- Unngå lange overskrifter, unødvendig tekst og for mange bokser eller illustrasjoner.
- Bruk figurer når de faktisk forklarer et matematisk poeng.
- Hold navigasjon og innholdsfortegnelse ren. Visuell formatering av oppgaveoverskrifter skal ikke lekke inn i navigasjon/TOC.
- Ikke bruk ikoner som pynt dersom de skaper støy eller forvirring.

## Vanskelighetsfarger

Vanskelighetsfarger skal **kun brukes i blandede oppgavesett** der elevene arbeider med oppgaver på ulike nivåer. De skal ikke brukes på vanlige oppgaver rett etter hvert teorikapittel.

Standardfargene i blandede oppgavesett er:
- Middels: grønn.
- Vanskelig: oransje/gul.
- Svært vanskelig: rød.

Fargene skal brukes på nivåoverskriftene i selve innholdet, ikke automatisk på navigasjon eller innholdsfortegnelse.

## Utskrift og PDF

Bøkene skal ha en god utskriftsfunksjon som gjør det enkelt å bruke innholdet på papir.

- Brukeren skal kunne skrive ut eller lagre et helt kapittel som PDF.
- Brukeren skal kunne velge og skrive ut enkeltstående delkapitler, eksempler eller oppgaver.
- Det skal være mulig å skrive ut et oppgavesett uten teori og eksempler.
- Oppgaver og løsningsforslag/fasit skal kunne skrives ut separat.
- Det skal være mulig å sette sammen et eget oppgavesett av valgte oppgaver fra ulike deler av boken.
- Utskriftsvisningen skal fjerne navigasjon, menyer og andre skjermelementer som ikke hører til faginnholdet.
- Formler, figurer, oppgavenummerering og overskrifter skal beholde korrekt utforming og være lesbare på papir.
- Utskriftsoppsettet skal gi eleven tilstrekkelig plass til å skrive mellomregning og svar der det er relevant.

Utskrift skal fungere både direkte til skriver og som lagring til PDF. Funksjonen skal utformes som en felles plattformstandard, slik at den kan gjenbrukes i alle bøkene.
