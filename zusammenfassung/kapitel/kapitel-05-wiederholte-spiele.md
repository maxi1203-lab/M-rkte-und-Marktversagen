---
kapitel: 05
thema: Wiederholte Spiele (endlich/unendlich, Folk-Theorem, Kartelle)
vo_einheit: 5
quelle: vorlesung/folien/einheit-05-wiederholte-spiele-transkript.txt
relevanz_klausur: mittel — typisch offene Aufgabe zur Kollusionsstabilität
verwandte_hu: 08, 09
stand: 2026-04-15
---

# Kapitel 5 — Wiederholte Spiele

## Worum geht's

Wenn dasselbe Stufenspiel (z.B. Gefangenendilemma, Bertrand-Duopol)
**mehrfach** gespielt wird, können Kooperation und Kartellstabilität
**entstehen**, die im einmaligen Spiel unmöglich sind — **aber nur**,
wenn das Spiel **unendlich oft** wiederholt wird (oder mit unbestimmtem
Ende). Bei **endlichem** Horizont zerfällt die Kooperation durch
Rückwärtsinduktion. Zentrale Werkzeuge: **Diskontfaktor $\delta$** und
**Trigger-Strategien**.

## Kernbegriffe

- **Stufenspiel**: das Spiel, das in jeder Runde gespielt wird (meist
  eine Normalform).
- **Diskontfaktor $\delta \in [0, 1)$**: Bewertung zukünftiger vs.
  heutiger Auszahlungen (oder Wahrscheinlichkeit, dass Spiel
  weitergeht).
- **Trigger-Strategie**: Plan "Kooperiere, solange alle kooperieren;
  bei Abweichung wechsle dauerhaft zur Bestrafung".
- **Grim-Trigger**: Bestrafung = Nash-GG des Stufenspiels **für immer**.
- **Tit-for-Tat**: Bestrafung nur eine Runde, dann zurück zu Kooperation.
- **Folk-Theorem**: Mit genügend hohem $\delta$ kann fast jedes
  individuell-rationale Auszahlungsprofil als SPE unterstützt werden.

## Modell

### Auszahlungen in wiederholten Spielen

Gesamte Auszahlung eines Spielers über alle Runden:

$$U_i = \sum_{t=0}^{T} \delta^t \, u_i^{(t)}$$

Für **unendliches** Spiel ($T = \infty$) und konstante Periodenauszahlung $u$:

$$U_i = u \cdot (1 + \delta + \delta^2 + \dots) = \frac{u}{1 - \delta}$$

Wenn erst ab Periode 1 (also $\delta + \delta^2 + \dots$):

$$= \frac{\delta \cdot u}{1 - \delta}$$

### Endlich wiederholtes Gefangenendilemma

- Letzte Runde: kein Zukunfts-Anreiz → dominante Strategie = Abweichung
  (Gestehen).
- Vorletzte Runde: da letzte Runde sowieso Abweichung, keine Drohung
  → Abweichung.
- Rückwärtsinduktion: in jeder Runde Abweichung.
- **Resultat**: endliche Wiederholung löst das Dilemma **nicht**.
  (Gilt für alle Stufenspiele mit einzigartigem Nash-GG.)

### Unendlich wiederholtes Gefangenendilemma

Können die Spieler kooperieren? Betrachte **Grim-Trigger**:
*"Kooperiere in jeder Runde, solange alle kooperiert haben. Sobald
jemand abweicht, spiele ab nächster Runde für immer das Stufen-Nash."*

**Bedingung für Kooperation als SPE:**

$$\underbrace{\frac{u_{\text{koop}}}{1-\delta}}_{\text{kooperativer Pfad}} \geq \underbrace{u_{\text{abweichung}} + \frac{\delta \cdot u_{\text{Nash}}}{1-\delta}}_{\text{Abweichung einmal, dann Strafe}}$$

Umgestellt:

