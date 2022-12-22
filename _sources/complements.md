# Complément sur les suites et les fonctions numériques
## Suites et critère de Chauchy
Le très grand intéret du critère de Cauchy provient du fait qu'il caractérise dans $\mathbb{R}$ les suites convergentes, sans que la limite apparaisse. D'où son utilisation dans l'étude des séries par exemple, ou encore pour montrer qu'une suite n'est pas convergente.

Le concept de suite de Cauchy correspond à la propriété que la distance entre deux termes de la suite devient arbitrairement petite (et non de plus en plus petite) quand ces termes sont de rang assez grand.

```{admonition} Définition (suite de chauchy)

Soit $(u_n)$ une suite réelle; on dit que $(u_n)$ est une suite de Cauchy ou vérifie le critère de Cauchy si :

$$
\forall \epsilon>0, \exists N \in \mathbb{N},  \forall p, n \in \mathbb{N}, \left\{
\begin{array}{ll}
 p\geq N\\
n\geq N\\
\end{array}
\right. \Rightarrow |u_p-u_n|<\epsilon
$$

```
```{admonition} Théorème (Critère de Cauchy)

Une suite de réels est convergente dans $\mathbb{R}$ si, et seulement si, c'est une suite de Cauchy.
```
Le critère de Cauchy est utilisé pour montrer qu'une suite $(u_n)$ est convergente (resp divergente) dans les cas où l'on peut obtenir facilement une majoration (resp minoration) de $|u_p−u_n|$ pour $n$ et $p$ assez grands. C'est le cas en particulier pour certaines séries.

## Comparaison des suites

```{admonition} Définition
Soient $(u_n)$, $(v_n)$ et $(\epsilon_n)$ trois suites telles qu'à partir d'un certain rang $u_n = v_nε_n$. On dit que :
- $u_n$ est dominée par $v_n$ lorsque la suite $(\epsilon_n)$ est bornée. Notation : $u_n = O(v_n)$.
- $u_n$ est négligeable devant $v_n$ lorsque la suite $(\epsilon_n)$ tend vers 0 ($\lim \epsilon_n =0$). Notation : $u_n = o(v_n)$.
- $u_n$ est équivalente à $v_n$ lorsque la suite $(\epsilon_n)$ tend vers 1 ($\lim \epsilon_n =1$). Notation : $u_n \sim v_n$.

```
```{admonition} Théorème (Caractérisations)
Lorsque la suite $v$ ne s'annule pas à partir d'un certain rang :
- $u_n = O(v_n)$ si et seulement si la suite $\frac{u}{v}$ est bornée.
- $u_n = o(v_n)$ si et seulement si $\lim \frac{u_n}{v_n}= 0$.
- $u_n \sim v_n$ si et seulement si $lim \frac{u_n}{v_n}= 1$.
```

```{admonition} Exemple

On a: 

- $n =o(n^2)$ (on prend $\epsilon = \frac{1}{n} \to 0$).
- $ln(n) = o(n)$ car$\frac{ln(n)}{n} \to 0$.
- $n\sin(n) = O(n)$ car $\frac{n\sin(n)}{n}=sin(n)$ bornée.
- $\sin(n) = O(1)$ car $\frac{\sin(n)}{1}=sin(n)$ bornée.
- $\frac{n}{n^2+1} \sim \frac{1}{n}$ car $\dfrac{\frac{n}{n^2+1}}{\frac{1}{n}} = \frac{n^2}{n^2 +1} \to 1$.
- $(1+\frac{1}{n})^n \sim e$ car $\dfrac{(1+\frac{1}{n})^n}{e} \to 1$.
```

```{admonition} Remarque 
- $u_n = O(1)$ signifie que la suite $(u_n)$ est bornée.
- $u_n = o(1)$ signifie que $u_n\to 0$.
- Si $u_n = o(v_n)$ alors $u_n = O(v_n)$.
- Si $u_n \sim v_n$ alors $u_n = O(v_n)$.
- Si $u_n = o(v_n)$ et $v_n = o(w_n)$, alors $u_n = o(w_n)$ (transitivité).
- Si $u_n = O(v_n)$ et $v_n = O(w_n)$, alors $u_n = O(w_n)$ (transitivité).
- $u_n \sim v_n \Leftrightarrow u_n − v_n = o(v_n)$.
- si $l \in \mathbb{R}$ et si $u_n \sim l$ alors $u_n \to l$ (réciproque vraie lorsque $l \neq 0$).
- Si $u_n = o(v_n)$ alors $\forall \lambda \in \mathbb{R}, \lambda u_n + v_n \sim v_n$.
```

