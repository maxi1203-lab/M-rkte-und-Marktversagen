---
kapitel: 03
thema: Oligopol (Cournot, Bertrand, Stackelberg als dyn. Vorgriff)
vo_einheit: 3
quelle: vorlesung/folien/einheit-03-oligopol-transkript.txt
relevanz_klausur: sehr hoch — Thema 5 (Duopol mit Subvention) + 10 (Cournot)
verwandte_hu: 05, 06
stand: 2026-04-15
---

# Kapitel 3 — Oligopol

## Worum geht's

Wenn **wenige Anbieter** den Markt teilen, hängt der Gewinn jedes
Unternehmens nicht nur von der eigenen Entscheidung, sondern auch von
den **strategischen Reaktionen** der anderen ab. Kernmodelle:

- **Cournot** (Mengenwettbewerb, simultan)
- **Bertrand** (Preiswettbewerb, simultan)
- **Stackelberg** (Mengen, sequentiell — wird in VL 4 vertieft)

Gleichgewichte werden über **Reaktionsfunktionen** und **Nash** bestimmt.
Oligopol-Wohlfahrt liegt **zwischen** Monopol und vollständigem Wettbewerb.

## Kernbegriffe

- **Reaktionsfunktion** $q_i^*(q_{-i})$: beste Antwort von Firma $i$,
  gegeben die Mengen der anderen.
- **Cournot-Nash-GG (CNE)**: $(q_1^*, q_2^*)$ mit $q_1^* = RF_1(q_2^*)$
  und $q_2^* = RF_2(q_1^*)$.
- **Bertrand-Paradox**: im Preiswettbewerb mit homogenen Gütern und
  identischen MC ergibt sich **$P = MC$** bereits bei 2 Anbietern.
- **Kollusion**: Koordination auf Monopolmenge; stabil nur unter
  bestimmten Bedingungen (vgl. VL 5).

## Cournot-Duopol

### Annahmen

- 2 Firmen, homogenes Gut, wählen **simultan** $q_1, q_2$.
- Inverse Nachfrage: $P(Q) = a - bQ$ mit $Q = q_1 + q_2$.
- Kostenfunktionen $C_i(q_i)$ — oft linear ($C_i = cq_i + F$).

### Beste-Antwort-Herleitung (linearer Fall)

Mit $P = a - b(q_1 + q_2)$ und $C_i = cq_i$:

$$\pi_1 = (a - b(q_1 + q_2))q_1 - cq_1$$

FOC nach $q_1$:

$$\frac{\partial \pi_1}{\partial q_1} = a - 2bq_1 - bq_2 - c = 0$$

$$\boxed{q_1^*(q_2) = \frac{a - c}{2b} - \frac{1}{2}q_2}$$

Analog: $q_2^*(q_1) = \tfrac{a-c}{2b} - \tfrac{1}{2}q_1$.

### Cournot-Nash-GG (symmetrischer Fall)

Einsetzen beider Reaktionsfunktionen:

$$q_i^* = \frac{a - c}{3b}, \quad Q^* = \frac{2(a-c)}{3b}, \quad P^* = \frac{a + 2c}{3}$$

Gewinn pro Firma: $\pi_i^* = \dfrac{(a-c)^2}{9b} - F$.

### Vergleich der Marktformen (lineare Nachfrage, identische MC)

| Marktform       | $Q$ gesamt | $P$ | $\pi_{\text{Firma}}$ | Wohlfahrt |
|-----------------|------------|-----|----------------------|-----------|
| Monopol         | $\tfrac{a-c}{2b}$  | $\tfrac{a+c}{2}$ | $\tfrac{(a-c)^2}{4b}$ | niedrig |
| **Cournot (2)** | $\tfrac{2(a-c)}{3b}$ | $\tfrac{a+2c}{3}$ | $\tfrac{(a-c)^2}{9b}$ je Firma | **mittel** |
| Vollst. Wettb. / Bertrand | $\tfrac{a-c}{b}$ | $c$ | $0$ | hoch |

**Merksatz:** Monopol $< Q_{\text{Cournot}} < Q_{\text{Wettbewerb}}$,
Preise umgekehrt.

### Graphische Darstellung (Reaktionsfunktionen)

- $q_1$ auf x-Achse, $q_2$ auf y-Achse.
- $RF_1$: Gerade mit Steigung $-2$ (im typischen linearen Fall).
- $RF_2$: Gerade mit Steigung $-\tfrac{1}{2}$.
- Schnittpunkt = **CNE**.
- **Kollusionspunkt** liegt *unter* dem CNE (beide produzieren weniger,
  teilen Monopolmenge).
- Einseitige Abweichung vom Kollusionspunkt = Bewegung **entlang**
  der eigenen Reaktionsfunktion → Anreiz, mehr zu produzieren.

## Bertrand-Duopol

### Setup

- Zwei Firmen, **homogenes** Gut, Preiswettbewerb (wählen $p_1, p_2$).
- Identische konstante MC $= c$, keine Kapazitätsschranke.
- Nachfrage geht komplett zur Firma mit dem **niedrigeren** Preis,
  bei $p_1 = p_2$ teilen sie sich den Markt.

### Bertrand-Nash-GG

**Einziges NGG:** $p_1^* = p_2^* = c$, Gewinn = 0.

