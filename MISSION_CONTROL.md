# Million Dollar Mission 2031 — Mission Control

> Overordnet styringsdokument for å bygge en internasjonal EdTech-virksomhet med matematikk, læring og AI som kjerne.

**Status:** Arbeidsdokument — strategi under validering  
**Tidshorisont:** 2026–2031  
**Startmarked:** Norge  
**Arbeidskapasitet:** Omtrent 10 timer per uke ved siden av eksisterende arbeid  
**Startmodell:** Solo-gründer med AI og automatisering som multiplikator

Dette dokumentet styrer prioriteringene på tvers av bokprosjektene og MathPlatform. Det erstatter ikke bokspesifikke faglige standarder eller tekniske beslutninger. Slike beslutninger hører hjemme i de respektive prosjektene.

---

## 1. Oppdraget

Bygge en lønnsom, skalerbar EdTech-bedrift som utvikler digitale matematikklæremidler og læringsverktøy med tydelig faglig kvalitet, god pedagogikk og nyttig AI.

Målet er å bygge et selskap med reell kundeverdi, gjentakende inntekter og betydelig egenkapitalverdi innen 2031. En selskapsverdi er ikke det samme som personlig, likvid formue. Personlig økonomisk trygghet og selskapets vekst skal derfor følges som to separate spor.

### Strategiske premisser

- Vi bygger en bedrift, ikke bare en samling lærebøker eller et hobbyprosjekt.
- Vi starter i Norge, men velger arkitektur og innholdsstruktur som ikke låser oss til Norge.
- Vi bruker AI og automatisering for å øke kapasiteten, ikke for å fjerne faglig kontroll.
- Vi validerer betalingsvilje tidlig. Produksjon alene er ikke bevis på et marked.
- Vi beskytter hovedinntekt, økonomisk trygghet og bærekraftig arbeidsbelastning.

## 2. Produktstrategi

### Produktvisjon

En digital matematikkressurs der elever kan lære, forstå og øve, og der lærere kan undervise, tilpasse og følge opp. Bøkene er inngangen til et større læringsprodukt; plattformen gjør det mulig å bygge og drifte flere slike produkter effektivt.

### Første produktretning

**En komplett digital matematikklærebok for 9. trinn**, ikke bare en oppgavegenerator. Den skal kunne brukes gjennom skoleåret og samtidig fungere som et supplement til eksisterende læremidler.

Mulige produktkomponenter:

1. **Lærebok:** læreplanforankret teori, forklaringer, eksempler og visuelle/interaktive forklaringer.
2. **Oppgavebank:** progresjon fra grunnleggende til utfordrende oppgaver, med svar og gjennomarbeidede løsninger.
3. **Elevassistent:** hint, forklaringer og ekstra trening som tar utgangspunkt i det eleven faktisk strever med.
4. **Lærerområde:** tilpasning og generering av oppgaver, oversikt over elevbehov og deling/utskrift.
5. **Kvalitet og kontroll:** lærere skal kunne gjennomgå, redigere, forkaste, regenerere og godkjenne AI-generert innhold før deling.

### Tre innholdskategorier — må holdes adskilt

- **Redaksjonelt godkjent bokinnhold:** offisielt faginnhold som er kvalitetssikret og versjonert.
- **Godkjente oppgaver og løsninger:** oppgaver som er kontrollert og godkjent for bruk.
- **Dynamisk AI-generert tilleggsinnhold:** forslag som ikke blir en del av den offisielle boken før nødvendig menneskelig kontroll og godkjenning.

AI skal bruke riktig læreplan, terminologi, notasjon og metodene som faktisk er undervist i den aktuelle boken.

### Produktportefølje

| Produktspor | Rolle i porteføljen | Nåværende retning |
|---|---|---|
| 9. trinn | Kandidat for første komplette skoleprodukt og markedsvalidering | Bygge bok og pilotere med lærere/elever |
| T-matte | Eget faglig produkt og testarena for gjenbruk | Videreutvikle eksisterende bok |
| R-matte | Eksisterende faglig produkt og teknisk/pedagogisk erfaring | Videreutvikle R1/R2 |
| MathPlatform | Felles teknisk fundament og arbeidsmåte | Bygge bare det som flere bøker faktisk trenger |

At flere bøker utvikles parallelt betyr ikke at alle skal ha samme forretningsmessige prioritet til enhver tid. Vi kan produsere i flere bokspor, men må velge én tydelig hovedhypotese for kundevalidering om gangen.

### Kunder og betalingsmodell — fortsatt hypoteser

Mulige brukergrupper er elever, lærere, foresatte og skoler. Bruker og betalende kunde er ikke nødvendigvis samme person.

Vi skal undersøke minst to mulige innganger:
- Lærer/skole som kjøper et verktøy og læremiddel for undervisningen.
- Elev/foresatt som kjøper tilgang til læring og øving.

