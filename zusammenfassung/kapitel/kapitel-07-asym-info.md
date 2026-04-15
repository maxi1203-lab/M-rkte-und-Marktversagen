---
kapitel: 07
thema: Asymmetrische Information (Adverse Selection, Moral Hazard, Signalling)
vo_einheit: 7
quelle: vorlesung/folien/einheit-07-asymmetric-info-transkript.txt
relevanz_klausur: hoch — Thema 9 (Lemons-Problem) der gefailten Klausur
verwandte_hu: 11, 12
stand: 2026-04-15
---

# Kapitel 7 — Asymmetrische Information

## Worum geht's

Wenn eine Marktseite **besser informiert** ist als die andere, führt das
zu Marktversagen. Zwei Hauptformen:

- **Adverse Selection** (*Hidden Information*, **vor** Vertragsschluss):
  die schlechten Typen verdrängen die guten, Markt kann zusammenbrechen
  (Akerlof-Lemons).
- **Moral Hazard** (*Hidden Action*, **nach** Vertragsschluss): der
  besser informierte Agent handelt schlechter, weil er die Konsequenzen
  nicht voll trägt (Versicherungsnehmer, Manager).

Lösungsansätze: **Signalling**, **Screening**, **Anreiz-Verträge**
(Principal-Agent).

## Kernbegriffe

- **Asymmetrische Information**: ungleicher Wissensstand zwischen
  Marktteilnehmern.
- **Hidden Information**: der Typ einer Partei ist privat bekannt
  (Gesundheit, Qualität).
- **Hidden Action**: das Verhalten ist nicht beobachtbar (Sorgfalt).
- **Pooling-Gleichgewicht**: alle Typen wählen dasselbe Signal/denselben
  Vertrag; keine Typentrennung.
- **Separierendes Gleichgewicht**: verschiedene Typen wählen
  verschiedene Signale/Verträge; Typen werden identifiziert.
- **Signal**: beobachtbare, kostspielige Handlung, die Typ vermittelt
  (Spence: Bildung).
- **Screening**: uninformierte Partei bietet Vertragsmenü, aus dem
  sich Typen selbst offenbaren (Rothschild-Stiglitz).

## Adverse Selection: Akerlof-Lemons-Markt

### Setup

- Gebrauchtwagenmarkt: gute Autos und "Lemons" (Schrottautos).
- Verkäufer kennt Qualität, Käufer nicht.
- Zahlungsbereitschaft Käufer: gut = 1000, schlecht = 500.
- Mindestpreis Verkäufer: gut = 800, schlecht = 0.

### Ergebnis bei symmetrischer Information

- Gute Autos werden für 800–1000 gehandelt.
- Schlechte Autos werden für 0–500 gehandelt.
- **Effiziente Allokation**.

### Ergebnis bei asymmetrischer Information

Käufer berechnet Erwartungswert: mit Anteil $q$ guter Autos ist sein
Reservationspreis $E[W] = q \cdot 1000 + (1-q) \cdot 500 = 500 + 500q$.

- Für Preis $p$ treten gute Autos nur an, wenn $p \geq 800$.
- Wenn $p < 800$: nur Lemons im Markt, $q = 0$, Käufer zahlt max 500.
- Wenn $p \geq 800$: alle Autos im Markt, $q$ beibehalten.

**Fall 1** (6 gute, 6 schlechte, $q = 0.5$): $E[W] = 750 < 800$.
Käufer zahlt höchstens 750 → gute Verkäufer bleiben weg →
**Markt bricht auf schlechte Autos ein**.

**Fall 2** (8 gute, 4 schlechte, $q = 2/3$): $E[W] = 833 > 800$.
Käufer zahlt 833 → alle Verkäufer bieten an → **Markt funktioniert**.

**Kernidee:** Die Existenz eines funktionierenden Marktes hängt vom
**Anteil guter Typen** ab. Unterhalb einer Schwelle bricht der Markt
zusammen — selektion des "adverse" Typs.

### Lösungen

1. **Signalling** (Spence 1973): besser informierte Seite sendet
   kostspieliges Signal, das für schlechten Typ **relativ** teurer ist.
   Beispiel: Bildung auf Arbeitsmarkt, Garantieversprechen bei Autos.
2. **Screening** (Rothschild-Stiglitz 1976): schlechter informierte
   Seite bietet Vertragsmenü; Typen offenbaren sich durch Wahl.
   Beispiel: Versicherungsverträge mit Selbstbehalt.
3. **Reputation**: wiederholte Interaktion macht Abweichung teuer
   (VL 5).
4. **Intermediäre / Zertifizierung**: TÜV, Rating-Agenturen.

## Signalling: Spence-Modell (Bildungssignal)

