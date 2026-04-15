# Hausübungen

Pro Hausübung ein Unterordner (`hausuebung-01`, `hausuebung-02`, ...).

## Inhalt pro Ordner

| Datei | Zweck |
|---|---|
| `angabe.pdf` / `angabe.md` | Aufgabenstellung (original oder abgetippt) |
| `loesung.md` | Eigene Lösung (auch unvollständig) |
| `musterloesung.pdf` | Offizielle Lösung, falls verfügbar |
| `notizen.md` | Gedanken, offene Fragen, Fehler, die du gemacht hast |

## Sonderfälle

- **Nur Lösung vorhanden, keine Angabe** → Datei `loesung-ohne-angabe.md`
  anlegen. Claude kann helfen, die wahrscheinliche Angabe zu rekonstruieren.
- **Nur Angabe, keine Lösung** → `loesung.md` mit `Status: entwurf` + deinen
  ersten Überlegungen.

## Neue Hausübung anlegen

1. Ordner kopieren: `cp -r vorlagen/hausuebung-XX hausuebungen/hausuebung-NN`
2. Angabe-Datei einfügen.
3. In `loesung.md` den Meta-Header ausfüllen.
