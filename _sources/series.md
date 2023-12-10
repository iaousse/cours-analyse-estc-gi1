# Les séries numériques

## Définitions et premières propriétés

```{admonition} Définition
Soit $(u_n)_{n\in\mathbb N}$ une suite d'éléments de $\mathbb R$ (ou $\mathbb C$). Pour tout $n\in\mathbb N$ on pose $S_n= \sum_{\substack{k=0}}^n u_k$ ($n^{-ème}$ somme partielle). La série de terme général $u_n$ est la suite $(S_n)_n$. $S_n$ est la somme partielle de rang $n$ de la série de terme général $u_n$.

$$
S_n=u_0+u_1+\dots+u_n
$$

```
La série de terme général est notée $\sum_{n\geq 0} u_n$ ou $\sum u_n$.

On s’intéresse à la limite de $\sum_{n\geq 0} u_n$ lorsque $n\to +\infty$.

On dira que la série $\sum u_n$ est :
- convergente (CV) si $\lim_{n\to +\infty} S_n$ existe, et on note alors $\sum_{n\geq 0}u_n$ cette limite ou encore $\sum_{\substack{n=0}}^{+\infty}u_n$.
- divergente (DIV) sinon.
- absolument convergente (AC) si la série de terme général $|u_n|$ (ou encore $\sum_{n\geq 0} |u_n|$) est convergente.

On dira aussi que la série converge simplement (CS) si elle converge mais pas absolument.

On peut définir de même la notion de convergence de la série $\sum_{n\geq p} u_n$ si $u_n$ n'est définie qu'a partir du rang $p$:

$$
\sum_{\substack{n\geq p}} u_n = u_p + u_{p+1}+ \ldots 
$$

La modification d'un nombre fini de termes de la série ne change pas sa nature (CV, AC, DIV, CS).


```{admonition} Proposition (Condition nécessaire)
Si la série $\sum_{n\geq 0}u_n$ converge alors $(u_n)$ converge vers 0.
```
Toute série dont le terme général ne converge pas vers 0 est donc divergente. Par exemple, la série de terme général $n$ ($\sum_{n\geq 0}n$) est divergente. Par contre si le terme général converge vers 0 cela ne veut pas dire que la série est convergente. La convergence de la suite de terme général vers 0 est condition nécessaire mais pas suffisante.

## Série harmonique $\sum_{n\geq 1} \dfrac{1}{n}$
La série harmonique (de terme général $\dfrac{1}{n}$) est divergente. En effet, pour montrer ca, on va montrer que la suite des somme partielle est plus grandes qu’une suite qui est divergente.

Soit $k\geq 1$. 

La fonction $f: x\mapsto \dfrac{1}{x}$ est continue sur l'intervalle $[k, k+1]$. D'autre part la fonction $g: x\mapsto \dfrac{1}{k}$ est constante sur cet intervalle.

De plus, nous avons pour tout $x\in [k, k+1], \dfrac{1}{x}\leq \dfrac{1}{k}$ c'est-a-dire, $f\leq g$ sur cet intervalle.

Par suite, $\int_k^{k+1}f(x)dx= \int_k^{k+1}\dfrac{dx}{x} \leq \int_k^{k+1} g(x)dx = \dfrac{1}{k}$.

Maintenant soit $n\geq 2$. Alors 

$$
\int_1^{2}\dfrac{dx}{x}+ \ldots + \int_{n-1}^{n}\dfrac{dx}{x}=\int_1^{n}\dfrac{dx}{x}\leq 1+ \dfrac{1}{2} + \ldots + \dfrac{1}{n} =S_n
$$

Nous avons $\int_1^{n}\dfrac{dx}{x}=ln(n)$. Or, $ln(n) \to +\infty$ donc $S_n \to +\infty$.

Enfin, la série $\sum \dfrac{1}{n}$ est divergente.

## Série géométrique $\sum_{n\geq 0} q^n$

La suite des sommes partielles est donnée par $S_n = 1+q+q^2 + \ldots + q^n$.

Donc 

$$
S_{n+1}= 1+q+q^2 + \ldots + q^n + q^{n+1}=1+q(1+q+q^2 + \ldots + q^n)=1+qS_n
$$

D'autre part,  

$$
S_{n+1}- S_n = q^{n+1}
$$

Donc 

$$
1+(q-1)S_n=q^{n+1}
$$

Si $|q|\neq 1$, 

$$
S_n = \dfrac{q^{n+1}-1}{q-1}=\dfrac{1-q^{n+1}}{1-q}
$$

et s'en suit alors que $S_n$ diverge si $|q| > 1$ et converge si $|q| < 1$. Dans ce dernier cas on a $Sn \to \dfrac{1}{1-q}$. 

Enfin, la série diverge si
$q = ±1$. En effet pour les deux cas, le terme général ne converge pa vers 0.

