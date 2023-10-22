
# Suites réelles: Définitions générales



```{admonition} Définition
Une suite est une application $u:\mathbb{N}\rightarrow\mathbb{R}.$

Pour $n\in \mathbb{N},$ on note $u(n)$ par $u_n$ et on l'appelle $n^{ieme}$ terme ou terme général de la suite $u.$

```

Une suite $u:\mathbb{N}\rightarrow\mathbb{R}$ est plus souvent notée par $(u_n)_{n\in \mathbb{N}},\,(u_n)_{n\geq0}$ ou simplement par $(u_n).$

Si une suite $u$ est définie à partir d'un certain entier naturel $n_0>0,$ alors dans ce cas on note cette suite par $(u_n)_{n\geq n_0}.$

```{admonition} Exemple
:class: seealso
1. Soit $(u_n)$ la suite définie par $u_n=\sqrt{n}-1.$ Les cinq premiers termes de cette suite sont $-1,0,\sqrt{2}-1,\sqrt{3}-1,1.$

2. Soit $(v_n)_{n\geq1}$ la suite définie par $v_n=\dfrac{1}{n(n+1)}.$ Les trois premiers termes de cette suite sont $\dfrac{1}{2},\dfrac{1}{6},\dfrac{1}{12}$

3. $((-1)^n)$ est une suite qui prends deux valeurs: 1 et $-1.$
```

```{admonition} Définition
Soit $(u_n)_{n\geq n_0}$ une suite.

1. $(u_n)_{n\geq n_0}$ est dite une suite croissante (resp. strictement croissante) si $u_{n+1}\geq u_n$ (resp. $u_{n+1}>u_n$), $\forall n\geq n_0.$

2. $(u_n)_{n\geq n_0}$ est dite une suite décroissante (resp. strictement décroissante) si $u_{n+1}\leq u_n$ (resp. $u_{n+1}<u_n$), $\forall n\geq n_0.$
```

```{admonition} Exemple
:class: seealso
1. La suite $(u_n)_{n\geq1}$ définie par $u_n=\dfrac{1}{n^2},\;\forall n\in \mathbb{N}^{*},$ est strictement décroissante. En effet, on a

\begin{eqnarray*}
u_{n+1}-u_n
&=& \dfrac{1}{(n+1)^2}-\dfrac{1}{n^2}\\
&=& \dfrac{n^2-(n+1)^2}{n^2(n+1)^2}\\
&=& \dfrac{n^2-n^2-2n-1}{n^2(n+1)^2}\\
&=& -\dfrac{2n+1}{n^2(n+1)^2}\\
& & <0
\end{eqnarray*}

2. La suite $(v_n)$ définie par $v_n=e^n,\;e^{n+1}-e^n=e^n e-e^n=e^n (e-1)>0. Donc elle est strictment croissante.$
```

```{admonition} Remarque
:class: tip
Si $(u_n)_{n\geq n_0}$ est une suite à termes strictement positifs, alors

1. $(u_n)_{n\geq n_0}$ est croissante si, et seulement si $\dfrac{u_{n+1}}{u_n}\geq1,\;\forall n\geq n_0.$

2. $(u_n)_{n\geq n_0}$ est décroissante si, et seulement si $\dfrac{u_{n+1}}{u_n}\leq 1,\;\forall n\geq n_0.$

Considérons à nouveau la suite $(v_n)$ telle que $v_n=e^n,\;\forall n\in \mathbb{N}.$ On sait que $v_n>0,\;\forall n\in \mathbb{N}.$ De plus, pour tout $n\in \mathbb{N}$ on a 

$$
\dfrac{v_{n+1}}{v_n}=\dfrac{e^{n+1}}{e^n}=e^{(n+1)-n}=e
$$

Donc $\dfrac{v_{n+1}}{v_n}>1,\;\forall n\in \mathbb{N}.$ Ainsi la suite $(v_n)$ est strictement croissante.
```

