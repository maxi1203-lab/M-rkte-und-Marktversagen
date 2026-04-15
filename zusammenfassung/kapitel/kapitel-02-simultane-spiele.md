---
kapitel: 02
thema: Simultane Spiele (Normalform, Nash-Gleichgewicht)
vo_einheit: 2
quelle: vorlesung/folien/einheit-02-simultane-spiele-transkript.txt
relevanz_klausur: sehr hoch — Thema 1+2 der nicht bestandenen Klausur
verwandte_hu: 03, 04
stand: 2026-04-15
---

# Kapitel 2 — Simultane Spiele

## Worum geht's

Bei **simultanen Spielen** entscheiden alle Spieler **gleichzeitig** (oder
zumindest ohne das Verhalten der anderen zu beobachten). Das Standard-
Werkzeug ist die **Normalform** (Auszahlungs-Matrix). Gesucht: ein
**strategisches Gleichgewicht**, in dem niemand einseitig abweichen will.
Hierarchie der Lösungskonzepte: **Dominanz** (stark > schwach) →
**iterative Elimination** → **Nash-Gleichgewicht** in reinen oder
gemischten Strategien.

## Kernbegriffe

- **Spiel** = (Spieler, Strategien, Auszahlungen, Information, Timing).
- **Normalform**: Auszahlungsmatrix $(u_1, u_2)$ pro Zellen-Kombination.
- **Strategie $s_i$**: vollständiger Handlungsplan für Spieler $i$.
- **Dominante Strategie**: $s_i^*$ liefert Spieler $i$ die höchste
  Auszahlung **für jede mögliche Strategie der anderen**.
- **Strikt dominierte Strategie**: gibt es eine andere, die immer strikt
  besser ist — kann **eliminiert** werden.
- **Beste Antwort** (BR): $s_i^*$ maximiert $u_i$ **gegeben** $s_{-i}$.
- **Nash-Gleichgewicht** (NGG): Strategieprofil $(s_1^*, \dots, s_n^*)$,
  bei dem **jede** Strategie beste Antwort auf die anderen ist.
- **Gemischte Strategie**: Wahrscheinlichkeitsverteilung über reine
  Strategien.

## Modell

### Normalform: was gehört rein

| Element | Symbol | Bsp. Gefangenendilemma |
|---------|--------|------------------------|
| Spieler-Menge | $I$ | $\{A, B\}$ |
| Strategiemengen | $S_i$ | $\{\text{gestehen}, \text{schweigen}\}$ |
| Auszahlungen | $u_i: S_1 \times \dots \times S_n \to \mathbb{R}$ | siehe Matrix |

### Gefangenendilemma (Standardbeispiel)

|          | **B gestehen** | **B schweigen** |
|----------|----------------|-----------------|
| **A gestehen** | $(-5, -5)$ | $(0, -10)$ |
| **A schweigen** | $(-10, 0)$ | $(-1, -1)$ |

- **Gestehen** ist dominante Strategie für beide.
- GGW $(G, G)$ liefert $(-5, -5)$, obwohl $(S, S)$ mit $(-1, -1)$
  Pareto-besser wäre. **Das Dilemma:** rationale Einzelentscheidungen
  führen zu kollektiv schlechtem Ergebnis.
- **Übertragbar** auf: Kartellstabilität, Klimaschutz, Werbung, Rüstung.

### Iterierte Elimination dominierter Strategien

1. Finde für jeden Spieler strikt dominierte Strategie.
2. Streiche sie aus der Matrix.
3. Wiederhole, bis nichts mehr eliminierbar ist.

Wenn ein einziges Profil übrig bleibt → dominance-solvable. Funktioniert
nur manchmal (oft bleibt mehr übrig; dann Nash nutzen).

### Nash-Gleichgewicht: Such-Algorithmus

1. Für jede Spalte (= Strategie von Spieler 2) die höchste Auszahlung
   von Spieler 1 **unterstreichen** (oder einkreisen).
2. Für jede Zeile die höchste Auszahlung von Spieler 2 unterstreichen.
3. Zelle, in der **beide** Werte markiert sind → Nash-GG.

**Formale Definition:**