Ikke bygg separate kommersielle løsninger for alle segmenter før vi har dokumentert behov, betalingsvilje og hvem som faktisk tar kjøpsbeslutningen.

## 3. Plattform- og arkitekturstrategi

Vi viderefører den eksisterende hybridmodellen:

- Hver bok eier eget faginnhold, bokspesifikke valg og publisering.
- MathPlatform eier felles standarder, maler, verktøy, kvalitetssikring og etter hvert delte tjenester.
- Bøkene skal kunne utvikles og publiseres selvstendig.
- Felles funksjonalitet skal gjenbrukes når det gir reell verdi, ikke fordi alt må samles i én kodebase.

**Prinsipp:** Skill mellom innhold, plattform og kommersielle tjenester. Ikke bygg en stor plattform før konkrete bok- og brukerbehov viser hva som må være felles.

## 4. AI-organisasjon og utviklingsmodell

AI skal fungere som et lite, koordinert team rundt gründeren. Rollene kan først være arbeidsmåter/instruksjoner og senere bli egne agenter når det er nyttig.

| Rolle | Ansvar |
|---|---|
| Product / Strategy Agent | Produktkrav, prioritering, brukerbehov og beslutningsgrunnlag |
| Research Agent | Læreplan, marked, konkurrenter, lærersamtaler og dokumentasjon |
| Engineering Agent | Arkitektur, implementasjon, kode og utviklerflyt |
| Math / Editorial Agent | Matematisk korrekthet, pedagogikk, språk og lærebokstandarder |
| QA / Evaluation Agent | Tester, faglige kontroller, regresjon og evaluering av AI-svar |
| Growth Agent | Posisjonering, distribusjon, innhold, salgseksperimenter og kundedialog |

### Teknologiprinsipper

- **Agent instructions:** varige rolle- og prosjektinstrukser lagres i versjonskontrollerte filer.
- **Skills:** repeterbare arbeidsflyter pakkes som gjenbrukbare ferdigheter med tydelige input, steg og kvalitetskriterier.
- **MCP / verktøy:** agenter får bare de verktøytilgangene oppgaven krever.
- **Harness:** tester, regler, evalueringer og sporbarhet rundt agentenes arbeid.
- **Subagenter:** brukes ved reelt parallelle deloppgaver eller uavhengig kontroll, ikke som pynt.
- **Menneskelig godkjenning:** nødvendig for publisering av faginnhold, vesentlige produktbeslutninger og risikofylte endringer.

Vi skal lære teknologien gjennom ekte produktarbeid. Hver ny komponent må ha en konkret nytte og en vedlikeholdskostnad som står i forhold til verdien.

## 5. Markedsvalidering og forretningsmodell

Den største risikoen er ikke om vi klarer å lage innhold eller kode. Det er om et tydelig kundeproblem er stort nok til at noen vil betale for løsningen, og om vi kan nå disse kundene effektivt.

### Første valideringsspørsmål

1. Hvilke konkrete problemer bruker lærere og elever tid på i matematikk?
2. Hvilke deler av en digital lærebok gir faktisk bedre læring eller undervisning?
3. Hvem har budsjett og myndighet til å kjøpe?
4. Hva bruker de i dag, og hvorfor er dagens løsning utilstrekkelig?
5. Hva må være på plass for at de skal stole på faginnhold og AI-funksjoner?
6. Vil de betale for en pilot, og hva må piloten inneholde?

Snakk med faktiske brukere. Ikke bruk «liker du ideen?» som hovedvalidering. Be om eksempler på dagens arbeidsflyt, problemer, eksisterende verktøy og tidligere kjøpsbeslutninger.

### Tidlige bevis på fremdrift

- Lærere og elever bruker produktet i reelle læringssituasjoner.
- Vi kan observere hva som fungerer og hva som feiler.
- Noen ønsker å fortsette etter pilotperioden.
- Minst noen kunder betaler eller forplikter seg til en konkret betalt pilot.
- Vi kan gjenta onboarding og leveranse uten at alt avhenger av gründerens manuelle innsats.

Omsetnings- og verdsettelsesmål skal først tallfestes som styringsmål når vi har bedre data om pris, konvertering, kundetype, kostnader og kapasitet. Tidligere ambisjonstall er ikke prognoser.

## 6. Arbeidskapasitet og prioritering

Utgangspunktet er omtrent 10 timer per uke. Dette er en ramme, ikke et krav om å fylle alle ledige timer.

Foreløpig fordeling:

