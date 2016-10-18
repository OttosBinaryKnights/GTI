# Übung 02
## 1. Es seien die Menge $M = \{a,b,c,d,e\}$ sowie die Relation $R\subseteq M_2$, definiert durch $R = \{(a, b), (a, c), (a, d), (d, c), (d, e)\}$, gegeben.

*Reflexiv:*
$\forall a \in A:(a,a) \in R$

*Symmetrie:*
$\forall a,b \in A:(a,b)\in R \Rightarrow (b,a)\in R$

*Transitivität:*
$\forall a,b,c \in A:aRb \land bRc \Rightarrow aRc$

* a) Bestimmen Sie die reflexive und transitive Hülle $R^* $ der Relation R.

  $R=\{(a,a),(b,b),(c,c),(a,b),(b,c),(a,c)\}$

  ![Relation01](Relation02.jpg)

* b) Zeichnen Sie die gerichteten Graphen $G = (M, R)$ und $G^* = (M, R^* )$.

---

## 2.
* **a) Beweisen Sie, dass die Menge der Wörter über einem Alphabet abzählbar unendlich ist.**

* **b) Beweisen Sie, dass die Menge der Sprachen über einem Alphabet überabzählbar unendlich ist.**

---

## 3. Beweisen Sie durch vollständige Induktion, dass die Ungleichung $n^2 > 2n + 1$ für alle natürlichen Zahlen $n\geq 3$ gilt.

es soll gelten: $n^2 > 2n + 1$

* Indunktionsanfang:
für $n=3$
$3^2>2*3+1$
$9>7$ -> w.A

* Indunktionsbehauptung:
$n^2>2n+1$

* Induktionsschritt $n \rightarrow (n+1)$
$(n+1)^2>2(n+1)+1$
$n^2+2n+1>2n+2+1$
$n^2+2n+1>2n+3 | -2n-1$
$n^2>2$ w.A für $n\geq 3$


---

## 4. Es sei $\sum = \{a, b\}$. Wir definieren eine Sprache L über $\sum$ induktiv wie folgt.
(1) ε gehört zu L.
(2) Falls $x \in L$ ist, dann gehört auch abxb zu L.
(3) Falls $x\in L$ ist, dann gehört auch bxba zu L.
(4) Falls $x\in L$ und $y\in L$,dann gehört auch xy zu L.

**Beweisen Sie durch strukturelle Induktion, dass alle Wörter in L doppelt so viele b wie a enthalten.**

Beweis durch struktuelle Induktion:

* IA: $ \varepsilon \in L, |\varepsilon|_ a =|\varepsilon|_ b=0$

* IV: $x,y \in L, |x|_ a =|x|_ b, |y|_ a=|y|_ b$

* IB:
  * 1) $axb \in L, |axb|_ a=|axb|_ b, \text{da } w=axb$
    $|w|_ a=|axb|_ a=1+|x|_ a=1+|x|_ b=(\text{laut IV})|axb|_ b=|w|_ b$

  * 2) $bxa \in L, |bxa|_ a=|bxa|_ b \rightarrow \text{analog zu 1)}$
  * 3) $xy \in L, |xy|_ a=|xy|_ b$
    $|xy|_ a=|x|_ a+|y|_ a=(\text{laut IV})|x|_ b+|y|_ b=|xy|_ b$

---

## 5. In der Vorlesung sitzen n Studenten, n ≥ 2, die sich teilweise gegenseitig kennen. Zeigen Sie, dass es zwei verschiedene Studenten gibt, die mit gleich vielen anderen Studenten bekannt sind.

---

## 6. Es seien die folgenden Zustandsdiagramme deterministischer endlicher Automaten $M_1$ und $M_2$ gegeben.

![Automat M1 und M2](AutomatM1M2.png)

* **a) Geben Sie formale Beschreibungen der Automaten M1 und M2 an.**

  * $M$ - Automat
  * $K$ - Menge der Zustände
  * $F$ - Menge Endzustände ($F \subseteq K$)
  * $\sum$ - Alphabet (nicht leere, engliche Menge von Zeichen)
  * $L$ - Sprache (Menge der Wörter)
  * $\delta$ - Überführungsfunktion
  * $s$ - Startzustand ($s \in K$)
  * $\vdash$ "überführt "

  **allg.: $M = (K, \sum, \delta, s, F  )$**

$M_1 = \{K_1, \sum, \delta_1, q_1, F_1 \}$
$K_1 = \{q_1, q_2, q_3\}$
$F_1 = \{q_2\}$
$\sum = \{a,b\}$
**Überführungsfunktion $\delta_1$**

| $\delta_1$ | | a | b |
| --- | --- | :---: | :---: |
| $q_1$ | |$q_2$ | $q_1$ |
| $q_2$ | |$q_3$ | $q_3$ |
| $q_3$ || $q_2$ | $q_1$ |


$M_2 = \{K_2, \sum, \delta_2, q_1, F_2 \}$
$K_2 = \{q_1, q_2, q_3, q_4\}$
$s = q_1$
$F_2 = \{q_1, q_4\}$
$\sum = \{a,b\}$
**Überführungsfunktion $\delta_2$**

| $\delta_2$ | | a | b |
| --- | --- | :---: | :---: |
| $q_1$ | |$q_1$ | $q_2$ |
| $q_2$ | |$q_3$ | $q_4$ |
| $q_3$ || $q_2$ | $q_1$ |
| $q_4$ || $q_3$ | $q_4$ |

* **b) Geben Sie für beide Automaten die Folge der Konfigurationen bei der Verarbeitung der Ein-
gabe aabb an.**

  * $M_1:(q1,aabb) \vdash_{M1} (q2, abb))$
$\vdash_{M1} (q3, bb))$
$\vdash_{M1} (q1, b))$
 $\vdash_{M1} (q1, \epsilon))$
$\rightarrow$ nicht akzeptiert, da $q_1 \notin F$

  * $M_2:(q1,aabb) \vdash_{M2} (q1, abb))$
$\vdash_{M2} (q1, bb))$
$\vdash_{M2} (q2, b))$
 $\vdash_{M2} (q4, \epsilon))$
$\rightarrow$ akzeptiert, da $q_4 \in F_2$

* **c) Wird jeweils das Wort aabb akzeptiert? Begründen Sie ihre Antwort.**

  $M_1:$ Nein, $q_1 \notin F$

  $M_2:$ Ja, $q_4 \in F$

* **d) Wird jeweils das leere Wort ε akzeptiert? Begründen Sie ihre Antwort.**
Nur bei $M_2$ da Startzustand $q1$ auch Endzustand ist.
