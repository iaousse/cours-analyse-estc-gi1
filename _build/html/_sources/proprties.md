# Propriétés de $\mathbb{R}$

## Addition et multiplication


Ce sont les propriétés dont on a habitué. Pour $a,\,b,\,c\in\mathbb{R},$ on a:

- $a+b=b+a$
- $a\times b=b\times a$
- $a+0=a$
- $ a\times 1=a \mbox{ si } a\neq0$
- $a+b=0\Leftrightarrow a=-b$
- $ab=1\Leftrightarrow a=\frac{1}{b}$
- $(a+b)+c=a+(b+c)$
- $(a\times b)\times c=a\times(b\times c)$
- $a\times(b+c)=a\times b+a\times c$
- $a\times b=0\Leftrightarrow(a=0 \mbox{ ou } b=0)$

On résume toutes ces propriétés en disant que :

```{admonition} Proposition
:class: important
$(\mathbb{R},+,\times)$ est un corps commutatif.
```
## Ordre sur $\mathbb{R}$


Nous allons voir que les réels sont ordonnés. La notion d'ordre est générale et nous allons définir cette notion sur un
ensemble quelconque. Cependant gardez à l'esprit que pour nous $E=\mathbb{R}$ et $\mathcal{R}=\leq$

```{admonition} Définition
Soit $E$ un ensemble.

1. Une relation $\mathcal{R}$ sur $E$ est un sous-ensemble de l'ensemble produit $E\times E.$ Pour $(x,y)\in E\times E,$ on dit que $x$ est en relation avec $y$ et on note $x\mathcal{R}y$ pour dire que $(x,y)\in R.$

2. Une relation $\mathcal{R}$ est une relation d'ordre si 
    - $\mathcal{R}$ est _réflexive_: Pour tout $x\in E,$ $x\mathcal{R}x$

    - $\mathcal{R}$ est _antisymétrique_: pour tout $x,y\in E,$ $(x\mathcal{R}y\:\mbox{et} y\mathcal{R}x) \Rightarrow x=y.$

    - $\mathcal{R}$ est _transitive_: pour tout $x,y,z\in E,$ $(x\mathcal{R}y\:\mbox{et} y\mathcal{R}z)\Rightarrow x\mathcal{R}z$

```

```{admonition} Définition
Une relation d'ordre $\mathcal{R}$ sur un ensemble $E$ est totale si pour tout $x, y\in E$ on a $x\mathcal{R}y$ ou $y\mathcal{R}x.$ On dit aussi que
$(E,\mathcal{R})$ est un ensemble totalement ordonné.
```

```{admonition} Proposition
:class: important
La relation $\leq$ sur $\mathbb{R}$ est une relation d'ordre, et de plus, elle est totale.
```

Nous avons donc:

- pour tout $x\in \mathbb{R}, x\leq x,$

- pour tout $x, y \in \mathbb{R},$ si $x\leq y$ et $y\leq x$ alors $x=y,$

-  pour tout $x, y, z\in\mathbb{R}$ si $x \leq y$ et $y \leq z$ alors $x \leq z.$

```{admonition} Remarque
:class: tip
Pour $(x, y)\in \mathbb{R}^{2}$ on a par définition:

$x\leq y \Leftrightarrow y-x\in \mathbb{R}_{+}$

$x<y\Leftrightarrow x\leq y\quad\mbox{et}\quad x\neq y$

Les opérations de $\mathbb{R}$ sont compatibles avec la relation d'ordre $\leq$ au sens suivant, pour des réels $a, b,c, d:$

$a\leq b \quad\mbox{et}\quad c\leq d)\Rightarrow a+c\leq b+d$

$a\leq b \quad\mbox{et}\quad c\geq0)\Rightarrow a\times c\leq b\times c$
```


```{admonition} Définition
On définit le maximum de deux réels $a$ et $b$ par:

$$
\max(a,b)=\left\{
\begin{array}{ll}
a\mbox{ si } a\geq b\\
b \mbox{ si } b>a
\end{array}
\right.
$$

```


## Propriété d'Archimède