| Arbeidsområde | Timer/uke | Hensikt |
|---|---:|---|
| Produkt og bokutvikling | 5 | Lage noe brukere kan teste |
| Brukersamtaler, pilot og salg | 2 | Validere behov og betalingsvilje |
| Plattform og AI-arbeidsflyt | 2 | Bygge gjenbrukbare muligheter der behovet er dokumentert |
| Strategi og økonomi | 1 | Prioritere og følge opp risiko |

Fordelingen justeres etter hva som er flaskehalsen. I en tidlig fase kan kundesamtaler være viktigere enn mer kode. Ikke øk arbeidstiden ved å ofre søvn eller nødvendig restitusjon.

### Prioriteringsregel

Når nye ideer dukker opp, vurder dem etter:
1. Kundeverdi og dokumentert behov.
2. Hvor raskt vi kan teste hypotesen.
3. Potensial for gjentakende inntekter.
4. Gjenbruk på tvers av bøker.
5. Kostnad, risiko og vedlikehold.

Vi velger få prioriteringer per arbeidsperiode. «Interessant teknologi» er ikke i seg selv en prioritet.

## 7. Veikart — neste 90 dager

Dette er et første arbeidsutkast. Vi skal oppdatere det når brukerinnsikt og faktisk fremdrift gir bedre grunnlag.

### Fase 1 — Samle retning og validere problem (uke 1–2)

- Avklare hovedbruker og første betalende kundesegment som hypotese.
- Gjennomføre minst fem strukturerte lærersamtaler, med konkrete eksempler fra praksis.
- Kartlegge eksisterende 9.-trinnsinnhold, T-matte, R-matte og gjenbrukbare tekniske deler.
- Definere hva en pilot må bevise.

### Fase 2 — Definere pilotproduktet (uke 3–4)

- Velge ett kapittel eller én avgrenset læringsenhet for en komplett pilot.
- Definere elevreise og lærerreise.
- Fastsette faglige, pedagogiske, tekniske og AI-relaterte akseptansekriterier.
- Avklare hvordan AI-generert tilleggsinnhold godkjennes.

### Fase 3 — Bygge og teste (uke 5–8)

- Lage en ende-til-ende pilot: lærestoff, eksempler, oppgaver, løsninger og lærer-/elevfunksjon.
- Automatisere de viktigste faglige og tekniske kontrollene.
- Teste med lærere og elever så tidlig som mulig.
- Dokumentere feil, friksjon og læringsbehov.

### Fase 4 — Pilot og betalingsvilje (uke 9–12)

- Kjøre en avgrenset pilot i reell undervisning eller hjemmebruk.
- Samle observerbare tilbakemeldinger og bruksdata med forsvarlig personvern.
- Teste konkret pris eller betalt pilot, ikke bare generell interesse.
- Beslutte: fortsette, endre målgruppe/produkt eller stoppe hypotesen.

### Fase 5 — Strategisk gjennomgang (uke 13)

- Oppsummere hva vi har lært.
- Vurdere om produktet løser et viktig problem.
- Bestemme neste 90-dagers mål og hva vi bevisst ikke skal gjøre.

## 8. Styringsmodell på tvers av arbeidsrom

| Arbeidsrom | Ansvar |
|---|---|
| Million Dollar Mission / Mission Control | Strategi, portefølje, prioritering, forretning og samlet fremdrift |
| 9. trinn | Innhold og produktutvikling for 9. trinn |
| T-matte | Innhold og produktutvikling for T-matte |
| R-matte | Innhold og produktutvikling for R1/R2 |
| MathPlatform / teknisk arbeid | Felles arkitektur, verktøy, standarder og AI-infrastruktur |

Arbeidsrommene skal følge beslutninger i dette dokumentet og i PRINCIPLES.md, men bokspesifikke faglige beslutninger skal ikke flyttes hit.

### Når en beslutning skal løftes hit

- Den påvirker mer enn én bok.
- Den endrer produktretning, målgruppe eller forretningsmodell.
- Den påvirker felles arkitektur eller vesentlige kostnader.
- Den krever prioritering mellom parallelle prosjekter.
- Den endrer tidsbruk, risiko eller mål for selskapet.

### Ukentlig Mission Control

Én gang i uken går vi gjennom:

1. Hva ble faktisk levert?
2. Hva lærte vi fra brukere eller tester?
3. Hva er den største flaskehalsen?
4. Hvilken beslutning må tas?
5. Hva er ukens viktigste leveranse?
6. Hva skal vi eksplisitt la være å gjøre?

Hold møtet kort og beslutningsorientert. Oppdater dette dokumentet når en beslutning endrer retningen.

## 9. Beslutningslogg og åpne spørsmål

### Besluttet retning

