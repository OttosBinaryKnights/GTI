# Übung 8
## Aufgabe 1:
**Ist die Sprache $L = \{xy | x,y \in \{a,b\}^* \text{ und }|x| = |y|\}$ kontextfrei? Begründen Sie ihre Antwort!**

![Automat](Automat1.jpg)

---
## Aufgabe 2:
**Ist die Sprache $L=\{a^ib^jc^k | 0 \leq i \leq j \leq k \}$  kontextfrei? Begründen Sie ihre Antwort!**

---
## Aufgabe 3:
**Sei G eine kontextfreie Grammatik in Chomsky Normalform. Zeigen Sie, dass jeder Syntaxbaum für ein Wort der Länge n aus L(G) genau $2n-1$ Knoten besitzt, die mit Nichtterminalen beschriftet sind.**

NT-Knoten = Nichtterminale Knoten

Blatt = Terminale = n


![Baum](tree.png)

Anzahl der Knoten soll 2n-1 sein
 * I.Anfang: für n=1: 1 Blatt $\Rightarrow$ 1 NT-Knoten

 * I.Schritt: n>1 Blätter

 ![Tree](tree2.png)
 $T_L$ hat k Blätter;
 $T_R$ hat n-k Blätter

 * I.V.:

 $T_L$ hat $2k-1$ Knoten

 $T_R$ hat $2(n-k)-1$ Knoten

 $\Rightarrow |NT|=|T_L|+|T_R|+Root =(2k-1) + (2(n-k)-1) +1 = 2n-1$

---
## Aufgabe 4:
**Sei $G=(\{S,A,B,C\},\{a,b\},R,S)$ mit**
$$R=\{S \rightarrow AB | BC, A \rightarrow BA | a, B \rightarrow CC | b, C \rightarrow AB | a\}$$

**eine kontextfreie Grammatik in Chomsky Normalform. Überprüfen Sie mit Hilfe des CYK-Algorithmus, ob baaba zu L(G) gehört. Welche Präfixe von baaba gehören zu L(G)?**

w=baaba

$\begin{matrix}
   &  1  &  2    &  3    &  4  &  5    \\
   &  b  &  a    &  a    &  b  &  a    \\
 1 & {B} &  .    &  .    &  .  &  .    \\
 2 &     & {A,C} &  .    &  .  &  .    \\
 3 &     &       & {A,C} &  .  &  .    \\
 4 &     &       &       & {B} &  .    \\
 5 &     &       &       &     & {A,C} \\
\end{matrix}$
$\Rightarrow \begin{matrix}
   &  1  &  2    &  3    &  4    &  5    \\
   &  b  &  a    &  a    &  b    &  a    \\
 1 & {B} & {A,S} &  .    &  .    &  .    \\
 2 &     & {A,C} & {B}   &  .    &  .    \\
 3 &     &       & {A,C} & {S,C} &  .    \\
 4 &     &       &       & {B}   & {A,S} \\
 5 &     &       &       &       & {A,C} \\
\end{matrix}$
$\Rightarrow \begin{matrix}
   &  1  &  2    &  3        &  4    &  5    \\
   &  b  &  a    &  a        &  b    &  a    \\
 1 & {B} & {A,S} & \emptyset &  .    &  .    \\
 2 &     & {A,C} & {B}       & {B}   &  .    \\
 3 &     &       & {A,C}     & {S,C} & {B}   \\
 4 &     &       &           & {B}   & {A,S} \\
 5 &     &       &           &       & {A,C} \\
\end{matrix}$
$\Rightarrow \begin{matrix}
   &  1  &  2    &  3        &  4        &  5      \\
   &  b  &  a    &  a        &  b        &  a      \\
 1 & {B} & {A,S} & \emptyset & \emptyset &  .      \\
 2 &     & {A,C} & {B}       & {B}       & {S,A,C} \\
 3 &     &       & {A,C}     & {S,C}     & {B}     \\
 4 &     &       &           & {B}       & {A,S}   \\
 5 &     &       &           &           & {A,C}   \\
\end{matrix}$
$\Rightarrow \begin{matrix}
   &  1  &  2    &  3        &  4        &  5      \\
   &  b  &  a    &  a        &  b        &  a      \\
 1 & {B} & {A,S} & \emptyset & \emptyset & {S,A,C} \\
 2 &     & {A,C} & {B}       & {B}       & {S,A,C} \\
 3 &     &       & {A,C}     & {S,C}     & {B}     \\
 4 &     &       &           & {B}       & {A,S}   \\
 5 &     &       &           &           & {A,C}   \\
\end{matrix}$

$S\in N[1,5] \rightarrow w \in L(G)$

---
## Aufgabe 5:
**Sei $M=(\{q_1,...,q_7\},\{0\},\{0,x,\sqcup \},\delta,q_1,q_5,q_6)$ die durch folgendes Diagramm gegebene Turing-Maschine:**
![Automat](Automat.png)

 a) **Geben Sie die Berechnung von M bei Eingabe 00 an.**

 $\begin{matrix}
 (\varepsilon,q_1,00 ) & \vdash_M (\varepsilon, q_2, 0)\\
  & \vdash_M (x,q_3,\varepsilon) \\
  & \vdash_M (\varepsilon,q_7,x) \\
  & \vdash_M (\varepsilon,q_7,\sqcup x) \\
  & \vdash_M (\varepsilon,q_2,x) \\
  & \vdash_M (\varepsilon, q_2, \varepsilon) \\
  & \vdash_M (x\sqcup, q_5, \varepsilon)
 \end{matrix}$

 b) **Welche Wörter aus $\{\varepsilon, 0, 00, 000, 0000, 00000\}$ gehören zu L(M)?**

  $w_{accept}=\{0,00,0000\}$

  $w_{reject}=\{\varepsilon, 000,00000\}$

 c) **Welche Sprache wird von M entschieden?** *(ohne Beweis)*

 $L(M)=\{0^n| n=\{1,2,4\}\}$ oder $L(M)=\{0^{2^n}|n\leq0\}$

---
## Aufgabe 6:
**Ist jede reguläre Sprache auch eine rekursive Sprache? Begründen Sie ihre Antwort!**

---
## Aufgabe 7:
**Begründen Sie jeweils ihre Antwort auf die folgenden Fragen:**

 a) **Ist die Klasse der rekursiv aufzählbaren Sprachen abgeschlossen unter Vereinigung?**

 b) **Ist die Klasse der rekursiv aufzählbaren Sprachen abgeschlossen unter Konkatenation?**
