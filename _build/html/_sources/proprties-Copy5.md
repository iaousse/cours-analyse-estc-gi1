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
$(\mathbb{R},+,\times)$ est un corps commutatif.
```
## Ordre sur $\mathbb{R}$


Nous allons voir que les réels sont ordonnés. La notion d'ordre est générale et nous allons définir cette notion sur un
ensemble quelconque. Cependant gardez à l'esprit que pour nous $E=\mathbb{R}$ et $\mathcal{R}=\leq$

```{admonition} Définition
Soit $E$ un ensemble.

1. Une relation $\mathcal{R}$ sur $E$ est un sous-ensemble de l'ensemble produit $E\times E.$ Pour $(x,y)\in E\times E,$ on dit que $x$ est en relation avec $y$ et on note $x\mathcal{R}y$ pour dire que $(x,y)\in R.$

2. Une relation $\mathcal{R}$ est une relation d'ordre si 
    - $\mathcal{R}$ est \textit{réflexive}: Pour tout $x\in E,$ $x\mathcal{R}x$

    - $\mathcal{R}$ est \textit{antisymétrique}: pour tout $x,y\in E,$ $(x\mathcal{R}y\:\mbox{et} y\mathcal{R}x) \Rightarrow x=y.$

    - $\mathcal{R}$ est \textit{transitive}: pour tout $x,y,z\in E,$ $(x\mathcal{R}y\:\mbox{et} y\mathcal{R}z)\Rightarrow x\mathcal{R}z$

```

```{admonition} Définition
Une relation d'ordre $\mathcal{R}$ sur un ensemble $E$ est totale si pour tout $x, y\in E$ on a $x\mathcal{R}y$ ou $y\mathcal{R}x.$ On dit aussi que
$(E,\mathcal{R})$ est un ensemble totalement ordonné.
```

```{admonition} Proposition
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

On définit le maximum de deux réels $a$ et $b$ par:

$$
\max(a,b)=\left\{
\begin{array}{ll}
a\mbox{ si } a\geq b,\\
b \mbox{ si } b>a.
\end{array}
\right}
$$

****************************8
**
****************************8

```{admonition} Exercice
:class: note
Comment définir $\max(a,b,c),$ $\max(a_1,...,a_n)$? Et $\min(a,b)$?
```
