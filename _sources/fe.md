# Intégrale des fonctions en escalier

$a$ et $b$ désignent deux réels tels que $a < b $. Toutes    les fonctions sont supposées définies sur $[a, b]$ et a valeurs réelles.
Le but de l'intégration est de définir un nombre qui, pour une fonction $f$ positive sur un segment $[a, b]$ , mesure l'aire délimitée par sa courbe représentative, l'axe des abscisses et les deux droites d'équations $x = a$ et $x = b$.
Ce nombre sera appelé intégrale de $f$ sur $[a, b]$ et notée : 

$$
\int_a^b f(x)dx
$$


## Subdivision d'un segment


```{admonition} Définition 1
* On appelle subdivision de $[a, b]$ toute famille $u=(x_i)_{i=0}^n$ telle que $n \in \mathbb{N}^\star$ et 

$$
a=x_0 < x_1 < \ldots < x_n=b
$$

* On appelle pas ou module de la subdivision $u=(x_i)_{i=0}^n$, le reel 

$$
\delta(u)=\max_{i \in [1, n]}(x_i - x_{i-1})
$$
```
```{admonition} Exemple
Une subdivision $(x_i)_{i=0}^n$ ou $n$ un entier naturel non nul est dite a pas constant si:

$$
\forall i \in \{0, \ldots, n\}, x_i = a+i\dfrac{b-a}{n}
$$

Son module est $\dfrac{b-a}{n}$
```


```{admonition} Définition 2
Si $u$ et $v$ sont deux subdivisions de $[a, b]$ , on dit que $u$ est plus fine que $v$ si tout élément de $v$ est élément de $u$.
```




```{admonition} Proposition 1
Pour toutes subdivisions $u$ et $v$ de $[a, b]$ il existe une subdivision plus fine que  $u$ et $v$.
```

## Fonctions en escalier


```{admonition} Définition 3


Une fonction $\varphi$ de $[a,b]$ dans $\mathbb{R}$ est dite en escalier si l'on peut trouver une subdivision $u=(x_i)_{i=0}^n$ de $[a, b]$ telle que $\varphi$ soit constante sur chacun des intervalles $]x_{i-1}, x_i[, (1\leq i \leq n)$.
La subdivision $u$ est dite adaptée à la fonction $\varphi$. 

```


```{admonition} Exemples


- Une fonction constante sur l’intervalle $[a,b]$ est une fonction en escalier sur $[a,b]$.
- La fonction _partie entière_ est une fonction en escalier sur segment $[a,b]$ (pensez à une subdivision adaptée!).

```

**Remarques**:

1. Une fonction en escalier prend un nombre fini de valeurs. En particulier, elle est bornée.
2. Si $u$ est une subdivision adaptée à une fonction $\varphi$ en escalier, alors toute subdivision plus fine que $u$ est adaptée à $\varphi$.
3. Si $\varphi$ et $\psi$ sont deux fonctions en escalier sur $[a. b]$, alors il existe une subdivision adaptée à $\varphi$ et $\psi$.


```{admonition} Proposition 2
L'ensemble des fonctions en escalier sur $[a, b]$ est un sous-espace vectoriel de l'espace des fonctions définies sur $[a, b]$
```


```{admonition} Démonstration
:class: dropdown

Soient $\varphi$ et $\psi$ deux fonctions en escalier sur $[a, b]$.

Soient $\lambda$ et $\mu$ deux réels.

D'après la proposition 1 il existe une subdivision $u=(x_i)_{i=0}^n$ adaptées à $\varphi$ et $\psi$.
Donc les deux fonctions sont constantes sur $]x_{i-1}, x_{i}[$
Il en est de même pour $\lambda \varphi + \mu \psi$ (constante sur $]x_{i-1}, x_{i}[$).
Donc, $u$ est une subdivision adaptée pour $\lambda \varphi + \mu \psi$ qui est par la suite une fonction en escalier.

Les autres conditions sont faciles à vérifier !
```

## Intégrale d'une fonction en escalier