- Oppdraget er å bygge en EdTech-bedrift, ikke bare publisere enkeltbøker.
- Norge er første marked; internasjonal skalerbarhet er langsiktig retning.
- Første produktretning er en komplett digital lærebok for 9. trinn, også egnet som supplement.
- 9. trinn, T-matte og R-matte er separate produkt-/bokspor.
- Bøkene eier eget innhold; plattformen leverer gjenbrukbar infrastruktur.
- AI-generert tilleggsinnhold skal holdes adskilt fra redaksjonelt godkjent bokinnhold.
- AI skal brukes som en praktisk arbeidsorganisasjon, med læring og streng kvalitetssikring.
- Omtrent 10 timer per uke er foreløpig kapasitet.

### Må valideres eller besluttes

- Hvem er første betalende kunde: lærer, skole, elev eller foresatt?
- Hvilken pris og betalingsmodell fungerer?
- Hvilket 9.-trinnskapittel gir best pilot og raskest læring?
- Hvilke plattformfunksjoner må være felles fra starten?
- Hvilke AI-roller bør automatiseres først?
- Hvilke juridiske, personvernmessige og læreplanmessige krav må avklares før pilot med elever?

Ikke behandle åpne spørsmål som vedtatte beslutninger. Registrer beslutninger med dato, begrunnelse og konsekvenser når de tas.

## 10. Suksesskriteriet

Vi lykkes ikke bare fordi vi har skrevet mange kapitler, bygget en elegant arkitektur eller tatt i bruk avanserte AI-agenter.

Vi lykkes når vi har laget et produkt som elever og lærere faktisk bruker, som gir dokumenterbar verdi, som noen betaler for, og som kan leveres og forbedres på en repeterbar måte — uten at virksomheten er avhengig av at gründeren jobber stadig flere timer.


## 11. Markedsvalidering — intervjuguide

**Formål:** Finne ut hvilket matematikkrelatert problem som er viktig nok til at noen vil betale for å få det løst, hvem som opplever problemet, og hvem som faktisk kan kjøpe en løsning.

Dette er en undersøkelse av dagens situasjon — ikke en salgspitch. Vi skal ikke anta at lærere, elever, foresatte eller skoler er riktig første kundesegment før vi har samlet bevis.

### Fem hovedspørsmål

1. **Hvilket problem er faktisk stort nok til at noen vil betale for å få det løst?**
2. **Hvem opplever problemet oftest?**
3. **Hvordan løser de det i dag?**
4. **Hva koster dagens løsning i tid og penger?**
5. **Hvem har myndighet til å kjøpe et bedre verktøy?**

### Slik stiller vi spørsmålene

- Be om konkrete eksempler fra respondentens egen hverdag. Spør gjerne: «Kan du fortelle om siste gang dette skjedde?»
- Undersøk hva personen faktisk gjør i dag, ikke hva vedkommende tror hen ville gjort med et tenkt produkt.
- Spør hvor ofte problemet oppstår, hvem som blir berørt, og hvilke konsekvenser det får.
- Undersøk tidsbruk, eksisterende verktøy, lisenser, ekstrakostnader og manuelt arbeid.
- Skill mellom bruker, faglig anbefaler, beslutningstaker og betaler. Det kan være fire forskjellige roller.
- Ikke spør bare om personen liker ideen eller ville brukt AI. Høflig entusiasme er ikke dokumentert betalingsvilje.
- Ikke presenter løsningen for tidlig. La respondenten beskrive problemet og dagens arbeidsflyt først.

### Oppfølgingsspørsmål

- Hvor ofte skjer dette — daglig, ukentlig eller sjeldnere?
- Hva skjer hvis problemet ikke blir løst?
- Hva har dere allerede prøvd?
- Hva fungerer dårlig med dagens løsning?
- Hvem bestemmer om dere kan kjøpe et nytt verktøy?
- Hvilket budsjett ville et slikt kjøp eventuelt komme fra?
- Har dere tidligere betalt for å løse et lignende problem?

### Registrering etter hver samtale

For hver samtale registrerer vi:
- Respondentens rolle og kontekst (uten unødvendige personopplysninger).
- Problemet beskrevet med respondentens egne ord.
- Et konkret eksempel og hvor ofte det skjer.
- Dagens løsning og alternativer.
- Anslått tidsbruk og direkte kostnader.
- Hvem som bruker, anbefaler, beslutter og betaler.
- Tegn på faktisk betalingsvilje eller manglende interesse.
- Viktigste overraskelse og hva vi bør undersøke videre.

### Første valideringsrunde

Mål: minst fem samtaler med variasjon i perspektiver, for eksempel privatmattelærer, skolelærer, elev og foresatt. Dette er et læringsutvalg, ikke et statistisk representativt utvalg.

**Beslutningsregel:** Vi velger ikke første betalende kundesegment ut fra hvem som er lettest å nå eller hvem som liker ideen best. Vi velger ut fra problemets styrke, hyppighet, kostnad, tilgjengelighet og en troverdig kjøpsvei.
