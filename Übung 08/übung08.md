# Übung 8
## Aufgabe 1:
**Ist die Sprache $L = \{xy | x,y \in \{a,b\}^* \text{ und }|x| = |y|\}$ kontextfrei? Begründen Sie ihre Antwort!**

## Aufgabe 2:
**Ist die Sprache $L = \{a^ib^jc^k | 0 \seq i \seq j \seq k\}$ kontextfrei? Begründen Sie ihre Antwort!**

## Aufgabe 3:
Sei G eine kontextfreie Grammatik in Chomsky Normalform. Zeigen Sie, dass jeder Syntaxbaum fu ̈r ein Wort der La ̈nge n aus L(G) genau 2n−1 Knoten besitzt, die mit Nichtterminalen beschriftet sind.

## Aufgabe 4:
 SeiG=({S,A,B,C},{a,b},R,S)mit
R={S → AB|BC A → BA|a B → CC|b
C → AB|a}
eine kontextfreie Grammatik in Chomsky Normalform. U ̈ berpru ̈fen Sie mit Hilfe des CYK-Algorithmus, ob
baaba zu L(G) geho ̈rt. Welche Pra ̈fixe von baaba geho ̈ren zu L(G)?
## Aufgabe5:
Sei M=({q1,...,q7},{0},{0,x,⊔},δ,q1,q5,q6) die durch folgendes Diagramm gegebene Turing-Maschine:
￼￼q7 ⊔ ;⊔, R
0 ;0, L x ;x, L
￼￼x ;x, R
q2
⊔ ;⊔, L
￼￼￼￼￼q1
q6
0 ;⊔, R
0 ;x, R
0 ;0, R
q3
q4
￼￼￼￼￼￼￼⊔ ;⊔, R x ;x, R
⊔ ;⊔, R q5
⊔ ;⊔, R
x ;x, R
0 ;x, R
￼￼￼￼x ;x, R

￼(a) Geben Sie die Berechnung von M bei Eingabe 00 an.

(b) Welche Wo ̈rter aus {ε, 0, 00, 000, 0000, 00000} geho ̈ren zu L(M)? (c) Welche Sprache wird von M entschieden? (ohne Beweis)

## Aufgabe 6:
Ist jede regula ̈re Sprache auch eine rekursive Sprache? Begru ̈nden Sie ihre Antwort!

## Aufgabe 7:
Begru ̈nden Sie jeweils ihre Antwort auf die folgenden Fragen:
(a) Ist die Klasse der rekursiv aufza ̈hlbaren Sprachen abgeschlossen unter Vereinigung?
(b) Ist die Klasse der rekursiv aufza ̈hlbaren Sprachen abgeschlossen unter Konkatenation?