```{admonition} Remarque
:class: tip
Il se peut qu'une suite ne soit ni croissante ni décroissante. Voilà deux exemples:

1. La suite $(u_n)$ telle que $u_n=(-1)^n$ est une suite ni croissante ni décroissante.

2. Considérons la suite $(v_n)$ définie par $v_n=\sin(n\dfrac{\pi}{2}),\;n\in\mathbb{N}.$ Ces premiers termes sont:

$v_0=\sin(0)=0,\;v_1=\sin(\dfrac{\pi}{2}),\;v_2=\sin(\pi)=0,\;v_3=\sin(3\dfrac{\pi}{2})=-1,\;v_4=\sin(2\pi)=0,...$
```

```{admonition} Définition
Une suite $(u_n)_{n\geq n_0}$ est dite monotone (resp. strictement monotone) si $(u_n)_{n\geq n_0}$ est croissante ou décroissante (resp. strictement croissante ou strictement décroissante).
```

```{admonition} Définition
Soit $(u_n)_{n\geq n_0}$ une suite.

1. $(u_n)_{n\geq n_0}$ est dite majorée si $\exists M\in \mathbb{R}$ tel que $u_n\leq M,\;\forall n\geq n_0.$

2. $(u_n)_{n\geq n_0}$ est dite minorée si $\exists m\in \mathbb{R}$ tel que $u_n\geq M,\;\forall n\geq n_0.$

3. $(u_n)_{n\geq n_0}$ est dite bornée si $(u_n)_{n\geq n_0}$ est minorée et majorée.
```

```{admonition} Exemple
:class: seealso
On considère les trois suites $(u_n),\;(v_n)$ et $(w_n)$ définies par leurs termes généraux

$$
u_n=1+n^2,\quad v_n=5-n(n+1),\quad w_n=2+\dfrac{1}{n+1},\quad n\in \mathbb{N}
$$

- Pour tout $n\in \mathbb{N},$ on a $u_n\geq1.$ Donc $(u_n)$ est minorée par 1.

- Pour tout $n\in \mathbb{N},$ on a $v_n\leq1.$ Donc $(v_n)$ est majorée par 5.

- Pour tout $n\in \mathbb{N},$ on a $2<w_n\leq 3.$ La suite est donc bornée.
```
```{admonition} Remarque
:class: tip
Soit $(u_n)_{n\geq n_0}$ une suite réelle.

1. Si $(u_n)_{n\geq n_0}$ est croissante, alors $(u_n)_{n\geq n_0}$ est minorée par son premier terme.

2. Si $(u_n)_{n\geq n_0}$ est décroissante, alors $(u_n)_{n\geq n_0}$ est majorée par son premier terme.
```

```{admonition} Proposition
:class: seealso
Soit $(u_n)_{n\geq n_0}$ une suite réelle. Alors $(u_n)_{n\geq n_0}$ est bornée si et seulement si

$$
\exists M\geq0\;\mbox{tel que}\;\forall n\geq n_0:\quad |u_n|\leq M
$$

```
# Convergence d'une suite réelle
```{admonition} Définition
On dit qu'une suite réelle $(u_n)$ converge vers un réel $\ell$ lorsque pour tout $\varepsilon>0,$ il existe $N\in \mathbb{N}$ tel que pour tout entier $n>N,$ on a $|u_n-\ell|<\varepsilon.$

Dans ce cas, $\ell$ est appelée limite de la suite $(u_n).$ On dit alors que $(u_n)$ a pour limite $\ell$ ou $(u_n)$ tend vers $\ell$ et on écrit

$$
\lim_{n \rightarrow +\infty}u_n = \ell
$$
ou $u_n\rightarrow \ell,$ quand $n\rightarrow+\infty$
```

Intuitivement, $\lim_{n \rightarrow +\infty}u_n = \ell$ signifie que les termes de la suite $(u_n)$ se rapprochent de $l$ toujours plus de $\varepsilon$ lorsque l'indice $n$ augmente indéfiniment.

