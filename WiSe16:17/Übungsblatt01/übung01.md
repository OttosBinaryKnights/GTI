# Übung 1
## 1. Welche Behauptungen über Mengen sind wahr, welche falsch? Begründen Sie Ihre Antwort.

* a) **$\emptyset \subseteq \emptyset$**
-> wahr, weil beide kein Elemente haben (also jedes Element kommt in beiden vor)
Ø ist Teilmenge jeder Mengr

 * b) **$\emptyset \in \emptyset$**
-> falsch, weil leere Menge enthält keine Elemente

 * c) **$\emptyset \subseteq \{\emptyset\}$**
 -> wahr, Leere Menge ist Teilmenge jeder Menge!

 * d) **$\emptyset \in \{\emptyset\}$**
 -> wahr, $\{\} \in \{\{\}\}$ Menge enthält $\{\}$ als Element

 * e) **$\emptyset \in 2^{\emptyset}$**
-> falsch, laut Definition:
Def. $2^A$ Potenzmenge: Menge aller Teilmengen von A
Potenzmenge von $\emptyset$ umfasst nur $\emptyset$.

 * f) **$\emptyset \subseteq 2^{\emptyset}$**
-> wahr ???

---

## 2. Welche Behauptungen über Mengen sind wahr, welche falsch? Begründen Sie Ihre Anwort.

* a) **$\{a,b\}\subseteq \{a,b,\{a,b\}$**
* b) **$\{a,b\}\in \{a,b,\{a,b\}$**
* c) **$\{a,b\}\subseteq 2^{\{a,b,\{a,b\}\}}$**
* d) **$\{\{a,b\}\}\subseteq 2^{\{a,b,\{a,b\}\}}$**
* e) **$\{\{a,b\}\}\in 2^{\{a,b,\{a,b\}\}}$**
* f) **$\{a,\{a,b\}\}\subseteq 2^{\{a,b,\{a,b\}\}}$**

---

## 3. Welche Behauptungen über Mengen sind wahr, welche falsch? Begründen Sie Ihre Anwort.

* a) **$\forall M_1,M_2:(M_1\cup M_2)=(M_2\cup M_1)$**
* b) **$\forall M_1,M_2: (M_1-M_2)=(M_2-M_1)$**
* c) **$\forall M_1,M_2,M_3: (M_1\cap M_2)\cap M_3 = M_1 \cap (M_2 \cap M_3)$**
* d) **$\forall M_1,M_2,M_3: (M_1 - M_2)- M_3 = M_1 - (M_2 - M_3)$**

---

## 4. Listen Sie jeweils alle Elemente der folgenden Mengen auf.

* a) **$M_1=\{5x|x\in \mathbb{N}_0, x\leq 4\}$**
* b) **$M_2=\{x\in \mathbb{N} | 1\leq x^3 \leq 100\}$**
* c) **$M_3=\{x\in \mathbb{N} | \exists y \in \mathbb{N} :x=6y \land 1\leq x\leq 50$**
* d) **$M_4=\{x\in \mathbb{N} | \forall y \in \mathbb{N} :x=6y \land 1\leq x\leq 50$**

---

## 5. Beschreiben Sie in natürlicher Sprache, welche Elemente in den folgenden Mengen bezüglich des Universums $U = \{a, b, c, d\}$ enthalten sind.

* a) **$M_1 = \{X\subseteq U | \exists Y\subseteq U:X\cup Y = \{a,b\}\}$**
* b) **$M_1 = \{X\subseteq U | \exists Y\subseteq U:X\cap Y = \{a,b\}\}$**

---

## 6. Geben Sie für die folgenden Mengen einen mathematischen Ausdruck an, der keine natürlichsprachlichen Wörter enthält.

* a) **Die Menge aller geraden natürlichen Zahlen.**
* b) **Die Menge aller Mengen über $\{a,b,c,d\}$, die ein a enthalten.**


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
