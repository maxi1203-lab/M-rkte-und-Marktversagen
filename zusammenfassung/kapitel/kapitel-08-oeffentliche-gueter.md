---
kapitel: 08
thema: Öffentliche Güter (Samuelson, Trittbrettfahrer, 2-Dörfer-Spiel)
vo_einheit: 8
quelle: vorlesung/folien/einheit-08-oeffentliche-gueter-transkript.txt
relevanz_klausur: mittel-hoch — Thema 6 (Öff. Güter, 2 Dörfer) der gefailten Klausur
verwandte_hu: 12, 13
stand: 2026-04-15
---

# Kapitel 8 — Öffentliche Güter

## Worum geht's

**Öffentliche Güter** sind **nicht-rival** (Konsum einer Person verringert
nicht den Konsum anderer) und **nicht-ausschließbar** (niemand kann vom
Konsum ausgeschlossen werden). Daher: **Trittbrettfahrer-Problem** —
individuell rationale Beiträge führen zu Unter-Bereitstellung.
Sozial optimale Menge per **Samuelson-Bedingung**. Bereitstellungs-
Mechanismen: Staat (Steuern), freiwillige Beiträge (instabil),
Lindahl-Preise, Clarke-Groves.

## Kernbegriffe

- **Rivalität**: Konsum durch einen reduziert Konsum durch andere.
- **Ausschließbarkeit**: anderer kann vom Konsum ausgeschlossen werden
  (technisch oder rechtlich).
- **2×2-Matrix** nach Samuelson:

| | **Rivalität ja** | **Rivalität nein** |
|---|-----------------|-------------------|
| **Ausschluss ja** | privates Gut (Apfel) | Klubgut (Pay-TV, Autobahnmaut) |
| **Ausschluss nein** | Common-Pool (Fischbestand) | **öffentliches Gut** (Landesverteidigung, Straßenbeleuchtung) |

- **Samuelson-Bedingung**: $\sum_i MRS_i = MC$ (Summe der individuellen
  Grenzraten der Substitution = Grenzkosten der öff. Gut-Bereitstellung).
- **Trittbrettfahrer** (free rider): Spieler, der öff. Gut nutzt, ohne
  beizutragen.
- **Lindahl-Preise**: individuelle Preise proportional zum MRS →
  effiziente Bereitstellung, aber Präferenz-Revelation Problem.

## Modell

### Samuelson-Bedingung (effiziente Bereitstellung)

Bei privaten Gütern: $MRS_i = P$ für **jeden** Konsumenten, also
$MRS_i = MC$ im GGW.

Bei öffentlichen Gütern: **alle** Konsumenten "konsumieren" dieselbe Menge
→ Sozial optimal ist, wenn die **Summe** der individuellen Grenznutzen
den Grenzkosten entspricht:

$$\boxed{\sum_{i=1}^{N} MRS_i = MC}$$

**Graphisch**: individuelle Nachfragekurven werden **vertikal** addiert
(statt horizontal wie bei privaten Gütern).

### Beispiel: 2 Personen, öffentliches Gut G, privates Gut x

$U_A(x_A, G) = x_A + \ln G$, $U_B(x_B, G) = x_B + \ln G$.
Preis $p_x = 1$, Kosten des öff. Guts $p_G = 2$.

- $MRS_A = \dfrac{1/G}{1} = 1/G$. Analog $MRS_B = 1/G$.
- Samuelson: $1/G + 1/G = 2 \Rightarrow 2/G = 2 \Rightarrow G^* = 1$.
- Privates Optimum (jeder für sich): $MRS_i = p_G$ → $1/G = 2 \Rightarrow G = 0.5$ pro Person, aber nur eine Einheit kann bereitgestellt werden → Free-Riding.

**Der Punkt**: sozial optimal ist **mehr als jeder freiwillig beiträgt**.

### Trittbrettfahrer-Spiel (2 Dörfer)

Standardaufgabe in der Klausur (vgl. "2-Dörfer-Spiel" in der
Fehleranalyse):

- 2 Dörfer, jedes kann 0 oder 1 Einheit Brücke bauen (Kosten $c = 10$,
  Nutzen je Dorf $v = 7$).
- Brücke entsteht, sobald **mindestens eines** baut.

Auszahlungsmatrix:

| | **B baut** | **B baut nicht** |
|---|----------|------------------|
| **A baut** | $(7-10, 7-10) = (-3, -3)$ | $(-3, 7)$ |
| **A baut nicht** | $(7, -3)$ | $(0, 0)$ |

