# Übung 13
## Aufgabe 1:
*Ist die Sprache $\{\langle G\rangle | G \text{ ist eine kontextfreie Grammatik und } \varepsilon \in L(G)\}$ entscheidbar? Begründen
Sie ihre Antwort.*

Ja.

Beispiel:

$S\rightarrow AB$

$A\rightarrow CC$

$B\rightarrow \varepsilon$

$C\rightarrow \varepsilon$

$S\rightarrow \varepsilon$

Ausschluss aller, die auf Epsilon abbilden

$\{B,C\}$

$\{B,C,A\}$

$\{B.C,A,S\}$


---
## Aufgabe 2:
*Sei $HITTING-SET = \{\langle C,k\rangle | C = \{C_1,...,C_m\}$ ist eine Familie von m Teilmengen einer endlichen Menge U, und es gibt eine Menge $S \subseteq U$ der Größe höchstens k, so dass für alle Teilmengen $C_i$ in C gilt $S\cup C_i \neq 0\}$. Zeigen Sie $VERTEX-COVER \preceq P HITTING-SET$.*

HITTING-SET ->
* Beispiel: $U=\{A,B,C.D\}$
$C_1=\{A\}, C_2=\{C\}$

* ges.:
gesucht ist ein HITTING-SET mit einem nicht leeren Set der größe k.
$S=\{A,B,C\}$

Reduktion von VERTEX-COVER auf HITTING-SET:

$<G,k>$ $G=(U,E)$

$U=V$

$C=E$

1. Redukrionskunktion

|     |     $ <\sqcup,C,k'>,wenn x=<G,k>$ |
| --- | ------ |
| f(x)= |    |
|     |   $\varepsilon,sonst$

$\sqcup = V, C=E,k'=k$

2. zeigen, dass es in polynomieller Zeit berechenbar ist

3. Zeigen, dass die Abbildung richtig ist

 $x\in V-C \Leftrightarrow t(x)\in H-S$

 $<G,k>\in V,C \Leftrightarrow <V,E,k> \in H-S$

---
## Aufgabe 3:
*Zeigen Sie dass CLIQUE eine NP-vollständige Sprache ist.*

**Hinweis: Reduzieren Sie $INDEPENDENT-SET$ auf $CLIQUE$. Sie brauchen dabei nicht nachzuweisen, dass die
Reduktionsfunktion in polynomieller Zeit berechenbar ist.**

---
## Aufgabe 4:
*Sei $G = (V,E)$ ein ungerichteter Graph. Eine Knotenmenge $V' \subseteq V$ heißt dominierend, falls jeder Knoten aus $V-V'$ durch eine Kante mit einem Knoten in V′ verbunden ist. Zeigen Sie, dass $DOMINATING-SET = \{ \langle G,k\rangle | G \text{ besitzt eine dominierende Knotenmenge der Groesse} k\}$ eine NP-vollständige Sprache ist.*

**Hinweis: Konstruieren Sie zu einem ungerichteten Graphen G einen Graphen G′ wie im folgenden Beispiel angedeutet und zeigen Sie dann, dass G eine überdeckende Knotenmenge (vertex cover) der Größe k besitzt, genau dann wenn G′ eine dominierende Knotenmenge (dominating set) der Größe k besitzt.**
![Graph](Graph.png)

1. Zeigen, dass dominating Set in NP liegt

* raten einer Lösung und prüfen ob die Lösung richtig ist.
* Verfahren ist in polynomieller Zeit lösbar.

2. $V-C \preceq_P DOMINATING-SET $

|     | $<G',k'>,x=<G,k>$ |
| --- | ----------------- |
| $f(x)=$ |               |
|     | $\varepsilon, sonst$ |

$k=k', G'=(V\cup V', E\cup E'), \forall e = \{v_1,v_2\}\in E \Rightarrow V_e \in V'$

$\{v_1,v_e\} \in E'$

$\{v_2,v_e\} \in E'$

3. zeigen, dass es equivalent ist

$<G,k>\in V-C\Leftrightarrow <G',k'>\in D-S$

---
## Aufgabe 5:
*Beim Problem $SUBGRAPH \text{ } ISOMORPHISM$ sind zwei ungerichtete Graphen G und H gegeben, und es ist zu entscheiden, ob G isomorph zu einem Teilgraphen von H ist, d.h., ob die Knoten $u_1,...,u_m$ von G so injektiv auf Knoten $v_{i_1},...,v_{i_m}$ abgebildet werden können, dass $v_{i_j}$ und v_{i_k} durch eine Kante in H verbunden sind genau dann wenn $u_j$ und $u_k$ durch eine Kante in G verbunden sind. Zeigen Sie, dass $SUBGRAPH \text{ } ISOMORPHISM$ eine NP-vollständige Sprache ist.*

**Hinweis: Reduzieren Sie $INDEPENDENT-SET$ auf $SUBGRAPH \text{ } ISOMORPHISM$. Sie brauchen dabei nicht nachzuweisen, dass die Reduktionsfunktion in polynomieller Zeit berechenbar ist.**
