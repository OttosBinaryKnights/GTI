# Definitionen
### Symbole
Elemente eines Alphabets

### Alphabet
Nichtleere, endliche Menge von Symbolen

### Wort
Konkatenation von Symbolen (endlich)

### leere Wort
ein Wort ohne Symbole (Länge = 0)

### Sprache
Vereinigung von Wörtern?????

### Potenzmenge
Menge aller Teilmengen (Beinhaltet keine Elemente!!)

### Teilmenge
Alle Elemente kommen in beiden Mengen vor.

## Operationen
### Konkatenation

---
## Zustandsübergangsdiagramme
### Formale Notation
**allg.: $M = (K, \sum, \delta, s, F  )$**
* $M$ - Automat
* $K$ - Menge der Zustände
* $F$ - Menge Endzustände ($F \subseteq K$)
* $\sum$ - Alphabet (nicht leere, engliche Menge von Zeichen)
* $L$ - Sprache (Menge der Wörter)
* $\delta$ - Überführungsfunktion
* $s$ - Startzustand ($s \in K$)
* $\vdash$ "überführt "

### Epsilonübergang E(q)
Menge aller Zustände, die vom Zustand q über $\epsilon$-Übergänge erreicht werden können

##Reguläre Ausdrücke

### reguläre Ausdrücke
 1. $\emptyset$ reh. Ausdruck
 2. $\sigma, \sigma \in \Sigma $ reg. Ausdruck
 3. $\alpha, \beta,$ reg Ausdruck; $(\alpha \cup \beta)$ reg Ausdruck
 4. $\alpha, \beta,$ reg Ausdruck; $(\alpha \beta)$ reg Ausdruck
 5. $\alpha, \beta,$ reg Ausdruck; $(\alpha)^* $ reg Ausdruck

### reguläre Sprachen
 Sprachen die von endliche Automaten akzeptiert werden

#### Pumping Lemma (AUSWENDIG!)
 * $\forall L \in REG$
 * $\exists n \in N, n >= 0$
 * $\forall w \in L, |w| >= 0$
 * $\exists x,y,z \in \sum^* : w=xyz, y \neq \epsilon, |xy| <= n$,
 * $\forall i >= 0: xy^iz \in L$

<<<<<<< HEAD
## Kellerautomat
### Formale Notation
 **allg.: $M = (K, \sum, \Gamma, \delta, s, F  )$**
 * $M$ - Automat
 * $K$ - Menge der Zustände
 * $F$ - Menge Endzustände ($F \subseteq K$)
 * $\sum$ - Alphabet (nicht leere, engliche Menge von Zeichen)
* $\Gamma$ - akzeptierte Zeichen des Kellers
 * $L$ - Sprache (Menge der Wörter)
 * $\delta$ - Überführungsfunktion
 * $s$ - Startzustand ($s \in K$)
 * $\vdash$ "überführt "

## Grammatik
### kontextfrei
=======
## Deterministische Turing-Maschinen
Eine deterministische Turing-Maschine ist ein 7-Tupel $(K,\Sigma,\Gamma,\delta,s,q_{accept},q_{reject})$, wobei gilt:
* K ist eine endliche Menge von Zuständen,
* $\Sigma$ ist ein Alphabet, das Eingabealphabet, das das Blanksymbol ⊔ nicht enthält,
* $\Gamma$ ist ein Alphabet, das Bandalphabet, das alle Elemente von $\Sigma$ und das Blanksymbol ⊔ enthält,
* $s \in K$ ist der Startzustand,
* $q_{accept} \in K$ ist der akzeptierende Halteszustand,
* $q_{reject} \in K$ ist der verwerfende Halteszustand, $q_{reject}\neq q_{accept}$,
* $\delta:(K-\{q_{accept},q_{reject}\})\times \Gamma \rightarrow K \times \Gamma \times \{L,R,S\}$ ist die Übergangsfunktion.
>>>>>>> origin/master
