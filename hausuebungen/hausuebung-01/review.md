---
autor: reviewer-agent (manuell ausgeführt, Demo-Lauf)
datum: 2026-04-15
inputs:
  solver: loesung-claude-unabhaengig.md
  scribe: loesung-handschrift-transkript.md
gesamt_bewertung: gemischt (aufgabe 1: angabe-mismatch; aufgabe 2: OK; aufgabe 3 handschrift ohne angabe)
neu_rechnen_empfohlen: false (Handschrift-Aufgabe 1 sollte separat mit ihrer eigenen Angabe abgeglichen werden, wenn diese auftaucht)
---

# Hausübung 01 — Review

## Übersicht

| Teilaufgabe | Code | Kurz-Bemerkung |
|-------------|------|----------------|
| 1 (a)–(e)   | ANGABE_MEHRDEUTIG | Handschrift löst eine ANDERE Kostenfunktion ($C = 72+4q+2q^2$) als beide im Repo vorhandenen Angaben. Kein direkter Vergleich möglich. |
| 2 (a)       | OK  | Tabelle nicht in Handschrift, aber Claude-Tabelle konsistent |
| 2 (b)       | OK  | Q*=5'000, P*=35, π*=37'500 — übereinstimmend |
| 2 (c)       | OK  | Erlösmax Q=6'000, P=30; Gewinnmax Q=5'000, P=35 — beide identisch |
| 3           | —   | Handschrift hat eine Aufgabe 3, die in keiner unserer Angaben vorkommt. Nicht prüfbar. |

## Detail

### Aufgabe 1 — ANGABE_MEHRDEUTIG

**Handschrift löst:** $C(q) = 72 + 4q + 2q^2$ (Ergebnis: $q^* = 6$, $P = 28$).
**Claude (altsemester-Angabe):** $c(x) = x^3 - 8x^2 + 30x + 5$ (Ergebnisse in Aufg. 1 a–e).

→ **Beide Lösungen sind jeweils korrekt für die Aufgabe, die sie lösen**, aber
sie lösen nicht dieselbe Aufgabe.

**Lernpunkt:** Die zu HÜ 01 passende Angabe muss noch identifiziert werden.
Möglicherweise gibt es eine **dritte Semester-Variante**, zu der du dir die
Angabe (oder zumindest den Angabetext) beschaffen solltest. Bis dahin ist
die Handschrift zu Aufgabe 1 kein gültiger Abgleich.

**Aktion:** Frage an User — gibt es noch eine weitere HÜ01-Angabe (evtl.
aus einem Tutorium oder aus einem anderen Semester)?

---

### Aufgabe 2 — alle Teile OK

Handschrift und Claude stimmen in allen Ergebnissen überein:

- $Q^* = 5'000$, $P^* = 35$, $\pi^* = 37'500$
- $Q^{**} = 6'000$, $P^{**} = 30$, $TR^{**} = 180'000$

Handschrift hat zusätzlich eine **sehr prägnante Intuition** am Rand:
*"Bei maximalem Umsatz sind die Grenzkosten höher als der Grenzerlös.
Maximaler Gewinn: MR = MC."* — das ist der Kerngedanke, gut gemerkt.

**Kleine Ergänzung, die in der Handschrift fehlt:** Explizite Berechnung
des Gewinns bei Q*=5'000 und expliziter Hinweis, dass der Gewinn trotz
Gewinnmaximum **immer noch abhängig von Fixkosten** ist. Hier: wegen
$F=100'000$ schrumpft der Marktgewinn auf $37'500$, aber wäre $F$ größer
als die Deckungsspanne von $137'500$, würde Presto den Markt verlassen.

**Lernpunkt:** *"Menge bei MR=MC finden"* ist nur ein Teil. **"Gewinn
auch tatsächlich ausrechnen"** → prüfen, ob Markt-Bleib-Bedingung
($\pi \geq 0$) erfüllt ist.

---

### Aufgabe 3 — in Handschrift vorhanden, in Angabe nicht

Handschrift zeigt eine weitere Aufgabe mit $Q(P) = 40 - 2P$, $MC = 2$,
Ergebnis $Q = 18$, $P = 11$, $\pi = 162$. In unserer `angabe-altsemester.pdf`
gibt es nur zwei Aufgaben.

**Möglich:** Aufgabe 3 kommt aus einer dritten Semester-Variante der HÜ
und gehört thematisch hierher (einfaches Monopol + Markteintritt).

**Claude-Check (ungeprüft, als Bonus):**
$P(Q) = 20 - Q/2$, $MR = 20 - Q$. $MR = MC: 20 - Q = 2 \Rightarrow Q = 18$,
$P = 11$, $\pi = (11-2) \cdot 18 = 162$. Handschrift ist korrekt.

---

## Hinweise für den Coach

### Aufgabe 2 — Intuition vertiefen

Beide Lösungen ankommen, aber der **Unterschied zwischen Gewinn- und
Erlösmax** ist das, was in der Klausur gern geprüft wird.

**Stufe 1 (Denkanstoß):**
> "Warum liegt das Erlösmaximum *rechts* vom Gewinnmaximum, nicht links?"

**Stufe 2 (Richtung):**
> "Schau dir an, was zwischen $Q = 5'000$ und $Q = 6'000$ passiert:
> $MR$ fällt von $10$ auf $0$, $MC$ steigt von $10$ auf $11$. Was heißt das?"

**Stufe 3 (fast fertig):**
> "Jede Einheit zwischen 5'000 und 6'000 bringt weniger zusätzlichen Erlös
> ($MR < 10$) als sie Kosten verursacht ($MC > 10$). Also sinkt der
> Gewinn, aber der Erlös steigt noch bis $MR = 0$. Formel:
> $\dfrac{d\pi}{dQ} = MR - MC$."

**Stufe 4 (Komplettlösung):** siehe loesung-claude-unabhaengig.md

### Muster-Quiz-Fragen

1. Bei welcher Elastizität $|\varepsilon|$ liegt das Erlösmaximum?
   *(Antwort: $|\varepsilon| = 1$)*
2. Wenn Fixkosten $F$ sich ändern, ändert sich $Q^*$? Warum (nicht)?
   *(Antwort: nein, solange $\pi \geq 0$ — nur Markt-Bleib-Entscheidung)*
3. Was wäre $Q^*$ bei Wettbewerb (statt Monopol) und gleicher
   Kostenfunktion? *(Antwort: $P = MC$, also $60 - 0.005Q = 5 + 0.001Q$,
   $Q = 9'167$ — aber Achtung, das ist dann kein Monopol mehr.)*
