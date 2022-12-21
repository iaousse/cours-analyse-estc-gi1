# Intégration sur un intervalle quelconque


Dans les chapitres précédents, nous avons définies $\int_a^b f(t)dt$, pour une fonction continue ou continue par morceaux sur $[a, b]$. Dans le présent chapitre, étant donnée une fonction continue seulement sur $]a, b[$, on cherche a donner un sens a $\int_a^b f(t)dt$.

## Intégration sur un intervalle semi-ouvert

```{admonition} Définition
Soit $f$ une fonction continue sur l'intervalle $[a, b[$ ou $(-\infty <a < b \leq +\infty)$.
On dit que l'intégrale $\int_a^b f(t)dt$ converge ou est convergent si la fonction $x\mapsto \int_a^x f(t)dt$, qui est définie sur $[a, b[$  possède une limite finie en $b$.
```

On note donc $\int_a^b f(t)dt = \lim_{x\to b} \int_a^x f(t)dt$. Si cette intégrale n'est pas convergente, on dit qu’elle est convergente. L'intégrale $\int_a^b f(t)dt$ est dite impropre (ou généralisée). On dit aussi qu'il y a une impropreté en $b$. Ou encore que l'intégrale est généralisée en $b$.
 
**Remarques :**
- Si f est continue sur $[a, b]$, on retrouve la définition de l'intégrale d'une fonction continue sur le segment $[a, b]$.
- Si $b$ est fini et $f$ admet un prolongement par continuité en $b$, l'intégrale $\int_a^b f(t)dt$ converge, car si $\tilde{f}$ est le prolongement par continuité de $f$, on obtient:

$$
\lim_{x \to b} \int_a^x f(t)dt = \lim_{x\to b} \int_a^x \tilde{f}(t)dt = \int_a^b \tilde{f}(t)dt
$$

On dit qu'on a une "fausse impropreté" en $b$.

- Si $b=+\infty$, l'intégrale $\int_a^b f(t)dt$ est toujours impropre.


```{admonition} Proposition

Si $f$ est une fonction continue sur l'intervalle $[a, b[$, $(-\infty <a < b \leq +\infty)$, l'intégrale $\int_a^b f(t)dt$ est convergent si, et seulement si, toute primitive $F$ de $f$ possède une limite finie en $b$ et l'in a alors:

$$
\int_a^b f(t)dt = \lim_{x\to b} F(x) - F(a)
$$
```

```{admonition} Preuve
Nous avons $\int_a^x f(t)dt=F(x)-F(a)$.
```

**Remarques :**

- Dans le cas où on connait une primitive de $f$, on peut ainsi déterminer la nature convergente ou divergente de l'intégrale et la calculer.

- Il résulte de cette proposition que si $c\in ]a, b[$, l'intégrale $\int_a^b f(t)dt$ converge si, et seulement si, $\int_c^b f(t)dt$ converge. La nature de l'intégrale $\int_a^b f(t)dt$ ne dépend pas donc que du comportement de $f$ au voisinage de l'impropre $b$.

```{admonition} Exemples

- la fonction $ t \mapsto e^{-t}$ est continue sur $[0, +\infty[$ et a pour primitive la fonction $t\mapsto -e^{-t}$. Comme $\lim_{t \to +\infty} -e^{-t} = 0$, l'integrale $\int_0^{+\infty} e^{-t}dt$ converge et 

$$
\int_0^{+\infty}e^{-t}dt = \lim_{t\to +\infty} -e^{-t} + e^{0} = 1
$$

2- L'intégrale $\int_0^{+\infty} sin(t)dt$ diverge, car la fonction $-cos$, primitive de $sin$ n'a pas de limite en $+\infty$.
```

## Reste d'une intégrale convergente

```{admonition} Définition

Soit $f$ une fonction continue sur l'intervalle $[a, b[$, $(-\infty <a < b \leq +\infty)$

On suppose que l'intégrale $\int_a^b f(t)dt$  est convergente. On appelle reste de cette intégrale impropre l'intégrale $\int_x^b f(t)dt$ ou $x\in]a, b[$.
```

```{admonition} Proposition
Soit $f$ une fonction continue sur l'intervalle $[a, b[$, $(-\infty <a < b \leq +\infty)$ telle que l'intégrale $\int_a^b f(t)dt$ converge, Le reste $\int_x^b f(t)dt$ ou $x\in ]a, b[$ a pour limite 0 quand $x$ tend vers $b$.
```
```{admonition} Preuve
Nous avons $\lim_{x\to b} \int_x^b f(t)dt = \lim_{x\to b} ( \lim_{u\to b} F(u)- F(x)) = \lim_{u\to b} F(u)- \lim_{x\to b}F(x) =0$
```

On définit de la même façon l'intégrale d'une fonction continue sur $]a, b]$.