$$\delta \geq \frac{u_{\text{abweichung}} - u_{\text{koop}}}{u_{\text{abweichung}} - u_{\text{Nash}}}$$

**Interpretation:** Je größer der **kurzfristige Abweichungsgewinn** relativ
zur langfristigen **Strafe**, desto höher muss $\delta$ sein, damit
Kooperation hält.

### Beispiel: Bertrand-Kartell

Stufenspiel: Bertrand-Duopol, MC = $c$. Einmalig: Nash = $(c, c)$, Gewinn 0.
Kooperation = Monopolpreis $P^M$ teilen, Gewinn pro Firma $\pi^M / 2$.

- Koop-Pfad: $\dfrac{\pi^M / 2}{1 - \delta}$ pro Firma.
- Abweichung (minimal unterbieten): Monopolgewinn $\pi^M$ in einer Runde,
  dann 0 auf ewig.
- Bedingung: $\dfrac{\pi^M/2}{1-\delta} \geq \pi^M \Rightarrow \delta \geq \tfrac{1}{2}$.

**Kartell hält**, wenn Firmen die Zukunft stark genug bewerten.

### Folk-Theorem (intuitiv)

In einem unendlich wiederholten Spiel mit hinreichend hohem $\delta$
können **fast alle** Auszahlungsvektoren, die besser sind als das Stufen-
Nash und individuell rational sind, als SPE unterstützt werden.

**Praktische Konsequenz**: Wiederholung eröffnet ein **Kontinuum** an
Kooperations-Gleichgewichten. Selektion zwischen ihnen: Fokalpunkte,
Normen, Kommunikation.

## Typische Klausuraufgaben

1. **Diskontfaktor-Schwelle** für Kartellstabilität berechnen (offene
   Aufgabe, 4–8 Pkt).
2. **Endlich vs. unendlich argumentieren**: warum Kartell bei endlichem
   Horizont zusammenbricht.
3. **Trigger-Strategien vergleichen**: Grim vs. Tit-for-Tat.
4. **Anwendung Klimaverhandlungen / OPEC**: Welche Faktoren erhöhen
   $\delta$? (Transparenz, Information über Abweichungen, wiederholte
   Interaktion).

## Stolpersteine

- **"Unendlich" ≠ sehr lang**: schon bei großem, aber endlichem $T$
  zerfällt Kooperation durch Rückwärtsinduktion. Es braucht **unbestimmtes**
  Ende (oder unendlich).
- **Geometrische Reihe**: $\sum_{t=0}^{\infty} \delta^t = \tfrac{1}{1-\delta}$,
  aber $\sum_{t=1}^{\infty} \delta^t = \tfrac{\delta}{1-\delta}$. Häufige
  Fehlerquelle beim Einsetzen.
- **Abweichungsgewinn pro Periode** korrekt ermitteln: nicht
  Gesamtauszahlung, sondern **einmalige** Abweichung in der ersten Runde,
  dann lebenslange Bestrafung.
- **Stufenspiel-Nash als Bestrafung**: funktioniert nur, wenn Nash auch
  glaubwürdig gespielt werden kann (ist immer SPE des Teilspiels, ✓).
- **Paradoxon**: Bei endlichem Horizont ist **kein** Kooperationspfad
  SPE — auch nicht in der ersten Runde. Studierende denken oft
  "naja, zumindest in der Mitte könnten sie kooperieren" — **nein**.

## Verwandte Inhalte

- HÜ 08 (Stackelberg + Wh-Spiele) — Kartell-Rechnung mit Diskontfaktor
- HÜ 09 (Wh-Spiele + Kartelle)
- Verbindung zu VL 3 (Bertrand-Paradox aufgelöst durch Wiederholung)
- Verbindung zu VL 4 (Rückwärtsinduktion auch hier, aber mit unendlichem
  Horizont nicht direkt anwendbar → Grenzwertbetrachtung)
