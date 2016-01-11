# Übung 11

## Aufgabe 1:
*Besitzen die folgenden Postschen Korrespondenzsysteme eine Lösung? Besitzen sie eine spezielle
Lösung?*

* (a) ((a,ab),(b,ca),(ca,a),(abc,c))
* (b) ((001,01), (0011,111), (11,111), (101,010))

Allgemein:
* $((x_1,y_1)(x_2,y_2),...,(x_n,y_n))$ mit $x_i,y_i \in \Sigma^* $
 Lsg.: nicht-leere Folge $(i_1,i_2,...,i_k)$ von Indizes von $\{1,2,...,n\}$ falls

 $$x_{i_1}x_{i_2}...x_{i_k}=y_{i_1}y_{i_2}...y_{i_k}$$

Spezielle Lsg.: $(i_1,i_2,...,i_k)$ falls $i_1=1$

* a)

 $((a,ab),(b,ca),(ca,a),(abc,c))$

| $x_1=a$ | $x_2=b$ | $x_3=ca$ | $x_4=abc$ |
| ------- | ------- | -------- | --------- |
| $y_1=ab$ | $y_2=ca$ | $y_3=a$ | $y_4=c$  |

Lsg.: $I=(1,2,3,1,4)$ (spezielle Lsg., da $i_1=1$)

$abcaaabc=abcaaabc$

* b)

 $((001,01), (0011,111), (11,111), (101,010))$

 $11101001=11101001$

 Lsg.: $I= (3,4,1)$

---
## Aufgabe 2:
*Welche der folgenden Sprachen sind entscheidbar, welche nicht? Begründen Sie ihre Antworten.*

* (a) {⟨G⟩ | G ist eine Grammatik und L(G) ∈ P}
* (b) {⟨G⟩ | G ist eine kontextfreie Grammatik und L(G) ∈ NP}

---
## Aufgabe 3:
*Welche der folgenden Sprachen sind entscheidbar, welche nicht? Begründen Sie ihre Antworten.*

* (a) {⟨G1,G2⟩ | G1 und G2 sind kontextfreie Grammatiken und L(G1) = L(G2)}
* (b) {⟨G1,G2⟩ | G1 und G2 sind kontextfreie Grammatiken und L(G1)∪L(G2) ist kontextfrei}

---
## Aufgabe 4:
*Zeichnen Sie ein Venn-Diagramm, das die Beziehungen der Klassen der*

* (a) regulären Sprachen,
* (b) kontextfreien Sprachen,
* (c) entscheidbaren Sprachen,
* (d) rekursiv aufzählbaren Sprachen und
* (e) Sprachen, deren Komplement rekursiv aufzählbar ist,

*bezüglich Enthaltensein, Schnitt, ...widerspiegelt. Wo ist die Klasse P in diesem Diagramm einzuordnen?*
