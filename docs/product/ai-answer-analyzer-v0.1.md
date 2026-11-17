# AI-besvarelsesanalysator — produkt- og teknisk kravspesifikasjon v0.1

**Status:** Første avgrensede pilot — krav under validering  
**Dato:** 17. november 2026  
**Eier:** MathPlatform  
**Første faglige testområde:** T-matte, kapittel 2 (algebra)  
**Mål:** Undersøke om en elev kan fotografere en håndskrevet matematikkbesvarelse og få en pålitelig, pedagogisk gjennomgang.

---

## 1. Produktidé

Eleven løser en oppgave på vanlig papir og fotograferer besvarelsen med mobil eller nettbrett. MathPlatform forsøker å lese oppgaven og elevens løsning, analysere matematisk korrekthet og presentasjon, og gir konkrete tilbakemeldinger.

Eleven skal ikke måtte skrive på en bestemt digital flate eller følge én bestemt løsningsrekkefølge. Systemet skal vurdere matematikken eleven faktisk har skrevet.

**Kjerneprinsipp:** Systemet skal være ærlig om hva det kan lese og hva det kan konkludere med. Det skal aldri dikte opp uleselig tekst, mellomregninger eller feil.

## 2. Problem og brukerbehov

Elever arbeider ofte på papir, med stor variasjon i håndskrift, oppsett, symbolbruk og løsningsmetoder. Mange bruker ikke nettbrett med penn. En løsning som krever digital håndskrift eller fullstendig strukturert inntasting, vil derfor være en dårlig hovedinngang.

Eleven trenger:
- å kunne bruke papir og vanlig mobilkamera;
- å få vurdert både svar og fremgangsmåte;
- å forstå hvor og hvorfor en eventuell feil oppstår;
- å få hint og forslag som hjelper videre, ikke bare fasit;
- å få beskjed om hva som må fotograferes eller skrives tydeligere dersom besvarelsen ikke kan leses.

Lærer/privatlærer trenger at tilbakemeldingen er faglig pålitelig, etterprøvbar og tydelig på usikkerhet.

## 3. Mål for prototype v0.1

Prototypen skal demonstrere én ende-til-ende arbeidsflyt:

1. Eleven velger eller oppgir oppgaven.
2. Eleven tar ett eller flere bilder av besvarelsen på papir.
3. Systemet vurderer bildekvalitet og lesbarhet.
4. Systemet tolker oppgavetekst, mellomregninger, symboler og sluttresultat.
5. Systemet analyserer om fremgangsmåten er matematisk gyldig.
6. Systemet vurderer om presentasjonen er forståelig og tilstrekkelig strukturert.
7. Eleven får en pedagogisk tilbakemelding med konkrete neste steg.
8. Hvis systemet er usikkert, ber det om et nytt bilde eller en presisering i stedet for å gjette.

### Ikke mål for v0.1

- Full elevprofil eller langsiktig læringsanalyse.
- Automatisk karaktersetting eller standpunktvurdering.
- Lærerdashboard og skoleadministrasjon.
- Sanntidsregistrering av alt eleven skriver.
- Egenutviklet håndskriftgjenkjenningsmodell.
- Støtte for alle fag, alle matematikknivåer og alle typer figurer.
- Automatisk publisering av AI-genererte oppgaver eller fasiter.

## 4. Funksjonelle krav

### FR-01 — Oppgavekontekst

Systemet må kjenne oppgaven som skal vurderes. I første pilot velges oppgaven fra en forhåndsdefinert testoppgave eller oppgis som tekst. Ikke baser vurderingen utelukkende på at modellen skal finne og forstå oppgaven fra bildet.

### FR-02 — Bildeopplasting

- Støtte vanlige mobilbilder.
- Støtte flere bilder/sider for én besvarelse.
- Beholde rekkefølgen på sidene.
- Gi enkel veiledning om lys, fokus, utsnitt, skygger og at hele besvarelsen må være med.
- Ikke kreve Remarkable, nettbrett eller digital penn.

