---
kapitel: 09
thema: Externalitäten (Coase, Pigou, Internalisierung)
vo_einheit: 9
quelle: vorlesung/folien/einheit-09-externalitaeten-transkript.txt
relevanz_klausur: sehr hoch — Thema 7 der nicht bestandenen Klausur
verwandte_hu: 14
stand: 2026-04-15
---

# Kapitel 9 — Externalitäten

## Worum geht's

Eine **Externalität** liegt vor, wenn die Handlung eines Akteurs den
Nutzen oder die Kosten eines anderen **direkt** beeinflusst, **ohne**
dass dies über den Preismechanismus internalisiert wird. Folge: das
Marktgleichgewicht ist **ineffizient** (zu viel bei neg. Extern.,
zu wenig bei pos. Extern.). Lösungen: **Coase** (Verhandlung bei
klaren Eigentumsrechten), **Pigou** (Steuer/Subvention), oder
**Internalisierung** (Fusion, Regulierung, Quoten).

## Kernbegriffe

- **Positive Externalität**: Dritte profitieren, ohne zu zahlen
  (Impfung, F&E, schöner Vorgarten).
- **Negative Externalität**: Dritte tragen Schaden, ohne entschädigt
  zu werden (Lärm, Emissionen, Staus).
- **Privates Optimum**: max $\pi$ nur nach *eigenen* Kosten/Nutzen.
- **Soziales Optimum**: max Gesamtwohlfahrt unter Einbezug aller Effekte.
- **Soziale Grenzkosten (SMC)** $= PMC + MD$ (Marginal Damage).
- **Pigou-Steuer** $t = MD(Q^{\text{sozial}})$: erhöht private
  Grenzkosten auf soziale.
- **Coase-Theorem**: bei klaren Property Rights und niedrigen Transaktions-
  kosten führen Verhandlungen zum effizienten Ergebnis — **unabhängig
  von der Zuteilung** der Rechte.

## Modell

### Privates vs. soziales Optimum (negative Externalität)

Beispiel-Setup: Firma produziert $Q$, verursacht dabei Schaden $D(Q)$
bei Dritten.

| Größe | Privat (Firma) | Sozial (Planer) |
|-------|----------------|-----------------|
| Kosten | $PMC(Q)$       | $SMC(Q) = PMC + MD$ |
| Optimum | $P = PMC$     | $P = SMC$ |
| Menge   | $Q^{\text{priv}}$ | $Q^{\text{soz}} < Q^{\text{priv}}$ |

**Wohlfahrtsverlust (DWL):** Dreieck zwischen $SMC$ und $PMC$ von
$Q^{\text{soz}}$ bis $Q^{\text{priv}}$.

### Klausurfall "Windkraft-Hotel" (Probeprüfung Aufg. 2.3)

$\pi_W = 44r - 2r^2$, $\pi_H = 64g - 2g^2 - 2rg$.
Windräder $r$ verursachen Schaden $2rg$ beim Hotel.

**(1) Fusion (Internalisierung):** Gemeinsame Gewinnfunktion
$\Pi = \pi_W + \pi_H = 44r - 2r^2 + 64g - 2g^2 - 2rg$.

FOCs:
- $\partial \Pi / \partial r = 44 - 4r - 2g = 0$
- $\partial \Pi / \partial g = 64 - 4g - 2r = 0$

Lösung: $r = 8, g = 12$.

**(2) Pigou-Zahlung:** Wind muss $2rg$ an Hotel zahlen.
- Wind max $\pi_W - 2rg = 44r - 2r^2 - 2rg$
- FOC nach $r$: $44 - 4r - 2g = 0 \Rightarrow r^*(g) = 11 - g/2$
- Hotel max $\pi_H$ unabhängig vom Schaden (wird entschädigt):
  $\partial \pi_H / \partial g = 64 - 4g = 0 \Rightarrow g = 16$.

→ Mit Pigou stellt sich **dasselbe** $r = 8, g = 16$ ein wie bei
Fusion? Moment, nicht ganz — Hotel bekommt Zahlung und wählt unabhängig,
Wind berücksichtigt Schaden. Je nach Ausgestaltung kann Pigou das
soziale Optimum replizieren, wenn die Steuer **am sozialen Optimum**
bemessen wird.

### Coase-Theorem (Coase 1960)

