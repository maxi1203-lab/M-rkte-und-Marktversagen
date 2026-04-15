---
kapitel: 04
thema: Dynamische Spiele (extensive Form, Rückwärtsinduktion, SPE)
vo_einheit: 4
quelle: vorlesung/folien/einheit-04-dynamische-spiele-transkript.txt
relevanz_klausur: sehr hoch — Probeprüfungsaufg. 2.2 explizit
verwandte_hu: 07, 08
stand: 2026-04-15
---

# Kapitel 4 — Dynamische Spiele

## Worum geht's

Bei **dynamischen Spielen** ziehen die Spieler **nacheinander** und können
das Verhalten der Vorgänger beobachten. Das wichtigste Darstellungsmittel
ist die **extensive Form** (Spielbaum). Standardlösung: **Rückwärts-
induktion** → **teilspielperfektes Gleichgewicht (SPE)**, das die
Schwäche von Nash-GG in dyn. Spielen (unglaubwürdige Drohungen) ausschließt.

## Kernbegriffe

- **Extensive Form / Spielbaum**: Knoten = Entscheidungspunkte,
  Kanten = Strategien, Blätter = Auszahlungen.
- **Informationsmenge**: Punkte, die ein Spieler nicht unterscheiden
  kann (wichtig für unvollkommene Info).
- **Strategie** (hier!): vollständiger Handlungsplan für **jeden**
  Entscheidungspunkt, auch hypothetische.
- **Teilspiel**: Unterbaum, der an einem Entscheidungsknoten beginnt.
- **Teilspielperfektes Gleichgewicht (SPE)**: Strategieprofil, das in
  **jedem** Teilspiel ein Nash-GG bildet.
- **Rückwärtsinduktion**: vom Ende her Entscheidungen optimieren, dann
  im Baum nach oben.
- **Unglaubwürdige Drohung**: Strategie, die bei tatsächlicher
  Ausführung suboptimal wäre → wird von SPE ausgeschlossen.

## Modell

### Extensive Form — Elemente

Ein Spielbaum spezifiziert:
1. **Menge der Spieler**
2. **Reihenfolge der Züge** (welche Spieler wann, in welchen Knoten)
3. **Strategiemenge an jedem Knoten**
4. **Informationsstand** des ziehenden Spielers (was er beobachtet hat)
5. **Auszahlungen an den Endknoten**

### Strategie in einem dynamischen Spiel

**Wichtig**: Strategie $\neq$ einmalige Entscheidung. Strategie ist ein
Plan, der **für jeden möglichen Entscheidungsknoten** festlegt, was
getan wird — **auch** wenn dieser Knoten im realisierten Spielverlauf
nicht erreicht wird.

Beispiel (Markteintritt, Firma A entscheidet "aggressiv/friedlich" je
nachdem ob Firma B eintritt):
- Strategie von A: $(s_A^{\text{falls B eintritt}}, s_A^{\text{falls B nicht}})$.
- Mögliche Strategien: (aggressiv, aggressiv), (aggressiv, friedlich),
  (friedlich, aggressiv), (friedlich, friedlich) — **4 Strategien**,
  auch wenn B nur eine Entscheidung trifft.

### Rückwärtsinduktion (Algorithmus)

1. Gehe zu den **letzten** Entscheidungsknoten im Baum.
2. Bestimme für jeden letzten Knoten die optimale Aktion des ziehenden
   Spielers (maximiert seine Auszahlung).
3. Ersetze den Knoten durch die resultierende Auszahlung.
4. Wiederhole für die **vorletzten** Knoten, jetzt unter Berücksichtigung
   der schon bestimmten Reaktionen.
5. Arbeite dich bis zur Wurzel hoch.
6. Das entstandene Strategieprofil ist das **SPE**.

### Beispiel: Markteintritt

```
                A
              /   \
        Enter      Stay Out
           |         |
           B         (0, 10)
          / \
      Fight   Accommodate
     (-3,-3)  (5, 5)
```

**Rückwärtsinduktion:**
- Im Knoten B: "Fight" gibt -3, "Accommodate" gibt 5 → B wählt Accommodate.
- Im Knoten A: A weiß, dass B bei Eintritt akkommodiert → Eintritt gibt 5,
  Stay Out gibt 0 → A wählt Enter.
- **SPE:** A = "Enter", B = "Accommodate wenn A eintritt".
- Ergebnis auf dem Pfad: (5, 5).

