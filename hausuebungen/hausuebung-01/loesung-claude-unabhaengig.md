---
autor: solver-agent (manuell ausgeführt, Demo-Lauf)
datum: 2026-04-15
seed: unabhängig (Handschrift bewusst ignoriert)
konfidenz_gesamt: hoch
angabe_gelesen: angabe-altsemester.pdf
---

# Hausübung 01 (altsemester) — unabhängige Lösung (Claude)

## Aufgabe 1 — Unternehmen "Alpha" im vollständigen Wettbewerb

**Kostenfunktion:** $c(x) = x^3 - 8x^2 + 30x + 5$

### (a) Grenzkosten

$$MC(x) = \frac{dc}{dx} = 3x^2 - 16x + 30$$

### (b) Durchschnittliche variable Kosten

Variable Kosten $= c(x) - F = x^3 - 8x^2 + 30x$ (Fixkosten $F=5$).

$$AVC(x) = \frac{VC}{x} = x^2 - 8x + 30$$

### (c) Graph

Beides nach unten geöffnete Parabeln? Nein — $MC$ und $AVC$ sind aufwärts-
gekrümmt mit positivem Minimum.

- $MC$: Min bei $x = 16/6 = 8/3 \approx 2.67$, $MC_{min} = 3(8/3)^2 - 16(8/3) + 30 = 64/3 - 128/3 + 90/3 = 26/3 \approx 8.67$.
- $AVC$: Min bei $x = 4$ (aus $2x - 8 = 0$), $AVC_{min} = 16 - 32 + 30 = 14$.
- $MC$ schneidet $AVC$ **in dessen Minimum** — klassische Eigenschaft.

### (d) Shutdown-Bedingung

Kurzfristig produziert Alpha nur, wenn $P \geq \min AVC = 14$.
**Kleinste positive Menge: $x = 4$** (bei $P = 14$).
Für $P < 14$ → Produktion = 0.

### (e) Preis, bei dem Alpha genau 6 Einheiten produziert

Im Wettbewerb: $P = MC$.
$MC(6) = 3 \cdot 36 - 16 \cdot 6 + 30 = 108 - 96 + 30 = \boxed{42}$

### Konfidenz
hoch — Standardrechnung, Plausibilitäts-Check: $AVC(6) = 36 - 48 + 30 = 18 < 42 = P$ ✓
(P > AVC, also wird tatsächlich produziert).

---

## Aufgabe 2 — Presto Products, Monopol

$P(Q) = 60 - 0.005Q$
$TC = 100'000 + 5Q + 0.0005Q^2$
$MR = 60 - 0.01Q$, $MC = 5 + 0.001Q$

### (a) Tabelle ($Q = 0, 1'000, \dots, 10'000$ in $1'000$-Schritten)

| Q     | P  | TR       | MR  | TC      | MC | Π       |
|-------|----|----------|-----|---------|----|---------|
| 0     | 60 | 0        | 60  | 100'000 | 5  | -100'000|
| 1'000 | 55 | 55'000   | 50  | 105'500 | 6  | -50'500 |
| 2'000 | 50 | 100'000  | 40  | 112'000 | 7  | -12'000 |
| 3'000 | 45 | 135'000  | 30  | 119'500 | 8  | 15'500  |
| 4'000 | 40 | 160'000  | 20  | 128'000 | 9  | 32'000  |
| **5'000** | **35** | **175'000** | **10** | **137'500** | **10** | **37'500** |
| 6'000 | 30 | 180'000  | 0   | 148'000 | 11 | 32'000  |
| 7'000 | 25 | 175'000  | -10 | 159'500 | 12 | 15'500  |
| 8'000 | 20 | 160'000  | -20 | 172'000 | 13 | -12'000 |
| 9'000 | 15 | 135'000  | -30 | 185'500 | 14 | -50'500 |
| 10'000| 10 | 100'000  | -40 | 200'000 | 15 | -100'000|

### (b) Aus der Tabelle

- **Gewinnmaximum:** $Q = 5'000$, $P = 35$, $\pi = 37'500$.
- **Erlösmaximum:** $Q = 6'000$, $P = 30$, $TR = 180'000$.

### (c) Rechnerisch

**Gewinnmaximum** ($MR = MC$):
$60 - 0.01Q = 5 + 0.001Q$
$55 = 0.011Q$
$Q^* = 5'000$, $P^* = 35$, $\pi^* = 37'500$.

**Erlösmaximum** ($MR = 0$):
$60 - 0.01Q = 0 \Rightarrow Q^{**} = 6'000$, $P^{**} = 30$, $TR^{**} = 180'000$.

**Warum nicht gleich?** Erlösmaximierung ignoriert Kosten. Bei $MR = 0$
ist eine weitere Einheit **null Erlös**, aber positive Kosten ($MC = 11$),
also sinkt der Gewinn. Beim Gewinnmaximum hingegen ist $MR = MC > 0$:
der Monopolist stoppt früher.

Intuition: Erlös-Max entspricht $|\varepsilon| = 1$ (einheitselastisch), das
ist der Punkt, an dem lineare Nachfrage die "Erlöskuppe" erreicht.
Der Gewinn-Max liegt **links davon**, wo die Nachfrage elastischer ist.

### Konfidenz
hoch — Tabellen-Einträge und analytisches Ergebnis stimmen bei $Q = 5'000$ und $Q = 6'000$ überein.

---

## Selbst-Kritik

- Aufgabe 1 ist reine Standard-Mikro, Ergebnis sollte übereinstimmen.
- Aufgabe 2: Tausender-Apostrophe sind **einfache Fehlerquelle**
  (Text-PDF zeigt "10000" statt "10'000"). Wer $Q$ bis $100'000$ statt
  $10'000$ liest, bekommt negative Gewinne überall.
- Keine Grafik gezeichnet — Beschreibung muss reichen.