### FR-03 — Lesbarhetskontroll

Systemet skal først vurdere om bildet og håndskriften kan tolkes.

Det skal kunne markere:
- hele besvarelsen lesbar;
- deler av besvarelsen lesbare;
- bestemte linjer/symboler usikre;
- besvarelsen ikke lesbar nok til faglig vurdering.

Når noe er uklart, skal systemet:
- si nøyaktig hvilken del som er uklar, så langt det lar seg gjøre;
- be eleven ta nytt bilde, zoome inn eller skrive den aktuelle linjen på nytt;
- forklare hvordan bildet kan forbedres;
- avstå fra å vurdere den uklare delen.

Det skal ikke presentere en usikker OCR-tolkning som et faktum.

### FR-04 — Rekonstruksjon av løsning

Systemet skal forsøke å rekonstruere elevens faktiske løsning i riktig rekkefølge, inkludert:
- uttrykk og likninger;
- mellomregninger;
- tekstlige forklaringer;
- piler, innrykk, nummerering og andre strukturelle signaler når de er relevante;
- overstrykninger og alternative forsøk når de kan tolkes.

Tolkningen skal kunne kontrolleres mot originalbildet. I prototypen bør den rekonstruerte teksten vises til testeren eller eleven før endelig analyse dersom lesesikkerheten ikke er høy.

### FR-05 — Matematisk vurdering

Vurderingen skal skille mellom:
1. sluttresultat;
2. gyldigheten av matematiske steg;
3. logisk sammenheng og begrunnelse;
4. metodevalg og eventuell effektivitet;
5. presentasjon og lesbar struktur.

Systemet skal godta ulike gyldige løsningsmetoder og ulik rekkefølge på operasjoner. Det skal ikke sammenligne elevens løsning med én fasitlinje om gangen.

En alternativ metode skal ikke merkes som feil bare fordi den avviker fra eksempelløsningen. Eventuelle krav til metode må komme fra oppgaven eller den eksplisitte faglige konteksten.

### FR-06 — Pedagogisk tilbakemelding

Tilbakemeldingen skal være konkret, respektfull og tilpasset elevens nivå. Den skal, når det er relevant, inneholde:
- hva eleven har gjort riktig;
- hvor første sikre feil eller brudd oppstår;
- hvorfor dette er et problem;
- et hint eller spørsmål som hjelper eleven videre;
- forslag til hvordan eleven kan kontrollere eller forbedre løsningen;
- en alternativ metode når den faktisk gir læringsverdi.

Systemet skal ikke automatisk avsløre hele løsningen dersom et hint er tilstrekkelig. Eleven bør kunne be om mer hjelp trinnvis.

### FR-07 — Tilbakemelding på presentasjon

Systemet skal gi separat tilbakemelding på hvor forståelig og ryddig løsningen er, for eksempel:
- om mellomregninger er vist;
- om det er tydelig hvilken linje som følger av hvilken;
- om likhetstegn brukes riktig;
- om symboler og variabler er konsekvente;
- om sluttresultatet er tydelig markert;
- om forklaringer mangler der et steg ikke er selvforklarende.

**Viktig:** Presentasjonskvalitet skal ikke blandes sammen med matematisk korrekthet. Utydelig håndskrift skal ikke automatisk tolkes som svak matematisk forståelse, og pen håndskrift skal ikke gi uttelling for en matematisk feil.

### FR-08 — Usikkerhet og trygg stopp

Systemet skal kunne returnere minst disse statusene:
- `readable`: tilstrekkelig lesbart for vurdering;
- `partially_readable`: deler kan vurderes, andre deler krever ny innsending;
- `unreadable`: kan ikke vurderes forsvarlig;
- `needs_clarification`: tolkningen er tvetydig og må avklares.

Det skal skille mellom:
- usikkerhet om hva eleven har skrevet;
- usikkerhet om matematisk korrekthet;
- manglende informasjon i oppgaven;
- reell matematisk tvetydighet.

Systemet skal ikke gi en sikker konklusjon når grunnlaget er utilstrekkelig.

