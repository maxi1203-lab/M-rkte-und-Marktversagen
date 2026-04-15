# SC-Diagnose — Lösungen & Rechenweg

> **SPOILER.** Erst öffnen, wenn dein Arbeitsblatt fertig ist!

---

## Aufgabe 1.1 — **Richtig: a. 6750**

**Schritt 1: inverse Nachfrage.**
Aus $Q = 250 - 0.5 P$ folgt $P = 500 - 2Q$.

**Schritt 2: Gewinnfunktion.**
$\pi = P \cdot Q - TC = (500 - 2Q) Q - 50Q - 5.5 Q^2 = 500Q - 2Q^2 - 50Q - 5.5 Q^2 = 450 Q - 7.5 Q^2$

**Schritt 3: FOC.**
$\pi' = 450 - 15 Q = 0 \Rightarrow Q^* = 30$

**Schritt 4: Gewinn einsetzen.**
$\pi^* = 450 \cdot 30 - 7.5 \cdot 900 = 13500 - 6750 = \boxed{6750}$

**Alternative:** Mit $MR$ und $MC$ direkt rechnen:
$MR = 500 - 4Q$, $MC = 50 + 11Q$. $MR = MC \Rightarrow 500 - 4Q = 50 + 11Q \Rightarrow Q = 30$.

**Stolperstein:** Nachfrage in inverse Form umstellen. Nicht $P = Q/0.5$
rechnen (das wäre $P = 2Q$, Vorzeichen weg).