### Nash-GG vs. SPE

In dynamischen Spielen kann es **mehr Nash-GG als SPE** geben. Die extra
Nash-GG beruhen auf **unglaubwürdigen Drohungen**.

**Wichtig zum Merken:** Jedes SPE ist ein Nash-GG, **aber nicht jedes
Nash-GG ist SPE**.

Im Markteintritts-Beispiel:
- **Nash-GG 1**: A=Enter, B=Accommodate. ✓ auch SPE.
- **Nash-GG 2**: A=Stay Out, B="Fight wenn Eintritt". ✓ Nash, aber
  **nicht SPE**: B's Drohung "Fight" ist unglaubwürdig, weil sie B
  selbst schaden würde, wenn sie ausgeführt werden müsste.

SPE **eliminiert** solche unglaubwürdigen Drohungen.

### Normalform aus extensiver Form

Man kann ein dyn. Spiel immer in Normalform schreiben, indem man alle
vollständigen Strategien (= Handlungspläne) auflistet. Die Normalform
zeigt **alle Nash-GG**, aber nicht die Teilspielperfektion — daher die
extensive Form + Rückwärtsinduktion bevorzugt.

## Stackelberg als dynamisches Spiel

Stackelberg-Duopol ist der **Standard-Anwendungsfall** (VL 3 + 4):
- Firma 1 wählt $q_1$ zuerst.
- Firma 2 beobachtet $q_1$ und wählt $q_2$.
- Lösung per Rückwärtsinduktion:
  1. $q_2^*(q_1) = \tfrac{a - c - bq_1}{2b}$ (Follower-Reaktionsfunktion)
  2. Firma 1 setzt dies in $\pi_1$ ein und maximiert:
     $\pi_1 = (a - b q_1 - b q_2^*(q_1)) q_1 - c q_1$
  3. FOC nach $q_1$: $q_1^* = \tfrac{a-c}{2b}$, $q_2^* = \tfrac{a-c}{4b}$.
- **Leader produziert doppelt so viel wie Follower**; Leader hat
  höheren Gewinn (**First-Mover-Advantage**).

## Typische Klausuraufgaben

1. **Spiel in extensiver Form darstellen** (aus Text), **alle
   Strategien** auflisten. Probeprüfungsaufg. 2.2 hat genau das:
   simultan vs. sequentiell, Strategien von Spieler 2:
   $(hh, hn, nh, nn)$ — 4 Strategien, weil je nach Züg von A.
2. **SPE per Rückwärtsinduktion** bestimmen.
3. **Unglaubwürdige Drohungen** identifizieren (Nash-GG, die nicht
   SPE sind).
4. **Stackelberg vs. Cournot** vergleichen.

## Stolpersteine

- **Strategie ≠ Aktion**: Strategie spezifiziert Verhalten an **jedem**
  Knoten. Probeprüfung 2.2 b): Spieler 2 hat **4 Strategien** (hh, hn,
  nh, nn), nicht 2!
- **Backward induction mit gleichen Auszahlungen**: wenn ein Spieler
  an einem letzten Knoten indifferent ist, sind beide Auszahlungen
  optimal → ggf. **mehrere SPE**.
- **SPE-Anzahl unterschätzen**: bei Indifferenz können es mehrere sein.
- **Normalform-Transformation**: alle Strategien (nicht nur Aktionen)
  auflisten, dann Matrix. Fehlerquelle: vergessene Strategien.
- **Leader-Advantage kennt man nur bei strategischen Substituten**
  (Cournot-artig). Bei strategischen Komplementen (Bertrand mit
  differenzierten Gütern) ist **Second-Mover Advantage** möglich.
- **Rückwärtsinduktion nur bei vollkommener Information** anwendbar
  (jeder sieht alle Züge davor). Sonst: sequentielle Gleichgewichte
  (nicht klausur-relevant).

## Verwandte Inhalte

- HÜ 07 (Dynamische Spiele) — Drill extensive Form + SPE
- HÜ 08 (Stackelberg + Wiederholte Spiele) — Stackelberg-Rechnen
- Probeprüfung 21.02.2024 Aufg. 2.2 (simultan vs. sequentiell, SPE)
- Verbindung zu VL 5 (wiederholtes Spiel = Sonderfall der dynamischen
  Spiele mit sich wiederholender Normalform)