## 5. Foreslått teknisk arbeidsflyt

Arkitekturen skal være leverandøruavhengig. Vi tester eksisterende tjenester og modeller før vi velger leverandør.

1. **Inntak:** Motta bilde(r), oppgave-ID/oppgavetekst og nødvendig kontekst.
2. **Bildeforbehandling:** Roter, beskjær og vurder oppløsning/kontrast. Behold originalbildet som referanse.
3. **Håndskrift- og dokumenttolking:** Bruk én eller flere eksisterende OCR-/matematikkgjenkjenningstjenester eller multimodale modeller.
4. **Strukturert representasjon:** Lag en rekonstruksjon av oppgave, linjer, uttrykk, tekst og rekkefølge, med usikkerhetsmarkeringer og kobling til bildeutsnitt.
5. **Matematisk analyse:** Undersøk uttrykk, beregninger og overganger med deterministiske kontroller der det er mulig, supplert med modellbasert resonnering.
6. **Konsistenskontroll:** Kontroller at analysen faktisk bygger på det som ble lest fra bildet. Ved uenighet mellom tolkinger skal systemet be om avklaring.
7. **Pedagogisk respons:** Generer elevtilbakemelding fra verifiserte observasjoner, ikke direkte fra et ustrukturert bilde alene.
8. **Presentasjon:** Vis resultat, begrunnelse, usikkerhet og neste steg.

### Viktig om matematisk kontroll

En symbolsk matematikkmotor kan kontrollere mange uttrykk og likheter, men kan ikke alene forstå alle gyldige løsningssteg eller elevens begrunnelse. For eksempel må divisjon med et uttrykk håndteres med kontroll av at uttrykket ikke er null, og kvadrering kan introdusere falske løsninger. Numerisk likhet alene beviser heller ikke at et transformasjonstrinn er ekvivalent.

Derfor kombineres:
- deterministiske kontroller for beregninger og symbolsk ekvivalens der det er forsvarlig;
- eksplisitte regler og domenekunnskap;
- AI-tolkning av struktur, metode og forklaringer;
- stopp/avklaring når bevisgrunnlaget ikke er godt nok.

## 6. Teknologier som skal undersøkes

Dette er kandidater for evaluering, ikke vedtatte leverandørvalg:
- Mathpix eller tilsvarende matematikk-OCR for håndskrevne uttrykk og dokumenter.
- Multimodale modeller med bildeinnlesing for dokumentstruktur, kontekst og forklaring.
- SymPy eller tilsvarende symbolsk verktøy for avgrensede algebraiske kontroller.
- Egen regel-/testkode for oppgavetyper og kjente feil der dette gir pålitelighet.

Vi skal sammenligne minst to ulike tolkeoppsett på samme testmateriale. Vurder leverandørvilkår, pris, personvern, datalagring, databehandleravtale og om elevdata brukes til modelltrening før en tjeneste velges.

## 7. Første testområde og datasett

**Første faglige område:** T-matte kapittel 2 — algebra.

Vi starter smalt, men velger oppgaver som viser variasjon:
- forenkling og algebraiske uttrykk;
- parenteser og distribusjon;
- faktorisering og forkorting;
- brøkuttrykk;
- likninger eller andre relevante oppgavetyper fra kapittelet.

Testmaterialet bør inneholde minst 20 besvarelser før vi trekker sterke konklusjoner. En første teknisk røykprøve kan starte med 3–5 besvarelser.

Materialet skal dekke:
- tydelig, middels og vanskelig håndskrift;
- gode og dårlige bilder;
- flere sider;
- overstrykninger og rettelser;
- ulike gyldige løsningsmetoder og rekkefølger;
- korrekte løsninger;
- ulike typer feil;
- ufullstendige løsninger.

Besvarelsene må være anonymiserte og brukes med nødvendig tillatelse. Ikke last opp identifiserbare elevopplysninger til eksterne AI-tjenester uten avklart behandlingsgrunnlag og nødvendige avtaler.