**Aussage:** Wenn (i) Eigentumsrechte klar zugeordnet sind, (ii) keine
Transaktionskosten bestehen, und (iii) Verhandlungen möglich sind, dann
erreichen die Parteien das **effiziente** Ergebnis durch Verhandlung —
und zwar **unabhängig davon, wer die Rechte hat**.

**Logik:** Die Partei, für die das Ergebnis wertvoller ist, kauft das
Recht. Beispiele:

- *Rechte für Hotel*: Wind zahlt Hotel für Erlaubnis, Räder aufzustellen.
- *Rechte für Wind*: Hotel zahlt Wind für Reduktion der Anzahl.

In **beiden** Fällen landet man am effizienten Punkt, aber die
**Verteilung** der Rente unterscheidet sich.

### Kritik am Coase-Theorem

- **Transaktionskosten** oft hoch (viele Geschädigte, Info-Asymmetrien).
- **Rechte unklar** in vielen Kontexten (Luft, Meer).
- **Verhandlungsmacht** asymmetrisch (Holdout, Free-Rider).
- **Präferenz-Revelation** schwierig bei öffentlichen Gütern / großer
  Gruppe.

### Pigou-Steuer vs. Coase-Verhandlung

| Aspekt | Pigou-Steuer | Coase-Verhandlung |
|--------|--------------|--------------------|
| Staatliche Intervention | ja (Steuersatz festlegen) | nein (nur Rechte zuweisen) |
| Info-Bedarf | hoch (MD(Q*) kennen) | niedriger |
| Skalierung | auch bei vielen Beteiligten | nur bei wenigen praktikabel |
| Verteilung | Staat bekommt Steuer | Parteien teilen Rente |
| Effizienz | bei korrekter Steuer ✓ | bei Coase-Bedingungen ✓ |

## Positive Externalitäten

Spiegelbildlich: Privatanbieter produziert **zu wenig** (z.B. F&E, Impfung).

- **Sozialer Grenznutzen** $SMB = PMB + ME$ (marginal external benefit).
- **Pigou-Subvention** $s = ME$ schiebt privates Angebot zur sozial
  optimalen Menge.

## Verwandte Konzepte

- **Öffentliche Güter** (Kap. 8): extreme Form positiver Externalität
  (alle genießen, niemand zahlt).
- **Trittbrettfahrer** bei öffentlichen Gütern = Coase-Versagen bei
  großer Gruppe.
- **Lemons-Markt** (Kap. 7): Externalität zwischen guten und schlechten
  Verkäufern (letztere verderben den Markt für erstere).

## Typische Klausuraufgaben

1. **Gegeben PMC, MD, Nachfrage** → privates vs. soziales Optimum
   berechnen, DWL-Dreieck identifizieren.
2. **Pigou-Steuersatz** bestimmen, der soziales Optimum herstellt.
3. **Coase-Verhandlungsfall**: 2 Akteure, verschiedene Eigentumsrechte-
   Zuteilungen, zeige dass effiziente Menge in beiden Fällen erreicht
   wird.
4. **Fusionsfall**: wie bei Probeprüfung 2.3 — gemeinsamer
   Gewinnmaximierer vs. getrennte Maximierer mit Haftung.

## Stolpersteine

- **Sozial optimale Menge** liegt bei negativer Extern. **unter** der
  privaten, nicht darüber. Klassischer Vorzeichenfehler.
- **DWL-Dreieck**: zwischen $SMC$ und $PMC$ (bei negativer Extern.),
  nicht zwischen Nachfrage und $PMC$.
- **Coase-Theorem ist unabhängig von der Verteilung der Rechte, aber
  nicht unabhängig von ihrer Zuweisung**. Eigentumsrechte **müssen
  klar** sein, sonst Verhandlungs-Versagen.
- **Pigou-Steuer am privaten Optimum berechnet** = falsch. Muss am
  **sozialen** Optimum bemessen werden.
- **Internalisierung durch Fusion ≠ Internalisierung durch Steuer**:
  Fusion ist nur bei wenigen Akteuren sinnvoll.
- **Externalität ≠ Marktmacht**. Externalität kann auch im
  Wettbewerbsmarkt auftreten. Beim Monopol kommen beide Ineffizienzen
  zusammen.

## Verwandte Inhalte

- HÜ 14 (Externalitäten)
- Probeprüfung 21.02.2024 Aufg. 2.3 (Windkraft-Hotel, 8 Pkt)
- Verbindung zu VL 8 (öffentliche Güter als Spezialfall positiver Extern.)