```{admonition} Proposition (Propriété d'Archimède)
:class: important
$\mathbb{R}$ est _archimédien_, c'est-à-dire: 

$$
\forall x\in \mathbb{R},\exists n\in \mathbb{N};\,n> x
$$

Autrementdit, Pour tout réel $x,$ il existe un entier naturel $n$ strictement plus grand que $x.$
```


Cette propriété peut sembler évidente, elle est pourtant essentielle puisque elle permet de définir la partie entière
d'un nombre réel:

```{admonition} Proposition (partie entière)
:class: important
Soit $x\in R,$ il existe un unique entier relatif, la partie entière notée $E(x),$ tel que:

$$
E(x)\leq x< E(x)+1
$$

```

```{admonition} Exemple
:class: warning
- $E(2, 853) = 2, E(\pi) = 3, E(-3,5) =-4.$

- $E(x)=3\Leftrightarrow 3\leq x <4$

```


Pour la démonstration de la proposition de la [partie entière](partent) il y a deux choses à établir: d'abord qu'un tel entier $E(x)$ existe et ensuite
qu'il est unique:

```{admonition} Preuve
 :class: seealso, dropdown
- **Existence**

Supposons $x>0$.

Par la propriété d'Archimède il existe $n\in N$ tel que $n>x.$ 

L'ensemble $K:=\{k\in \mathbb{N}; k\leq x\}$ est donc fini (car pour tout $k$ dans $K,$ on a $0\leq k \leq n$). 

Il admet donc un plus grand élément
$k_{max} =\max K.$ 

On a alors $k_{max}\leq x$ car $k_{max} \in K,$ et $k_{max} + 1 > x$ car $k_{max} + 1 \notin K.$ Donc $k_{max}\leq x < k_{max} + 1$ et on prend donc $E(x)= k_{max}.$

- **Unicité:**

Si $k$ et $l$ sont deux entiers relatifs vérifiant $k \leq x < k + 1$ et $l \leq x < l + 1,$ on a donc $k \leq x < l + 1$. 

donc par transitivité $k < l + 1.$ 

En échangeant les rôles de $l$ et $k,$ on a aussi $l< k + 1.$ 

On en conclut que $l-1 < k < l + 1,$ mais
il n'y a qu'un seul entier compris strictement entre $l-1$ et $l+1,$ c'est $l.$ 

Ainsi $k = l.$

Le cas $x < 0$ est similaire.

```

## Valeur absolue

```{admonition} Définition
Pour un nombre réel $x,$ on définit la valeur absolue de $x$ par:


$$
|x|=\left\{
\begin{array}{ll}
x\quad\mbox{si}\quad x\geq0,\\
-x \quad\mbox{si}\quad x<0
\end{array}
\right.
$$

```

```{admonition} Proposition
:class: important
1. $|x|\geq0,\quad |x|=|-x|;\quad |x|>0\Leftrightarrow x\neq0$

2. $\sqrt{x^2}=|x|$

3. $|xy|=|x||y|$

4. Inégalité triangulaire: $|x+y|\leq |x|+|y|$

5. $||x|-|y||\leq |x-y|$
```


Sur la droite numérique, $|x-y|$ représente la distance entre les réels $x$ et $y$ ; en particulier $|x|$ représente la distance
entre les réels $x$ et 0. De plus on a $|x-a|<r\Leftrightarrow a-r<x<a+r.$




# Densité de $\mathbb{Q}$ dans $\mathbb{R}$


## Intervalle


```{admonition} Définition
Un intervalle de $\mathbb{R}$ est un sous-ensemble $I$ de $\mathbb{R}$ vérifiant la propriété:

$$
\forall a,\,b\in I,\;\forall x\in \mathbb{R},\;(a\leqslant x\leqslant b\Rightarrow x\in I)
$$
```

```{admonition} Remarque
:class: tip
Par définition;

- $I=\varnothing$ est un intervalle.

- $I=\mathbb{R}$ est aussi un intervalle.
```

