---
description: Startet den Doppel-Check-Workflow für eine Hausübung. Solver + Scribe laufen parallel, dann Reviewer, dann präsentiert Coach-Claude das Ergebnis gestuft.
argument-hint: "<hü-nummer> [--solver-only|--scribe-only|--diff-only|--force]"
---

# /hu-review — Doppel-Check-Workflow für eine Hausübung

Argumente: `$ARGUMENTS`

## Parsing

- Erstes Argument: HÜ-Nummer (zweistellig, z.B. `03`). Pflicht.
- Optionale Flags:
  - `--solver-only` → nur Solver laufen lassen
  - `--scribe-only` → nur Scribe laufen lassen
  - `--diff-only` → überspringt Solver und Scribe, läuft nur Reviewer
  - `--force` → überschreibt existierende Output-Dateien (sonst: Warnung)

Wenn kein HÜ-Argument: frag den User *"Welche HÜ-Nummer?"* und stoppe.

## Pre-Checks

Vor allem anderen:

1. Ordner `hausuebungen/hausuebung-NN/` existiert? Sonst: Warnung + Stopp.
2. Mindestens eine Angabe-Datei vorhanden (`angabe.pdf` oder
   `angabe-textversion.txt`)? Sonst: Warnung + Stopp.
3. Für Scribe: `loesung-handschrift.pdf` existiert? Wenn nicht, Scribe
   überspringen, User informieren.
4. Wenn Output-Dateien existieren und kein `--force`: User fragen, ob
   überschrieben werden soll.

## Ablauf

### Phase 1 — parallel: Solver + Scribe

Starte BEIDE Agenten **im selben Assistant-Turn** (parallele Tool-Calls),
damit sie unabhängig arbeiten:

```
Agent(subagent_type="solver",  prompt="Löse HÜ NN. Angabe: <pfad>. KEINE Handschrift lesen.")
Agent(subagent_type="scribe",  prompt="Transkribiere HÜ NN. Handschrift-PDF: <pfad>.")
```

Warte bis beide fertig sind.

### Phase 2 — sequenziell: Reviewer

```
Agent(subagent_type="reviewer", prompt="Vergleiche HÜ NN: solver-output + scribe-output.")
```

### Phase 3 — Coach-Claude (du selbst)

Lies `review.md` und präsentiere dem User **gestuft**:

1. **Zuerst nur** die Übersichts-Tabelle (welche Teilaufgaben OK, welche
   Abweichungen).
2. **Frage**: *"Möchtest du bei Teilaufgabe X einen ersten Denkanstoß,
   oder willst du zuerst selbst nochmal schauen?"*
3. Bei Anfrage: Stufe-1-Hinweis zeigen, dann abwarten.
4. Erst nach expliziter Anforderung: Stufe-2, -3, schließlich -4.
5. Zum Schluss: eine der Quiz-Fragen aus `review.md` stellen.

**Goldene Regel:** Komplettlösung NIE spontan ausrollen. Der Student
soll sich die Antwort erarbeiten.

## Commit

Nach erfolgreichem Durchlauf:

```
git add hausuebungen/hausuebung-NN/
git commit -m "hausuebung-NN: doppel-check durchlauf (solver+scribe+review)"
```

## Beispiel

```
User: /hu-review 03
Claude: [startet Solver und Scribe parallel]
        [~2 min]
        [startet Reviewer]
        [~30s]

        → Übersicht HÜ 03:
        Aufg. 1 OK · Aufg. 2 RECHENFEHLER_SCHREIBWEISE · Aufg. 3 KONZEPTFEHLER
        Möchtest du Aufg. 3 zuerst selbst nochmal rechnen, oder einen Stufe-1-Hinweis?

User:   Stufe-1
Claude: "Wann produziert eine Firma überhaupt? …"
```
