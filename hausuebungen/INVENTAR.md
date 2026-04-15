# Inventar Hausübungen

## Zwei Semester parallel

Dieses Repo enthält **zwei parallele Sätze Hausübungen** mit teils identischen
Themen, aber **unterschiedlichen Zahlen / Aufgabenstellungen**:

- **`angabe-altsemester.pdf`** — älteres Semester; hierzu existieren deine
  handschriftlichen Lösungen (`loesung-handschrift.pdf`).
- **`angabe-aktuell.pdf`** — aktuelles Semester; noch keine Lösungen. Dies
  ist der Fokus für die anstehende Klausur.

Vorteil: Du kannst jedes Thema **zweimal** lösen — einmal mit Abgleich zu
deiner Handschrift (Doppel-Check mit `reviewer`), einmal als frischer
Solver-Lauf für die aktuellen Zahlen. Abweichungen zwischen den beiden
Angaben zeigen, welche Varianten die Prüferin gerne einsetzt.

## Übersicht

| HÜ | Thema (aus altsemester-Titel) | altsemester-Angabe | aktuell-Angabe | Handschrift | Offiz. Lösung |
|----|-------------------------------|:---:|:---:|:---:|:---:|
| 01 | Vollständige Konkurrenz + Monopol | ✓ | ✓ | ✓ | — |
| 02 | Monopol + Elastizitäten            | ✓ | ✓ | ✓ | — |
| 03 | Preisdiskr. + Simultane Spiele     | ✓ | ✓ | ✓ | — |
| 04 | Simultane Spiele                   | ✓ | ✓ | ✓ | — |
| 05 | Oligopol                           | ✓ | ✓ | ✓ | — |
| 06 | Oligopol II                        | ✓ | ✓ | ✓ | — |
| 07 | Dynamische Spiele                  | ✓ | ✓ | ✓ | — |
| 08 | Stackelberg + Wh-Spiele            | ✓ | ✓ | ✓ | — |
| 09 | Wh-Spiele + Kartelle               | ✓ | ✓ | ✓ | — |
| 10 | Entscheidung unter Risiko          | ✓ | ✓ | ✓ | — |
| 11 | Risiko + Lemons                    | ✓ | ✓ | ✓ | — |
| 12 | AsymInfo + Öff. Güter              | ✓ | ✓ | —  | — |
| 13 | Öffentliche Güter                  | ✓ | ✓ | —  | — |
| 14 | Externalitäten                     | ✓ | —  | —  | — |

## Workflow pro HÜ

Siehe [`../lernplan/doppelcheck-workflow.md`](../lernplan/doppelcheck-workflow.md).

### Standard (altsemester mit Handschrift)

```
/hu-review NN           # benutzt angabe-altsemester.pdf + loesung-handschrift.pdf
```

### Aktuelles Semester (frisch)

```
/hu-review NN --current  # benutzt angabe-aktuell.pdf, ohne Handschrift-Abgleich
```

(Flag wird bei Bedarf in `.claude/commands/hu-review.md` ergänzt.)

## Zum Mapping Handschrift ↔ HÜ-Nummer

Die handschriftliche `klausurvorbereitung.pdf` nummerierte **Hausübung 1–11**
und deckt nicht alle 14 offiziellen HÜ ab. Die Zuordnung wurde per
Topic-Heuristik vorgenommen und ist möglicherweise **nicht 1:1**.
Bei der ersten Nutzung des Doppel-Check-Workflows stichprobenartig prüfen,
ob `loesung-handschrift.pdf` in `hausuebung-NN/` tatsächlich zur
`angabe-altsemester.pdf` im gleichen Ordner gehört. Bei Mismatch:
`loesung-handschrift.pdf` in den passenden Ordner verschieben.