```{admonition} Théorème (croissances comparées)

Soient $\alpha, \beta > 0$:
- si $\alpha < \beta$ alors $n^\alpha = o(n^\beta)$ et $ \frac{1}{n^\beta} = o(\frac{1}{n^\alpha})$.
- $ln(n)^\alpha = o(n^\beta)$.
- $n^\alpha =o(e^{n\beta})$ et $n^\alpha =o(e^{n^\beta})$.
- $\forall a \in \mathbb{R}, a^n =o(n!)$ et $n^\alpha = o(n!)$.
- $n! = o(n^n)$.
```



```{admonition} Théorème (les équivalents usuels)

- Soit $(u_n)$ une suite de limite nulle ($\lim u_n =0$). On a:

    - Si $f : ]− a;a[\to \mathbb{R}$ (avec $a > 0$) est dérivable en $0$, et si $f'(0) \neq 0$, alors on a $f(u_n)− f(0) \sim f'(0)u_n$.
    - $\sin(u_n) \sim u_n$, 
    - $e^{u_n} - 1 \sim u_n$, 
    - $ln(1+u_n)\sim u_n$, 
    - $\tan(u_n) \sim u_n$, 
    - $(1+u_n)^\alpha -1 \sim \alpha u_n$.
- Soit $P(x) = \sum_{k=0}^{p} a_kx^k$ une fonction polynomiale avec $a_p \neq 0$, alors $P(n) \sim a_pn^p$ (équivalence avec le
terme de plus haut degré).
- Soit $Q(x) =\frac{P(x)}{R(x)}$ une fraction rationnelle avec $a_px^p$ le terme de plus haut degré de $P$ ($a_p \neq 0$) et $b_rx^r$ celui de $R$ ($b_r \neq 0$), alors $Q(n) \sim \frac{a_p}{b_r}n^{p−r}$ (équivalence avec le rapport des termes de plus haut degré).

```

```{admonition} Théorème 
Soient $u$ et $v$ deux suites,
- Si $u_n \sim v_n$ alors les deux suites ont le meme singe à partir d'un certain rang.
- Si $u_n \sim v_n$ et si $\lim v_n = l \in \mathbb{R}\cup \{+\infty, -\infty\}$, alors $\lim u_n = l$.
- Si $u_n \sim v_n$ et si $a_n \sim b_n$, alors $u_na_n \sim v_nb_n$ (compatibilité avec la multiplication).
- Si $u_n \sim v_n$ et si $v$ ne s'annule pas à partir d'un certain rang, alors $\frac{1}{u_n} \sim \frac{1}{v_n}$ (compatibilité avec le
passage à l'inverse).
- Si $u_n \sim v_n$ et si $v_n > 0$ ne s'annule pas à partir d'un certain rang, alors $u_n^\alpha \sim v_n^\alpha$ pour tout réel $\alpha$
(compatibilité avec les puissances constantes).

```

```{warning}
- Si $u_n = o(v_n)$ et $w_n = o(v_n)$ ce ne veut pas dire que $u_n=w_n$!!!
- Il n'y a pas compatibilité avec l'addition en général, par exemple : $n+\frac{1}{n} \sim n$ et $−n \sim 1−n$, mais $\frac{1}{n}$
n'est pas équivalent à $1$.
- Ces propriétés sont utiles pour les calculs de limites qui ne peuvent pas être faits directement : on essaie de se
ramener à un équivalent plus simple (s'il y en a ...) dont on sait calculer la limite.
```

```{note}
L'écriture $u_n = v_n + o(w_n)$ signifie que $u_n-v_n = o(w_n)$.
```

```{admonition} Exemples

- $\dfrac{1}{n} = o(1)$
- $1=o(n)$
- $(\dfrac{1}{2})^n = o(n)$
- $n^2 = o(n^3)$
- $(ln(n))^2 = o(n)$
- $3^n = o(n!)$
- $e^n = o(3^n)$
- $n^3 = o(e^n)$
- $\dfrac{1}{n+1} = \dfrac{1}{n} + o(\dfrac{1}{n})$
- $n^2 + 2ln(n) + 4 + \dfrac{1}{n} \sim n^2$
- $\dfrac{2}{n} - \dfrac{4}{n^2} + \dfrac{2}{n^4} \sim \dfrac{2}{n}$
- $2n^2 - n+n^3 \sim n^3$
- $ln(n) + (ln(n))^2 \sim (ln(n))^2$

```
```{admonition} Théorème (formule de stirling)

$n! \sim (\frac{n}{e})^n\sqrt{2\pi n}$

```
## Dérivées successives

