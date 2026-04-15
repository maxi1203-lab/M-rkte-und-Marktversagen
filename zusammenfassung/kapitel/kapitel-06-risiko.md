---
kapitel: 06
thema: Entscheidung unter Risiko (Erwartungsnutzen, Risikoaversion)
vo_einheit: 6
quelle: vorlesung/folien/einheit-06-risiko-entscheidungen-transkript.txt
relevanz_klausur: hoch — SC-typisch (Sicherheitsäquivalent, Erwartungsnutzen)
verwandte_hu: 10, 11
stand: 2026-04-15
---

# Kapitel 6 — Entscheidung unter Risiko

## Worum geht's

**Risiko** heißt: Ergebnisse einer Entscheidung sind stochastisch
(Wahrscheinlichkeiten bekannt, anders als *Unsicherheit* ohne W'keiten).
Das Standardmodell ist die **Erwartungsnutzen-Hypothese** (vNM):
ein rationaler Entscheider maximiert $E[u(x)]$ statt $E[x]$. Aus der
**Krümmung** von $u(\cdot)$ ergibt sich Risikoeinstellung. Messbar über
**Sicherheitsäquivalent** und **Risikoprämie**.

## Kernbegriffe

- **Lotterie** $L = [(x_1, p_1), (x_2, p_2), \dots, (x_n, p_n)]$ mit
  $\sum p_i = 1$.
- **Erwartungswert** $E[L] = \sum p_i x_i$.
- **Erwartungsnutzen** $E[u(L)] = \sum p_i u(x_i)$.
- **Nutzenfunktion** $u: X \to \mathbb{R}$, stetig, monoton steigend
  (mehr ist besser).
- **Risikoaversion** ⟺ $u$ konkav ($u'' < 0$).
- **Risikoneutralität** ⟺ $u$ linear.
- **Risikofreude** ⟺ $u$ konvex.
- **Sicherheitsäquivalent** $S(L)$: sichere Zahlung, die gleichen
  Erwartungsnutzen liefert wie die Lotterie.
- **Risikoprämie** $RP(L) = E[L] - S(L) \geq 0$ (bei Risikoaversion).

## Modell

### Erwartungsnutzen-Hypothese (vNM)

Ein rationaler Entscheider hat Präferenzen über Lotterien, die durch eine
Nutzenfunktion $u$ repräsentiert werden, sodass

$$L_1 \succeq L_2 \iff E[u(L_1)] \geq E[u(L_2)]$$

Maximierung von $E[u(L)]$, **nicht** von $E[L]$ (außer bei
Risikoneutralität).

### Risikoaversion geometrisch

Sei $L$ eine 50-50-Lotterie zwischen $x_1$ und $x_2$. Dann:

- **Erwartungswert**: $E[L] = 0.5 \cdot x_1 + 0.5 \cdot x_2$
- **Erwartungsnutzen**: $E[u(L)] = 0.5 \cdot u(x_1) + 0.5 \cdot u(x_2)$

In der Grafik $u(x)$-gegen-$x$:

- $u(E[L])$ = Punkt auf der Kurve über $E[L]$.
- $E[u(L)]$ = Punkt auf der **Sehne** zwischen $(x_1, u(x_1))$ und
  $(x_2, u(x_2))$ über $E[L]$.
- Bei konkavem $u$: $u(E[L]) > E[u(L)]$ (**Jensen**). Also lieber
  sicherer Erwartungswert als die Lotterie → **risikoavers**.

### Sicherheitsäquivalent $S(L)$

Definition:

$$u(S(L)) = E[u(L)]$$

Rechnerische Schritte (Standard-Klausuraufgabe):

1. $E[u(L)] = \sum p_i u(x_i)$ berechnen.
2. $S = u^{-1}(E[u(L)])$.

**Beispiel** (vgl. Probeprüfung Aufg. 1.6):
$u(w) = 10 w^{0.5}$, Investition zahlt $25$ mit $p=0.4$, $100$ mit $p=0.6$.

- $E[u] = 0.4 \cdot 10 \sqrt{25} + 0.6 \cdot 10 \sqrt{100} = 0.4 \cdot 50 + 0.6 \cdot 100 = 20 + 60 = 80$
- $u(S) = 80 \Rightarrow 10\sqrt{S} = 80 \Rightarrow \sqrt{S} = 8 \Rightarrow S = 64$.

### Risikoprämie

$$RP(L) = E[L] - S(L)$$

Im Beispiel: $E[L] = 0.4 \cdot 25 + 0.6 \cdot 100 = 70$, also
$RP = 70 - 64 = 6$. Das ist der Betrag, den der Entscheider **bereit ist
aufzugeben**, um das Risiko loszuwerden.

### Typische Nutzenfunktionen

| $u(w)$ | Risikoeinstellung | Bemerkung |
|--------|-------------------|-----------|
| $w$    | risikoneutral     | keine RP |
| $\sqrt{w}$ (bzw. $a \sqrt{w}$) | risikoavers | Standard-Klausurform |
| $\ln w$ | risikoavers       | fallende abs. RA |
| $1 - e^{-\alpha w}$ | risikoavers | konstante abs. RA |
| $w^2$  | risikofreudig     | selten in Klausur |

### Arrow-Pratt-Maße

- **Absolute Risikoaversion**: $A(w) = -\dfrac{u''(w)}{u'(w)}$.
- **Relative Risikoaversion**: $R(w) = w \cdot A(w)$.

Je größer $A(w)$, desto größer die Risikoprämie (bei kleinen Risiken:
$RP \approx \tfrac{1}{2} A(w) \sigma^2$). **Nicht-klausurkritisch**, aber
hilfreich als Interpretation.

### Versicherungs-Logik

Standard-Entscheidung: Lotterie $L$ mit Verlust-Risiko vs. faire
Versicherung zum Preis $p = E[\text{Verlust}]$.

- **Risikoavers**: zahlt bis zu $E[\text{Verlust}] + RP$, also **mehr
  als fair** — deshalb existiert Versicherungsmarkt trotz Profit.
- **Risikoneutral**: indifferent gegenüber fairer Versicherung.
- **Risikofreudig**: würde sogar Geld nehmen, um sich *nicht* zu
  versichern.

## Typische Klausuraufgaben

1. **Gegeben $u$, Lotterie** → berechne $E[u], S, RP$. Standard SC oder
   Einstiegs-SC (Probeprüfung Aufg. 1.2, 1.6).
2. **Indifferenz-Aufgaben**: Student ist indifferent zwischen sicherer
   Zahlung und Lotterie; $u$-Wert eines Punkts gegeben → $u(x)$ an
   einem anderen Punkt bestimmen. (Probeprüfung Aufg. 1.2)
3. **Versicherung ja/nein** bei gegebener Nutzenfunktion.
4. **Risikoprämie-Interpretation** in Worten.

## Stolpersteine

- **$E[u(L)] \neq u(E[L])$!** Die häufigste Falle. Bei konkavem $u$ gilt
  $E[u] < u(E)$; das ist exakt der Grund, warum $S < E[L]$.
- **Reihenfolge** bei Sicherheitsäquivalent: Erst $E[u]$ rechnen, dann
  $u^{-1}$ — nicht $u^{-1}$ auf die Wahrscheinlichkeiten anwenden.
- **$\sqrt{}$ vs. Hoch-0.5**: bei $u(w) = aw^{0.5}$ oft Faktor $a$
  vergessen. Im Beispiel mit $10w^{0.5}$ ist $u(64) = 80$, nicht $64$.
- **Wahrscheinlichkeiten prüfen**: $\sum p_i = 1$? Oft subtil
  verschoben in Aufgabentexten.
- **Risikoneutral vs. risikoavers**: bei linearem $u$ → $S = E[L]$,
  $RP = 0$. Wenn die Klausur fragt "was ist RP bei linearer Nutzenfkt?",
  ist die Antwort **0**, nicht "nicht definiert".
- **Geldeinheiten** und **Nutzen-Einheiten** nicht verwechseln. $S$ und
  $E[L]$ sind in Geldeinheiten, $u(\cdot)$ nicht.

## Verwandte Inhalte

- HÜ 10 (Entscheidung unter Risiko) — Drill-Rechnungen
- HÜ 11 (Risiko + Lemons) — kombiniert mit Adverse Selection
- Probeprüfung 21.02.2024 Aufg. 1.2 (U(100)-Aufgabe), 1.6 ($S=64$)
- Verbindung zu VL 7 (Asym. Info): Versicherungsmärkte
