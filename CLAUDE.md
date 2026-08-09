# CLAUDE.md, Alexanders Brain

Zentrale Anweisung für dieses Repository. Wird bei jedem Session-Start geladen.

## Architektur

GitHub ist Master Truth. Alle Zahlen, Fakten und Entscheidungen liegen versioniert hier, nirgendwo sonst.
Notion (falls später angebunden) ist Spiegel und Lese-Oberfläche, nie die Quelle.
Memory hält ausschließlich Präferenzen: Stil, Ton, wiederkehrende Vorlieben. Niemals Zahlen oder Fakten.
Web liefert Live-Daten, wird nie dauerhaft gespeichert und immer mit Datum versehen.

## Datenquellen-Reihenfolge

1. GitHub (`skills/<name>/references/`, `0X-bereich/data/`)
2. Dateien, die gerade im Chat hochgeladen wurden
3. Notion (nur für Edits, die noch nicht in GitHub sind)
4. Memory (nur Stil und Stimme)
5. Web (Live-Daten, immer mit Datum kennzeichnen)

Bei Widerspruch zwischen Quellen gewinnt die höhere Position in dieser Liste.

## Repo-Struktur

```
CLAUDE.md              diese Datei
README.md              Karte des Repos
skills/                Skill-Definitionen (Claude sucht hier nach SKILL.md)
  _meta/                voice-rules.md, ggf. source-map.yaml, drift-log.md
00-inbox/               unsortierter Eingang, roh, wird regelmäßig aufgeräumt
01-business/            Hauptjob / Business
02-immobilien/          Immobilien
03-energie/             Energie
04-finanzen/            Vermögen, Konten, Investments
05-recht-vertraege/     Recht, Verträge
06-usa/                 USA-Themen
07-familie/             Familie
08-it-admin/            IT und Admin
09-lernen-wissen/       Lernen, Wissen, Kurse
90-archive/             abgeschlossene oder veraltete Inhalte
docs/                   Architektur, Boundary, Sync (falls benötigt)
tools/                  Automation, Scripts (falls benötigt)
```

Jeder Lebensbereich `0X-bereich/` folgt derselben inneren Struktur:

```
0X-bereich/
  README.md            Navigation, Links zu relevanten Skills
  data/                Wahrheitsdaten: Fakten, Zahlen, Listen
  briefings/            datierte Analysen, Format YYYY-MM-DD-thema.md
  decisions/            Entscheidungs-Logs, gleiches Datumsformat
```

`00-inbox/` und `90-archive/` sind Ausnahmen ohne diese Unterstruktur, siehe deren jeweilige README.md.

## Voice Rules (Pflicht)

Siehe `skills/_meta/voice-rules.md`. Gilt für jeden Output, den Claude in Alexanders Namen formuliert, egal ob Mail, Chat-Antwort, Briefing oder Analyse.

## Boundary Protocol

Default ist schreibbar in GitHub, ohne Nachfrage.

Für sensible Themen (Geld, Verträge, private Korrespondenz, Gesundheit, alles unter 04-finanzen, 05-recht-vertraege) gilt: GitHub schreiben ist ok, aber jedes Rausgeben (Mail, Nachricht) und jeder Notion-Push braucht Freigabe pro Vorgang, bevor etwas den Kreis verlässt.

Boundary-Klassen pro Skill, siehe jeweilige SKILL.md:

- **P0 sensibel**: Geld, Verträge, private Korrespondenz, Gesundheit. Freigabe pro Vorgang vor jedem Rausgeben.
- **P1 normal**: Standard. GitHub und Notion-Spiegel ohne Nachfrage ok.
- **P2 methodik-only**: Skills ohne eigene Daten, reine Schreib- oder Denkhilfen. Kein Sync nötig.

## Bei Unklarheiten

Nicht raten. Wenn eine Zahl, ein Fakt oder eine Quelle unklar ist, nachfragen statt zu ergänzen.