```{admonition} Définition
Soit une fonction $f$ dérivable sur $D \subset \mathbb{R}$. Sa fonction dérivée $f^{'}$ est appelé dérivée première (ou d'ordre 1) de la fonction $f$ sur $D$.
$f^{"}$, est appelé dérivée seconde (ou d'ordre 2) de la fonction $f$.
Par itération, pour tout naturel $n > 2$, on définit la fonction dérivée n-ième (ou d'ordre $n$), notée $f^{(n)}$ comme étant la fonction dérivée de la fonction dérivée d'ordre $(n − 1)$, soit : $f^{(n)}= (f^{(n-1)})^{'}$.
```

```{admonition} Exemple
Déterminer les dérivées d'ordre 1, 2 et 3 des fonctions suivantes :
- $f(x) = x^4 - 2x^2 + x- 1$
- $g(x) = cos(2x) + sin(2x)$
```
```{admonition} Exercice
Soit la fonction $f$ définie sur $] − 1 ; +\infty[$ par : $f(x) = \ln(x + 1)$.
1. Calculer les dérivées d'ordre 1, 2, 3 et 4. 
1. En déduire et Démontrer par récurrence l'expression de la dérivée d'ordre $n$.
```

## Fonctions de classe $\mathscr{C}^n$
```{admonition} Définition
On note :
- $\mathscr{C}^0(I)$ est l'ensemble des fonctions continues sur $I$.
- $\mathscr{C}^1(I)$ est l'ensemble des fonctions continûment dérivables sur $I$, i.e. l'ensemble des fonctions qui sont dérivables sur $I$ dont la fonction dérivée $f^{'}$ est continue sur $I$.
- $\mathscr{C}^n(I)$ est l'ensemble des fonctions $n$ fois continûment dérivables sur $I$, i.e. l'ensemble des fonctions n-fois dérivables sur $I$ dont la fonction dérivée n-ième $f^{(n)}$ est continue sur $I$ ;
- $\mathscr{C}^\infty(I)$ est l'ensemble des fonctions indéfiniment dérivables sur $I$.

```
## Dérivée n-ième usuelles

```{admonition} Proposition 
Soient $a\in \mathbb{R}$, $n\in \mathbb{N}$, $f$ et $g$ deux fonctions telles ques $\forall x \in \mathbb{R}, f(x) = x^n$ et $g(x) = (x-a)^n$. Alors $f$ et $g$ sont de classe $\mathscr{C}^\infty$ sur $\mathbb{R}$ et $\forall k \in \mathbb{N}, \forall x \in \mathbb{R},$

$$ 
f^{(k)}(x) =\left\{
\begin{array}{ll}
n(n-1)\times ...\times (n-k+1)x^{n-k} \quad\mbox{si} \;k \leq n\\
0 \quad\mbox{si}\;k>l
\end{array}
\right.
$$

$$
g^{(k)}(x) =\left\{
\begin{array}{ll}
n(n-1)\times ...\times (n-k+1)(x-a)^{n-k} \quad\mbox{si} \;k \leq n\\
0 \quad\mbox{si}\;k>l
\end{array}
\right.
$$

```
```{admonition} Proposition 
Soient $a\in \mathbb{R}$, $f$ et $g$ deux fonctions telles ques $\forall x \in \mathbb{R^{*}}, f(x) = \dfrac{1}{x}$ et $\forall x \in \mathbb{R}\setminus \{a\}, g(x) = \dfrac{1}{x-a}$. Alors $f$ et $g$ sont de classe $\mathscr{C}^\infty$ sur $\mathbb{R^{*}}$ et $\mathbb{R}\setminus \{a\}$ respectivement et on a:
- $\forall n \in \mathbb{N}, \forall x \in \mathbb{R^{*}}, f^{(n)}(x) =\dfrac{(-1)^nn!}{x^{n+1}}$
- $\forall n \in \mathbb{N}, \forall x \in \mathbb{R^{*}}, g^{(n)}(x) =\dfrac{(-1)^nn!}{(x-a)^{n+1}}$

```