```{admonition} Proposition 3
Soit $\varphi$ une fonction en escalier sur $[a, b]$ et $u=(x_i)_{i=0}^n$ une subdivision  adaptées à $\varphi$. Soit $c_i$ la valeur prise par $\varphi$ sur $]x_{i-1}, x_i[$ pour $i \in \{1, \ldots, n\}$ (i.e $\varphi(x)=c_i$ pour tout $x \in ]x_{i-1}, x_i[$). Alors la quantité

$$
\sum_{i=1}^nc_i(x_i-x_{i-1})
$$

ne dépend pas de la subdivision choisie.

Cette quantité s'appelle `l'intégrale` de $\varphi$ sur  $[a, b]$ et on le note:

$$
\int_a^b \varphi(x)dx=\int_{[a, b]}\varphi
$$
```


```{admonition} Démonstration
:class: dropdown

Pour toute $u$ une subdivision adaptée à la fonction $\varphi$, on note 

$$
I(\varphi, u)= \sum_{i=1}^nc_i(x_i-x_{i-1})
$$

Le but est de montrer que $\forall u, v$ subdivision adaptée à $\varphi$, $I(\varphi, u)=I(\varphi, v)$

- Si $v$ est plus fine que $u$,
Elle est obtenue en rajoutant un nombre fini d'éléments à la subdivision $u$. Pour démontrer que $I(\varphi, u)=I(\varphi, v)$, il suffit de le démontrer dans le cas où  $v$ a un élément de plus que $u$.


Soit donc $u=(x_i)_{i=0}^n$ et $v=(x_1, \ldots, x_p, y, x_{p+1}, \ldots, x_n)$

