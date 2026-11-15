# AI-arbeidsflyt

## Arbeidsmodell: learn + strict

AI skal bidra til å få arbeidet gjort og samtidig forklare relevante teknologier, verktøy og arkitekturvalg. Kvalitetsnivået er strict: faglig, pedagogisk, visuelt og teknisk arbeid skal kontrolleres hver for seg.

## Repository-harness

- `AGENTS.md` inneholder alltid gjeldende prosjektregler, autonomi og godkjenningsgrenser.
- `AI_SYSTEM.md` beskriver arkitekturen og skiller implementerte funksjoner fra planlagte.
- `.agents/skills/<skill-name>/SKILL.md` inneholder gjenbrukbare prosedyrer som lastes ved relevante oppgaver.
- `.agents/roles/` inneholder spesialistoppdrag som kan delegeres til faktiske subagenter når runtime støtter det.
- Bokspesifikke krav ligger i bokrepoet eller i de bokspesifikke standardene her.

## Skill-ruting

Bruk riktig skill når oppgaven matcher:
- `math-content-authoring`: skrive eller endre teori, eksempler, oppgaver og løsninger.
- `math-content-review`: kontrollere matematisk korrekthet.
- `pedagogical-review`: kontrollere læreplan, progresjon og læringsdesign.
- `book-build-qa`: bygge, teste og kontrollere generert bok.

En skill er ikke en agent. En rollebeskrivelse er heller ikke en kjørende subagent. Rapporter bare faktisk bruk av selvstendige agenter når runtime har startet dem.

## Før AI endrer noe

1. Les README, AGENTS og relevante prosjektinstrukser.
2. Finn gjeldende standarder og tidligere beslutninger.
3. Undersøk eksisterende implementasjon før du foreslår en ny.
4. Avklar om endringen gjelder plattformen, en bestemt bok eller begge.
5. Lag en kort plan før større endringer, og fortsett deretter uten å be om klarsignal for hvert rutinemessige steg.

## Under arbeidet

- Følg dokumenterte standarder.
- Ikke finn opp nye konvensjoner hvis en eksisterende standard dekker behovet.
- Skill mellom bekreftede fakta, antakelser og forslag.
- Ved matematikk: bruk en separat kontrollpass og deterministiske verktøy når de er tilgjengelige.
- Ved design: kontroller faktisk rendering, ikke bare Markdown-kilden.
- Gjennomfør trygge steg i samme arbeidsøkt: inspect → plan → implement → test → fix → retest → report.
- Stopp bare ved reelle mangler, motstridende krav eller beslutninger som tilhører produkteier.

## Godkjenningsgrenser

AI kan selvstendig inspisere, redigere innenfor oppdraget, opprette branch, kjøre tester, rette feil og forberede PR. Merge, publisering, deploy, tilgangsendringer, sletting av brukerdata og betalte tjenester krever separat eksplisitt godkjenning.

## Etter arbeidet

- Oppsummer hva som er endret og hvor.
- Oppgi hvilke kontroller som faktisk er utført, med resultater.
- Oppgi kjente begrensninger og hva som ikke lot seg kontrollere.
- Oppdater dokumentasjon når nye regler blir vedtatt.
- Ikke marker arbeid som ferdig hvis vesentlig kvalitetssikring gjenstår.

## Teknologilæring

Forklar relevante begreper kort og knyttet til arbeidet: agent, subagent, skill, MCP, harness, modell, verktøy og CI. Ikke innfør teknologi bare fordi den er ny; vurder nytte, vedlikeholdskostnad og modenhet.
