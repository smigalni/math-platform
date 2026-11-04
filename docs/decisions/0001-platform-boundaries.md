# ADR 0001: Ansvarsdeling mellom plattform og lærebøker

- **Status:** Foreløpig beslutning
- **Dato:** 2026-11-04

## Kontekst

Prosjektet skal støtte flere selvstendige digitale matematikklærebøker. En tett kobling mellom bokrepositoriene og plattformen vil gjøre bøker vanskeligere å vedlikeholde og utvikle uavhengig.

## Beslutning

Vi velger en hybrid modell med løs kobling:
- Hver bok eier faginnhold, bokstruktur som er spesifikk for faget, og egen publisering.
- Plattformen eier felles standarder, dokumentasjon, maler, kvalitetssikringsverktøy og gjenbrukbare tekniske komponenter.
- Felles verktøy skal kunne tas i bruk av bokrepositorier uten at bøkene må dele samme innholdsstruktur.

## Konsekvenser

- Bøker kan utvikles og publiseres uavhengig.
- Felles forbedringer kan gjenbrukes.
- Vi må versjonere og dokumentere grensesnitt mellom plattformverktøy og bokrepositorier.
- Vi unngår å bygge et stort felles rammeverk før konkrete behov er testet.