```{admonition} Définition
Soit $u_n$ une suite réelle.

1. On dit que $(u_n)$ tend vers $+\infty$ (et on écrit $\lim_{n \rightarrow +\infty}u_n =+\infty$) lorsque pour tout $A>0,$ il existe $N\in \mathbb{N}$ tel que pour tout entier $n>N,$ on a 

$$
u_n>A
$$

2. On dit que $(u_n)$ tend vers $-\infty$ (et on écrit $\lim_{n \rightarrow +\infty}u_n =-\infty$) lorsque pour tout $A<0,$ il existe $N\in \mathbb{N}$ tel que pour tout entier $n>N,$ on a 

$$
u_n<A
$$

```
```{admonition} Remarque
:class: tip
Une suite $(u_n)$ est dite convergente si elle admet une limite finie. Dans le cas contraire, elle est divergente.
```

```{admonition} Proposition
:class: seealso
Si une suite est convergente alors sa limite est unique.
```
```{admonition} Preuve
:class: seealso, dropdown
On procède par l'absurde. Soit $(u_n)_{n\in \mathbb{N}}$ une suite convergente ayant deux limites $\ell$ et $\ell',$ $\ell\neq \ell'.$  Choisissons $\varepsilon>0$ tel que $\varepsilon<\dfrac{|\ell-\ell'|}{2}$

Comme $\lim_{n \rightarrow +\infty}u_n=\ell,$ il existe $N_1$ tel que $n\geq N_1$ implique $|u_n-\ell|<\varepsilon.$

De même, $\lim_{n \rightarrow +\infty}u_n=\ell',$ il existe $N_2$ tel que $n\geq N_2$ implique $|u_n-\ell'|<\varepsilon.$

Notons $N=\max(N_1, N_2)$ on a alors pour ce $N :$

$$
|u_N-\ell|<\varepsilon\qquad\mbox{et}\qquad|u_N-\ell'|<\varepsilon
$$

Donc $|\ell-\ell'|=|\ell-u_N+u_N-\ell'|\leqslant |\ell-u_N|+|u_N-\ell'|$  d'après l'inégalité triangulaire. On en tire $|\ell-\ell'|\leqslant\varepsilon+\varepsilon=2\varepsilon<|\ell-\ell'|,$ ce qui est impossible, d'où la contradiction.
```
```{admonition} Exemple
:class: seealso
1. On a 

    $$
    \lim_{n \rightarrow +\infty} \dfrac{1}{\sqrt{n}}=0
    $$

    La suite $(\dfrac{1}{\sqrt{n}})$ est alors une suite convergente et elle converge vers 0.

2. On a

    $$
    \lim_{n \rightarrow +\infty} 1-n^2=-\infty
    $$

    La suite $(1-n^2)$ est donc une suite divergente.
```

```{admonition} Proposition
:class: seealso
Soit $q\in \mathbb{R}^{*}.$ On considère la suite $u_n=q^n,\:n\in \mathbb{N}.$ On a:

1. Si $q\leq-1:$ La suite $(u_n)$ est divergente et n'admet pas de limite, ni finie ni infinie.

2. Si $-1<q<1:$ La suite $(u_n)_n$ est convergente et $\lim_{n \rightarrow +\infty}u_n=0$

3. Si $q>1:$ La suite $(u_n)_n$ est divergente et $\lim_{n \rightarrow +\infty}u_n=+\infty$
```

```{admonition} Proposition
:class: seealso
Soit $(u_n)$ une suite réelle et soit $\ell\in \mathbb{R}.$ On a

$$
\lim_{n \rightarrow +\infty}u_n=\ell\Leftrightarrow \lim_{n \rightarrow +\infty}|u_n-\ell|=0.
$$

```