```{admonition} Proposition 
Les fonctions $\exp, \ln, \sin, \cos$ sont de classe $\mathscr{C}^\infty$ sur leur domaine de définition et on pour tout $n\in \mathbb{N}$:

- $\exp^{(n)}(x) = \exp(x)$
- $\ln^{(n)}(x) = \dfrac{(-1)^{n-1}(n-1)!}{x^{n}}$
- $\sin^{(n)}(x) = \sin(x+n\frac{\pi}{2})$
- $\cos^{(n)}(x) = \cos(x+ n\frac{\pi}{2})$
```

```{admonition} Proposition
Si $f$ et $g$ sont deux fonctions de classe $\mathscr{C}^n$ sur un intervalle $I$, alors pour tout $\lambda\in \mathbb{R}, (\lambda f + g)$ et $fg$ sont encore des fonctions de classe $\mathscr{C}^n$ et de plus : 
- $(αf + g)^{(n)} = αf^{(n)} + g^{(n)}$
- $(fg)^{(n)} = \sum_{i=0}^{n} \binom{n}{k}f^{(k)}g^{(n-k})$ ( avec $\binom{n}{k} =\dfrac{n!}{k!(n-k)!})$
```

```{admonition} Proposition
Soient $I$ et $J$ deux intervalles et soit $f : I \to \mathbb{R}$ et $g : J \to \mathbb{R}$ avec $f(I) \subset J$.
Si $f$ est de classe $\mathscr{C}^n$ sur $I$, et si $g$ est de classe $\mathscr{C}^n$ sur $J$, alors $g\circ f$ est de classe $\mathscr{C}^n$ sur $I$.
```

```{admonition} Remarques
- $\forall \alpha \in \mathbb{R}, x \mapsto x^\alpha=\exp(\alpha\ln(x))$ est de classe $\mathscr{C}^\infty$ sur $]0, +\infty[$.
- $\forall a >0, x \mapsto a^x=\exp(x\ln(a))$ est de classe $\mathscr{C}^\infty$ sur $\mathbb{R}$.
- Si $f$ et $g$ sont deux fonctions de classe $\mathscr{C}^n$ sur un intervalle $I$ et si $g$ ne s'annule pas sur l'intervalle $I$, alors la fonction $ x \mapsto\dfrac{f(x)}{g(x)}$ est de classe $\mathscr{C}^n$ sur l'intervalle $I$.

```

## Comparaison des fonctions
Soit I un intervalle de $\mathbb{R}$ et $a\in \bar{I}$. Nous supposerons ici que $f$ et $g$ sont deux fonctions qui ne s'annulent pas sur un voisinage de $a$ privé de $a$.
Il s'agit ici de comparer les 2 fonctions au voisinage de $a$.  Pour cela, formons leur rapport $\dfrac{f(x)}{g(x)}$ et regardons ce qui se passe lorsque $x \to a$.

```{admonition} Définition 

1. Si $\dfrac{f(x)}{g(x)}$ est bornée au voisinage de $a$, on dira que $f$ est dominée par $g$ au voisinage de $a$ et on écrit: 

$$
f  \underset{x\to a}{O}(g) \mbox{ ou } f  \underset{a}{O}(g) \mbox{ ou encore } f = O(g) \mbox{ au voisinage de } a
$$

1. Si $\dfrac{f(x)}{g(x)}$ tend vers $0$ lorsque $x$ tend vers $a$ ($\underset{x\to a}{\lim} \dfrac{f(x)}{g(x)}= 0$), on dira que $f$ est négligeable devant $g$ au voisinage de $a$ et on écrit: 


$$
f  \underset{x\to a}{o}(g) \mbox{ ou } f  \underset{a}{o}(g) \mbox{ ou encore } f = o(g) \mbox{ au voisinage de } a
$$

1. Si $\dfrac{f(x)}{g(x)}$ tend vers $1$ lorsque $x$ tend vers $a$ ($\underset{x\to a}{\lim} \dfrac{f(x)}{g(x)}= 1$), on dira que $f$ et $g$ sont équivalentes au voisinage de $a$ et on écrit: 


$$
f  \underset{x\to a}{\sim}g \mbox{ ou } f  \underset{a}{\sim}g \mbox{ ou encore } f \sim g \mbox{ au voisinage de } a
$$

```