```{admonition} Théorème
La série $\sum_{n\geq 0}q^n$ converge si, et seulement si, $|q|<1$. Le cas échéant $\sum_{n= 0}^{+\infty}q^n=\dfrac{1}{1-q}$
```

```{admonition} Définition
Soit $\sum u_n$ une série convergente. On appelle reste d’ordre n de cette série
la quantité $R_n$ donnée par

$$
R_n = \sum_{k=n+1}^{\infty}u_k
$$

On a alors 

$$
S= \sum_{i=0}^{\infty}u_k = S_n + R_n
$$

```

```{admonition} Proposition
Le reste d’ordre n d’une série convergente $\sum u_n $ tend vers 0, lorsque $n\to +\infty$.
```

```{admonition} Proposition
Soient $\sum u_n$ et $\sum v_n$ deux séries convergentes. Alors $\sum (u_n + \lambda v_n)$ converge pour tout $\lambda \in \mathbb R$.
```




```{admonition} Proposition
Soient $\sum u_n$ et $\sum v_n$ deux séries convergentes telles que $u_n \leq v_n$. Alors

$$
\sum_{i=0}^\infty u_n \leq \sum_{i=0}^\infty v_n
$$

```

## Séries à termes positifs

```{admonition} Lemme
Soit $\sum u_n$ une série a termes positifs, $u_n\geq 0$. Alors $\sum u_n$ converge si et seulement si la suite des somme partielles est majorée, c'est-a-dire $\exists M>0$ tel que $S_n=\sum_{k=0}^n u_k \leq M, \forall n$.
```

```{admonition} Théorème (Critères de convergence)

Soient les deux séries $\sum u_n$ et $\sum v_n$. Alors on :

1. Si $0\leq u_n \leq v_n$, alors on a $\sum v_n$ converge $\Rightarrow \sum u_n$ converge et $\sum u_n$ diverge $\Rightarrow \sum v_n$ diverge.
2. si $\dfrac{u_n}{v_n} \to 1$ lorsque $n \to +\infty$ alors $\sum u_n$ et $\sum v_n$ sont de même nature.
3. S'il existe $\alpha >1$ tel que $n^\alpha u_n \to 0$ alors $\sum u_n$ converge.
4. Soit $u_n \geq 0$ telle que $\sqrt[n]{u_n} \to l$ alors, $\sum u_n$ converge si $l<1$ et diverge si $l>1$. (Règle de Cauchy).
5. Soit $u_n>0$ telle que $\dfrac{u_{n+1}}{u_n} \to l$, alors $\sum u_n$ converge si $l<1$ et diverge si $l>1$. (Règle de D'Alembert).

Pour le cas $l=1$ dans les regles de Cauchy et D'Alembert on ne peut pas identifier la nature de la série. Dans ce cas on doit utiliser d'autres méthodes (déjà citées) ou d'étudier la suite des sommes partielles.
```

### Exemple: Serie de Riemann

On considere la serie $\dfrac{1}{n^\alpha}$ avec $\alpha \in \mathbb R$.

- Si $\alpha \leq 0$ alors $\dfrac{1}{n^\alpha}= n^{-\alpha} \nrightarrow  0$ donc la série $\sum \dfrac{1}{n^\alpha}$ diverge.
- Si $\alpha =1$ alors il s'agit de la série harmonique qui divergente.
- si $0 < \alpha$,  on a $\dfrac{1}{n}<\dfrac{1}{n^\alpha}$ donc la série $\sum \dfrac{1}{n^\alpha}$ diverge d'après le critère de comparaison.
- si $\alpha > 1$, alors on a pour $k\geq 2$:

$$
\dfrac{1}{k^\alpha} \leq \int_{k-1}^{k} \dfrac{dx}{x^\alpha}
$$

Donc 

$$
S_n= \sum_{k=1}^{n} \dfrac{1}{k^\alpha} \leq \int_1^n \dfrac{dx}{x^\alpha}
$$

Or $\alpha > 1$ donc $\int_1^\infty \dfrac{dx}{x^\alpha}$ existe est $\lim_{n \to +\infty} \int_1^n \dfrac{dx}{x^\alpha}= \int_1^\infty \dfrac{dx}{x^\alpha}$

Alors, $S_n$ est croissante et majorée donc convergente :

$$
\sum_{n=1}^{+\infty} \dfrac{1}{k^\alpha} = \lim_{n \to +\infty} S_n \leq \int_1^\infty \dfrac{dx}{x^\alpha}.
$$

```{admonition} Théorème (Séries de Riemann)
La serie $\sum \dfrac{1}{n^\alpha}$, $\alpha \in \mathbb R$, converge si et seulement si $\alpha >1$.
```

