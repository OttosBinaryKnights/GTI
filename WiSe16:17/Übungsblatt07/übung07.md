# Übungsblatt 07
## 1. Beweisen Sie, dass die folgenden Sprachen kontextfrei sind, indem Sie jeweils eine kontextfreie Grammatik angeben, die die Sprache erzeugt.
* __a) $L=\{aubw|u,w\in \{a,b\}^* , |u|=|w|\}$__
* __b) $L=\{x^R\#y|x,y\in \{0,1\}^* , \text{x ist Teilwort von y}\}$__

---

## 2. Es sei $G=(V,\Sigma , R,S)$ eine kontextfreie Grammatik. Im Beweis der Herstellung einer zu $G$ äquivalenten Grammatik $G'$ in Chomsky Normalform wird bei der Eliminierung der $\varepsilon$-Regeln die Menge $V_{\varepsilon}=\{A\in V|A\Rightarrow_G^* \varepsilon$ benutzt. Geben Sie einen Algorithmus an, der $V_{\varepsilon}$ bestimmt, und begründen Sie dass er terminiert und korrekt ist.

---

## 3. Gegeben ist die kontextfreie Grammatik $G=(\{S,A,B,C\},\{a,b,c\},R,S)$ mit folgenden Regeln in R:

__$S\rightarrow ASA|ACA$
$A\rightarrow aAa|B|C$
$B\rightarrow bB|A|b$
$C\rightarrow cC|\varepsilon$__

__Konstruieren Sie – gemäß des in der Vorlesung angegebenen Algorithmus – eine zu $G$ äquivalente $G'$ in Chomsky-Normalform.__


---

## 4. Es sei $G=(\{S,A,B,C\},\{a,b\},R,S)$ mit $R=\{S\rightarrow AB|BC, A\rightarrow BA|a, B\rightarrow CC|b, C\rightarrow AB|a\}$ eine kontexfreie Grammatik in Chomsky Normalform. Bestimmen Sie mit Hilfe des in der Vorlesung angegebenen Algorithmus von Cocke, Younger und Kasami, ob das Wort baaba zu $L(G)$ gehört sowie welche Präfixe von baaba von $G$ erzeugt werden und welche nicht.

---

## 5. Geben Sie für die folgende Sprache einen Kellerautomaten an, der sie akzeptiert.
__$$L=\{a^mb^n \in \{a,b\}^* |m\geq n\geq 0\}$$__
