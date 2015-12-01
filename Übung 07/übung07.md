# Übung 7
## Aufgabe 1:
**Sei $\Sigma = \{0,1,\#\}$. Geben Sie eine kontextfreie Grammatik an, die die Sprache
$$\{x^R\#y | x,y \in \{0,1\}^*, x \text{ ist ein Teilwort von y}\}$$
erzeugt.**

$G=\{\{S,A,B\},\{0,1,\#\},\{S\rightarrow AB, A\rightarrow 0B0|1B1|\#A, B\rightarrow OA|1A|\varepsilon\}, S\}$

---
## Aufgabe 2:
**Geben Sie für die Sprache $\{xc^n | x \in \{a,b\}^* \text{ und die Anzahl der Vorkommen von a in x ist n}\}$ einen Kellerautomaten an, der die Sprache akzeptiert.**

![Automat](Automat2.jpg)

---
## Aufgabe 3:
**Sei $M=(K,\Sigma,\Gamma,\Delta,s,F)$ ein Kellerautomat mit $K=\{s,f\}, \Sigma = \Gamma = \{a,b\},F=\{f\}$ und
$$\Delta = \{((s,a,\varepsilon),(s,aaa)),((s,\varepsilon,\varepsilon),(f,\varepsilon)),((f,b,aa),(f,\varepsilon))\}$$**

a) **Welche Sprache wird von M akzeptiert?**

$\{ w \in \{a,b\}^* | 2*|w|_a = 3*|w|_b\}$

b) **Transformieren Sie M in einen äquivalenten Kellerautomaten M′ in Normalform.**

![Automat](Automat3_GNF.jpg)

---
## Aufgabe 4:
**Sei $M=(K,\Sigma,\Gamma,\Delta,s,F)$ der durch nebenstehendes Zustandsübergangsdiagramm gegebene Kellerautomat. M ist in Normalform. In der Vorlesung haben wir ein Konstruktionsverfahren kennengelernt, um eine kontextfreie Grammatik G zu erzeugen, so dass $L(G)=L(M)$. Geben Sie eine Ableitung für das Wort $aababb \in L(G)$ an. Sie brauchen hier nur jene Produktionsregeln der Grammatik zu erzeugen, die Sie für die Ableitung benötigen.**

![Automat](Automat1.png)

| Zustand | restliches Eingabewort | Kellerinhalt | Regel |
| :-----: | :--------------------: | :----------: | :---: |
|    s    |         aababb         |              | $(s,a,\varepsilon),(s,a)$ |
|    s    |         ababb          |       a      | $(s,a,\varepsilon),(s,a)$ |
|    s    |         babb           |      aa      | $(s,b,\varepsilon),(s,b)$ |
|    s    |         abb            |     baa      | $(s,a,b),(s,\varepsilon)$ |
|    s    |          bb            |      aa      | $(s,b,a),(s,\varepsilon)$ |
|    s    |           b            |       a      | $(s,b,a),(s,\varepsilon)$ |
|    s    |    $\varepsilon$       | $\varepsilon$ |                          |

oder

$(s,aababb,\varepsilon)\Rightarrow_M (s,ababb,a)$

$\Rightarrow_M (s,babb,aa)$

$\Rightarrow_M (s,abb,baa)$

$\Rightarrow_M (s,bb,aa)$

$\Rightarrow_M (s,b,a)$

$\Rightarrow_M (s,\varepsilon,\varepsilon)$

---
## Aufgabe 5:
**Sei $G=(V,\Sigma,R,S)$ eine kontextfreie Grammatik mit $\Sigma = \{a, b\}, V = \{S, B, U \}$ und $R = {S \rightarrow BU, B \rightarrow aBa | bBb | \varepsilon, U \rightarrow aUb | \varepsilon}$**

a) **Konstruieren Sie mit Hilfe des in der Vorlesung angegeben Verfahrens einen Kellerautomaten M, der L(G) akzeptiert.**

![Automat](Automat5a.jpg)

b) **Geben Sie einen Syntaxbaum für aaab an.**

![Baum](Baum5b.jpg)

c) **Geben Sie eine Linksableitung für aaab an.**

| Regel                      | Ableitung |
|  ------------------------  |  -------  |
|                            | S         |
| $S\rightarrow BU$          | BU        |
| $B\rightarrow aBa$         | aBaU      |
| $B\rightarrow \varepsilon$ | aaU       |
| $U\rightarrow aUb$         | aaaUb     |
| $U\rightarrow \varepsilon$ | aaab      |

d) **Geben Sie eine akzeptierende Berechnung des Kellerautomaten M für das Eingabewort aaab an.**

| $(p,aaab,\varepsilon)$ | $\vdash_M (q,aaab,S)$ |
| ---------------------- | -------------------- |
|                        | $\vdash_M (q,aaab,BU)$ |
|                        | $\vdash_M (q,aaab,aBaU)$ |
|                        | $\vdash_M (q,aab,BaU)$ |
|                        | $\vdash_M (q,aab,aU)$ |
|                        | $\vdash_M (q,ab,U)$ |
|                        | $\vdash_M (q,ab,aUb)$ |
|                        | $\vdash_M (q,b,Ub)$ |
|                        | $\vdash_M (q,b,b)$ |
|                        | $\vdash_M (q,\varepsilon,\varepsilon)$ |

---
## Aufgabe 6:
**Beweisen oder widerlegen Sie:
Die Sprache $\{a^nb^ma^n | n,m \leq 0 \text{ und m ist gerade} \} = \{a^nb^ma^n | n,m \leq 0\} \cap L(a^* (bb)^* a^*)$ ist kontextfrei.**

---
## Aufgabe 7:
**Beweisen oder widerlegen Sie: Die Sprache $L=\{a^{3k}ba^{2k}ba^k | k \leq 0\}$ ist kontextfrei.**
