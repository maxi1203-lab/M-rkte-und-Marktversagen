# Doppel-Check-Workflow

Das Herzstück, damit dieses Repo **kein Lösungsarchiv**, sondern ein
**Lernwerkzeug** wird. Hier steht, *wie* man mit dem Repo arbeitet, nicht
*was* drinsteht.

## Prinzip

Drei Perspektiven, unabhängig voneinander erzeugt, dann verglichen:

1. **Deine Handschrift** — was du tatsächlich auf dem iPad gerechnet hast.
2. **Claude unabhängig** — was Claude selbst als Lösung produziert, *ohne*
   deine Handschrift gesehen zu haben.
3. **Diff & Einordnung** — eine dritte Instanz vergleicht beide und
   klassifiziert Abweichungen.

Das schützt vor zwei Fallen:

- **Bestätigungsfehler:** Wenn Claude deine Lösung „review-t", neigt er
  dazu, deine Fehler nicht zu sehen, weil sie in seinem Kontext bereits
  „richtig" markiert sind.
- **Claude-Spickzettel:** Wenn Claude zuerst die Musterlösung sieht, rechnet
  er nicht mehr selbst — er reproduziert.

## Agenten

Definiert in `.claude/agents/`:

| Agent    | Input                                | Output                               | Darf NICHT |
|----------|--------------------------------------|--------------------------------------|------------|
| solver   | `angabe.pdf`                          | `loesung-claude-unabhaengig.md`     | Handschrift lesen |
| scribe   | `loesung-handschrift.pdf`             | `loesung-handschrift-transkript.md` | Selbst rechnen |
| reviewer | beide oberen Outputs + Angabe         | `review.md`                          | Selbst neu rechnen |

## Bedienung

### Kompletter Durchlauf

```
/hu-review 03
```

Im Hintergrund:

1. Solver und Scribe laufen **parallel**.
2. Reviewer läuft danach.
3. Coach-Claude zeigt dir nur die **Übersichts-Tabelle** und fragt, wo du
   einen Denkanstoß willst.

### Teil-Durchläufe

```
/hu-review 03 --solver-only     # nur Claude-Lösung
/hu-review 03 --scribe-only     # nur Transkription
/hu-review 03 --diff-only       # beide Lösungen existieren → nur Review
/hu-review 03 --force           # existierende Outputs überschreiben
```

## Wann manuell eingreifen

- Reviewer meldet `NEU_RECHNEN_EMPFOHLEN` → du (oder Claude im Coach-Modus)
  rechnet die fragliche Teilaufgabe nochmal per Hand, bevor Stufe-3 /
  Stufe-4 Hinweis ausgegeben wird.
- Scribe markiert viele `[unleserlich]` → Handschrift nochmal sauber
  abfotografieren oder zur Not selbst transkribieren.
- Solver ist sehr unsicher (Konfidenz niedrig) → prüfen, ob VO-Folien in
  `vorlesung/folien/` die nötige Notation/Konvention erklären; Solver
  nochmal mit diesem Kontext starten.

## Anti-Pattern

- **Nicht** alle 14 HÜ in einer Woche durch den Workflow jagen und
  Lernblätter stapeln. Lieber 1–2 pro Woche, dafür das `lernblatt.md`
  wirklich schreiben und die Quiz-Fragen beantworten.
- **Nicht** Stufe-4-Hinweis anschauen, bevor Stufe 1-3 wirkungslos waren.
- **Keine** Lösungen von Kommiliton\*innen in diesen Workflow einspeisen
  ohne klare Kennzeichnung — das verfälscht den Solver-Input.

## Datei-Lifecycle pro HÜ

```
Woche X: /hu-review NN
         → solver + scribe + review fertig
         → lernblatt.md manuell schreiben (5 Min)

Woche X+2: Retrospektive: Quiz aus lernblatt.md beantworten.
           Offene Punkte aus review.md nochmal durchgehen.

Vor Klausur: lernblatt.md als Karteikarte benutzen.
```
