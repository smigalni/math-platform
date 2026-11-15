# Produktspesifikasjon: AI-støttede ekstraoppgaver for lærere

- **Status:** Forslag til produktkrav for videre prototyping
- **Dato:** 2026-11-15
- **Område:** Lærerområde i Math Platform

## 1. Formål

Læreren skal kunne lage målrettede ekstraoppgaver når en elev eller elevgruppe strever med et avgrenset matematisk tema. Oppgavene skal være forankret i den aktuelle læreboka og dens faglige progresjon, ikke genereres som generiske oppgaver løsrevet fra undervisningen.

Eksempel: En elev strever med intervallnotasjon. Læreren velger temaet og får forslag til flere oppgaver som bruker bokas begreper, notasjon og metoder.

## 2. Grunnprinsipp

**AI foreslår; læreren bestemmer.**

AI-generert innhold er utkast og skal aldri automatisk bli del av den offisielle læreboka eller vises som godkjent elevinnhold. Læreren må kunne kontrollere både oppgaven og løsningen før deling eller utskrift.

## 3. Brukerflyt

1. Læreren åpner lærerområdet og velger riktig bok, kapittel og et avgrenset tema.
2. Læreren beskriver kort hva eleven strever med og kan angi ønsket nivå, antall oppgaver og eventuell oppgavetype.
3. Systemet henter relevant faglig kontekst fra den valgte boka: læreplanmål, begreper, notasjon, metoder, progresjon og relevante eksempler.
4. AI lager et utkast med oppgaver og tilhørende løsningsforslag.
5. Læreren går gjennom hvert element og kan:
   - redigere oppgavetekst og løsning
   - fjerne en oppgave
   - be om en ny variant eller regenerere et utkast
   - godkjenne enkeltoppgaver eller en hel samling
6. Først etter godkjenning kan læreren dele oppgavene med elever eller skrive dem ut.
7. Utkast og godkjente læreroppgaver kan finnes igjen i lærerområdet.

## 4. Krav til faglig kontekst

Genereringen skal være bok- og temaspesifikk. Systemet skal så langt relevant bruke:

- riktig læreplan og kompetansemål for boka
- bokas begreper og terminologi
- bokas notasjon og skrivemåte
- metoder elevene faktisk er introdusert for
- riktig faglig nivå og progresjon
- relevante eksempler og oppgavetyper fra det aktuelle kapitlet

AI skal ikke introdusere metoder eller forutsetninger som ligger utenfor den valgte progresjonen uten at læreren uttrykkelig ber om det.

Hvis konteksten er utilstrekkelig eller motstridende, skal systemet synliggjøre usikkerheten i stedet for å late som om oppgaven er kvalitetssikret.

## 5. Innholdsstatus og skille mellom innholdstyper

Innhold skal ha en tydelig status og eier:

| Innholdstype | Eier | Kan vises som offisielt bokinnhold? |
|---|---|---|
| Redaksjonelt godkjent lærebokinnhold | Bokredaksjonen | Ja |
| AI-generert utkast | Lærerens arbeidsområde | Nei |
| Lærerredigert, ikke godkjent utkast | Lærer | Nei |
| Lærergodkjent ekstraoppgave | Lærer | Nei – det er godkjent for lærerens bruk, ikke del av den offisielle boka |

Lærergodkjenning betyr at læreren har kontrollert innholdet for den aktuelle undervisningssituasjonen. Det er ikke det samme som redaksjonell godkjenning av læreboka.

## 6. Funksjonelle krav

### Må-krav for første prototype

- Velge bok, kapittel og tema.
- Opprette et AI-utkast med oppgaver og løsninger.
- Vise oppgave og løsning sammen for lærerens kontroll.
- Redigere oppgave og løsning separat.
- Fjerne enkeltoppgaver.
- Regenerere enkeltoppgaver uten å måtte forkaste resten av samlingen.
- Godkjenne oppgaver før deling eller utskrift.
- Holde lærerinnhold tydelig adskilt fra offisielt bokinnhold.

### Bør-krav etter første prototype

- Velge antall oppgaver og vanskelighetsnivå.
- Lagre samlinger og fortsette redigering senere.
- Lage varianter med samme læringsmål, men andre tall eller kontekster.
- Se hvilken bok- og kapittelkontekst som ble brukt ved generering.
- Eksportere en ryddig utskriftsversjon med separat fasit.

## 7. Kvalitets- og sikkerhetskrav

- Oppgaver og løsninger må kunne kontrolleres matematisk.
- Systemet skal ikke fremstille AI-generert innhold som verifisert bare fordi det er generert.
- Lærerens godkjenning skal være en eksplisitt handling.
- Deling og utskrift skal bare bruke godkjente oppgaver.
- Det skal være mulig å se om en oppgave er AI-generert, redigert eller godkjent.
- Unngå å sende direkte identifiserende elevopplysninger til genereringsmodellen; tema og læringsbehov skal normalt være tilstrekkelig.
- Feil eller manglende faglig kontekst skal håndteres synlig og forsiktig.

## 8. Avgrensning for første prototype

Første prototype skal validere lærerens arbeidsflyt fra tema til godkjent oppgavesamling. Den skal ikke forsøke å bygge et komplett adaptivt læringssystem.

Utenfor første prototype:

- automatisk diagnostisering av elever
- automatisk tildeling av oppgaver uten lærerens kontroll
- elevchat direkte med generativ AI
- automatisk publisering i den offisielle læreboka
- avansert analyse av elevdata

## 9. Foreslåtte akseptansekriterier

Prototypen kan vurderes som vellykket når en lærer kan:

1. Velge et presist tema i en bestemt bok.
2. Generere en liten samling oppgaver med løsningsforslag som bruker riktig terminologi og metode.
3. Oppdage og rette en feil i en oppgave eller løsning.
4. Fjerne en oppgave og regenerere en annen uten å miste resten.
5. Godkjenne samlingen og dele eller skrive den ut.
6. Bekrefte at lærerinnholdet ikke har blitt blandet inn i den offisielle boka.

## 10. Åpne arkitekturbeslutninger

Disse punktene skal undersøkes før implementering, ikke avgjøres ved gjetning:

- Hvordan læreridentitet, tilgang og roller skal håndteres.
- Hvordan bokinnhold og faglig kontekst gjøres tilgjengelig for generering.
- Hvordan oppgaver, versjoner, status og godkjenning lagres.
- Hvilke modeller og leverandører som kan brukes, og hvordan kostnader og personvern håndteres.
- Hvordan eksport og deling skal fungere på tvers av ulike bokrepositorier.

Løsningen skal bevare prinsippet om at hver bok eier sitt faginnhold og sin publisering, mens plattformen leverer felles funksjonalitet.
