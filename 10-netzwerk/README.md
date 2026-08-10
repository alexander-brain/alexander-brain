# 10-netzwerk

Kontaktnetzwerk, gruppiert nach Business-Kontext. Boundary: **P0, sensibel**. Enthält private Kontaktdaten (Adressen, private Emails, Telefonnummern) von rund 1.190 Personen, nicht nur von Alexander selbst. GitHub schreiben ist ok, jedes Rausgeben (Export, Mail, Weitergabe an Dritte) oder jeder Notion-Push braucht Freigabe pro Vorgang.

## Inhalt

- `data/kontakte.csv` vollständiger Kontaktbestand: Name, Firma, Abteilung, Position, Emails, Telefone, Notiz. Ein Kontakt pro Zeile, sortiert nach Firma, dann Nachname.
- `data/gruppen-business-kontext.md` dieselben Kontakte geclustert nach dem Firmenfeld: Organisationen mit mehreren Kontakten zuerst, dann Einzelkontakte mit Firma, dann Kontakte ohne Firmenangabe.

## Herkunft

Importiert aus `alexander_lenk_und_1.189_weitere.vcf` (Apple Kontakte-Export), Stand 2026-08-10. 1.190 vCards im Export, davon 2 komplett leere Stubs entfernt und 2 Karten für Alexander selbst entfernt (kein Netzwerk-Kontakt). Ergebnis: 1.186 Kontakte in `kontakte.csv`.

## Datenqualität, bitte beim Lesen beachten

Das Firmenfeld aus dem iPhone-Adressbuch ist nicht immer ein Firmenname. Bei vielen Kontakten steht dort stattdessen eine Rolle ("Rechtsanwalt", "Notar", "Steuerberater") oder eine private Beziehung ("Onkel", "Cousine", "Putzfrau"). Das wurde unverändert übernommen, nicht interpretiert oder umsortiert. Ähnlich klingende Firmennamen (zum Beispiel "WSC", "WSC Berlin", "WSC Caputh") wurden nicht automatisch zusammengeführt, das wäre eine Annahme gewesen. Details siehe Kopf von `gruppen-business-kontext.md`.

Rund 45 Prozent der Kontakte (539 von 1.186) haben kein Firmenfeld befüllt und tauchen deshalb nur in `kontakte.csv` auf, nicht in der Gruppierung.

## Nutzung

Für "wer aus meinem Netzwerk passt zu Projekt X": zuerst `gruppen-business-kontext.md` nach passenden Organisationen oder Rollen durchsuchen, bei Bedarf `kontakte.csv` für Kontaktdaten und Notizen nachschlagen. Beide Dateien sind Wahrheitsdaten und werden bei neuem Kontaktexport aktualisiert, nicht manuell einzeln gepflegt.

## Relevante Skills

Noch keine. Ein Skill, der gezielt nach passenden Netzwerkkontakten für ein Projekt oder Thema sucht, wäre ein sinnvoller nächster Schritt.