## Exemples
1. La série de terme général $u_n =\dfrac{2^{2n}e^{-2n}}{n}$ ($\sum \dfrac{2^{2n}e^{-2n}}{n}$)

    Par la règle de D’Alembert, on a
    
    $$
    \dfrac{u_{n+1}}{u_n}=\dfrac{\dfrac{2^{2n+2}e^{-2n-2}}{n+1}}{\dfrac{2^{2n}e^{-2n}}{n}}=\left(\dfrac{2}{e}\right)^2 \dfrac{n}{n+1} \to \left(\dfrac{2}{e}\right)^2 <1
    $$
    
    Donc la série est convergente.
2. La série de terme général $u_n = (\dfrac{n}{n+1})^{n^2}$

    Par la règle de Cauchy, on a
    
    $$
    \sqrt[n]{u_n} = \sqrt[n]{\left(\dfrac{n}{n+1}\right)^{n^2}} = \sqrt[n]{\left(\dfrac{1}{\dfrac{n+1}{n}}\right)^{n^2}} = \sqrt[n]{\left(1+\dfrac{1}{n}\right)^{-n^2}}=\left(\dfrac{1}{1+n}\right)^{-n}=\dfrac{1}{\left(1+\dfrac{1}{n}\right)^n}
    $$
    
    Or, $(1+\dfrac{1}{n})^n \to e$. Donc, $\sqrt[n]{u_n}= \dfrac{1}{(1+\dfrac{1}{n})^n} \to \dfrac{1}{e} < 1$
    
    Par suite la série est convergente.
    
3. Soit $u_n = (\dfrac{an}{n+1})^{n^2}$ avec $a\in \mathbb R^+$. On veut étudier la nature de la série de terme général $u_n$.

    Par la régle de Cauchy, on a $\sqrt[n]{u_n} = \sqrt[n]{\left(\dfrac{a}{1+\dfrac{1}{n}}\right)^{n^2}} = \left(\dfrac{a}{1+\dfrac{1}{n}}\right)^{n}= \dfrac{a^n}{1+\dfrac{1}{n}}$.
    - si $a<1$ nous avons $\sqrt[n]{u_n} \to 0 < 1$, donc la série de terme général $u_n$ converge.
    - si $a=1$ nous somme dans le cas de l'exemple précédant. La série de terme général $u_n$ converge.
    - si $a>1$ nous avons $\sqrt[n]{u_n} \to +\infty$, donc la série de terme général $u_n$ diverge.
    
    Par suite, la série $\sum (\dfrac{an}{n+1})^{n^2}$ avec $a\in \mathbb R^+$ converge si et seulement si $a \leq 1$.
4. La serie de terme general $u_n = \int_0^{\frac{\pi}{n}} \dfrac{\sin x}{1+x^2}dx$

    Pour tout $x \in [0, \frac{\pi}{n}] \subset [0, \pi]$ on a $1 \leq 1+x^2 \leq 1+ \pi^2$. Donc $\dfrac{1}{1+\pi^2} \leq \dfrac{1}{1+x^2} \leq 1$. D’où,
    
    $$
    \dfrac{\sin x}{1+x^2} \leq \sin x
    $$
    
    et ca par ce que $\forall x \in [0, \pi], \sin(x)\leq 0$. On en déduit,
    
    $0 \leq u_n =  \int_0^{\frac{\pi}{n}} \dfrac{\sin x}{1+x^2}dx \leq  \int_0^{\frac{\pi}{n}} \sin x dx = 1- \cos \frac{\pi}{n}$
    
    Et puisque $\lim_{n\to +\infty} \dfrac{1- \cos \frac{\pi}{n}}{\frac{\pi}{n}} = 1$ (pourquoi?) donc la serie de terme general $1- \cos \frac{\pi}{n}$ est de meme nature que la serie de terme general $\dfrac{\pi^2}{n^2}$. mais cette serie est convergente car c'est une serie de Reimann ($2>1$). Donc $1- \cos \frac{\pi}{n}$ est convergente et par compariason la serie de terme general $u_n$ est convergente.
    
    
## Séries alternées

```{admonition}
La série $\sum u_n$ est dite alternée si et seulement si pour tout $n \in \mathbb N$, on a
$u_n = (−1)^n|un|$ ou $u_n = −(−1)^n|un|$.
```

```{admonition} Théorème (Critère spécial des séries alternées)
Soit $\sum u_n$ une série alternée. Si la suite $(|u_n|)_n$ est décroissante et $|u_n| \to 0$, alors $\sum u_n$ converge.
```

```{admonition} Exemple
La série de terme général $u_n = \dfrac{(-1)^n}{n}$ est une série alternée. En effet, elle s'écrit comme $(-1)^n|u_n|$. La série n'est pas absolument convergente car $|u_n|= \dfrac{1}{n}$. Donc on ne peut rien dire à ce stade. En revanche, on remarque que la suite $(|u_n|)_n$ est décroissante et $|u_n| \to 0$. Donc, en appliquant le critère spécial des séries alternées la série de terme général $u_n = \dfrac{(-1)^n}{n}$ est convergente.
```
