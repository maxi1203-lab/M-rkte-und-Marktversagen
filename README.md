# Märkte und Marktversagen — VO Universität Innsbruck

Persönliches Arbeits- und Lern-Repository zur Vorlesung **Märkte und Marktversagen**
an der Universität Innsbruck. Ziel: eine extrem professionelle, strukturierte
Klausurvorbereitung mit Claude Code als Lern- und Arbeitsassistent.

> **Prüfungstermin:** ca. **Ende Mai 2026** (ca. 6 Wochen ab 15.04.2026).
> Aktueller Stand der Vorbereitung: siehe [`lernplan/README.md`](lernplan/README.md).

---

## Inhalt / Struktur

```
.
├── vorlesung/                VO-Material (offiziell)
│   ├── folien/               VO-Folien (PDF/PPTX) pro Einheit
│   └── mitschrift/           Eigene Mitschriften pro Einheit
│
├── hausuebungen/             Übungsblätter des Kurses
│   ├── hausuebung-01/        je Übung: Angabe, Lösung, Notizen
│   ├── hausuebung-02/
│   ├── hausuebung-03/
│   └── vorlagen/             Leer-Templates für neue Übungen
│
├── probeklausuren/           Probeklausuren & Altklausuren
│   ├── probeklausur-01/
│   └── altklausuren/         Alte Klausuren (wenn verfügbar)
│
├── zusammenfassung/          Eigene Lern-Zusammenfassung
│   ├── kapitel/              Kapitelweise Summaries
│   ├── formelsammlung/       Zentrale Formeln
│   └── definitionen/         Begriffe & Definitionen
│
├── lernplan/                 6-Wochen-Lernplan + Fortschritt
│
├── literatur/                Lehrbücher, Paper, Links
│
├── uebungen-zusatz/          Zusatzaufgaben & Übungen
│
└── notizen/                  Offene Fragen & eigene Beispiele
    ├── fragen-an-prof/
    └── eigene-beispiele/
```

Jeder Unterordner hat ein eigenes `README.md` mit Detail-Instruktionen.

---

## Konventionen

### Dateinamen

- Kleinbuchstaben, Bindestriche statt Leerzeichen, keine Umlaute (`ue` statt `ü`).
- Durchnummerieren mit führenden Nullen: `hausuebung-01`, `probeklausur-02`.
- Suffixe:
  - `-angabe.pdf` → Aufgabenblatt
  - `-loesung.md` → eigene (oder offizielle) Lösung
  - `-notizen.md` → Gedanken, Fragen, Stolpersteine
  - `-musterloesung.pdf` → offizielle Musterlösung (falls vorhanden)

### Status-Markierungen in Lösungen

Am Anfang jeder `-loesung.md` Datei:

```
Status: [entwurf | in-arbeit | review | fertig]
Konfidenz: [niedrig | mittel | hoch]
Offene Fragen: - ...
```

### Commit-Messages

Kurz, beschreibend, deutsch OK:

- `hausuebung-02: angabe hinzugefügt`
- `hausuebung-01: lösung aufg. 3 fertig`
- `probeklausur-01: teil-lösung, frage 2 offen`
- `zusammenfassung: externalitäten überarbeitet`

---

## Workflow mit Claude Code

### 1. Neues Material hochladen

1. Datei in den passenden Unterordner legen (PDF/PPTX/Bild/TXT).
2. Claude fragen: *"Lies Datei X und fasse zusammen"* oder
   *"Erstelle Lösungsgerüst für Aufgabe Y".*

### 2. Lösungen ausarbeiten

- Unfertige Lösungen als `*-loesung.md` mit `Status: in-arbeit` ablegen.
- Claude um **strukturierte Review** bitten:
  *"Prüfe meine Lösung, finde Fehler, schlage Verbesserung vor — aber löse sie nicht für mich."*
- Erst wenn du selbst verstanden hast → `Status: fertig` setzen.

### 3. Aufgaben ohne Angabe (nur Lösung vorhanden)

→ ablegen in passendem Ordner, Datei benennen als
`*-loesung-ohne-angabe.md`. Claude kann helfen, die **wahrscheinliche Angabe zu
rekonstruieren** und so den Lernwert zurückzugewinnen.

### 4. Klausurvorbereitung

- Wöchentlicher Review gegen [`lernplan/README.md`](lernplan/README.md).
- Probeklausuren **unter Zeitdruck** durcharbeiten, erst danach Lösung ansehen.

---

## Nächste Schritte (Checklist)

- [ ] VO-Folien aller bisherigen Einheiten in `vorlesung/folien/` hochladen
- [ ] Vorhandene Hausübungen (Angaben + Teil-Lösungen) in `hausuebungen/` ablegen
- [ ] Verfügbare Probeklausuren in `probeklausuren/` ablegen
- [ ] Kursinfos (Syllabus, Prüfungsordnung) in `literatur/` hinterlegen
- [ ] Lernplan in `lernplan/README.md` an die tatsächlichen Themen anpassen

---

## Lizenz / Nutzung

Privates Lern-Repository. Offizielle Kursmaterialien (Folien, Angaben,
Musterlösungen) unterliegen dem Urheberrecht der jeweiligen Lehrenden bzw. der
Universität Innsbruck und werden **nicht öffentlich geteilt**.
