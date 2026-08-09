# Alexanders Brain

Persönliches Second Brain: versioniertes Wissens- und Arbeitssystem, gepflegt mit Claude Code. GitHub ist die einzige Wahrheit, siehe [`CLAUDE.md`](./CLAUDE.md) für die Architektur.

## Karte

| Ordner | Inhalt |
|---|---|
| `skills/` | Skill-Definitionen (SKILL.md je Skill), plus `_meta/` mit Voice Rules |
| `00-inbox/` | Unsortierter Eingang, roh, wird regelmäßig aufgeräumt |
| `01-business/` | Hauptjob / Business |
| `02-immobilien/` | Immobilien |
| `03-energie/` | Energie |
| `04-finanzen/` | Vermögen, Konten, Investments (P0, sensibel) |
| `05-recht-vertraege/` | Recht, Verträge (P0, sensibel) |
| `06-usa/` | USA-Themen |
| `07-familie/` | Familie (P0, sensibel) |
| `08-it-admin/` | IT und Admin |
| `09-lernen-wissen/` | Lernen, Wissen, Kurse |
| `90-archive/` | Abgeschlossene oder veraltete Inhalte |
| `docs/` | Architektur, Boundary, Sync |
| `tools/` | Automation, Scripts |

Jeder Lebensbereich `0X-bereich/` hat `README.md`, `data/`, `briefings/`, `decisions/`. Details dazu in `CLAUDE.md`.

## Nutzung

Fakten ablegen: "Speicher das in mein Finanzen-Brain." Claude schreibt es als Reference File oder in `data/` und committet.

Analyse: "Wie steht Projekt X?" Claude zieht aus GitHub, rechnet, antwortet, legt bei Bedarf ein datiertes Briefing ab.

Entscheidungen: wichtige Weichenstellungen als `decisions/YYYY-MM-DD-thema.md`.

Stil: "Merk dir, ich mag kurze Mails ohne Bullets." Geht in Memory oder `skills/_meta/voice-rules.md`, nie in die Daten.
