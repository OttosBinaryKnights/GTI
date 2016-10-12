# Übung 12
## Aufgabe 1:
*Seien A und B jeweils NP-vollständig. Gilt dann $B \preceq_PA$ und $A\preceq_PB$? Begründen Sie ihre Antwort.*

$A,B\in NPC$

Beweis:
es sei $\forall L \in NP$

$$L \preceq_PB \Rightarrow A \preceq_PB$$
$$ L \preceq_PA \Rightarrow B \preceq_PA$$

$\rightarrow$ möglich

---
## Aufgabe 2:
*Seien $A,B\subset \Sigma^ * $ Sprachen in P, die jeweils nicht leer und jeweils von $\Sigma^ *$ verschieden sind. Gilt dann $A\preceq_PB$? Begründen Sie ihre Antwort.*

$A,B \subset \Sigma^* , A \land B \text{ nicht-leer } , \in P$, $A \neq \Sigma^* \land B \neq \Sigma^* $

|               | b,   | falls $x\in A$ |
| ------------- | ---- | -------------- |
| $f(x)=\Bigg\{$ |      |                |
|               | b'   | falls $x \notin A$ |

ein festes b, welches Element von B ist, lässt sich finden, da B echte Teilmenge von $\Sigma^* $ ist.

dann ist $A \preceq_P B$ möglich, da $x \in A \Leftrightarrow f(x)\in B$ erfüllt ist.

$\rightarrow A \preceq_P B$ ist möglich.

---
## Aufgabe 3:
*Beim Problem 3-FÄRBBARKEIT ist zu entscheiden, ob die Knoten eines ungerichteten Graphen G so mit drei verschiedenen Farben gefärbt werden können, dass keine zwei benachbarten Knoten, also Knoten, die durch eine Kante verbunden sind, die gleiche Farbe haben.
Zeigen Sie 3-FÄRBBARKEIT$\preceq_P$SAT.*

$G$, 3-färbbar, $\alpha:V\rightarrow\{r,g,b\}$

$G(V,E)$

$\forall \{u,w\}\in E:\alpha(u)\neq \alpha(w)$

3 Variablenpro Knoten $u:x_r^u,x_y^u,x_b^u$

---
## Aufgabe 4:
*Zeigen Sie, dass die Sprache $DOUBLE-SAT = \{\langle \phi \rangle |\phi$ ist eine Boolesche Formel in konjunktiver Normalform, fuer die es mindestens zwei verschiedene erfuellende Belegungen der Variablen gibt} eine NP- vollständige Sprache ist.*

---
## Aufgabe5:
*Ein Kachelproblem ist gegeben durch ein Viertupel $D=(D,d_1,H,V)$,wobei D eine endliche Menge von Kacheln ist, $d_1$ eine dieser Kacheln und $H,V\subseteq D\times D$. Gesucht ist eine Funktion $f:Z\times N\rightarrow D$, so dass $f(1,1)=d_1$ und$(f(m,n),f(m+1,n))\in H$ für alle $m\in Z,n\in N$ und $(f(m,n),f(m,n+1))\in V$ für alle $m\in Z, n \in N$. Eine solche Funktion nennen wir D -Kachelung.
Zeigen Sie, dass die Sprache $\{\langle D \rangle | \text{ es gibt eine D -Kachelung}\}$ nicht entscheidbar ist.*

**Hinweis: Zeigen Sie $H\varepsilon \preceq \{\langle D\rangle | \text{ es gibt keine D-Kachelung}\}$.**

![Kachel](Kachel.png)