```{admonition} Exemple
:class: seealso
Soit $(v_n)_{\geq1}$ la suite définie par $v_n=\dfrac{2n-1}{n}.$ On a

$$
\lim_{n \rightarrow +\infty}|v_n-2|=\lim_{n \rightarrow +\infty}|-\dfrac{1}{n}|=\lim_{n \rightarrow +\infty}\dfrac{1}{n}=0
$$

En on déduit que $\lim_{n \rightarrow +\infty}v_n=2.$
```
```{admonition} Proposition (Opérations sur les limites des suites) 
:class: seealso
Soient $(u_n)$ et $(v_n)$ deux suites et soient $\alpha$ et $\beta$ dans $\mathbb{R},$

1. Si $\lim_{n \rightarrow +\infty} u_n=\alpha$ et $\lim_{n \rightarrow +\infty} v_n=\beta,$ alors

    $$
    \lim_{n \rightarrow +\infty}(u_n+v_n)=\alpha+\beta\quad\mbox{et}\quad \lim_{n \rightarrow +\infty}(u_n\times v_n)=\alpha\times \beta
    $$

2. Si $\lim_{n \rightarrow +\infty} u_n=\alpha$ alors pour tout $\lambda\in \mathbb{R}$ on a 

    $$
    \lim_{n \rightarrow +\infty} (\lambda u_n)=\lambda\alpha
    $$

3. Si $\lim_{n \rightarrow +\infty} u_n=\alpha$ et $\alpha\neq0$ alors on a $\lim_{n \rightarrow +\infty}\dfrac{1}{u_n}=\dfrac{1}{\alpha}.$

4. Si $\lim_{n \rightarrow +\infty} u_n=\pm\infty$ alors on a $\lim_{n \rightarrow +\infty}\dfrac{1}{u_n}=0,$

5. Si $\lim_{n \rightarrow +\infty} u_n=\pm\infty$ et $\lim_{n \rightarrow +\infty} v_n=\alpha,$ avec $\alpha\in \mathbb{R}$ alors $\lim_{n \rightarrow +\infty} (u_n+v_n)=\lim_{n \rightarrow +\infty} u_n$

6. Si $\lim_{n \rightarrow +\infty} u_n=\pm\infty$ et $\lim_{n \rightarrow +\infty} v_n=\alpha,$ avec $\alpha\in \mathbb{R}^{+}$ alors $\lim_{n \rightarrow +\infty} (u_n \times v_n)=\lim_{n \rightarrow +\infty} u_n$

7. Si $\lim_{n \rightarrow +\infty} u_n=+\infty$ et $\lim_{n \rightarrow +\infty} v_n=+\infty,$ alors $\lim_{n \rightarrow +\infty} (u_n+v_n)=+\infty$ et $\lim_{n \rightarrow +\infty}(u_n\times v_n)=+\infty.$

8. Si $\lim_{n \rightarrow +\infty} u_n=-\infty$ et $\lim_{n \rightarrow +\infty} v_n=-\infty,$ alors $\lim_{n \rightarrow +\infty} (u_n+v_n)=-\infty$ et $\lim_{n \rightarrow +\infty} (u_n\times v_n)=+\infty.$

9. Si $\lim_{n \rightarrow +\infty} u_n=+\infty$ et $\lim_{n \rightarrow +\infty} v_n=-\infty,$ alors $\lim_{n \rightarrow +\infty} (u_n\times v_n)=-\infty.$

```

```{admonition} Exemple
:class: seealso
1. On a $\lim_{n \rightarrow +\infty}(\dfrac{-2}{\sqrt{n}-3}+3n+1)=+\infty,$ puisque $\lim_{n \rightarrow +\infty}(\dfrac{-2}{\sqrt{n}-3}) =0$ et $\lim_{n \rightarrow +\infty}(3n+1)=+\infty.$

2. On a $\lim_{n \rightarrow +\infty}\dfrac{\dfrac{2}{3n}-5}{1+n+e^n}=0,$ puisque $\lim_{n \rightarrow +\infty}\dfrac{2}{3n}-5=-5$ et $\lim_{n \rightarrow +\infty}1+n+e^n=+\infty.$
```

Parfois on tombe sur l'une des quatres "**formes indéterminées**" suivantes $+\infty-\infty,\;0\times \pm\infty,\;\dfrac{\pm\infty}{\pm\infty},\;\dfrac{0}{0}.$



**Limites usuelles utiles**

- $\lim_{n \rightarrow +\infty} n\sin(\dfrac{1}{n})=\lim_{n \rightarrow +\infty}\dfrac{\sin(\dfrac{1}{n})}{\dfrac{1}{n}}=1,$

- $\lim_{n \rightarrow +\infty}n^2\cos (1-\dfrac{1}{n})=\lim_{n \rightarrow +\infty}\dfrac{\cos(1-\dfrac{1}{n})}{(\dfrac{1}{n})^2}=\dfrac{1}{2},$