Il est claire que la fonction $\varphi$ sur $]x_p, y[$ et $]y, x_{p+1}[$. Donc :


$$
\begin{aligned}
I(\varphi, v) & =  \sum_{i=1}^{p-1}c_i(x_i-x_{i-1})+c_p(y-x_p) + c_p(x_{p+1}-y) + \sum_{i=p+2}^{n}c_i(x_i-x_{i-1})  \\ \\
 & =  \sum_{i=1}^{n}c_i(x_i-x_{i-1}) = I(\varphi, u) 
\end{aligned}
$$

- Dans le cas général:

D'après la proposition 1, il existe une subdivision $w$ plus fine que $u$ et $v$, cette subdivision est aussi adaptée à $\varphi$ (remarque 2).
Donc on aura d'une part $I(\varphi, w)=I(\varphi, u)$ et d'autre part $I(\varphi, w)=I(\varphi, v)$.

Par conséquent, 

$$
I(\varphi, v)=I(\varphi, u)
$$

```

## Propriétés de l'intégrale des fonctions en escalier
 

```{admonition} Proposition 4
Montrer que :

1- pour toutes fonctions en escalier sur $[a, b]$ $\varphi$ et $\psi$, et pour tous réels $\alpha$ et $\beta$ nous avons:

$$
\int_{[a, b]}\alpha\varphi + \beta\psi = \alpha\int_{[a, b]}\varphi + \beta\int_{[a, b]}\psi
$$

2- une fonction en escalier positive a une intégrale positive.

3- si  $\varphi$ et $\psi$ sont deux fonctions en escalier sur $[a, b]$ alors:

$$
\varphi \leq \psi \Rightarrow  \int_{[a, b]}\varphi \leq \int_{[a, b]}\psi
$$

```


```{admonition} Démonstration
:class: dropdown
1-

Soient $\varphi$ et $\psi$ deux fonctions en escalier sur $[a, b]$ et $\alpha$ et $\beta$ deux réels.

Soit $u=(x_i)_{i=0}^n$ une subdivision adaptée à  $\varphi$ et $\psi$. Si, pour $i \in \{1, \ldots, n\}$, $c_i$ et $d_i$ sont respectivement les valeurs prises par $\varphi$ et $\psi$ sur $]x_{i-1}, x_i[$ alors $\alpha\varphi + \beta\psi$ est une fonction en escalier qui prend $\alpha c_i + \beta d_i$ sur $]x_{i-1}, x_i[$.

Nous avons donc,


$$
\begin{aligned}
\int_{[a, b]}\alpha\varphi + \beta\psi & = \sum_{i=1}^{n}(\alpha c_i + \beta d_i)(x_i-x_{i-1})   \\ \\
 & =  \alpha\sum_{i=1}^{n} c_i(x_i-x_{i-1}) +  \alpha\sum_{i=1}^{n} d_i(x_i-x_{i-1}) \\ \\
 & = \alpha\int_{[a, b]}\varphi + \beta\int_{[a, b]}\psi
\end{aligned}
$$

2- 

Soit $\varphi$ une fonction en escalier sur $[a, b]$ qui est positive et  $u=(x_i)_{i=0}^n$ une subdivision adaptée à $\varphi$. Puisqu’elle est positive, les valeurs $c_i$ prise par $\varphi$ sont positives. D'autre part, puisque pour tout $i \in \{1, \ldots, n\}, x_{i-1} \leq x_i$ (par définition de la subdivision) alors $\int_{[a, b]}\varphi = \sum_{i=1}^{n} c_i(x_i-x_{i-1}) \geq 0$.

3-

La fonction $\varphi - \psi$ est une fonction en escalier positive donc son intégral est positive.

```


```{admonition} Proposition 5
Une fonction $\varphi$ est en escalier sur $[a, b]$ si et seulement si pour tout $c \in ]a, b[$, ses restrictions sur $]a, c[$ et $]c, b[$ le sont. Le cas échéant,

$$
\int_{[a, b]}\varphi = \int_{[a, c]}\varphi_{|[a, c]} + \int_{[c, b]}\varphi_{|[c, b]}
$$



```


```{admonition} Démonstration
:class: dropdown

- $\Rightarrow$
    Soit $\varphi$ une fonction en escalier sur $[a, b]$ et $u$ une subdivision adaptée à $\varphi$. On ajoutant $c$ a la subdivision $u$ on obtient un subdivision $v=(x_i)_{i=0}^n$ qui est encore adaptée à $\varphi$. Soit $p$ l'entier naturel tel que $c=x_p$. Alors nous avons :
    * $(x_1, \ldots, x_p)$ une subdivision de  $[a, c]$ et puisque $\varphi$ est constante sur chaque $]x_{i-1}, x_{i}[$ donc $\varphi_{|[a, c]}$ est fonction en escalier sur $[a, c]$. Nous avons donc :

    $$
    \int_{[a, c]}\varphi_{|[a, c]} = \sum_{i=1}^{p} c_i(x_i-x_{i-1})
    $$

    * $(x_{p+1}, \ldots, x_n)$ une subdivision de  $[c, b]$ et puisque $\varphi$ est constante sur chaque $]x_{i-1}, x_{i}[$ donc $\varphi_{|[c, b]}$ est fonction en escalier sur $[c, b]$. Nous avons donc :

    $$
    \int_{[c, b]}\varphi_{|[c, b]} = \sum_{i=p+1}^{n} c_i(x_i-x_{i-1})
    $$

    Par suite :

    $$
    \begin{aligned}
    \int_{[a, b]}\varphi &= \sum_{i=1}^{n} c_i(x_i-x_{i-1})=\sum_{i=1}^{p} c_i(x_i-x_{i-1}) + \sum_{i=p+1}^{n} c_i(x_i-x_{i-1}) \\ \\ 
     &= \int_{[a, c]}\varphi_{|[a, c]} + \int_{[c, b]}\varphi_{|[c, b]}
    \end{aligned}
    $$


* $\Leftarrow$
Supposons que $\varphi_{|[a, c]}$ et $\varphi_{|[c, b]}$ sont en escalier sur $[a, c]$ et $[c, b]$ respectivement.

Soit $u=(x_i)_{i=0}^p$ (respectivement $v= (x_i)_{i=0}^q$) une subdivision de $[a, c]$ (respectivement de $[c, b]$) adaptée à $\varphi_{|[a, c]}$ (respectivement q $\varphi_{|[c, b]}$). 

Alors, $(x_0, \ldots, x_{p-1}, x_p=c=y_1, \ldots, y_q)$ est une subdivision $[a, b]$. De plus $\varphi$ est constante sur chaque intervalle $]x_{i-1}, x_{i}[$ et $]y_{i-1}, y_{i}[$. Donc $\varphi$ est en escalier sur $[a, b]$.

```