```{admonition} Remarque
- Notation : $f(x) = O(g(x))$, $f(x) = o(g(x))$, $f(x) \sim g(x)$ au voisinage de $a$.
- Par abus de langage, on notera $O(g)$ (respectivement $o(g)$) toute fonction étant un grand $O$  (repectivement petit $o$) de $g$ au voisinage de $a$.
- Lorsque $f(x) = O(g(x))$, on pourra dans un calcul remplacer $f(x)$ par $O(g(x))$ mais **ATTENTION! IL EST FAUX de remplacer $O(g(x))$ par $f(x)$**.
- Lorsque $f(x) = o(g(x))$, on pourra dans un calcul remplacer $f(x)$ par $o(g(x))$ mais **ATTENTION! IL EST FAUX de remplacer $o(g(x))$ par $f(x)$**.
- **Ne JAMAIS écrire que $f(x) \underset{a}{\sim}0$  puisque la fonction nulle ne vérifie pas les conditions d'application de la définition!!**
- Il faut toujours specifier le voisinage du point dont on compare deux fonctions!
- $f = O(1)$ au voisinage de $a$ signifie que $f$ est bornée au voisinage de $a$.
- $f = o(1)$ au voisinage de $a$ signifie que $f$ tend vers $0$ lorsque $x\to a$ ($\underset{x\to a}{\lim} f(x) = 0$).
- Il n'y a aucune relation entre $f(x) \underset{a}{\sim} g(x)$ et $\underset{x\to a}{\lim} f(x) - g(x) = 0$.
```

```{admonition} Exemples
1. Soit $f(x) = 3x^5 − x^4 + 2x$. Alors:
    - $f(x) = O(x)$ au voisinage de $0$.
    - $f(x) = O(x^5)$ au voisinge de $+\infty$.
    - $f(x) = o(x)$ au voisinge de $0$.
    - $f(x) = o(x^6)$ au voisinage de $+\infty$.

2. Si $P$ est une fonction polynomiale non nulle :
    - $P$ est équivalente à son monôme de plus haut degré au voisinage de $+\infty$
    - $P$ est équivalente à son monôme de plus bas degré au voisinage de $0$
2. Au voisinage de $+\infty$ : $ch(x) \sim \dfrac{e^x}{2}$ et $sh(x) \sim \dfrac{e^x}{2}$

```

```{admonition} Remarque
Une fonction donnée admet une infinité d'équivalents au voisinage d'un point a. Seulement l'intérêt
d'un équivalent est de remplacer une fonction par une autre fonction plus simple. On choisira donc toujours l'équivalent le
plus simple.

Par exemple, au voisinage de $+\infty$ on a:
- $x^3 - 2x^2 + 3x-5 \sim x^3$
- $x^3 - 2x^2 + 3x-5 \sim x^3-5x+8$
- $x^3 - 2x^2 + 3x-5 \sim x^3+4x^2-6$
- $x^3 - 2x^2 + 3x-5 \sim x^3 - 2x^2$

Seul le premier équivalent a un intérêt!!
```

```{admonition} Proprietes

- Soit $p, q \in \mathbb{N}$ alors $x^p = o(x^q)$ au voisinage de $0$ $\Leftrightarrow p<p$.
- Si au voisinage d'un point $a$ on a $f(x) = o(g(x))$ alors $f(x) = O(g(x))$.

- Soient $\alpha, \beta, \gamma >0$ trois reels strictment positifs:
    - Comparaison $\ln$ et puissances:
        - au voisinage de $+\infty$: $(\ln(x))^\alpha = o(x^\beta)$.
        - au voisinage de 0+: $|\ln(x)|^\alpha = o(\frac{1}{x^\beta})$.
    -  Comparaison puissance et exponentielle :
        - au voisinage de $+\infty$: $x^\beta = o(e^{\gamma x})$
        - au voisinage de $+\infty$: $x^\beta = o(a^{x})$ si $a>1$.
        - au voisinage de $-\infty$: $e^{\gamma x} = o(\frac{1}{x^\beta})$ si $\beta \in \mathbb{N}$.
```