$$(s_1^*, \dots, s_n^*) \text{ ist NGG} \iff \forall i, \forall s_i \in S_i: \quad u_i(s_i^*, s_{-i}^*) \geq u_i(s_i, s_{-i}^*)$$

### Nash-Existenz (Nash 1950)

- In jedem **endlichen** Spiel existiert **mindestens ein** NGG, ggf. in
  gemischten Strategien.
- Reine NGG können **null, eins oder mehrere** sein.

### Multiple Gleichgewichte: Battle of the Sexes

|          | **Eva Boxen** | **Eva Theater** |
|----------|--------------|-----------------|
| **Adam Boxen** | $(2, 1)$ | $(0, 0)$ |
| **Adam Theater** | $(0, 0)$ | $(1, 2)$ |

Zwei reine NGG: (B,B) und (T,T). **Selektionsproblem** — wie wählen?
- Kommunikation vor dem Spiel
- Fokal-Punkte (Schelling)
- Commitment ("Adam hat Boxkarten gekauft")
- Pareto-Dominanz, falls vorhanden
- Gemischtes NGG (s.u.)

### Gemischte Strategien

Spieler $i$ wählt Strategie $s_{ij}$ mit Wahrscheinlichkeit $p_{ij}$.
Erwarteter Nutzen:

$$E[u_i] = \sum_{s_{-i}} \left[\prod_{k \neq i} p_k(s_k)\right] \cdot u_i(s_i, s_{-i})$$

**Indifferenz-Bedingung** (Kernidee):
Im gemischten NGG ist Spieler $i$ zwischen seinen Reinstrategien
**indifferent**. Die Gegner-Mischung muss Spieler $i$ genau indifferent
machen — daraus löst man die Wahrscheinlichkeiten.

**Rechentrick** für 2×2-Spiele:
- Sei $q$ = Wahrscheinlichkeit, dass Spieler 2 Strategie "links" spielt.
- Spieler 1 indifferent ⟹ $u_1(\text{oben}, q) = u_1(\text{unten}, q)$.
- Nach $q$ auflösen. Analog für $p$ (Spieler 1 Wahrscheinlichkeit).

## Typische Klausuraufgaben

1. **Matrix gegeben → dominante Strategie, Nash-GG in reinen Strategien**
   (SC, "Wer hat eine dominante Strategie?" — vgl. Probeprüfung Aufg. 1.4).
2. **Matrix → gemischtes NGG bestimmen** (offene Aufgabe, 3×3 oder 2×2).
3. **Spiel in Normalform bringen** aus Text-Beschreibung.
4. **Werbung-/Cournot-/Preis-Spiel** als simultanes Spiel modellieren.

## Stolpersteine

- **"Dominant" ≠ "Nash"**. Jedes Profil in dominanten Strategien ist
  NGG — umgekehrt gilt es nicht. Nash ist das schwächere Konzept.
- **"Dominiert" ≠ "dominiert wird"**. Man eliminiert die Strategie,
  die *für sich selbst* schlechter ist (nicht die, die andere dominiert).
- **Strikte vs. schwache Dominanz**: bei iterierter Elimination nur
  **strikt** dominierte Strategien eliminieren, sonst können GGW
  verloren gehen.
- **Multiple Nash-GG**: nicht "Ausweg suchen" durch Pareto — die Aufgabe
  fragt oft nach **allen** NGG. Erst wenn *"welches wird gespielt"*
  gefragt ist, Selektionskriterien anwenden.
- **Gemischtes NGG vergessen**: wenn kein reines existiert und die
  Aufgabe nach NGG fragt, musst du das gemischte finden.
- **Matrix-Fehler**: beim Transkribieren aus Text oft Zeilen/Spalten
  verwechselt — Wer-spielt-was nochmal prüfen.

## Verwandte Inhalte

- HÜ 03 (Preisdiskr. + Simultane Spiele) → Matrix-Aufgaben
- HÜ 04 (Simultane Spiele) → Hauptübung dazu
- Probeprüfung 21.02.2024, Aufg. 1.4 (dominante Strategie) und 2.2
  (simultan vs. sequentiell)
- Verwandt in VL 3 (Oligopol als strategisches Spiel) und VL 4
  (dynamische Spiele = Normalform erweitert um Timing)