- $\lim_{n \rightarrow +\infty} n\ln(1+\dfrac{1}{n})=\lim_{n \rightarrow +\infty}\dfrac{\ln(1+\dfrac{1}{n})}{\dfrac{1}{n}}=1,$

-  $\lim_{n \rightarrow +\infty} n(e^{\dfrac{1}{n}})=1,$

-  $\lim_{n \rightarrow +\infty} \dfrac{(\ln (n))^{\alpha}}{n}=0,$

-  $\lim_{n \rightarrow +\infty} n^{\alpha}e^{-n}=0.$

```{admonition} Proposition
:class: seealso
1. Soient $(u_n)$ et $(v_n)$ deux suites convergentes telles que $\forall n\in \mathbb{N}:\, u_n \leq v_n$ (ou $u_n < v_n$). Alors 

    $$
    \lim_{n \rightarrow +\infty} u_n \leq \lim_{n \rightarrow +\infty} v_n
    $$

2. Soient $(u_n)$ et $(v_n)$ deux suites telles que $\forall n\in \mathbb{N}:\,u_n\leq v_n$ et $\lim_{n \rightarrow +\infty} u_n=+\infty.$ Alors 

    $$
    \lim_{n \rightarrow +\infty} v_n=+\infty
    $$

3. Soient $(u_n)$ et $(v_n)$ deux suites telles que $\forall n\in \mathbb{N}:\,u_n\leq v_n$ et $\lim_{n \rightarrow +\infty} v_n=-\infty.$ Alors 

    $$
    \lim_{n \rightarrow +\infty} u_n=-\infty
    $$

```

```{admonition} Théorème (Théorème des "gendarmes")
:class: seealso
Si $(u_n),$ $(v_n)$ et $(w_n)$ sont trois suites telles que 

$$
\forall n\in \mathbb{N}:\; u_n\leq w_n\leq v_n
$$

et si $\lim_{n \rightarrow +\infty}u_n=\lim_{n \rightarrow +\infty}v_n=\ell,$ alors la suite $(w_n)$ est convergente. De plus on a 

$$
\lim_{n \rightarrow +\infty} w_n=\ell
$$

```

```{admonition} Exemple
:class: seealso
Calculer, à l'aide de Théorème des "gendarmes", la limite suivante 

$$
\lim_{n \rightarrow +\infty}(1+\dfrac{\sin (n)}{n})
$$

```

