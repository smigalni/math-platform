# Felles standard for matematiske visualiseringer

**Status:** Vedtatt retning – teknologivalg skal valideres gjennom en prototype før de låses.  
**Omfang:** Alle bokprosjekter som bruker Math Platform, blant annet 9trinn-matte, R1 og R2.

## 1. Formål

Matematiske figurer og visualiseringer er en del av faginnholdet, ikke dekorasjon. De skal være matematisk korrekte, pedagogisk tydelige, visuelt profesjonelle og stabile på skjerm og papir.

Vi skal utvikle ett gjenbrukbart visualiseringssystem. Bøkene skal kunne bruke samme komponenter og kvalitetskontroller, men fortsatt eie sitt eget faginnhold og kunne bygges og publiseres selvstendig.

Lærerens og redaktørens tid skal brukes på matematikk og pedagogikk, ikke på å oppdage tekniske feil i figurer.

## 2. Visualiseringskategorier

Systemet skal støtte tre hovedformer:

1. **Statisk:** ferdig figur som inngår i læreboktekst, oppgaver, fasit eller PDF.
2. **Interaktiv:** eleven kan for eksempel zoome, flytte punkter, endre parametere eller rotere en 3D-visning.
3. **Dynamisk/forklarende:** en styrt sekvens som viser en matematisk prosess eller sammenheng trinn for trinn.

En visualisering kan ha både en interaktiv skjermversjon og en statisk, utskriftsvennlig versjon. Interaktivitet skal aldri være eneste måte å få tilgang til nødvendig faglig informasjon på.

## 3. Faglig dekningsområde

### 2D-grafer og koordinatsystemer
- Funksjoner, grafer og flere grafer i samme koordinatsystem.
- Akser, skala, rutenett, nullpunkter og skjæringspunkter.
- Tangenter, sekant, stigningstall og derivasjon.
- Parametere, ulikheter, intervaller og stykkevis definerte funksjoner.
- Statistiske diagrammer og fordelinger.

### 2D-geometri og konstruksjoner
- Trekanter, firkanter, polygoner og sirkler.
- Vinkler, lengder, parallelle og vinkelrette linjer.
- Høyder, medianer, halveringslinjer, hjelpelinjer og konstruksjoner.
- Markering av like sider, vinkler, punkter og geometriske relasjoner.

### 3D og romgeometri
- Romfigurer, prismer, pyramider, sylindre, kjegler og kuler.
- Koordinatsystemer i rommet, punkter, vektorer, linjer og plan.
- Flater og tredimensjonale funksjonsgrafer.
- Rotasjon, volum, avstander og romlige sammenhenger.
- Roterbar visning der dette gir læringsverdi.

### Andre visualiseringer
- Sannsynlighetstrær og kombinatoriske oversikter.
- Histogram, boksplott og normalfordeling.
- Tallinjer, intervaller, mengder og fortegnsskjema.
- Programmerings- og algoritmeillustrasjoner.
- Pedagogiske sekvenser som viser mellomsteg i en løsning.

Dekningsområdet er et langsiktig funksjonskrav. Vi skal ikke implementere alt samtidig.

## 4. Arkitekturprinsipper

- **Felles grensesnitt:** Bøkene bruker et dokumentert grensesnitt og felles visuelle standarder.
- **Løst koblet:** Hver bok skal kunne bygges og publiseres selvstendig. En feil i visualiseringssystemet skal ikke gjøre bokinnhold eller publisering utilgjengelig uten at dette fanges opp.
- **Data og presentasjon skilles:** Matematiske data, uttrykk, punkter, begrensninger og geometriske relasjoner skal ikke blandes unødvendig med visuell styling.
- **Riktig verktøy til riktig oppgave:** 2D-grafer, geometriske konstruksjoner, 3D og statiske illustrasjoner kan kreve ulike renderere bak samme grensesnitt.
- **Vektor først:** Bruk skalerbare formater for diagrammer og figurer der det er hensiktsmessig. Unngå uskarpe eller unødvendig tunge rasterbilder.
- **Responsivt:** Figurer skal fungere på mobil, nettbrett og PC uten at akser, etiketter eller viktige detaljer forsvinner.
- **Utskriftsvennlig:** Figurer skal kunne gjengis i PDF og på papir. Farge skal ikke være eneste måte å formidle forskjeller på.
- **Tilgjengelighet:** Bruk lesbare etiketter, kontrast, tekstalternativ/beskrivelse og tastaturbetjening der det er relevant.
- **Reproduserbart:** Samme kilde og konfigurasjon skal gi samme figur i bygg og test, med mindre dynamikk er uttrykkelig tilsiktet.

## 5. Visuell standard

Alle visualiseringer skal følge en felles visuell profil som passer lærebøker:

- Ren, rolig bakgrunn og tydelig hierarki.
- Konsistent typografi, linjetykkelse, punktstørrelse, piler og markører.
- Akser og rutenett skal være tydelige, men ikke dominere.
- Matematiske etiketter skal bruke korrekt notasjon og være plassert slik at de ikke kolliderer.
- Farger skal ha konsekvent betydning, god kontrast og fungere i gråtoner så langt det er mulig.
- Unngå 3D-effekter, skygger og pynt som ikke støtter matematikken.
- Utsnitt og skala skal fremheve det matematiske poenget uten å villede.
- Figurtekster og alternative beskrivelser skal forklare hva eleven skal se etter, ikke bare gjenta tittelen.

Designstandardene i `docs/standards/design.md` gjelder også for figurer.

## 6. Faglig korrekthet

En figur er ikke godkjent bare fordi den ser pen ut.