```{admonition} Définition
Un intervalle ouvert est un sous-ensemble de $\mathbb{R}$ de la forme $]a,b[= \{x\in \mathbb{R},\,a<x<b\}$, où $a$ et $b$ sont des éléments de $\mathbb{R}.$
```

La notion de voisinage sera utile pour les limites.

```{admonition} Définition
Soit $a$ un réel, $V\subset R$ un sous-ensemble. On dit que $V$ est un voisinage de $a$ s'il existe un intervalle ouvert $I$ tel que $a \in I$ et $I \subset V.$
```


## Densité

```{admonition} Théorème
:class: important
1. $\mathbb{Q}$ est dense dans $\mathbb{R}$: tout intervalle ouvert (non vide) de $\mathbb{R}$ contient une infinité de rationnels.

2.  $\mathbb{R}\setminus \mathbb{Q}$ est dense dans $\mathbb{R}$ : tout intervalle ouvert (non vide) de $\mathbb{R}$ contient une infinité d'irrationnels.
```





# Borne supérieure
## Maximum, minimum

```{admonition} Définition
Soit $A$ une partie non vide de $\mathbb{R}.$ Un réel $\alpha$ est un plus grand élément de $A$ si :
$\alpha\in A$ et $\forall x\in A,\,x\leqslant \alpha.$
S'il existe, le plus grand élément est unique, on le note alors $\max A.$
Le plus petit élément de $A,$ noté $\min A,$ s'il existe est le réel $\alpha$ tel que $\alpha\in A$ et $\forall x\in A, \,x\geqslant \alpha.$

Le plus grand élément s'appelle aussi le maximum et le plus petit élément, le minimum. Il faut garder à l'esprit que
le plus grand élément ou le plus petit élément n'existent pas toujours.
```
```{admonition} Exemple
:class: warning
- 3 est un majorant de $]0, 2[ ;$

- −7,$\pi,$ 0 sont des minorants de $]0,+\infty[$ mais il n'y a pas de majorant.

Si un majorant (resp. un minorant) de $A$ existe on dit que $A$ est majorée (resp. minorée).
Comme pour le minimum et le maximum il n'existe pas toujours de majorant ni de minorant, en plus on n'a pas
l'unicité.

Soit $A =[0,1[$

1. les majorants de $A$ sont exactement les éléments de $[1,+\infty[,$

2. les minorants de $A$ sont exactement les éléments de $]−\infty,0].$

```

## Borne supérieure, borne inférieure

```{admonition} Définition
Soit $A$ une partie non vide de $\mathbb{R}$ et $\alpha$ un réel.


1. $\alpha$ est la borne supérieure de $A$ si $\alpha$ est un majorant de $A$ et si c'est le plus petit des majorants. S'il existe on le
note $\sup A.$

2. $\alpha$ est la borne inférieure de $A$ si $\alpha$ est un minorant de $A$ et si c'est le plus grand des minorants. S'il existe on le
note $\inf A.$
```

```{admonition} Exemple
:class: warning
Soit $A =]0,1].$

1. $\sup A = 1$ : en effet les majorants de $A$ sont les éléments de $[1,+\infty[.$ Donc le plus petit des majorants est 1.


2. $\inf A = 0:$ les minorants sont les éléments de $] −\infty,0]$ donc le plus grand des minorants est 0.


- $\sup[a, b] = b,$

- $\inf[a, b]=a,$


- $\sup]a, b[= b,$

- $]0,+\infty[$ n'admet pas de borne supérieure,


- $\inf]0,+\infty[= 0.$

```

```{admonition} Théorème
:class: important
Toute partie de $\mathbb{R}$ non vide et majorée admet une borne supérieure.
```
De la même façon : Toute partie de $\mathbb{R}$ non vide et minorée admet une borne inférieure.

```{admonition} Proposition (Caractérisation de la borne supérieure)
:class: important
Soit $A$ une partie non vide et majorée de $\mathbb{R}.$ La borne supérieure de $A$ est l'unique réel $\sup A$ tel que

1. si $x\in A,$ alors $x \leqslant\sup A,$

2. pour tout $y < \sup A,$ il existe $x\in A$ tel que $y < x.$

```