Toute suite convergente est bornée. La réciproque est fausse: la suite $((-1)^n)$ est bornée mais elle diverge (elle n'admet pas de limite).En revanche, on a le résultat suivant.

```{admonition} Théorème
:class: seealso
1. Toute suite croissante et majorée est convergente.

2. Toute suite décroissante et minorée est convergente.
```
```{admonition} Preuve
:class: seealso, dropdown
On montrera l'assertion "Toute suite convergente est bornée." En effet, soit $(u_n)_{n\in \mathbb{N}}$ une suite convergeant vers le réel $\ell.$ En appliquant la définition de limite avec $\varepsilon=1,$  on obtient qu'il existe un entier naturel $N$ tel que pour $n\geq N$ on ait, $|u_n-\ell|\leq1,$ et donc pour $n\geq N$ on a

$$
|u_n|=|\ell+(u_n-\ell)|\leq |\ell|+|u_n-\ell|\leq |\ell|+1
$$

Donc si on pose $M=\max(|u_0|,|u_1|,...,|u_{N-1}|,|\ell|+1)$

on a alors $\forall n\in \mathbb{N},\,|u_n|\leq M.$
```
# Suites adjacentes

```{admonition} Définition
Deux suites $(u_n)$ et $(v_n)$ sont dites adjacentes si $(u_n)$ est celle qui est croissante, l'autre est décroissante et leur différente et leur différence tend vers 0.
```

```{admonition} Remarque
:class: tip
 Si $(u_n)$ et $(v_n)$ sont deux suites adjacentes et si $(u_n)$ est celle qui croissante (donc $(v_n)$ est décroissante) alors 
 
$$
\forall n\in \mathbb{N}:\; u_n\leq v_n
$$

```

```{admonition} Preuve
:class: seealso, dropdown

On pose :

$$ 
w_n = v_n - u_n 
$$

Etudions le sens de variation de $ (w_n) $:

Pour cela, calculons la différence $ w_{n+1} - w_n $:

$$
\begin{align}
w_{n+1} - w_n &= (v_{n+1} - u_{n+1}) - (v_n - u_n) \\
&= v_{n+1} - u_{n+1} - v_n + u_n \\
&= (v_{n+1} - v_n) + (u_n - u_{n+1})
\end{align}
$$

Comme $ (v_n) $ est décroissante, alors :

$$
v_{n+1} - v_n \leq 0
$$

Et comme $ (u_n) $ est croissante, alors :

$$
u_{n+1} - u_n \geq 0
$$

Donc, $ u_n - u_{n+1} \leq 0 $.

En combinant ces deux inégalités, on a :

$$
w_{n+1} - w_n \leq 0
$$

On en conclut que la suite $ (w_n) $ est décroissante.

De plus, comme $ (w_n) $ converge vers 0 (par définition des suites adjacentes), la suite $ (w_n) $ est positive pour tout $ n \in \mathbb{N} $.

```


Pratiquement, pour montrer que deux suites $(u_n)$ et $(v_n)$ sont adjacentes, on commence par chercher celle qui est plus grande que l'autre. On montre alors que la plus grande est décroissante et que l'autre (la plus petite) est croissante puis on montre que la différence des deux suites converge vers 0.

```{admonition} Exemple
:class: seealso
Les deux suites $(1+\dfrac{1}{n})_{n>0}$ et $(1-\dfrac{1}{n})_{n>0}$ sont adjacentes.
```

```{admonition} Théorème
:class: seealso
Deux suites adjacentes sont convergentes et convergent vers la même limite.
```

```{admonition} Preuve
:class: seealso, dropdown
On montre que les suites $(u_n)$ et $(v_n)$ convergent :

$u_n < v_n <v_0$ car la suite $(v_n)$ est décroissante.

Donc $(u_n)$ est croissante majorée par $v_0$ donc converge.

De même, 
$u_0 < u_n < v_n$ car $(u_n)$ est croissante donc $(v_n)$ est décroissante minorée et convergente.

Montrons qu'elles ont même limite :
On pose $\lim_{n \to +\infty} u_n = L$ et $\lim_{n \to +\infty} v_n = L'$.
On a : $\lim_{n \to +\infty} (v_n - u_n) = 0$ donc $L - L' = 0$ et $L = L'$.


```


```{admonition} Exemple
:class: seealso
On pose $u_n=\sum_{k=1}^{n}\dfrac{1}{k^2},\quad n\in \mathbb{N}^{*}.$

L'objectif de cet exemple est de montrer que la suite $(u_n)_{n\geq1}$ est une suite convergente. Soit $(v_n)_{n\geq1}$ la suite définie par $v_n=u_n+\dfrac{2}{n+1},\quad n\geq1.$

Montrons que les deux suites $(u_n)_{n\geq1}$ $(v_n)_{n\geq1}$ sont adjacentes.

- Remarquons tout d'abord que $u_n\leq v_n,\;n\geq1.$ Montrons alors que $(u_n)_{n\geq1}$ est croissante et que $(v_n)_{n\geq1}$ est décroissante.

On a $\forall n\geq 1:\quad u_{n+1}-u_n=\dfrac{1}{(n+1)^2}.$

Donc $(u_n)_{n\geq1}$ est croissante. Et pour tout $n\geq1$ on a

\begin{eqnarray*}
v_{n+1}-v_n
&=& u_{n+1}+\dfrac{2}{n+2}-u_n-\dfrac{2}{n+1}\\
&=& \dfrac{1}{(n+1)^2}+\dfrac{2}{n+2}-\dfrac{2}{n+1}\\
&=& \dfrac{-n}{(n+1)^2 (n+2)}.
\end{eqnarray*}

Donc $v_{n+1}-v_n\leq0,\;n\geq1.$ Ainsi, la suite $(v_n)_{n\geq1}$ est décroissante.

- On a $\lim_{n \rightarrow +\infty}(v_n-u_n)=\lim_{n \rightarrow +\infty}\dfrac{2}{n+1}=0.$

En on déduit les deux suites $(u_n)_{n\geq1}$ $(v_n)_{n\geq1}$ sont adjacentes. Donc $(u_n)_{n\geq1}$ et $(v_n)_{n\geq1}$ convergent vers la même limite. En particulier, la suite $(u_n)_{n\geq1}$ est convergente.

```

# Suites récurrentes

```{admonition} Définition
Une suite $(u_n)_{n\geq n_0}$ est dite récurrente si elle est définie par son premier terme $u_{n_0}$ et une relation de récurrence de forme

$$
u_{n+1}=f(u_n),\quad\forall n\geq n_0
$$

où $f$ est une fonction définie sur un intervalle $I$ de $\mathbb{R}.$
```

## Exemples remarquables de suites récurrentes

**Suites arithmétiques:**

```{admonition} Définition 

Une suite $(u_n)_{n\geq n_0}$ est dite **arithmétique** si elle est définie par son premier terme $u_{n_0}$ et

$$
\exists r\in \mathbb{R},\;\forall n\geq n_0:\quad u_{n+1}=u_n +r
$$

Dans ce cas, le réel $r$ est appelé la raison de la suite $(u_n)_{n\geq n_0}.$

```

```{admonition} Proposition
:class: seealso
Si $(u_n)_{n\geq n_0}$ est une suite arithmétique de raison $r,$ alors $u_n=u_{n_0}+(n-n_0)r,\, \forall n\geq n_0.$ En particulier, on a 

- si $r>0$:
    
    $$
    \lim_{n \rightarrow +\infty}u_n=+\infty
    $$
 
- si $r<0$:
    
    $$
    \lim_{n \rightarrow +\infty}u_n=-\infty
    $$
    
- si $r=0$:
    
    $$
    \lim_{n \rightarrow +\infty}u_n=u_0
    $$

```

```{admonition} Proposition
:class: seealso
Soit $(u_n)_{n\geq n_0}$ une suite arithmétique de raison $r$,($r\neq0$) et de premier terme $u_{n_0},$ la somme des termes successifs de la suite $(u_n)$ s'exprime par la formule suivante:

$$
u_p+u_{p+1}+...+u_n=(n-p+1)\dfrac{u_p+u_n}{2}=(n-p+1)\dfrac{2u_p+(n-p)r}{2}\;n_0\leq p\leq n
$$

```
**Suites géométriques:**

```{admonition} Définition
Une suite $(u_n)_{n\geq n_0}$ est dite **géométrique** si elle est définie par son premier terme $u_{n_0}$ et

$$
\exists q\in \mathbb{R},\;\forall n\geq n_0:\quad u_{n+1}=qu_n
$$

Dans ce cas, le réel $q$ est appelé la raison de la suite $(u_n)_{n\geq n_0}.$
```

```{admonition} Proposition
:class: seealso
Si $(u_n)_{n\geq n_0}$ est une suite géométrique non nulle de raison $q(q\neq0),$ alors $u_n=u_{n_0}q^{n-n_0},\;\forall n\geq n_0.$ Et en particulier, on a

1. Si $q>1,$ alors $\lim_{n \rightarrow +\infty}u_n=\pm\infty,$

2. Si $-1<q<1,$ alors $\lim_{n \rightarrow +\infty}u_n=0,$

3. Si $q\leq-1,$ la suite $(u_n)_{n\geq n_0}$ diverge.
```

```{admonition} Proposition(Série géométrique)  
:class: seealso

Si $(u_n)_{n\geq n_0}$ est une suite géométrique de raison $q(q\neq1),$ alors

$$
\sum_{k=n_0}^{n}u_k= u_{u_0}\dfrac{1-q^{n-n_0+1}}{1-q},\quad\forall n\geq n_0
$$

```

```{admonition} Exemple
:class: seealso
Soit $(u_n)$ la suite définie par $u_0=1$ et $u_{n+1}=\dfrac{1}{2}u_n, \; n\in \mathbb{N}.$ Donc $(u_n)$ est une suite géométrique de raison $q=\dfrac{1}{2}.$ Le terme général de cette suite est $u_n=\dfrac{1}{2}^n,\,n\in \mathbb{N}.$ Ainsi puisque $-1<\dfrac{1}{2}<1,$ alors $\lim_{n \rightarrow +\infty}u_n=0.$

Pour $n\in \mathbb{N},$ on pose $S_n=\sum_{k=0}^{n}u_k.$ On a alors

$$
S_n=\dfrac{1-\dfrac{1}{2^{n+1}}}{1-\dfrac{1}{2}}=2(1-\dfrac{1}{2^{n+1}})
$$

Autrement dit $1+\dfrac{1}{2}+\dfrac{1}{2^2}+...+\dfrac{1}{2^n}=2(1-\dfrac{1}{2^{n+1}}).$

D'autre part, on a 

$$
\lim_{n \rightarrow +\infty}u_n=2
$$

On écrit alors $\sum_{k=0}^{+\infty}u_k=2$
```

## Convergence d'une suite récurrente

Dans toute la suite, soit $(u_n)_{n\geq n_0}$ une suite récurrente définie par son premier terme et par la relation $u_{n+1}=f(u_n),\,n\geq n_0,$ où $f$ est une fonction numérique donnée.

```{admonition} Théorème
:class: seealso
Soit $f$ une fonction continue sur un intervalle $I$ avec $f(I)\subset I.$ Si $u_{n_0}\in I$ et si la suite récurrente $(u_n)$ est convergente, alors la limite $\ell$ de cette suite est une solution de l'équation $f(x)=x.$
```

Le théorème précédent impose sur la suite $(u_n)_{n\geq n_0}$ d'être convergente. Et si les autres conditions du théorème sont satisfaites, alors la limite de $(u_n)_{n\geq n_0}$ est parmi les solutions de l'équation $f(x)=x.$ En ajoutant une condition supplémentaire sur la fonction $f,$ la convergence de $(u_n)_{n\geq n_0}$ sera alors assurée:

```{admonition} Théorème
:class: seealso
Supposons que $f:[a,b]\rightarrow [a,b]$ une fonction continue et croissante et supposons que $u_{n_0}\in [a,b].$ Alors la suite récurrente $(u_n)$ est monotone et converge vers $\ell\in [a,b]$ vérifiant $f(\ell)=\ell.$
```

```{admonition} Remarque
:class: tip
La monotonie de $(u_n)_{n\geq n_0}$ dans le théorème précédent s'obtienne en comparant seulement les deux premiers termes de la suite $(u_n)_{n\geq n_0}:$

- Si $u_{n_0}\leq u_{n_0+1}$ alors $(u_n)_{n\geq n_0}$ est croissante.

-  Si $u_{n_0}\geq u_{n_0+1}$ alors $(u_n)_{n\geq n_0}$ est décroissante.
```

```{admonition} Exemple
:class: seealso
Soit $(u_n)_{n\in \mathbb{N}}$ la suite définie par: $u_0=\dfrac{1}{3}$ et $u_{n+1}=u_n-u_{n}^{2}.$

On a $u_{n+1}=f(u_n),$ avec $f(x)=x-x^2.$ La fonction $f$ est continue sur $[0,\dfrac{1}{2}]$ et on peut vérifier que $f$ est croissante sur cet intervalle et que $f([0,\dfrac{1}{2}])\subset [0,\dfrac{1}{2}].$

On en déduit que $(u_n)_n$ est monotone: on a $u_0=\dfrac{1}{3}$ et $u_1=2/9,$ donc $u_0> u_1.$ Ainsi $(u_n)_n$ est décroissante. De plus $(u_n)_n$ converge vers $\ell\in [0,\dfrac{1}{2}]$ vérifiant $f(\ell)=\ell.$ Or $f(\ell)=\ell\Leftrightarrow \ell-\ell^2=\ell\Leftrightarrow -\ell^2=0\Leftrightarrow \ell=0.$

Ainsi, on a $\lim_{n \rightarrow +\infty}u_n=0.$
```
