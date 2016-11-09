# Übungsblatt 05
## 1. Konstruieren Sie (gemäß der Konstruktion für die Abschlusseigenschaften, wie im Beweis des Satzes von Kleene benutzt) für jede der Sprachen, die durch die folgenden regulären Ausdrücke über $\{a,b\}$ beschrieben werden, einen (nichtdeterministischen) endlichen Automaten, der die Sprache akzeptiert. Geben Sie jeweils den Zustandsgraphen des Automaten an.

a) $a^* b$
b) $\emptyset^* \cup aaa$

---

## 2. Es seien $\Sigma$ ein Alphabet und $\alpha$ ein regulärer Ausdruck über $\Sigma$. Geben Sie einen Algorithmus zur Konstruktion eines regulären Ausdrucks $\alpha'$ für das Komplement der Sprache $L(\alpha)$ bezüglich $\Sigma$ an, also mit $L(\alpha)=L(\alpha)$.
*Hinweis: Sie dürfen für den zu konstruierenden Algorithmus alle Algorithmen der Vorlesung als Anweisung verwenden.*

---

## 3. Beweisen Sie, dass die Sprache $L=\{ww^R | w\in \{a,b\}^* \}$ nicht regulär ist.

---

## 4. Beweisen Sie, dass die Sprache $\{a^{n^2}| n\geq 1\} $ nicht regulär ist.

---

## 5. Welche der folgenden Sprachen sind regulär, welche nicht? Beweisen Sie jeweils Ihre Antwort.

* a) $L=\{w\in \{0,1\}^* | w \text{ ist die Binaerdarstellung einer durch feunf teilbaren Zahl}\}$
* b) $L=\{xyx^R | x,y \in \{a,b\}^* \}$
* c) $L=\{w \in \{a,b,c\}^* | \text{die Anzahl der Vorkommen con c in w ist eine Primzahl}\}$

---

## 6. Welche der folgenden Aussagen sind wahr, welche falsch? Begründen Sie jeweils Ihre Antwort!

* a) Jede Teilmenge einer regulären Sprache ist eine reguläre Sprache.
-> wahr
* b) Falls $L \subseteq \Sigma^* $ regulär ist, dann ist auch $Pref(L)=\{w \in \Sigma^* | x=wy \text{ fuer } x | \in L,y\in \Sigma^* \}$ regulär.
* c) Wenn$L_1,L_2 \land L_3$ reguläre Sprachen sind, dann ist auch die Sprache $L_1 \cup L_2)-L3$ regulär.
