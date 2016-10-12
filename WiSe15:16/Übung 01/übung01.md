# Übung 1
## 1. Welche Behauptungen über Mengen sind wahr/falsch? Begründung?

 * __Ø ⊆ Ø__
-> wahr, weil beide kein Elemente haben (also jedes Element kommt in beiden vor)
Ø ist Teilmenge jeder Mengr

 * __Ø ∈ Ø__
-> falsch, weil leere Menge enthält keine Elemente

 * __Ø ∈ { Ø }__
 -> wahr,  *{}* ∈ {*{}*} Menge enthält {} als Element

 * __Ø ⊆ { Ø }__
 -> wahr, Leere Menge ist Teilmenge jeder Menge!

 * __Ø ⊆ 2^Ø__
-> wahr, laut Definition:

Def. 2^A Potenzmenge: Menge aller Teilmengen von A

Potenzmenge von Ø umfasst nur Ø.

 * __Ø ∈ 2^Ø__
-> wahr ???



## 2. Welche Behauptungen über Mengen sind wahr/falsch? Begründung?
__Alphabet:__ Jede nicht leere Menge (>= 1 Symbole)

 * __*{a,b}* ∈ {a,b,*{a,b}*}__
-> wahr: Alphabet {a,b} kommt als Symbol im anderen Alphabet vor

 * __{a,b} ⊆ {a,b,{a,b}}__
 -> wahr: a, b kommen als Element in der rechten Menge vor.

 *2^{a,b,{a,b}}: {Ø, {a}, {b}, {{a,b}}, {a,b}, {a,{a,b}}, {b,{a,b}}, {a,b,{a,b}}}*
 * __{a,b} ⊆ 2^{a,b,{a,b}}__
 -> falsch, weil Element a,b nicht rechts als Element vorkommt

 * __{{a,b}} ⊆ 2^{a,b,{a,b}}__
 -> wahr, weil Menge {a,b} als Element rechts vorkommt

 * __{a, {a,b}} ⊆ 2^{a,b,{a,b}}__
 -> falsch, weil Element a rechts nicht als Element vorkommt

 * __{a, {a,b}} ⊆ 2^{a,b,{a,b}}__
 -> wahr, Potenzmenge = { ..., {{a,b}}, ..}



## 3.
* __∀ L1,L2,L3 : (L1L2)L3 = L1(L2L3)__
-> wahr, Assoziativität

* __∀ L1,L2,L3 : (L1 ∪L2)L3 = L1L3 ∪L2L3__
-> wahr, Distributivität

* __∀ L1,L2,L3 : (L1 ∩L2)L3 = L1L3 ∩L2L3__
-> falsch, Konkatenation nicht kommutativ:

* __∀ L1,L2,L3 : (L1L2)∪L3 = (L1 ∪L3)(L2 ∪L3)__
-> falsch, Konkatenation nicht kommutativ:

## 4.
 * __{ε}^*=Ø__
 -> falsch

* __Ø∪Ø∗={ε}__
*

* __∀L:(L^+)^*=L^*__
-> wahr, da Kleene Star Abschluss. L^+ ohne ε mit ^* wieder mit ε (= ε in beiden enthalten)

* __{ε}^*={ε}__
-> wahr

* __∀L:0/L^*={ε}__
-> falsch, wenn L aus mehr als ε besteht, daher nicht ∀L

* __∀L:0/∪L^+=L^∗__
-> flasch, leere Menge != leeres Wort ε

## 5.
 * ∀L1,L2 :(L1L2)∗ =L∗1L∗2
 *
 * ∀L1,L2 :(L1∪L2)∗ =(L2∪L1)∗
-> wahr, da kommutativ

 * ∀L1,L2 :(L1∪L2)∗ =L∗1∪L∗2
-> falsch

 * ∀L1,L2 :L∗1∩L∗2 =(L1∩L2)∗
-> falsch

## 6.
### a) {w ∈ {a,b}∗ | genau ein Suffix von w beginnt mit a}
Alle Wörter können gebildet werden.

### b) {w ∈ {a,b}∗ | alle Präfixe von w mit Länge mindestens 1 enden mit b}
Jedes Wort mit Präfix (ungleich ε) enthält ein b
