# Übung 10

## Aufgabe 1:
*Wir betrachten folgendes Problem:*

*Gegeben eine deterministische Turingmaschine M, ein Zustand q und ein Wort w, besucht M jemals den Zustand q, wenn M mit Eingabe w gestartet wird?*

*Formulieren Sie das Problem als Sprache und zeigen Sie, dass die Sprache nicht entscheidbar ist.*

$$L=\{<M,q,w>| \text{ M eine Turingmaschine und erreicht q bei Eingabe von w} \}$$

$\rightarrow$ Akzeptanzproblem $A_{TM}$

$X \in A_{TM}$

$f(x)=\Bigl\{  
  \begin{matrix}
    \varepsilon & X \neq <M,w> \\
    <M,q_{acc},w> & X=<M,w>
  \end{matrix}
\Bigr\}$

$X\in A_{TM} \Leftrightarrow f(X) \in L$

---
## Aufgabe 2:
*Wir betrachten folgendes Problem:
Gegeben Turingmaschinen M1 und M2, gibt es ein Wort, bei dem beide halten?*

*Formulieren Sie das Problem als Sprache und zeigen Sie, dass die Sprache nicht entscheidbar ist.*

$$L=\{<M_1,M_2> | \exists w \in \Sigma^* \text{ und } M_1 \land M_2 \text{ halten bei Eingabe von w}\}$$

$A_{TM}=\{<M> | M $ hält bei Eingabe von $w\}$ ist unentscheidbar

Behauptung: $A_{TM} \leq L$

ges: $f \text{ mit } M \in A_{TM} \Leftrightarrow f(<M,w>)\in L$

$M_1=M$

$M_2$ mit $L(M_2)=\Sigma^* $

 $<M,w> \in A_{TM}$

 $\Rightarrow M$ hält bei $w$

 $\Rightarrow M_1 \land M_2$ halten bei $w$

 $\Rightarrow <M_1,M_2> \in L$

 $<M_1,M_2> \in L$

 $\Rightarrow \exists w'$ und $M_1,M_2$ halten bei $w$

 $\Rightarrow \exists w'$ bei dem M hält $w'=w$???

---
## Aufgabe 3:
*Welche der folgenden Sprachen sind entscheidbar, welche nicht? Begründen Sie ihre Antworten.*
* *(a) {⟨M⟩ | M besitzt geradzahlig viele Zustände}*

 ist entscheidbar, da abzählbar.

* *(b) {⟨M,w⟩ | M erreicht bei Eingabe w innerhalb der ersten 42 Schritte den Startzustand ein zweites Mal}*

 ist unentscheidbar
 
* *(c) {⟨M1,M2⟩ | M1,M2 sind Turingmaschinen und L(M1) ⊆ L(M2)}*
