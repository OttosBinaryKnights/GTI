# Übung 6
## Aufgabe 1:
**Die kontextfreie Grammatik G1 = (V,Σ,R,E) mit V = {E}, Σ = {o, +, ∗} und R = {E → E E + | E E ∗ | o}
erzeugt arithmetische Ausdrücke in Umgekehrter Polnischer Notation.**

(a) **Geben Sie eine Ableitung für das Wort o o o++ an.**

(b) **Geben Sie einen Syntaxbaum für das Wort o o o++o∗o o+∗o+ an.**

(c) **Gehört das Wort o o o o o o o+++∗∗ zu L(G1)?**

(d) **Ist die Grammatik G1 eindeutig? Begründen Sie ihre Antwort.**

## Aufgabe 2:
**Geben Sie eine kontextfreie Grammatik an, die die Sprache $\{a^ib^jc^kd^l$ | $i = j$ und $k = l$} erzeugt. **

 $G=(\{S,A,B \}, \{a,b,c,d\}, \{S -> AB, A -> aAb|\epsilon, B -> cBd|\epsilon\},S)$

## Aufgabe 3:
**Sei $G_3 = (\{S,A,B,T\},{a,c},R,S)$ mit $R=\{S \rightarrow AB|BA, A \rightarrow aA|ac, B \rightarrow Tc, T \rightarrow  aT |a\}$**

**Zeigen Sie, dass $G_3$ mehrdeutig ist.**


* Weg 1:

$S \rightarrow_{G3} AB \rightarrow_{G3} ATc \rightarrow_{G3} AcTc \rightarrow_{G3} acac$

* Weg 2:

$S \rightarrow_{G3} BA \rightarrow_{G3} TcA \rightarrow_{G3} Tcac \rightarrow_{G3} acac$

## Aufgabe 4:
**Konstruieren Sie mit dem Verfahren aus der Vorlesung zur Grammatik G4 = ({A, B, S}, {a, b}, R, S) mit R = {S → aaA, A → BAB | B | ε, B → bb | ε} eine äquivalente Grammatik G in Chomsky Normalform.**

## Aufgabe 5:
**Geben Sie für die Sprache
{w ∈ {a,b}∗ | w hat ungerade Länge und das mittlere Symbol ist ein a}
einen Kellerautomaten an, der die Sprache akzeptiert.**

## Aufgabe 6:
**Sei M der durch das folgende Diagramm gegebene Kellerautomat.**
a/b/ε
a/ε/a
b/a/ε
￼b/ε/b
ε/b/ε
sp
a/b/ε a/ε/a

(a) **Geben Sie eine akzeptierende Berechnung für das Wort baabbabb an. **

(b) **Welches ist die von M akzeptierte Sprache L(M)?**