**Warum?** Wenn $p_i > c$, hat Firma $j$ einen Anreiz, $p_j$ minimal zu
unterbieten und den ganzen Markt abzugreifen. Der einzige stabile Punkt
ist $p = MC$ → **Bertrand-Paradox**: zwei Anbieter reichen für
Wettbewerbsergebnis.

### Auflösungen des Paradox

- **Kapazitätsschranken** (Edgeworth).
- **Produktdifferenzierung** (Hotelling, nicht-homogenes Gut).
- **Dynamische Wiederholung** → Kollusion möglich (VL 5).

## Duopol mit Subvention (Thema 5 der gefailten Klausur)

> **VL 3 streift dieses Thema nicht explizit**, aber es taucht in der
> Kernzusammenfassung auf und ist klausurrelevant. Unten die
> Standard-Logik.

Angenommen, Firma 1 bekommt eine Subvention $s$ pro produzierter Einheit:

$$C_1(q_1) = (c - s) q_1$$

(effektive MC sinkt um $s$.)

**Konsequenz in Cournot:**

- Firma 1's Reaktionsfunktion verschiebt sich nach rechts-außen:
  $q_1^*(q_2) = \tfrac{a - (c-s)}{2b} - \tfrac{1}{2}q_2$.
- Neuer CNE hat $q_1^{**} > q_1^*$ und $q_2^{**} < q_2^*$.
- Gesamtmenge $Q$ steigt, Preis $P$ sinkt.
- Firma 1 gewinnt Marktanteil + Gewinn (Gewinner der Subvention).
- Firma 2 verliert (Wettbewerbsverzerrung).

**Klausurrelevante Interpretation:** Subvention kann strategisch von
einer Regierung eingesetzt werden, um der heimischen Firma einen
**Stackelberg-artigen** Vorteil zu verschaffen, selbst wenn das Spiel
eigentlich simultan ist (Brander-Spencer-Argument).

## Stackelberg-Vorschau (wird in VL 4 vertieft)

- Firma 1 wählt $q_1$ **zuerst**, Firma 2 beobachtet und wählt $q_2$.
- Lösung per **Rückwärtsinduktion**:
  1. $q_2^*(q_1)$ = RF₂ aus Cournot.
  2. Firma 1 maximiert $\pi_1$ unter Berücksichtigung, dass Firma 2
     auf RF₂ landet.
- Linearer Fall: $q_1^* = \tfrac{a-c}{2b}$ (Monopol-halbe),
  $q_2^* = \tfrac{a-c}{4b}$, $Q^* = \tfrac{3(a-c)}{4b}$.
- **First-Mover-Advantage**: Leader hat höheren Gewinn als Follower
  (wenn Mengen strategische Substitute sind).

## Typische Klausuraufgaben

1. **Cournot rechnen**: gegeben $P(Q)$ und $C_i$, finde CNE, $\pi$, Wohlfahrt.
   Vgl. Probeprüfung 21.02.2024, Aufg. 2.1 (P = 20 - 2Q, $C_i = 4q_i$).
2. **Reaktionsfunktionen graphisch** zeichnen + Kollusionspunkt markieren
   + erklären warum Kollusion nicht stabil ist (SPE-Argument).
3. **Bertrand-Paradox diskutieren** und eine Auflösung nennen.
4. **Subvention → CNE verschiebt sich**: wer gewinnt, wer verliert.
5. **Cournot vs. Stackelberg vergleichen** (Gewinne, Outputs).

## Stolpersteine

- **Cournot-Monopol-Verwechslung**: $MR = MC$ gilt nur im Monopol.
  In Cournot maximiert jede Firma ihre eigene $\pi_i$ mit
  $\tfrac{\partial \pi_i}{\partial q_i} = 0$ — das ist **nicht** dasselbe.
- **Steigung der Reaktionsfunktion**: im linearen Standardfall
  $-\tfrac{1}{2}$, nicht $-1$ oder $-2$. Oft verwechselt mit der
  Nachfrage-Steigung.
- **Symmetrie ausnutzen**: bei identischen Kostenfunktionen sind
  $q_1^* = q_2^*$ → Einsetzen in eine RF reicht.
- **Nach der Menge sofort den Preis vergessen**: nachdem $q^*$ gefunden
  ist, $P^* = a - bQ^*$ rechnen und Gewinn explizit ausrechnen
  (Klausur fragt meist nach beiden).
- **Bertrand ohne Produktdifferenzierung = P=MC**: nicht mit Cournot
  verwechseln. Beim Oligopol-SC-Aufgaben-Abgleich Matrix genau lesen,
  ob Preise oder Mengen gewählt werden.
- **Subvention ≠ Steuer**: Vorzeichen beim Verschieben der
  Reaktionsfunktion beachten. Subvention drückt MC runter → RF nach
  außen; Steuer umgekehrt.

## Verwandte Inhalte

- HÜ 05 (Oligopol) und HÜ 06 (Oligopol II) — Cournot/Bertrand-Drill
- Probeprüfung 21.02.2024 Aufg. 2.1 (Cournot mit Kollusion)
- Verbindung zu VL 4 (Stackelberg als dyn. Spiel)
- Verbindung zu VL 5 (wiederholtes Bertrand → Kollusion)
