# Utviklingsstandarder

## Repository-struktur

- Hver bok skal kunne utvikles og publiseres selvstendig.
- Felles verktøy og standarder skal ligge i plattformen eller distribueres på en kontrollert måte.
- Ikke innfør tett kobling mellom bokrepositorier uten et dokumentert behov.
- Dokumenter prosjektspesifikke avvik fra felles standarder.

## Git-arbeidsflyt

- Bruk `main` som stabil hovedgren.
- Start nytt arbeid fra oppdatert `main`.
- Bruk en egen, beskrivende feature- eller fix-branch for endringer.
- Hold én tydelig arbeidsoppgave per branch når det er praktisk.
- Kontroller diff og testresultater før merge.
- Merge først når endringen er klar; slett ferdigarbeidede branches for å holde repoet ryddig.
- Ikke påstå at en branch er slettet, en PR er merget eller en deploy er ferdig uten å kontrollere det.

## Endringer og regresjoner

- Gjør små, forståelige endringer.
- Bevar eksisterende fungerende innhold.
- Kontroller berørte sider og relevante felleskomponenter etter endringer.
- Når en feil skyldes en felles komponent eller standard, rett årsaken sentralt i stedet for å lappe mange enkeltsider.
- Oppdater dokumentasjonen når en standard eller arbeidsmåte endres.
