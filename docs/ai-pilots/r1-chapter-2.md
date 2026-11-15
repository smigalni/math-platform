# AI-pilot: R1 kapittel 2

- **Dato:** 2026-11-15
- **Bokrepo:** `smigalni/matte`
- **Branch:** `pilot/r1-kapittel-2-isolert`
- **Pull request:** [#21](https://github.com/smigalni/matte/pull/21)
- **Utgangspunkt:** `19710ea50cd5d293744f930499f1c2df93aadd7f`
- **Pilotcommit:** `9d0d936692b25e6096e0d0b5e026a05e28acd2e7`

## Formål

Prøve de nye AI-instruksjonene, skillene og spesialistrollene på et reelt kapittel uten å endre bokas arkitektur eller påvirke leveransen av 9.-trinnsboka.

## Hvordan piloten ble kjørt

Hovedagenten utførte én sammenhengende arbeidsøkt og brukte fire tydelig adskilte kontrollpass:

1. **Innholdspass:** leste kapittelstruktur, teori, oppgaver, fasiter og navigasjon.
2. **Matematikkpass:** kontrollerte utvalgte oppgaver og løsninger uavhengig, særlig 2.8.7 og 2.8.10–2.8.13, 2.P1.1, 2.P2.1–2.P2.3, anvendelsesoppgavene og parameteroppgave F i fordypningen.
3. **Pedagogikkpass:** vurderte progresjon, forkunnskaper, differensiering, programmering, blandede oppgaver, kapittelprøve og muntlig forberedelse.
4. **Teknisk QA-pass:** kontrollerte alle ni kapittel 2-sider for sentrale Markdown-/MathJax-mønstre og sammenholdt innholdet med bokas egne instruksjoner og kvalitetskonfigurasjon.

**Viktig begrensning:** Dette var fire separate review-pass utført av samme hovedagent i samme arbeidskontekst. Ingen uavhengige subagenter ble startet. Skillene og rollebriefene ble brukt som prosedyrer, ikke som separate kjørende agenter. Det er nettopp en avgrensningen piloten skal synliggjøre før vi velger en runtime for ekte delegering.

## Funn

### Matematikk

Ingen matematisk feil ble funnet i utvalget som ble kontrollert. Blant annet ble følgende kontrollert:

- Kontinuitets- og stigningstallkravene i 2.8.7 gir henholdsvis (b=a-1) og (b=a+2), og kan ikke oppfylles samtidig.
- Parameterfunksjonen i 2.8.10 gir hull ved (x=1), og ved (x=-1) hull bare når (a=1); ellers vertikal asymptote.
- 2.8.11 tar korrekt hensyn til opprinnelig definisjonsmengde i den rasjonale ulikheten.
- Polynomdivisjonen i 2.8.12 gir skrå asymptote (y=x+1), hull ((1,3)) og vertikal asymptote (x=-1).
- Logaritmeoppgaven 2.8.13 har definisjonsmengde ((-infty,1)\cup(3,\infty)), nullpunkter (2\pm\sqrt2), vertikale asymptoter (x=1,3) og verdimengde (ℝ).
- Kapittelprøvens parameteroppgaver og anvendelsesmodellen for temperatur ble kontrollert.

Dette er en målrettet kontroll av sentrale og krevende oppgaver, ikke en formell fullstendig matematisk revisjon av hver linje i hele kapittelet.

### Pedagogikk og struktur

Kapittel 2 har en tydelig grunnstruktur med teori, lokale oppgaver, fordypning, programmering, blandede oppgaver i nivågrupper, kapittelprøve, muntlig forberedelse og formeloversikt. Derivasjon er markert som en bro til kapittel 3 i stedet for å bli et skjult forkunnskapskrav.

Kompetansemålmatrisen ligger i `editorial/r1/` og er ikke studentinnhold. Denne piloten gjennomførte ikke en ny fullstendig Udir-revisjon.

### Teknisk og visuelt QA

Den statiske gjennomgangen fant to eksempler i `fordypning-asymptoter.md` som var skrevet som vanlige overskrifter i stedet for `example`-admonitions. De ble konvertert til etablerte eksempelbokser i commit `9d0d936`.

Etter endringen ble filen hentet på nytt og kontrollert:
- 2 eksempelbokser.
- 0 løse eksempeloverskrifter.
- 19 åpne og 19 lukkede display-matematikkavgrensninger.

En bred nettleserbasert visuell gjennomgang er ikke utført i denne piloten.

## Automatiske kontroller

På det opprinnelige kapittelcommit-et `19710ea` var både Book quality og Zensical build bestått.

Etter pilotrettingen på `9d0d936` startet GitHub Actions fire kontroller:
- Book quality / Markdown structure and math-book style (to jobber)
- Build documentation site (to jobber)

Ved opprettelsen av denne rapporten var disse kontrollene fortsatt **in progress**. De må kontrolleres på nytt før kapittelendringen kan regnes som teknisk verifisert.

## Resultat og læring

Piloten viser at repository-instruksjoner og skills kan gi en mer systematisk, selvstendig arbeidsflyt med inspeksjon, rollebaserte review-pass, retting og ny kontroll. Den viser ikke ennå at ekte subagenter kan samarbeide eller at MCP er konfigurert.

Neste tekniske steg bør derfor være å velge og teste en faktisk agent-runtime med støtte for delegering, tilgangskontroll og sporbare resultater. Før det bør vi beholde denne enkle arbeidsflyten; den gir verdi uten å innføre unødvendig kompleksitet.

## Menneskelig kontroll

- PR #21 skal fortsatt være draft og ikke merges eller publiseres uten eierens godkjenning.
- Visuell nettleserkontroll gjenstår.
- Ingen endringer ble gjort i 9.-trinnsboka.