```{admonition} Proposition

- Opérations sur les relations de comparaisons

    1. $f = o(g), g = o(h) \Leftarrow f = o(h)$ cad (transitivité) la même chose avec $O$
    2. $f_1 = o(g), f_2 = o(g) \Leftarrow f_1 + f_2 = o(g)$ cad $o(g) + o(g) = o(g)$ la même chose avec $O$
    3. $f_1 = o(g_1), f_2 = o(g_2) \Leftarrow f_1f_2 = o(g_1g_2)$ cad $o(g_1)o(g_2) = o(g_1g_2)$ la même chose avec $O$
    4. $f = o(g) \Leftarrow hf = o(hg)$ cad $ho(g) = o(hg)$ la même chose avec $O$
    5. $f = o(\lambda g) (\lambda \in \mathbb{R}^{*}) \Leftarrow f = o(g)$ cad $ o(\lambda g) = o(g)$ la même chose avec $O$

- Caractérisation de l'équivalence de deux fonctions
    On a au voisinage d’un point $a$ :  
    
    $$
    f(x) \sim g(x) \Leftrightarrow f(x) = g(x) + o(g(x))
    $$
    
    Cela sera particulieremet utile lorsqu’on souhaitera remplacer une expression par un équivalent dans une égalité


- Lien entre les relations de comparaison

On se place au voisinage d’un point $a$.
    1. Si $f(x) \sim g(x)$ alors $f(x) = O(g(x))$.
    2. Si $f(x) \sim g(x)$ et $f(x) = o(h(x))$ alors $g(x) = o(h(x))$.
    3. Si $f(x) \sim g(x)$ et    $h(x) = o(f(x))$ alors $h(x) = o(g(x))$


- Calculs avec des équivalents


    1. si $f(x) \underset{x\to a}{\to} l$ et $l\neq 0$ alors $f \underset{a}{\sim} l$
    2. si $f_1 \underset{a}{\sim} g_1$ et $f_2 \underset{a}{\sim} g_2$ alors $f_1f_2 \underset{a}{\sim} g_1g_2$ et $\dfrac{f_1}{f_2} \underset{a}{\sim} \dfrac{g_1}{g_2}$
    2. si $f \underset{a}{\sim} g$ et $f$ et $g$ sont positive alors $f^\alpha \underset{a}{\sim} g^\alpha$ pour tout $\alpha \in \mathbb{R}$.


```

```{admonition} Théorème (Les équivalents de références)
Les limites usuelles en 0, nous donnent les équivalents suivants au voisinage de $0$ :

- $\sin x \sim x$
- $\arcsin x \sim x$
- $sh x \sim x$
- $\tan x \sim x$
- $\arctan x \sim x$
- $th x \sim x$
- $1 − \cos x \sim \frac{x^2}{2}$

- $1 − ch x \sim \frac{x^2}{2}$
- $\ln(1 + x) \sim x$
- $e^x − 1 \sim x$
- $(1 + x)^α − 1 \sim αx$

Plus généralement, au voisinage de a lorsque $\underset{x\to a}{f(x) \to 0}$, on a :

- $\sin f(x) \sim f(x)$
- $\arcsin f(x) \sim f(x)$
- $sh f(x) \sim f(x)$
- $\tan f(x) \sim f(x)$
- $\arctan f(x) \sim f(x)$
- $th x \sim f(x)$
- $1 − \cos f(x) \sim \frac{f(x)^2}{2}$

- $1 − ch f(x) \sim \frac{f(x)^2}{2}$
- $\ln(1 + f(x)) \sim f(x)$
- $e^{f(x)} − 1 \sim f(x)$
- $(1 + f(x))^α − 1 \sim αf(x)$

```

```{admonition} Théorème (calcul avec les equivalence)
1. Si $\underset{x\to a}{f(x) \to l}$ et $l\neq 0$ alors $f\underset{a}{\sim}l$.

2. Si $f_1 \underset{a}{\sim}g_1$ et  $f_2 \underset{a}{\sim}g_2$ alors  $f_1f_2 \underset{a}{\sim}g_1g_2$ et  $\frac{f_1}{f_2} \underset{a}{\sim}\frac{g_1}{g_2}$.
3. Soit $\alpha \in \mathbb{R}$. Si $f \underset{a}{\sim}g$ et $f$ et $g$ sont positives alors $f^\alpha \underset{a}{\sim}g^\alpha$ .
```


```{admonition} Proposition (Un équivalent donne localement le signe de la fonction)

Soient deux fonctions $f, g : I \to \mathbb{R}$ et un point $a \in \bar{I}$.
Si au voisinage du point a, $f \sim g$ alors, il existe un voisinage $V$ de $a$ sur lequel $f$ et $g$ ont même signe.
```


```{admonition} Proposition (Un équivalent donne la limite)


Soient deux fonctions $f, g : I \to \mathbb{R}$ et un point $a \in \bar{I}$.

Si $f\underset{a}{\sim} g$ et $\underset{x\to a}{\lim} g(x) = l$ alors $\underset{x\to a}{\lim} f(x) = l$.
```