```{admonition} Définition
Soit $f$ une fonction continue sur l'intervalle $]a, b]$ ou $(-\infty \leq a < b < +\infty)$.
On dit que l'intégrale $\int_a^b f(t)dt$ converge ou est convergent si la fonction $x\mapsto \int_x^b f(t)dt$, qui est définie sur $]a, b]$  possède une limite finie en $a$.

```
On note donc $\int_a^b f(t)dt = \lim_{x\to a} \int_x^b f(t)dt$.

```{admonition} Proposition

Soit $f$ une fonction continue sur l'intervalle $]a, b]$ ou $(-\infty \leq a < b < +\infty)$, l'intégrale $\int_a^b f(t)dt$ est convergent si, et seulement si, toute primitive $F$ de $f$ possède une limite finie en $a$ et l'on a alors:

$$
\int_a^b f(t)dt = F(b) -\lim_{x\to a}F(x)
$$

```

```{admonition} Exemple
Montrons la convergence de $\int_0^1 ln(t)dt$, qui est impropre car la fonction $ln$ est continue sur $]0, 1]$ mais n'est pas définie en 0.

On obtient pour $x\in ]0, 1]$, en intégrant par parties,

$\int_x^1 ln(t)dt=[tln(t)]_{x}^1 - \int_x^1dt = xln(x)-1 + x$.

Comme $\lim_{x\to 0} xln(x)=0$, on en déduit que $\int_0^1ln(t)dt $ converge et $\int_0^1ln(t)dt =-1$. 
```

**Remarques :** Comme précédemment, si $f$ est continue sur $]a, b]$, le reste de l'intégrale convergente $\int_a^b f(t)dt$, qui est $\int_a^x f(t)dt$, tend vers 0 quand $x$ tend vers $a$.

## Intégrale d'une fonction sur un intervalle ouvert

```{admonition} Définition

Soit $f$ continue sur $]a, b[$ ou $(-\infty \leq a < b \leq +\infty)$, $c \in ]a, b[$. On dit que l'intégrale $\int_a^b f(t)dt$ converge si $\int_a^c f(t)dt$ et $\int_c^b f(t)dt$ convergent et l'on pose, en cas de convergence,

$$
\int_a^b f(t)dt = \int_a^c f(t)dt + \int_c^b f(t)dt
$$

```

Cette définition ne dépend pas du choix du point $c$ comme le montre la proposition suivante:

```{admonition} Proposition
Soit $f$ continue sur $]a, b[$ ou $(-\infty \leq a < b \leq +\infty)$, $c \in ]a, b[$. L'intégrale $\int_a^b f(t)dt$ converge si, et seulement si, toute primitive $F$ de $f$ sur $]a, b[$ possède une limite finie en $a$ et $b$ et en cas de convergence, on a

$$
\int_a^b f(t)dt = \lim_b F - \lim_a F
$$
```