## 8. Evalueringskriterier

Hver besvarelse vurderes mot en fasit-/lærervurdering som er laget uavhengig av AI-systemet.

Registrer minst:
1. **Lesenøyaktighet:** Ble uttrykk, tall, fortegn og symboler lest riktig?
2. **Struktur:** Ble rekkefølgen og koblingen mellom linjene forstått?
3. **Matematisk vurdering:** Ble riktige løsninger godkjent og reelle feil identifisert?
4. **Alternative metoder:** Ble gyldige alternative fremgangsmåter akseptert?
5. **Feillokalisering:** Fant systemet første relevante feil uten å finne på feil?
6. **Pedagogisk kvalitet:** Var hint og forklaringer korrekte og nyttige?
7. **Usikkerhet:** Stoppet systemet når bildet eller tolkningen var for usikker?
8. **Presentasjon:** Ga systemet relevante, separate råd om struktur og lesbarhet?

Ikke bruk én samlet «nøyaktighetsprosent» alene. Rapporter feiltypene separat, særlig falske feilmarkeringer og tilfeller der systemet burde ha stoppet, men ga en sikker vurdering.

### Foreløpige pilotmål

Dette er interne mål for å avgjøre om vi skal fortsette, ikke påstander om dagens teknologi:
- Ingen oppdiktede avlesninger presentert som sikre.
- Ingen sikker faglig konklusjon på besvarelser systemet selv har markert som uleselige.
- Gyldige alternative metoder skal ikke rutinemessig feilklassifiseres.
- Alle vurderinger skal kunne spores til konkrete deler av besvarelsen.
- Vi skal dokumentere både vellykkede og mislykkede eksempler.

Etter første runde justerer vi terskler og mål basert på faktisk kvalitet.

## 9. Personvern og ansvar

Fordi løsningen kan brukes av mindreårige:
- Samle inn minst mulig personopplysninger.
- Ikke be om navn, skole eller klasse på besvarelsesbildet.
- Fjern metadata fra bilder når mulig.
- Definer kort lagringstid og sletting for råbilder.
- Ikke bruk elevbesvarelser til modelltrening som standard.
- Avklar behandlingsgrunnlag, informasjon til elev/foresatt/skole og databehandleravtaler før reell elevpilot.
- Ikke bruk prototypen til karaktersetting eller andre avgjørelser med store konsekvenser.
- Gjør det tydelig at AI-tilbakemeldingen kan være feil og at lærer fortsatt har faglig ansvar.

## 10. Utenfor scope og produktprinsipper

- Papir er standard arbeidsflate; digital penn er ikke et krav.
- Flere bilder skal kunne inngå i én besvarelse.
- Ulike matematiske metoder og operasjonsrekkefølger skal aksepteres når de er gyldige.
- Faglig korrekthet og presentasjonskvalitet skal vurderes separat.
- AI skal gi hint før full løsning når det er pedagogisk hensiktsmessig.
- Usikkerhet skal vises tydelig.
- Ingen automatisk karaktersetting i v0.1.
- Løsningen skal være faglig avgrenset og kunne gjenbrukes på tvers av bøkene senere, men vi skal ikke bygge generell plattforminfrastruktur før piloten viser behovet.

## 11. Leveranser for første utviklingssyklus

1. Velge 3–5 representative, anonymiserte testbesvarelser.
2. Lage en fasit-/lærervurdering for hver besvarelse.
3. Teste minst to teknologiske oppsett for avlesning og analyse.
4. Dokumentere hva som ble lest feil, hvilke matematiske vurderinger som ble feil, og når systemet burde ha bedt om nytt bilde.
5. Lage en enkel ende-til-ende prototype for bilde → tolking → kontroll → tilbakemelding.
6. Beslutte om kvaliteten er god nok til en større test med minst 20 besvarelser.

**Beslutningsport:** Vi går ikke videre til større produktutvikling før vi har dokumentert at løsningen kan lese et representativt utvalg håndskrevne besvarelser, håndtere alternative metoder og si fra når den er usikker.