Kontroller blant annet:
- At koordinater, funksjonsuttrykk, mål, vinkler og relasjoner stemmer med oppgaven.
- At skala og proporsjoner ikke gir et misvisende inntrykk.
- At punkter, skjæringer, tangenter, vektorer og geometriske konstruksjoner er plassert korrekt.
- At avrunding og numerisk presisjon er tydelig når det er relevant.
- At figur og tilhørende tekst, oppgave og fasit beskriver samme situasjon.
- At 3D-perspektiv ikke skjuler eller forvrenger det som skal læres.
- At tilfeldige eller numeriske beregninger har dokumentert toleranse og stabile tester.

Der en figur er skjematisk og ikke målestokkriktig, skal det være tydelig. Ikke bruk en illustrasjon som bevis for en matematisk egenskap dersom egenskapen ikke er kodet eller kontrollert.

## 7. Obligatorisk test før review

Ingen ny eller endret visualiseringskomponent er klar for brukerreview før relevante kontroller er bestått.

### Automatiske tester
- Komponent- og enhetstester for matematiske beregninger og data.
- Tester av gyldige og ugyldige inndata, tomme data og grenseverdier.
- Kontroller av aksegrenser, skala, etiketter og geometriske invariants der dette er relevant.
- Integrasjonstest i en faktisk bokside.
- Bygging av bokprosjektet uten feil.
- Kontroll av interne lenker og ressurser; ingen 404 eller manglende figurfiler.
- Regresjonstest som sikrer at eksisterende figurer og innhold ikke blir ødelagt.

### Visuell kontroll
- Skjermbilder eller visuelle snapshots av representative figurer.
- Kontroll av mobil, nettbrett og stor skjerm.
- Kontroll av lys/mørk bakgrunn dersom begge støttes.
- Kontroll av utskrift/PDF, inkludert at figurer ikke klippes eller blir uleselige.
- Kontroll av at etiketter, symboler, formler og forklaringer ikke overlapper.
- Kontroll av interaksjon: zoom, panorering, parameterendring og rotasjon når funksjonen finnes.

### 3D-spesifikke kontroller
- Kontroller at akser, retninger, plan, punkter og vektorer er riktige.
- Kontroller at standard kameravinkel viser det sentrale poenget.
- Kontroller rotasjon og zoom på berøringsskjerm og med mus.
- Kontroller at en statisk reservevisning finnes for utskrift og situasjoner uten interaktiv støtte.

### Akseptansekriterium
Testresultater skal være synlige og knyttet til endringen. Ikke skriv «testet» dersom bare kildekoden er lest. Skill mellom:
- implementert,
- automatisk testet,
- visuelt kontrollert,
- testet i bok,
- publisert og verifisert.

En figur kan sendes til faglig review først når alle relevante tekniske og visuelle kontroller er bestått. Brukerreview skal primært handle om matematisk og pedagogisk kvalitet.

## 8. Teknologivalg og prototype

Vi skal ikke låse oss til ett bibliotek før vi har testet representative behov. Prototypen skal sammenligne aktuelle løsninger for:

1. Presise statiske 2D-figurer og geometri.
2. Interaktive funksjonsgrafer med parametere.
3. 3D-flater og romgeometri.
4. Eksport/utskrift og stabil rendering i dokumentasjonssider.

Vurderingskriterier:
- Matematisk presisjon og kontroll over akser/etiketter.
- Visuell kvalitet i lærebokformat.
- 2D- og 3D-kapasitet.
- Responsivitet og berøringsinteraksjon.
- Tilgjengelighet.
- Eksport til SVG eller annet egnet skalerbart format og PDF.
- Lisens, vedlikehold, dokumentasjon og langsiktig risiko.
- Enkel integrasjon med eksisterende bokprosjekter og bygg.

Vi velger færrest mulig avhengigheter som dekker behovene godt. Det er tillatt å bruke ulike spesialiserte renderere bak ett felles grensesnitt.

## 9. Innføringsplan

### Fase A – kartlegging
Kartlegg eksisterende figurer og tegningsbehov i 9trinn-matte, R1 og R2. Registrer hvilke typer som finnes, hvilke som fungerer, og hvilke som er mangelfulle. Ikke endre eller regenerer eksisterende bokinnhold i kartleggingsfasen.

### Fase B – teknisk prøve
Lag en isolert prototype med representative eksempler: en 2D-funksjonsgraf med tangent, en geometrisk konstruksjon, en 3D-flate og en romgeometrisk figur. Test dem automatisk og visuelt.

### Fase C – felles standard og komponenter
Dokumenter valgt arkitektur, grensesnitt, visuell profil, eksempler og testkrav. Lag gjenbrukbare komponenter og testverktøy.

### Fase D – pilot i én bok
Prøv systemet på avgrensede, nye eller uttrykkelig godkjente figurer i én bok. Bevar eksisterende innhold. Mål kvalitet, stabilitet, ytelse og hvor lett det er å produsere og vedlikeholde figurer.

### Fase E – kontrollert utrulling
Ta systemet i bruk i de andre bøkene først når piloten er bestått. Hver bok skal ha egen kontroll av bygg, figurer, lenker og publisering.

## 10. Arbeidsregel

Forfatteren/redaktøren skal kunne beskrive den matematiske hensikten og kontrollere faglig kvalitet. Utviklings- og QA-arbeidet skal håndtere implementasjon, rendering, test, feilsøking og dokumentasjon.

Ikke be brukeren om å reviewe en figur som ikke er teknisk testet. Ikke endre eksisterende kapittelinnhold som bieffekt av å innføre eller reparere visualiseringssystemet.