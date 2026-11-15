# Math Platform

Et felles fundament for utvikling, kvalitetssikring og videreutvikling av flere digitale matematikklærebøker.

## Formål

Plattformen skal gjøre det mulig å utvikle flere selvstendige lærebøker med felles tekniske verktøy, pedagogiske prinsipper, designstandarder og kvalitetskontroller. Hver bok eier sitt eget faginnhold og sin egen publisering. Plattformen skal støtte bøkene uten å gjøre dem unødvendig tett koblet til hverandre.

## Status

Prosjektet er i etableringsfasen. Før vi videreutvikler lærebokinnhold, dokumenterer vi standardene og arbeidsmåten som allerede er prøvd ut i `matte` og `tmatte`.

## Styrende dokumenter

- [Visjon](VISION.md)
- [Prinsipper og beslutninger](PRINCIPLES.md)
- [AI-systemarkitektur](AI_SYSTEM.md)
- [AI-arbeidsflyt](AI_WORKFLOW.md)
- [Repository-instruksjoner for AI](AGENTS.md)
- [Pedagogiske standarder](docs/standards/pedagogy.md)
- [Designstandarder](docs/standards/design.md)
- [Kvalitetsstandarder](docs/standards/quality.md)
- [Utviklingsstandarder](docs/standards/development.md)
- [Bokspesifikke standarder: R1](docs/standards/book-specific/matte-r1.md)
- [Bokspesifikke standarder: T-matte](docs/standards/book-specific/tmatte.md)
- [Arkitekturbeslutning 0001](docs/decisions/0001-platform-boundaries.md)
- [Bidragsveiledning](CONTRIBUTING.md)

## AI skills og roller

- Gjenbrukbare skills ligger i `.agents/skills/`.
- Spesialistbriefs ligger i `.agents/roles/`.
- Se [AI-systemarkitekturen](AI_SYSTEM.md) for forskjellen mellom skills, roller, subagenter, MCP og harness.

## Arbeidsmåte

Vi utvikler trinnvis: dokumenter beslutninger, prøv dem i en ekte bok, test med elever, samle tilbakemeldinger og forbedre standardene. Vi skal ikke bygge mer kompleksitet enn det erfaringen tilsier.