```{admonition} Théorème
Soit $\alpha$ un réel quelconque.

Si $a$ est un réel positif, l'intégrale $\int_0^a \dfrac{1}{t^\alpha} dt $ converge si, et seulement si, $\alpha <1$; l'intégrale $\int_a^{+\infty} \dfrac{1}{t^\alpha} dt $ converge si, et seulement si, $\alpha > 1$.


Plus généralement, si $a$ et $b$ sont des réels tels $a<b$, $\int_a^b \dfrac{1}{(t-a)^{\alpha}}dt $ converge si, et seulement si $\alpha <1$.
```


## Propriétés des intégrales convergentes

```{admonition} Définition
Soit $f : [a, b] \to \mathbb R$.

On suppose qu'il existe une subdivision $a_0=a < a_1 < \ldots < a_p=b$ de $[a, b]$ telle que $f$ soit définie et continue sur chaque intervalle $]a_k, a_{k+1}[$($0\leq k \leq (p-1)$). On dit que l'intégrale $\int_a^b f(t)dt$ converge si, pour $0\leq k \leq p-1$, $\int_{a_{k}}^{a_{k+1}} f(t)dt$ converge. Le cas échéant, on pose :

$$
\int_a^b f(t)dt = \sum_{k=0}^{p-1} \int_{a_{k}}^{a_{k+1}} f(t)dt
$$

```
**Remarques :**

- Dans la définition précédente, le résultat ne dépend pas de la subdivision choisie.
- Si $f$ est continue par morceaux alors les intégrales $\int_{a_{k}}^{a_{k+1}} f(t)dt$ convergent car sa restriction sur $[a_k, a_{k+1}]$ possède un prolongement par continuité en $a_k$ et $a_{k+1}$.

Les théorèmes qui suivent sont des versions "intégrales impropres" des propriétés des intégrales sur un segment.

```{admonition} Théorème

Soit $f$ et $g$ deux fonctions définies et continue sur l'intervalle $[a, b]$, $(-\infty \leq a < b \leq +\infty)$ sauf en un nombre fini de points, $\lambda$ et $\mu$ deux réels. Si les intégrales $\int_a^b f(t)dt$ et $\int_a^b g(t)dt$ convergent, alors $\int_a^b (\lambda f + \mu g)(t)dt$ converge et 

$$
\int_a^b (\lambda f + \mu g)(t)dt = \lambda\int_a^b f(t)dt + \mu\int_a^b g(t)dt
$$

```

```{admonition} Proposition

Soit $f$ une fonction définie et continue sur l'intervalle $[a, b]$, $(-\infty \leq a < b \leq +\infty)$ sauf en un nombre fini de points, $c \in ]a, b[$. Si l’intégrale $\int_a^b f(t)dt$ converge, alors $\int_a^c f(t)dt$  et $\int_c^b f(t)dt$ convergent et 

$$
\int_a^b f(t)dt =\int_a^c f(t)dt + \int_c^b f(t)dt
$$

```
 
### Positivité

```{admonition} Proposition
Soit $f$ une fonction definie sur $]a, b[$ ($-\infty \leq a < b \leq +\infty$).

Si $\int_a^b f(t)dt$ converge et si $f$ est positive sur $]a, b[$, alors on a $\int_a^b f(t)dt\geq 0$. Si de plus $f$ n'est pas la fonction nulle, on obtient $\int_a^b f(t)dt>0$.
```

```{admonition} Corollaire
Soient $f$ et $g$ deux fonctions définies et continues sur $]a, b[$ ($-\infty \leq a < b \leq +\infty$).
Si les intégrales $\int_a^b f(t)dt$ et $\int_a^b g(t)dt$ convergent et si $f\leq g$, alors on a 


$$
\int_a^bf(t)dt \leq \int_a^b g(t)dt
$$

Si de plus $f$ n'est pas égale à $g$. On obtient


$$
\int_a^b f(t)dt < \int_a^b g(t)dt
$$

```


### Intégration par parties

