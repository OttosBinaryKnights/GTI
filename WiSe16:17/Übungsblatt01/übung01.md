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
-> wahr, siehe a)

---

## 2. Welche Behauptungen über Mengen sind wahr, welche falsch? Begründen Sie Ihre Anwort.

* a) **$\{a,b\}\subseteq \{a,b,\{a,b\}\}$**
  -> wahr, a und b sind als Elemente in der Menge
* b) **$\{a,b\}\in \{a,b,\{a,b\}\}$**
  -> wahr
* c) **$\{a,b\}\subseteq 2^{\{a,b,\{a,b\}\}}$**
  -> falsch, weil Element a,b nicht rechts als Element vorkommt, nur als Menge
  $2^{\{a,b,\{a,b\}\}}= \{\emptyset,\{a\},\{b\},\{\{a,b\}\},\{a,b\},\{a,\{a,b\}\},\{b,\{a,b\}\},\{a,b,\{a,b\}\}\}$
* d) **$\{\{a,b\}\}\subseteq 2^{\{a,b,\{a,b\}\}}$**
  -> wahr, weil Menge {a,b} als Element rechts vorkommt
* e) **$\{\{a,b\}\}\in 2^{\{a,b,\{a,b\}\}}$**
  -> wahr
* f) **$\{a,\{a,b\}\}\subseteq 2^{\{a,b,\{a,b\}\}}$**
  -> falsch, da a nicht als Element vorhanden ist sondern als Menge

---

## 3. Welche Behauptungen über Mengen sind wahr, welche falsch? Begründen Sie Ihre Anwort.

* a) **$\forall M_1,M_2:(M_1\cup M_2)=(M_2\cup M_1)$**
-> wahr, da die Vereinigung von Mengen Kommutativ ist
* b) **$\forall M_1,M_2: (M_1-M_2)=(M_2-M_1)$**
-> falsch, Gegenbeispiel:
  * $M_1=\{a\}$
  * $M_2=\{a,b\}$
  * $\{\}\neq \{b\}$
* c) **$\forall M_1,M_2,M_3: (M_1\cap M_2)\cap M_3 = M_1 \cap (M_2 \cap M_3)$**
-> wahr, da der Schnitt von Mengen Assoziativ ist
* d) **$\forall M_1,M_2,M_3: (M_1 - M_2)- M_3 = M_1 - (M_2 - M_3)$**
-> falsch
  * Gegenbeispiel:
  $\{a\}-(\{a\}-\{a\})=\{a\}$
  $(\{a\}-\{a\})-\{a\}=\emptyset$

---

## 4. Listen Sie jeweils alle Elemente der folgenden Mengen auf.

* a) **$M_1=\{5x|x\in \mathbb{N}_0, x\leq 4\}$**
-> $M_1=\{0,5,10,15,20\}$
* b) **$M_2=\{x\in \mathbb{N} | 1\leq x^3 \leq 100\}$**
-> $M_2=\{1,...,4\}$
* c) **$M_3=\{x\in \mathbb{N} | \exists y \in \mathbb{N} :x=6y \land 1\leq x\leq 50$**
-> $M_3=\{6,12,18,24,30,36,42,48\}$
* d) **$M_4=\{x\in \mathbb{N} | \forall y \in \mathbb{N} :x=6y \land 1\leq x\leq 50$**
-> $M_4=\{\}$

---

## 5. Beschreiben Sie in natürlicher Sprache, welche Elemente in den folgenden Mengen bezüglich des Universums $U = \{a, b, c, d\}$ enthalten sind.

* a) **$M_1 = \{X\subseteq U | \exists Y\subseteq U:X\cup Y = \{a,b\}\}$**
-> Alle Teilmengen von $\{a,b\}$
* b) **$M_1 = \{X\subseteq U | \exists Y\subseteq U:X\cap Y = \{a,b\}\}$**
-> Alle Obermengen von $\{a,b\}$ (alle Mengen, die a und b enthalten)

---

## 6. Geben Sie für die folgenden Mengen einen mathematischen Ausdruck an, der keine natürlichsprachlichen Wörter enthält.

* a) **Die Menge aller geraden natürlichen Zahlen.**
-> $M_1=\{x\in \mathbb{N} |\exists y \in \mathbb{N}: x=2y\}$
* b) **Die Menge aller Mengen über $\{a,b,c,d\}$, die ein a enthalten.**
-> $U=\{a,b,c,d\}$
-> $M_2=\{X\subseteq U | a\in X\}$
