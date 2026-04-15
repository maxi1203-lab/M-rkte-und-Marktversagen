---
kapitel: 01
thema: Monopol
vo_einheit: 1
quelle: vorlesung/folien/einheit-01-monopol-transkript.txt
relevanz_klausur: hoch (SC + offene Fragen)
verwandte_hu: 01, 02, 03a
stand: 2026-04-15
---

# Kapitel 1 — Monopol

## Worum geht's (1 Absatz)

Wenn **nur ein Anbieter** auf dem Markt ist, ist der Preis nicht mehr gegeben
(wie im vollständigen Wettbewerb), sondern der Monopolist wählt entweder
**Menge oder Preis** entlang der Nachfragekurve. Er maximiert Gewinn bei
$MR = MC$, was zu einem Preis **über den Grenzkosten** führt. Resultat:
höherer Preis, kleinere Menge, und ein **Wohlfahrtsverlust (DWL)**
gegenüber dem Wettbewerbsgleichgewicht. Der Monopolist kann diesen
Mengenrückgang teilweise umgehen, indem er **preisdiskriminiert**.

## Kernbegriffe

- **Marktmacht**: Fähigkeit, Preis über MC zu setzen.
- **Grenzerlös** $MR = \dfrac{d(P(Q) \cdot Q)}{dQ} = P(Q) + Q \cdot P'(Q)$. Für
  fallende Nachfrage gilt $MR < P$.
- **Amoroso-Robinson-Beziehung**: $MR = P \cdot \left(1 - \dfrac{1}{|\varepsilon|}\right)$.
- **Lerner-Index**: $L = \dfrac{P - MC}{P} = \dfrac{1}{|\varepsilon|}$ — Maß
  für Marktmacht, zwischen 0 (Wettbewerb) und 1 (Monopol mit $|\varepsilon|=1$).
- **Deadweight Loss (DWL)**: Wohlfahrtsverlust gegenüber
  Wettbewerbsgleichgewicht, Dreieck zwischen Nachfrage- und MC-Kurve
  von $Q^*_{Monopol}$ bis $Q^*_{Wettbewerb}$.
- **Preisdiskriminierung**: unterschiedliche Preise für unterschiedliche
  Einheiten oder Käufer — drei Grade nach Pigou (1920).

## Das Modell

### Annahmen

- Ein Anbieter, viele Preisnehmer auf der Nachfrageseite.
- Nachfrage $Q(P)$ oder invers $P(Q)$, stetig, fallend.
- Kosten $C(Q)$, konvex (d.h. $MC$ steigend oder zumindest nicht-negativ).
- Monopolist kennt die Nachfrage.
- Kein Markteintritt möglich.

### Gleichgewichtsbedingung

Gewinnfunktion:

$$\pi(Q) = P(Q) \cdot Q - C(Q)$$

FOC (innere Lösung):

$$\boxed{MR(Q^*) = MC(Q^*)}$$

Einsetzen in Nachfrage liefert $P^* = P(Q^*)$.

### Lineares Standardbeispiel

Gegeben $P(Q) = a - bQ$, $C(Q) = F + cQ + \tfrac{d}{2}Q^2$.

- $MR = a - 2bQ$, $MC = c + dQ$
- $MR = MC \Rightarrow Q^* = \dfrac{a - c}{2b + d}$
- $P^* = a - b Q^*$
- $\pi^* = (P^* - \bar{AC}(Q^*)) \cdot Q^*$, Fixkosten $F$ nicht vergessen.

**Faustregel für die Klausur:** Bei linearer inverser Nachfrage $P = a - bQ$
ist die Grenzerlöskurve *"doppelt so steil"*: $MR = a - 2bQ$.

### Optimaler Preis via Elastizität

$$P^* = \dfrac{MC}{1 - \tfrac{1}{|\varepsilon|}}$$

Daraus: Je **weniger elastisch** die Nachfrage, desto höher der Monopolpreis
und desto größer der Markup. Bei $|\varepsilon| = 1$ wäre $P^* \to \infty$
(Nachfrage rechnerisch grenzwert-einheitselastisch).