```{admonition} Théorème

Soient $u$ et $v$ deux fonctions de classe $\mathcal C^1$ de $]a, b[$ dans $\mathbb R$ avec ($-\infty \leq a < b \leq +\infty$). Si le produit $uv$ possède une limite finie en $a$ et $b$, les intégrales $\int_a^b u^{'}(t)v(t)dt$ et $\int_a^b u(t)v^{'}(t)dt$ ont même nature et, en cas de convergence, on dispose de l’égalité

$$
\int_a^b u^{'}(t)v(t)dt= \lim_{b} uv - \lim_{a} uv - \int_a^b u(t)v^{'}(t)dt
$$


```
### Changement de variables

```{admonition} Théorème

Soient $\varphi$ une fonction de classe $\mathcal C^1$, strictement monotone, réalisant une bijection de $]\alpha, \beta[$ sur $]a, b[$ et $f : ]a, b[ \to \mathbb R$, continue. Les intégrales $\int_\alpha^\beta f(\varphi(t))\varphi^{'}(t)dt$ et $\int_a^b f(t)dt$ ont même nature et en cas de convergence

$$
\int_a^b f(t)dt = \int_\alpha^\beta f(\varphi(t))\varphi^{'}(t)dt \mbox{ si } \varphi \mbox{ est croissante}
$$

$$
\int_a^b f(t)dt = - \int_\alpha^\beta f(\varphi(t))\varphi^{'}(t)dt \mbox{ si } \varphi \mbox{ est décroissante}
$$

```

## Cas des fonctions positives


Pour la plupart des fonctions, on ne sait pas expliciter de primitive. C'est pourquoi il est utile de disposer de méthodes permettant de montrer la convergence des intégrales impropres sans en calculer la valeur. Dans cette section, on traite du cas où la fonction garde un signe constant au voisinage de l'impropreté.


### Condition nécessaire et suffisante de convergence

```{admonition} Théorème

Soit $f$ une fonction continue et positive sur $[a, b[$. L'intégrale $\int_a^b f(t)dt$ converge si, et seulement si, la fonction $x\mapsto \int_a^x f(t)dt$ est majorée sur $[a, b[$.

De même,

Si $f$ une fonction continue et positive sur $]a, b]$. L'intégrale $\int_a^b f(t)dt$ converge si, et seulement si, la fonction $x\mapsto \int_x^b f(t)dt$ est majorée sur $]a, b]$.

```

### Critère de comparaison

```{admonition} Théorème

Soient $f$ et $g$ deux fonctions continues sur $[a, b[$. On suppose qu'il existe $c\in [a, b[$ tel que $0\leq f(t)\leq g(t)$ pour tout $t\in [a, b[$.

Si l'intégrale $\int_a^b g(t)dt$ converge, alors $\int_a^b f(t)dt$ converge.

Si l'intégrale $\int_a^b f(t)dt$ diverge, alors $\int_a^b g(t)dt$ diverge.
```

## Cas des fonctions de signe quelconque

### Convergence absolue

```{admonition} Définition

Soit $f : [a, b] \to \mathbb R$ une fonction continue ($-\infty \leq a < b \leq +\infty$). On dit que l'intégrale $\int_a^b f(t)dt$ est absolument convergente si $\int_a^b |f(t)|dt$ est convergente.
```

```{admonition} Théorème
Soit $f : [a, b] \to \mathbb R$ une fonction continue ($-\infty \leq a < b \leq +\infty$). si $\int_a^b f(t)dt$ est absolument convergente, elle est convergente. De plus, on dispose de l'inégalité



$$
\left | \int_a^b f(t)dt\right | \leq \int_a^b |f(t)|dt
$$


```

```{admonition} Exemple
 Pour $\alpha >1$, l'intégrale $\int_1^{+\infty} \dfrac{sin(t)}{t^\alpha}dt$ est absolument convergente car, pour $t\geq 1$, $\left |\dfrac{sin(t)}{t^\alpha} \right | \leq \dfrac{1}{t^\alpha}$ et $\int_1^{+\infty} \dfrac{1}{t^\alpha}dt$ converge.

```




