# Übungsblatt 07
## 1. Beweisen Sie, dass die folgenden Sprachen kontextfrei sind, indem Sie jeweils eine kontextfreie Grammatik angeben, die die Sprache erzeugt.
* __a) $L=\{aubw|u,w\in \{a,b\}^* , |u|=|w|\}$__
* __b) $L=\{x^R\#y|x,y\in \{0,1\}^* , \text{x ist Teilwort von y}\}$__

---

## 2. Es sei $G=(V,\Sigma , R,S)$ eine kontextfreie Grammatik. Im Beweis der Herstellung einer zu $G$ äquivalenten Grammatik $G'$ in Chomsky Normalform wird bei der Eliminierung der $\varepsilon$-Regeln die Menge $V_{\varepsilon}=\{A\in V|A\Rightarrow_G^* \varepsilon\}$ benutzt. Geben Sie einen Algorithmus an, der $V_{\varepsilon}$ bestimmt, und begründen Sie, dass er terminiert und korrekt ist.

Def.:
Eine kontextfreie Grammatik $G=(V,\Sigma , R,S)$ heißt in Chomsky Normalform, falls alle Produktionsregeln in R eine der folgenden Formen haben:
$S\rightarrow \varepsilon$
$A\rightarrow a$ für ein a aus $\Sigma$
$A\rightarrow BC$ für $B,C\in V-\{S\}$

---

## 3. Gegeben ist die kontextfreie Grammatik $G=(\{S,A,B,C\},\{a,b,c\},R,S)$ mit folgenden Regeln in R:

__$S\rightarrow ASA|ACA$
$A\rightarrow aAa|B|C$
$B\rightarrow bB|A|b$
$C\rightarrow cC|\varepsilon$__

__Konstruieren Sie – gemäß des in der Vorlesung angegebenen Algorithmus – eine zu $G$ äquivalente $G'$ in Chomsky-Normalform.__

1) Elimination des Startsymbols auf rechten Seiten
$G=(\{S',S,A,B,C\},\{a,b,c\},R,S')$
$S'\rightarrow ASA|ACA$
$S\rightarrow ASA|ACA$
$A\rightarrow aAa|B|C$
$B\rightarrow bB|A|b$
$C\rightarrow cC|\varepsilon$
2) Elimination von ε-Regeln
$G=(\{S',S,A,B,C\},\{a,b,c\},R,S')$
$S'\rightarrow \varepsilon$
$S'\rightarrow ASA|ACA$
$S\rightarrow ASA|ACA$
$A\rightarrow aAa|B|C$
$B\rightarrow bB|A|b$
$C\rightarrow cC$
3) Elimination von Kettenregelzyklen
4) Elimination von Kettenregeln
5) Elimination von nichtisolierten Terminalsymbolen auf rechten Seiten
6) Elimination von langen rechten Seiten

---

## 4. Es sei $G=(\{S,A,B,C\},\{a,b\},R,S)$ mit $R=\{S\rightarrow AB|BC, A\rightarrow BA|a, B\rightarrow CC|b, C\rightarrow AB|a\}$ eine kontexfreie Grammatik in Chomsky Normalform. Bestimmen Sie mit Hilfe des in der Vorlesung angegebenen Algorithmus von Cocke, Younger und Kasami, ob das Wort baaba zu $L(G)$ gehört sowie welche Präfixe von baaba von $G$ erzeugt werden und welche nicht.

$w=baaba$

$\begin{matrix}
   &  1  &  2    &  3    &  4  &  5    \\
   &  b  &  a    &  a    &  b  &  a    \\
 1 & \{B\}&  .    &  .    &  .  &  .    \\
 2 &     & \{A,C\}&  .    &  .  &  .    \\
 3 &     &       & \{A,C\}&  .  &  .    \\
 4 &     &       &       & \{B\}&  .    \\
 5 &     &       &       &     & \{A,C\}\\
\end{matrix}$

$\Rightarrow \begin{matrix}
   &  1  &  2    &  3    &  4    &  5    \\
   &  b  &  a    &  a    &  b    &  a    \\
 1 & \{B\}& \{A,S\}&  .    &  .    &  .    \\
 2 &     & \{A,C\}& \{B\}  &  .    &  .    \\
 3 &     &       & \{A,C\}& \{S,C\}&  .    \\
 4 &     &       &       & \{B\}  & \{A,S\}\\
 5 &     &       &       &       & \{A,C\}\\
\end{matrix}$
$\Rightarrow \begin{matrix}
   &  1  &  2    &  3        &  4    &  5    \\
   &  b  &  a    &  a        &  b    &  a    \\
 1 & \{B\}& \{A,S\}& \emptyset &  .    &  .    \\
 2 &     & \{A,C\}& \{B\}      & \{B\}  &  .    \\
 3 &     &       & \{A,C\}    & \{S,C\}& \{B\}  \\
 4 &     &       &           & \{B\}  & \{A,S\}\\
 5 &     &       &           &       & \{A,C\}\\
\end{matrix}$
$\Rightarrow \begin{matrix}
   &  1  &  2    &  3        &  4        &  5      \\
   &  b  &  a    &  a        &  b        &  a      \\
 1 & \{B\}& \{A,S\}& \emptyset & \emptyset &  .      \\
 2 &     & \{A,C\}& \{B\}      & \{B\}      & \{S,A,C\}\\
 3 &     &       & \{A,C\}    & \{S,C\}    & \{B\}    \\
 4 &     &       &           & \{B\}      & \{A,S\}  \\
 5 &     &       &           &           & \{A,C\}  \\
\end{matrix}$
$\Rightarrow \begin{matrix}
   &  1  &  2    &  3        &  4        &  5      \\
   &  b  &  a    &  a        &  b        &  a      \\
 1 & \{B\}& \{A,S\}& \emptyset & \emptyset & \{S,A,C\}\\
 2 &     & \{A,C\}& \{B\}      & \{B\}      & \{S,A,C\}\\
 3 &     &       & \{A,C\}    & \{S,C\}    & \{B\}    \\
 4 &     &       &           & \{B\}      & \{A,S\}  \\
 5 &     &       &           &           & \{A,C\}  \\
\end{matrix}$


$S\in N[1,5] \rightarrow w \in L(G)$

**Welche Präfixe von baaba gehören zu L(G)?**
* überall wo S in der ersten Zeile Steht: nur ba

---

## 5. Geben Sie für die folgende Sprache einen Kellerautomaten an, der sie akzeptiert.
__$$L=\{a^mb^n \in \{a,b\}^* |m\geq n\geq 0\}$$__

Def.:
Ein Kellerautomat ist ein 6-Tupel $(K,\Sigma,\Gamma,\Delta,s,F)$, wobei gilt:
* $K$ ist eine endliche Menge von Zuständen,
* $\Sigma$ ist ein Alphabet, das Eingabealphabet,
* $\Gamma$ ist ein Alphabet, das Kelleralphabet,
* $s\in K$ ist der Startzustand,
* $\Delta \subseteq(K \times (\Sigma \cup \{\varepsilon\})\times \Gamma^* )\times(K\times\Gamma^* )$ ist die Übergangsrelation,
* $\Delta$ ist endlich und
* $F\subseteq K$ ist die Menge der Endzustände.

Ein Kellerautomat $M=(K,\Sigma,\Gamma,\Delta,s,F)$ akzeptiert ein Wort $w\in \Sigma^* $ genau dann wenn $(s,w,\varepsilon)\vdash_M^* (p,\varepsilon,\varepsilon)$ für ein $p \in F$.

![Kellerautomat](Kellerautomat.png)
