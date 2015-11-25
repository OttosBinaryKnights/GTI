# Übung 6
## Aufgabe 1:
**Die kontextfreie Grammatik $G_1 = (V,\Sigma,R,E)$ mit $V = \{E\}$, $\Sigma = \{o, +, * \}$ und $R = \{E \rightarrow E E + | E E * | o\}$
erzeugt arithmetische Ausdrücke in Umgekehrter Polnischer Notation.**

(a) **Geben Sie eine Ableitung für das Wort o o o++ an.**

$E \Rightarrow_{G_1} EE+ \Rightarrow_{G_1} EEE++ \Rightarrow_{G_1} oEE++$

$\Rightarrow_{G_1} ooE++ \Rightarrow_{G_1} ooo++$

(b) **Geben Sie einen Syntaxbaum für das Wort o o o++o∗o o+∗o+ an.**

![Baum](Aufgabe1b.svg)

(c) **Gehört das Wort o o o o o o o+++∗∗ zu L(G1)?**

![Beweis fehlt](Aufgabe1c.png)

*FALSCH: Beweis über Induktion*

*Ansatz: immer ein o mehr als Operatoren*

(d) **Ist die Grammatik G1 eindeutig? Begründen Sie ihre Antwort.**

nein, für das Wort $oo*oo+*$ gibt es zwei Bäume/Grammatiken:

$E  \Rightarrow_{G_1} EE* \Rightarrow_{G_1} EE*E* \Rightarrow_{G_1} EE*EE+* \Rightarrow_{G_1} oo*oo+*$

$E \Rightarrow_{G_1} EE* \Rightarrow_{G_1} EE* \Rightarrow_{G_1} EEE+* \Rightarrow_{G_1} EE*EE+* \Rightarrow_{G_1} oo*oo+*$

---
*verschiedene Ableitungen können den gleichen Syntaxbaum haben.*

*Ansatz: gnd. wenn eine eindeutige Rechtsableitung existiert*

*Beweis: Grammatik ist eindeutig rechtsableitung, daher ist sie eindeutig*

---
## Aufgabe 2:
**Geben Sie eine kontextfreie Grammatik an, die die Sprache $\{a^ib^jc^kd^l$ | $i = j$ und $k = l$} erzeugt.**
**Geben Sie eine kontextfreie Grammatik an, die die Sprache $\{a^ib^jc^kd^l$ | $i = j$ und $k = l$} erzeugt.**

 $G=(\{S,A,B \}, \{a,b,c,d\}, \{S -> AB, A -> aAb|\epsilon, B -> cBd|\epsilon\},S)$

 $R=\{S \rightarrow AB, A \rightarrow aAb| \varepsilon, B \varepsilon cBd | \varepsilon \}$

---
## Aufgabe 3:
**Sei $G_3 = (\{S,A,B,T\},{a,c},R,S)$ mit $R=\{S \rightarrow AB|BA, A \rightarrow aA|ac, B \rightarrow Tc, T \rightarrow  aT |a\}$**

**Zeigen Sie, dass $G_3$ mehrdeutig ist.**

Das Wort acac lässt sich durch mindestens verschiedene Anwendung von Regeln bilden lässt:
1. $S \Rightarrow_{G_3} AB \Rightarrow_{G_3} ATc \Rightarrow_{G_3} acTc \Rightarrow_{G_3} acac$
2. $S \Rightarrow_{G_3} BA \Rightarrow_{G_3} Bac \Rightarrow_{G_3} Tcac \Rightarrow_{G_3} acac$
3. $S \Rightarrow_{G3} BA \Rightarrow_{G3} TcA \Rightarrow_{G3} Tcac \Rightarrow_{G3} acac$

---
## Aufgabe 4:
**Konstruieren Sie mit dem Verfahren aus der Vorlesung zur Grammatik G4 = ({A, B, S}, {a, b}, R, S) mit R = {S → aaA, A → BAB | B | ε, B → bb | ε} eine äquivalente Grammatik G in Chomsky Normalform.**

* Gegeben:
 *  $S \rightarrow aaA$
 * $A \rightarrow BAB | B | \varepsilon$
 * $B \rightarrow bb | \varepsilon$

* Elimination von $\varepsilon$-Regeln:
 * $S \rightarrow aaA | aa$
 * $A \rightarrow BAB | B | BB | BA | AB | A$
 * $B \rightarrow bb$

* Elimination von Kettenregelzyklen
 * $A \rightarrow A$ fällt weg

* Elimination von Kettenregeln
 * $S \rightarrow aaA | aa$
 * $A \rightarrow BA | AB | BB | BAB | bb$
 * $B \rightarrow bb$

* Elimination nichtisolierter Terminalsymbole
 * $S \rightarrow T_aT_aA| T_aT_a$
 * $A \rightarrow BA | AB | BB | BAB | T_bT_b$
 * $B \rightarrow T_bT_b$
 * $T_a \rightarrow a$
 * $T_b \rightarrow b$

* Elimination langer rechter Seiten (mehr als 2 Nichtterminaler BAB)
* $S \rightarrow T_aT_aA| T_aT_a$
* $X \rightarrow T_aA$
* $A \rightarrow BA | AB | BB | BY | T_bT_b$
* $Y \rightarrow AB$
* $B \rightarrow T_bT_b$
* $T_a \rightarrow a$
* $T_b \rightarrow b$


---
## Aufgabe 5:
**Geben Sie für die Sprache $\{w \in \{a,b\}^* | w \text{hat ungerade Laenge und das mittlere Symbol ist ein a} \}$
einen Kellerautomaten an, der die Sprache akzeptiert.**
![Automat](Aufgabe5.jpg)

---
## Aufgabe 6:
**Sei M der durch das folgende Diagramm gegebene Kellerautomat.**
![Automat](Kellerautomat.png)

(a) **Geben Sie eine akzeptierende Berechnung für das Wort baabbabb an.**

|| Zustand | Input| Keller|
|:---: |:---: |:---: |:---: |:---: |
| $((s,a,b),(s,\varepsilon))$ | s | baabbabb | $\varepsilon$ |
| $((s,a,\varepsilon),(s,a))$ | s |  aabbabb |       b|
| $((s,b,a),(s,\varepsilon))$ | p |   abbabb | $\varepsilon$       |
| $((s,b,\varepsilon),(s,b))$ | p |   abbabb |       a       |
| $((s,a,b),(p,\varepsilon))$ | p |     babb |      aa       |
| $((s,a,\varepsilon),(p,a))$ | s |     babb |     aaa       |
| $((p,\varepsilon,\varepsilon),(s,a))$ | s |      abb |      aa       |
| $((p,\varepsilon, b),(s,\varepsilon))$ | s |       bb |     baa       |
|        | s |        b |      aa       |
|        | s | $\varepsilon$ |  a       |

(b) **Welches ist die von M akzeptierte Sprache L(M)?**

ungerade Anzahl von as & bs

$L(M)=\{w \in \{a,b\}^* | |w|_a \leq |w|_b \}$
