# Übung 3
## Aufgabe 1:
**Beweisen oder widerlegen Sie folgende Behauptung über Sprachen: $ \forall L_1, L_2, L_3: L_1 (L_2 - L_3) = L_1 L_2-L_1 L_3$ **

Gegenbeispiel: $L_1=\{b,bb\}; L_2=\{a,ba\}; L_3=\{a\}$

$$\{b,bb\} \{ba\} \neq \{ba,bba,bbba\} - \{ba,bba\}$$
$$\{bba,bbba\} \neq \{bbba\}$$

---
## Aufgabe 2:
**Gegeben seien die folgenden Zustandsübergangsdiagramme endlicher Automaten M1 und M2:
![img](img01.jpg)
Geben Sie formale Beschreibungen der Automaten M1 und M2 an.
Beantworten Sie die folgenden Fragen für jeden der beiden Automaten:**

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


$M_2 = \{K_2, \sum, \delta_2, s, F_2 \}$

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

* **a) Was ist die Folge der Zustände, die bei Eingabe aabb erreicht werden?**



 $M_1:(q1,aabb) \vdash_{M1} (q2, abb))$
 $\vdash_{M1} (q3, bb))$
 $\vdash_{M1} (q1, b))$
  $\vdash_{M1} (q1, \epsilon))$

 $\rightarrow$ nicht akzeptiert, da $q_1 \notin F$


 $M_2:(q1,aabb) \vdash_{M2} (q1, abb))$
 $\vdash_{M2} (q1, bb))$
 $\vdash_{M2} (q2, b))$
  $\vdash_{M2} (q4, \epsilon))$

 $\rightarrow$ akzeptiert, da $q_4 \in F_2$

* **b) Wird das Wort aabb akzeptiert?**

 $M_1:$ Nein, $q_1 \notin F$

 $M_2:$ Ja, $q_4 \in F$

* **c) Wird das leere Wort $\epsilon$ akzeptiert?**

 Nur bei $M_2$ da Startzustand $q1$ auch Endzustand

 ---

## Aufgabe 3:
 Sei M durch folgendes Zustandsübergangsdiagramm gegeben. Was ist L(M)? Beweisen Sie ihre Antwort!
 ![img](img02.jpg)

 ---

## Aufgabe 4:
Geben Sie deterministische endliche Automaten an, die die folgenden Sprachen akzeptieren:
 * a) $\{w \in \{a,b\}^* | w \text{ beginnt mit aba}\}$
 ![Automat](Automat_4a.jpg)

 * b) $\{w \in \{a,b\}^* |w \text{ enthaelt genau 2 a}\}$
  ![Automat](Automat_4b.jpg)

---

## Aufgabe 5:
Geben Sie deterministische endliche Automaten an, die die folgenden Sprachen akzeptieren:
 * a) $\{w \in \{a,b\}^* | \text{ in w folgt auf jedes a unmittelbar ein b}\}$
  ![Automat](Automat_5a.jpg)

 * b) $\{w \in \{a,b\}^* | w \text{ enthaelt das Teilwort aabab}\}$
 ![Automat](Automat_5b.jpg)

 ---

## Aufgabe 6:
**Geben Sie jeweils (nichtdeterministische) endliche Automaten an, die die folgenden Sprachen akzeptieren:**

*Unterschied zur deterministischem Automaten: Statt $\delta$ Überführungsfunktion ist's eine Überführungsrelation.*
 * a) $\{w \in \{a,b\}^* | w \text{ beginnt mit b und endet mit a}\}$
  ![Automat](Automat_6a.jpg)

 * b) $\{w \in \{0,7\}^* | w \text{ enthaelt das Teilwort 007}\}$
 ![Automat](Automat_6b.jpg)

 ---

## Aufgabe 7:
Geben Sie jeweils (nichtdeterministische) endliche Automaten an, die die folgenden Sprachen akzeptieren:

 * a) $\{w \in \{a,b\}^* | |w| \leq 3\}$
  ![Automat](Automat_7a.jpg)
 * b) $\{w \in \{a,b\}^* | w \text{an jeder ungeraden Position in w steht ein b}\}$
  ![Automat](Automat_7b.jpg)