- Jedes Dorf will, dass das **andere** baut (free riden).
- Reine Nash-GG: (A baut, B nicht) und (A nicht, B baut) — **asymmetrisch**.
- Gemischtes NGG: jedes baut mit $p = ?$ (Indifferenz-Rechnung).
- **Sozial optimal** (gemeinsam bauen): Kosten 10, Nutzen $2 \cdot 7 = 14$.
  Aber keiner allein trägt gerne 10, um nur 7 zu bekommen.
- **Kernproblem**: freiwillige Bereitstellung führt zu Unter-Produktion
  und Koordinationsversagen.

### Lösungen

1. **Staat** zwingt alle zur Beteiligung über Steuern → hebelt Trittbrett-
   problem aus, aber erfordert Präferenz-Wissen.
2. **Lindahl-Preise** (ideale Lösung): jeder zahlt Preis $p_i$ mit
   $\sum p_i = MC$, sodass $p_i = MRS_i$. Problem: Präferenzen sind
   privat → Menschen geben falsche Präferenzen an, um $p_i$ zu senken.
3. **Clarke-Groves-Mechanismus** (theoretisch elegant): jeder zahlt
   seinen **marginalen Schaden** für andere an → Anreiz, Präferenzen
   wahrheitsgemäß zu melden. Aber Budgetausgleich-Problem.
4. **Freiwillige Beiträge**: stabilisiert durch soziale Normen, Reputation,
   oder teil-Ausschließbarkeit (Spendenquittung = "Danke")

### Crowding-Out

Wenn der Staat selbst Beitrag leistet, reduzieren private Geber oft ihren
Beitrag um (fast) denselben Betrag → **Crowding-Out**. Im Extremfall:
vollständiges Crowding-Out, staatliche Bereitstellung hat keinen Netto-
Effekt. Empirisch: meist **unvollständig**, typisch 30–70% Crowding.

## Typische Klausuraufgaben

1. **Samuelson-Bedingung** anwenden bei gegebenen Nutzenfunktionen
   → Berechnung der effizienten Menge $G^*$.
2. **Nash-GG im Trittbrettfahrer-Spiel** (reine + gemischte, vgl.
   2-Dörfer-Setup).
3. **Klassifikations-Aufgabe**: Ist das ein öffentliches Gut?
   (Rivalität + Ausschließbarkeit prüfen.)
4. **Vergleich privates vs. öffentliches Gut**: horizontale vs.
   vertikale Aggregation der Nachfrage.

## Stolpersteine

- **Vertikale Aggregation vergessen**: bei öff. Gütern **summiert** man
  MRS, nicht Mengen. Häufigster Fehler.
- **Samuelson vs. privates Optimum**: privates Optimum $MRS_i = MC$ für
  jeden ⟹ $G$ ist zu niedrig. Nur die Summe ist relevant.
- **"Klub vs. öffentliches Gut"**: Autobahn mit Maut = Klub (ausschließbar).
  Klimaschutz = öff. Gut (nicht ausschließbar).
- **Trittbrettfahrer in gemischtem NGG**: Wahrscheinlichkeit richtig
  ansetzen — jedes Dorf ist indifferent zwischen bauen/nicht bauen, d.h.
  $p \cdot v_{\text{mit brücke}} + (1-p) \cdot v_{\text{ohne}} = c$ ...
  genaue Rechnung je nach Setup.
- **Nicht-Rivalität ≠ unendlich elastisch**: "nicht-rival" heißt nur,
  dass Konsum anderer nicht verringert wird. Bereitstellung ist
  trotzdem kostspielig.
- **Crowding-Out im Klausurkontext**: Frage oft konzeptionell ("was
  passiert mit privater Spende, wenn Staat selbst beiträgt?") — nicht
  quantitativ.

## Verwandte Inhalte

- HÜ 12 (AsymInfo + Öff. Güter)
- HÜ 13 (Öffentliche Güter) — Drill Samuelson-Rechnung
- Probeprüfung-Nachbau (z.B. "Herr X zahlt 18 EUR, Y 12 EUR …") geht
  typisch über die Samuelson-Formel.
- Verbindung zu VL 9 (Externalitäten — öff. Güter sind Sonderfall
  positiver Externalität mit Nicht-Rivalität)
- Verbindung zu VL 7 (Präferenz-Revelation ähnlich wie Screening)