Zwei Arbeitnehmer-Typen, hoch und niedrig produktiv. Bildung ist für
hohe Typen **billiger** zu erwerben ($c_H < c_L$).

**Separierendes Gleichgewicht:**
- Hohe Typen: Bildung $e^* > 0$, Lohn = hohe Produktivität.
- Niedrige Typen: keine Bildung, Lohn = niedrige Produktivität.

**Bedingung**: Bildungskosten müssen so gewählt sein, dass niedrige
Typen $e^*$ nicht nachahmen wollen. IC-Bedingung:

$$w_H - c_L(e^*) < w_L \quad \iff \quad e^* > \tfrac{w_H - w_L}{c_L}$$

**Problem**: Bildung hat in diesem Modell **keinen Produktivitätswert**,
sie dient nur als Signal → soziale Verschwendung, aber individuell
rational.

## Moral Hazard (Principal-Agent)

### Setup

- **Prinzipal** (z.B. Arbeitgeber) engagiert **Agenten** (z.B.
  Angestellte).
- Agent wählt Anstrengung $e$ (nicht beobachtbar).
- Ergebnis $y$ hängt von $e$ und Zufall ab.
- Prinzipal bezahlt Lohn $w(y)$ (nur von beobachtbarem $y$ abhängig).

### Erste-Best-Lösung (beobachtbares $e$)

Prinzipal zahlt Fixlohn, Agent trägt kein Risiko. Agent ist voll
abgesichert, Prinzipal trägt das Risiko (wenn risikoneutral). Anstrengung
ist vertraglich durchsetzbar.

### Zweite-Best-Lösung (hidden action)

Bei nicht-beobachtbarem $e$ muss der Vertrag **Anreize** setzen:
- **Individual Rationality (IR)**: Agent akzeptiert nur, wenn
  Erwartungsnutzen ≥ Outside Option.
- **Incentive Compatibility (IC)**: Agent wählt das gewünschte $e$
  freiwillig.
- **Risikotrade-off**: bei risikoaversem Agenten verteuert Risiko-
  übertragung den Vertrag → zweite-Best.

**Standard-Ergebnis**: bei risikoaversem Agenten ist optimaler Vertrag
**variabler Lohn** (teilweise Risikotragung), aber nicht voll
ergebnisabhängig. Das ist *suboptimal* im Vergleich zur ersten-Best-
Lösung, aber das **beste Erreichbare** unter asym. Info.

### Anwendungen

- **Versicherung**: Selbstbehalt damit Versicherungsnehmer vorsichtig bleibt.
- **Aktienoptionen** für Manager: Anreizangleichung.
- **Bonus-Zahlungen**, Provisionen.

## Typische Klausuraufgaben

1. **Lemons-Markt rechnen**: gegeben $q$, Reservations-Preise → bricht
   der Markt zusammen? Bei welchem $q^*$ liegt die Schwelle?
2. **Spence-Signalling**: IC-Bedingung für trennendes Gleichgewicht.
3. **Principal-Agent-Fall** einfach: IR + IC aufstellen, ersten-Best
   vs. zweite-Best.
4. **Diskussionsaufgabe**: "Wie löst Coase das Lemons-Problem (oder
   nicht)?" → nicht immer, weil Transaktionskosten.

## Stolpersteine

- **Adverse Selection vs. Moral Hazard**: Typ vs. Aktion. Merke:
  Adverse = *Auswahl von schlechten Typen*, Moral = *schlechtes
  Verhalten nach Abschluss*.
- **Lemons-Schwelle**: Markt bricht **nicht immer** zusammen, nur wenn
  Anteil guter Typen unter Schwelle fällt. Rechnung sorgfältig.
- **Signalling nur bei Kostendifferenz**: wenn $c_H = c_L$, kann kein
  Signal die Typen trennen.
- **Pooling vs. Separierend** verwechseln: im pooling kriegen alle
  denselben Vertrag, im separierend je nach Typ.
- **First-best vs. second-best** in Principal-Agent: erstes-Best
  setzt beobachtbares $e$ voraus; wenn Aufgabe "hidden action" sagt,
  ist zweites-Best gefragt.
- **Risikoneutraler Agent** macht Principal-Agent trivial: er trägt
  alles Risiko, voll ergebnisabhängiger Lohn, first-best.

## Verwandte Inhalte

- HÜ 11 (Risiko + Lemons): Lemons-Markt-Drill
- HÜ 12 (AsymInfo + Öff. Güter): kombiniert
- Verbindung zu VL 6 (Risikoaversion → P-A)
- Verbindung zu VL 8 (öff. Güter = Präferenz-Revelation, verwandt mit
  Screening)