**Bezug Kapitel:** [`kapitel-01-monopol.md`](../../../zusammenfassung/kapitel/kapitel-01-monopol.md#das-modell).

---

## Aufgabe 1.2 — **Richtig: c. 100**

Thelma ist **indifferent**, d.h. $U(100) = E[U(\text{Lotterie})]$.

$E[U] = 0.6 \cdot U(0) + 0.4 \cdot U(200) = 0.6 \cdot 20 + 0.4 \cdot 220 = 12 + 88 = \boxed{100}$

**Stolperstein:** Nicht $E[X] = 0.6 \cdot 0 + 0.4 \cdot 200 = 80$ rechnen
(das ist der Erwartungswert der Auszahlung, nicht des Nutzens). Die
Indifferenz-Bedingung ist über **Nutzen**, nicht Geld.

**Sanity-Check:** $U(100) = 100$ heißt, Thelma ist im Bereich 0–200 ein
bisschen risikoavers (sicheres 100 ist ihr gleich viel wert wie Lotterie
mit Erwartungsw. 80 → Risikoprämie = 20).

**Bezug Kapitel:** [`kapitel-06-risiko.md`](../../../zusammenfassung/kapitel/kapitel-06-risiko.md#erwartungsnutzen-hypothese-vnm).

---

## Aufgabe 1.3 — **Richtig: c. 4**

Konstante Preiselastizität heißt: $Q = 400 P^{-2}$ impliziert
$|\varepsilon| = 2$ (der Exponent).

**Schritt 1:** Amoroso-Robinson:
$MR = P \cdot (1 - 1/|\varepsilon|) = P \cdot (1 - 1/2) = 0.5 P$.

**Schritt 2:** $MC = dTC/dQ = 1.25 Q$.

**Schritt 3:** $P$ aus der Nachfrage:
$Q = 400 P^{-2} \Rightarrow P^2 = 400/Q \Rightarrow P = 20 / \sqrt{Q} = 20 \cdot Q^{-0.5}$

**Schritt 4:** $MR = MC$:
$0.5 \cdot 20 \cdot Q^{-0.5} = 1.25 Q$
$10 / \sqrt{Q} = 1.25 Q$
$10 = 1.25 \cdot Q \cdot \sqrt{Q} = 1.25 \cdot Q^{1.5}$
$Q^{1.5} = 8$
$Q = 8^{2/3} = \sqrt[3]{64} = \boxed{4}$

**Stolperstein:** Exponent $-2$ in $Q = 400 P^{-2}$ **ist** die Elastizität
(betragsmäßig). Bei Potenzfunktionen $Q = k P^{\alpha}$ ist $\varepsilon = \alpha$.

**Bezug Kapitel:** [`kapitel-01-monopol.md`](../../../zusammenfassung/kapitel/kapitel-01-monopol.md#optimaler-preis-via-elastizität).

---

## Aufgabe 1.4 — **Richtig: e. Kein Spieler**

**Spieler A:**

- Falls B eintritt: erhöhen → 5, senken → 20. **Senken besser.**
- Falls B nicht eintritt: erhöhen → 200, senken → 50. **Erhöhen besser.**
- Beste Antwort hängt von B ab → **A hat keine dominante Strategie**.

**Spieler B:**

- Falls A erhöht: eintreten → 50, nicht → 0. **Eintreten besser.**
- Falls A senkt: eintreten → -50, nicht → 0. **Nicht eintreten besser.**
- Beste Antwort hängt von A ab → **B hat keine dominante Strategie**.

→ Antwort **e**.

**Methode:** Für jeden Spieler separat prüfen. **Strategie-für-Strategie**
durchgehen, nicht die Matrix als Ganzes anschauen.

**Stolperstein:** Antwort **a** *"hängt davon ab"* klingt plausibel, aber
ist hier falsch, weil die Frage nicht nach der **besten Antwort** fragt,
sondern **ob eine dominante Strategie existiert** — und die existiert für
**keinen** der beiden → Antwort **e**.

**Bezug Kapitel:** [`kapitel-02-simultane-spiele.md`](../../../zusammenfassung/kapitel/kapitel-02-simultane-spiele.md#iterierte-elimination-dominierter-strategien).

---

## Aufgabe 1.5 — **Richtig: d. 900**

Preisdiskriminierung **ersten Grades** = **perfekte** Preisdiskriminierung:
der Monopolist nimmt von jeder Einheit genau die Zahlungsbereitschaft ab.

- Die produzierte Menge bei perfekter PD ist **dieselbe wie im Wettbewerb**,
  also wo $P(Q) = MC$:
  $50 - 0.5 Q = 20 \Rightarrow Q = 60$.
- Produzentenrente (PR) = Fläche zwischen $P(Q)$ und $MC$, von 0 bis 60.
- Diese Fläche ist ein **Dreieck** mit Grundseite 60 und Höhe $50 - 20 = 30$:

$$PR = \frac{1}{2} \cdot 60 \cdot 30 = \boxed{900}$$

**Stolperstein:**

- **PR = 0 (Antwort a)** wäre bei Wettbewerb **ohne** Produzentenrente —
  aber hier hat der Monopolist Marktmacht.
- **450 (Antwort c)** wäre die PR beim gewöhnlichen Monopol (ohne PD):
  $Q_{\text{Monopol}} = 30$ aus $MR = MC$ → $(35-20) \cdot 30 = 450$.
- **225 (Antwort b)** wäre die KR beim gewöhnlichen Monopol
  $(50-35) \cdot 30 / 2 = 225$.
- **PR bei 1. Grades = KR + PR des Wettbewerbs + DWL-Rückgewinn** = alles
  geht zum Produzenten. Konsumentenrente = 0 (wichtig!).

**Bezug Kapitel:** [`kapitel-01-monopol.md`](../../../zusammenfassung/kapitel/kapitel-01-monopol.md#preisdiskriminierung-pigou-1920).

---

## Aufgabe 1.6 — **Richtig: a. 64**

**Schritt 1: Erwartungsnutzen.**
$E[U] = 0.4 \cdot U(25) + 0.6 \cdot U(100)$
$= 0.4 \cdot 10 \sqrt{25} + 0.6 \cdot 10 \sqrt{100}$
$= 0.4 \cdot 10 \cdot 5 + 0.6 \cdot 10 \cdot 10$
$= 20 + 60 = 80$

**Schritt 2: Sicherheitsäquivalent.** Definition: $U(S) = E[U]$.
$10 \sqrt{S} = 80 \Rightarrow \sqrt{S} = 8 \Rightarrow S = \boxed{64}$

**Stolperstein:**

- **Antwort c. 80** — das ist der **Erwartungsnutzen** $E[U]$, nicht das
  Sicherheitsäquivalent. $S$ ist **in Geld**, nicht in Nutzen-Einheiten.
- **Antwort b. 70** wäre $E[W] = 0.4 \cdot 25 + 0.6 \cdot 100 = 70$,
  der **Erwartungswert der Lotterie** (in Geld). Bei Risikoaversion ist
  $S < E[W]$; die Differenz $E[W] - S = 70 - 64 = 6$ ist die
  **Risikoprämie**.
- **Antwort a. 64** ist korrekt, weil Quadratwurzel konkav → risikoavers
  → $S$ < $E[W]$.

**Bezug Kapitel:** [`kapitel-06-risiko.md`](../../../zusammenfassung/kapitel/kapitel-06-risiko.md#sicherheitsäquivalent-sl).

---

## Lernkarten-Destillat

Wenn du mir nur eine Zeile pro Aufgabe nehmen müsstest:

| Aufgabe | Thema | Kern-Formel |
|---------|-------|-------------|
| 1.1 | Monopol-Gewinn | Nachfrage invers stellen, $\pi = PQ - TC$, $\pi' = 0$ |
| 1.2 | Indifferenz in Nutzen | $U(\text{sicher}) = \sum p_i U(x_i)$ |
| 1.3 | Konstante Elastizität | $MR = P(1 - 1/|\varepsilon|)$; $|\varepsilon|$ = Exponent |
| 1.4 | Dominante Strategie | Spalten-für-Spalten prüfen, nicht Matrix global |
| 1.5 | PD 1. Grades | Menge wie Wettbewerb, PR = ganzes Dreieck Nachfrage-MC |
| 1.6 | Sicherheitsäquivalent | $U(S) = E[U]$, dann $U^{-1}$ anwenden |

Jetzt Auswertung:
[`diagnose-auswertung.md`](diagnose-auswertung.md)