Wichtig: Monopolist produziert **nie im unelastischen Bereich**
($|\varepsilon| < 1$), weil dort $MR < 0$.

### Wohlfahrtsanalyse

| Größe | Wettbewerb (P=MC) | Monopol |
|-------|-------------------|---------|
| Menge $Q$ | höher | niedriger |
| Preis $P$ | = MC | > MC |
| KR        | groß | kleiner |
| PR        | klein | groß (Monopolrente) |
| DWL       | 0 | > 0 |

**DWL-Dreieck:** zwischen $P(Q)$ und $MC(Q)$ für $Q \in [Q^*_{Monopol}, Q^*_{Wettbewerb}]$.

### Preisdiskriminierung (Pigou 1920)

| Grad | Mechanismus | Bsp. | Wohlfahrts-Effekt |
|------|-------------|------|-------------------|
| I. Grades (perfekt) | Preis = individuelle Zahlungsbereitschaft | Kunstauktion | $DWL = 0$, aber KR $= 0$: Monopolist schöpft **alles** ab |
| II. Grades (Selbstselektion) | Mengenrabatte, Tarifwahl | Handy-Tarife, Kino-Familypakete | KR > 0, weniger DWL als Einheitspreis |
| III. Grades (Gruppenpreise) | unterschiedliche Preise für identifizierbare Gruppen | Studentenrabatt, Senioren-Ticket | Preis pro Gruppe $i$: $P_i = MC / (1 - 1/|\varepsilon_i|)$ |

**Voraussetzungen** für Preisdiskriminierung:

1. Marktmacht (wir sind im Monopol — ✓).
2. Gruppen unterscheidbar (bei III. Grades) oder Signal glaubhaft (II. Grades).
3. **Keine Arbitrage** zwischen Gruppen (Ticket nicht weiterverkaufbar).

## Typische Klausuraufgaben

1. **Rechnen** von $Q^*, P^*, \pi^*$ bei gegebener $P(Q)$ und $C(Q)$ (SC + offen).
2. **Lerner-Index** aus gegebener Elastizität berechnen.
3. **Preisdiskriminierung I. Grades**: Berechne Produzentenrente als
   Dreiecksfläche unter $P(Q)$ bis $MC$ (Probeprüfung 2024, Aufg. 1.5).
4. **Interpretation:** *"Wieso verlangt Monopolist in Markt B einen höheren
   Preis als in Markt A?"* → Elastizitätsargument.

## Stolpersteine

- **MR mit P verwechseln.** $MR < P$ beim Monopol. Beim Wettbewerb: $P = MR$.
- **DWL** ist nicht der Gesamterlös-Verlust, sondern die **nicht realisierten
  Handelsgewinne**. Dreieck zwischen Nachfrage und MC, nicht zwischen
  Nachfrage und Preis.
- **Fixkosten $F$** beeinflussen $Q^*$ nicht (solange überhaupt produziert
  wird), aber sie entscheiden, ob $\pi^* \geq 0$ und damit ob Markteintritt.
- **Preisdiskriminierung I. Grades ist effizient** (Menge = Wettbewerbsmenge),
  aber **verteilungsunerwünscht** (KR = 0, Monopolist kassiert alles).
- **Einheit!** Ist $P$ in Euro pro Stück, Cent pro Download, oder pro 1000?
  Ergebnis-Plausibilisierung oft nur über Einheiten-Check.
- **Shutdown-Bedingung** kurzfristig: $P \geq \min AVC$ (nicht $\min AC$!).

## Verwandte Inhalte

- HÜ 01 (Alpha-Einervonvielen, Presto Products) → Basisrechnung Wettbewerb
  vs. Monopol.
- HÜ 02 (Wodka-Elastizität) → Amoroso-Robinson in Aktion.
- HÜ 03a (Preisdiskriminierung) → Pigou-3-Grade-Schema.
- Probeprüfung 2024, Aufg. 1.1 (Alpha-Software), 1.3 (konstante Elastizität),
  1.5 (Preisdiskr. I. Grades).
