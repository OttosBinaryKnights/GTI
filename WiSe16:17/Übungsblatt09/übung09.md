# Übungsblatt 09
## 1. Beweisen oder widerlegen Sie:
**Die Sprache $L=\{a^kba^{2k}ba^{3k}|k\geq 0\}$ ist kontextfrei.**
->nicht kontextfrei

---

## 2. Beweisen oder widerlegen Sie:
**Die Sprache $L=\{a^jb^kc^l|0\leq j\leq k\leq l\}$ ist kontextfrei.**
-> nicht kontextfrei

---

## 3. Es sei $G=(V,\Sigma,R,S)$ eine kontextfreie Grammatik in Chomsky Normalform, für die die erzeugte Sprache $L(G)$ endlich ist.
* a) Wie lang sind die Wörter in $L(G)$ höchstens? Begründen Sie Ihre Antwort.
* b) Wie viele Wörter enthält $L(G)$ höchstens? Begründen Sie Ihre Antwort.
*Hinweis: Betrachten Sie die Syntaxbäume die Wörter aus $L(G)$. Die gesuchten Zahlen in der Teilaufgabe b) lauten für Grammatiken $G$ mit $|\Sigma|=3$ und $|V | = 5$ genau 64 570 081 und für Grammatiken $G$ mit $|\Sigma| = 1$ und $|V | = 5$ genau 17.*

---

## 4. Es seien die Sprache $L=\{(ab)^nc^n|n\geq 0\}$ sowie der Homomorphismus $h: \{a, b, c\}^* \rightarrow \{0, 1\}^* $ mit $h(a) = 00, h(b) = 01$ und $h(c) = 10$ gegeben.
* a) Geben Sie eine kontextfreie Grammatik G mit $L(G) = L$ an.
* b) Geben Sie eine Grammatik $G'$ mit $L(G') = h(L)$ an.

---

## 5. Es ist die Turing-Maschine $M =(\{z_0,z_1,z_2,z_g,z_g',z_u,z_t,z_r,z_r',q_a,q_r\},\{a,b\},\{a,b,\sqcup \},\delta,z_0,q_a,q_r\})$ mit $\delta$ durch folgende Tabelle gegeben.

| $\delta$ | $z_0$ | $z_1$ | $z_2$ | $z_g$ | $z_g'$ | $z_r$ | $z_r'$ | $z_t$ | $z_u$ |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| $\sqcup$ |$(z_0,\sqcup,N)$ | $(z_1,\sqcup,N)$ | $(q_a,\sqcup,N)$ |$(z_g',\sqcup,R)$ | $(z_r,a,L)$ | $( z_r',\sqcup,L)$ | $(z_t,\sqcup,R)$ | $(z_0,\sqcup,R)$ |$(z_u,\sqcup,N)$ |
| $a$ |$(z_1,\sqcup,R)$|$(z_2,\sqcup,R)$|$(z_g,a,R)$|$(z_g,a,R)$|$(z_g',a,R)$|$(z_r,a,L)$|$(z_r',a,L)$|$(z_u,\sqcup,R)$|$(z_g,\sqcup,R)$|

* a) Geben Sie die Berechnung von M bei der Eingabe $aaaa$ an.
* b) Geben Sie an, welche Wörter aus der Menge $\{\varepsilon,a,aa,aaa,aaaa,aaaaa\}$ von $M$ akzeptiert
werden.
* c) Geben Sie an, welche Sprache von $M$ akzeptiert wird.
* d) Wird die Sprache $L(M)$ von $M$ entschieden? Begründen Sie Ihre Antwort kurz.
