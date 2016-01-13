# Belegaufgabe

| Name: | Erik Koltermann |
| ----- | --------------- |
| Matr-Nr: | 206354

**Die folgenden Aufgaben sind selbständig und schriftlich zu bearbeiten und bis spätestens zu Beginn der Vorlesung am 4. Januar 2016 abzugeben. Die Bearbeitungen können auch schon zuvor im ISG-Sekretariat G29-218 abgegeben werden. Beschriften Sie bitte jedes abgegebene Blatt mit ihrem Namen und ihrer Matrikelnummer. Hinweis: Was wir nicht lesen können, können wir nicht als richtig bewerten. Bei Aufgabe 1 gibt es für jede richtige Antwort 1,5 Punkte, für jede falsche Antwort 0,5 Punkte Abzug. Für eine korrekte Lösung der Aufgabe 2 gibt es 5 Punkte, für eine korrekte Lösung der Aufgabe 3 gibt es ebenfalls 5 Punkte.**

## Aufgabe 1:
**Welche der folgenden Behauptungen sind wahr, welche falsch (jeweils ohne Beweis!)?**


| wahr  | falsch  |    |
| :-----: | :-------: | ---- |
| $\circ$ | $\bullet$ | Es gibt eine rechtslineare Grammatik, die die Sprache $\{a^kb^k | k \geq 2\}$ erzeugt. |
| $\bullet$ | $\circ$   | Jede kontextfreie Sprache ist auch eine rekursive Sprache. |
| $\bullet$ | $\circ$   | Es gibt eine kontextfreie Grammatik, die $L = \{w \in \{a,b\}^* | w$ enthält mehr a als b erzeugt.} |
| $\bullet$  | $\circ$  | $\forall L_1,L_2:$ Falls $L_1$ eine rekursiv aufzählbare Sprache ist und $L_2$ eine reguläre, so ist $L_1 \cup L_2$ eine rekursiv aufzählbare Sprache. |
| $\bullet$  | $\circ$  | Es gibt eine Grammatik G, so dass für alle $x,y \in \{a,b\}^*$ mit $|x| = |y|$ gilt $xy \Rightarrow_G^* yx$.
| $\bullet$  | $\circ$  | Die Grammatik $G = (\{S\},\{b\},R,S)$ mit $R = \{S \rightarrow Sb | bS | b\}$ ist mehrdeutig. |
| $\bullet$  | $\circ$  | Sei L eine reguläre Sprache. Dann gibt es einen Kellerautomaten M mit nur 2 verschiedenen Zuständen, so dass $L(M) = L$ gilt. |
| $\bullet$  | $\circ$  | Die Sprache $\{ww^R w | w \in {a, b}^* \}$ ist entscheidbar.

---
## Aufgabe 2:
**Beweisen oder widerlegen Sie:
Die Sprache $\{a^ib^ja^kb^l | i, j,k,l \geq 0,i+ j = k+l\}$ ist regulär.**

Wiederlegen durch Pumping Lemma:
Annahme:
* L sei eine reguläre Sprache, dann gibt es eine Zhal n, so dass sich alle Wörter $w \in L$ mit $|w|\geq n$ in $w=xyz$ zerlegen lassen, sodass:
 * (1) $y \neq \varepsilon$
 * (2) $|xy| \leq n$
 * (3) $xy^iz \in L$ für alle $i \geq 0$

Wir betrachten für beliebige $n \in N$ das Wort
$$w=a^nb^na^nb^n$$
$$|w|=4n>n$$

Zerlegen in xy nur aus a's weil sonst $|xy|>n$

$x=a^l$ $y=a^m$ $m\geq 1$ folgt aus (2).

$z=a^{n-(l+m)}b^na^nb^n$

*Aufpumpen von i=2*

$y=a^2m$

$w=a^la^{2m}a^{n-l-m}b^na^nb^n$

$w=a^{n+m}b^na^nb^n \rightarrow i+j>k+l$

da $m \geq 1$ ist existiert keine Zerlegung, sodass die Bedingung $mj+i=k+l$ erfüllt ist.

$$\Rightarrow L \notin REG$$

---
## Aufgabe 3:
**Beweisen oder widerlegen Sie:
Die Sprache $\{a^nb^m | m,n \geq 0, n \neq 3m\}$ ist kontextfrei.**

Die Sprache ist kontextfrei.

Beweis durch aufstellen eines Kellerautomaten:

![Automat](Automat3.jpg)

--> ist falsch
