# Propriétés de l'intégrale


```{admonition} Proposition (linéarité)

Soient $f_1, f_2$ deux fonctions continues par morceaux sur $[a, b]$, $\lambda_1, \lambda_2 \in \mathbb R$. Alors :

$$
\int_{[a, b]} (\lambda_1f_1 + \lambda_2f_2) = \lambda_1 \int_{[a, b]} f_1 + \lambda_2 \int_{[a, b]} f_2
$$

```

On dit que l'intégrale est une forme linéaire sur l'espace vectoriel des fonctions continues par morceaux sur $[a, b]$. 



```{admonition} Démonstration
:class: dropdown
 - Soient $\epsilon>0$ et $f$ est une fonction continue par morceaux, alors il existe $\theta$ est fonction en escalier telle que $|f-\theta|\leq \epsilon$. On a $\theta - \epsilon \leq f \leq \theta + \epsilon$. Alors
 
 $$
 \int_{[a, b]} (\theta - \epsilon) \leq  \int_{[a, b]} f \leq  \int_{[a, b]} (\theta + \epsilon)
 $$
 
 et donc

$$
\left|\int_{[a, b]} f- \int_{[a, b]} \theta \right| \leq (b-a)\epsilon
$$

- Maintenant, soient $f_1$ et $f_2$ deux fonctions continues par morceaux sur $[a, b]$, ainsi que $\lambda_1, \lambda_2$ deux réels.

Pour $\epsilon>0$ quelconque, il existe $\theta_1, \theta_2$ deux fonctions en escalier telles que :

$$
|f_1 - \theta_1| \leq \epsilon ~~~ \mbox{ et } ~~~ |f_2 - \theta_2| \leq \epsilon
$$


Ce qui entraine 

$$
\left|\int_{[a, b]} f_1- \int_{[a, b]} \theta_1 \right| \leq (b-a)\epsilon
$$

et 

$$
\left|\int_{[a, b]} f_2- \int_{[a, b]} \theta_2 \right| \leq (b-a)\epsilon
$$

Donc

$$
|\lambda_1|\left|\int_{[a, b]} f_1- \int_{[a, b]} \theta_1 \right| \leq |\lambda_1|(b-a)\epsilon
$$

et 

$$
|\lambda_2|\left|\int_{[a, b]} f_2- \int_{[a, b]} \theta_2 \right| \leq |\lambda_2|(b-a)\epsilon
$$

Donc (puisque l'intégrale sur les fonctions en escalier est linéaire)

$$
\left|\lambda_1\int_{[a, b]} f_1- \int_{[a, b]} \lambda_1\theta_1 \right| \leq |\lambda_1|(b-a)\epsilon
$$

et 

$$
\left|\lambda_2\int_{[a, b]} f_2- \int_{[a, b]} \lambda_2\theta_2 \right| \leq |\lambda_2|(b-a)\epsilon
$$

Par suite

$$
\left|\lambda_1\int_{[a, b]} f_1 +\lambda_2\int_{[a, b]} f_2 - \left(\int_{[a, b]} \lambda_1\theta_1 + \int_{[a, b]} \lambda_2\theta_2\right)\right| \leq (|\lambda_1|+|\lambda_2|)(b-a)\epsilon
$$


On pose 

$$
f= \lambda_1 f_1 + \lambda_2 f_2 ~~ \mbox{ et } \theta = \lambda_1 \theta_1 + \lambda_2 \theta_2
$$

On a 

$$
|f-\theta| \leq |\lambda_1||f_1-\theta_1| + |\lambda_2||f_2 - \theta_2| \leq (|\lambda_1|+|\lambda_2|)\epsilon
$$


Et par suite

$$
\left|\int_{[a, b]} f- \int_{[a, b]} \theta \right| \leq (b-a)(|\lambda_1|+|\lambda_2|)\epsilon
$$

On pose 

$$
I = \int_{[a, b]} \theta = \int_{[a, b]} \lambda_1\theta_1 + \int_{[a, b]} \lambda_2\theta_2
$$

et 

$$
\Delta = \left|\int_{[a, b]} f- \left(\lambda_1\int_{[a, b]} f_1 +\lambda_2\int_{[a, b]} f_2\right)\right|
$$

Alors 

$$
\begin{aligned}
\Delta &=& \left|\int_{[a, b]} f- I + I - \left(\lambda_1\int_{[a, b]} f_1 +\lambda_2\int_{[a, b]} f_2\right)\right| \\ \\
& \leq & \left|\int_{[a, b]} f- I\right| + \left| I - \left(\lambda_1\int_{[a, b]} f_1 +\lambda_2\int_{[a, b]} f_2\right)\right| \\ \\
& \leq & 2(b-a)(|\lambda_1|+|\lambda_2|)\epsilon
\end{aligned}
$$

On en déduit 

$$
\forall \epsilon >0, \Delta \leq 2(b-a)(|\lambda_1|+|\lambda_2|)\epsilon
$$

Ce qui prouve que $\Delta =0$ et donc

$$
 \left|\int_{[a, b]} f = \lambda_1\int_{[a, b]} f_1 +\lambda_2\int_{[a, b]} f_2\right|
$$


```

Deux fonctions continues par morceaux sur l'intervalle $[a. b]$  qui sont égales sauf en un nombre fini de points ont la même intégrale car leur différence, qui est nulle sauf
en un nombre fini de points, est une fonction en escalier dont l'intégrale est nulle.


```{admonition} Proposition (relation de Chasles)

Soit $c \in [a, b]$ et $f$ une fonction définie sur $[a, b]$. 

La fonction $f$ est continue par morceaux sur $[a, b]$ si, et seulement si, ses
restrictions à $[a, c]$ et à $[c, b]$ sont continues par morceaux, et l'on a alors :

$$
\int_{[a, b]} f = \int_{[a, c]} f_{|[a, c]}  + \int_{[c, b]} f_{|[c, b]}
$$

```


```{admonition} Démonstration
:class: dropdown
 
Soit $\varphi \in \mathcal E^-(f)$ (une fonction en escalier plus petite que $f$).

On a $\varphi_{|[a, c]} \in \mathcal E^-(f_{|[a, c]})$ et $\varphi_{|[c, b]} \in \mathcal E^-(f_{|[c, b]})$.

Par suite 

$$
\begin{aligned}
\int_{[a, b]}\varphi &=& \int_{[a, c]} \varphi_{|[a, c]} + \int_{[c, b]} \varphi_{|[c, b]} \\ \\
&\leq& \int_{[a, c]} f_{|[a, c]} + \int_{[c, b]} f_{|[c, b]}
\end{aligned}
$$


Le réel $\int_{[a, c]} f_{|[a, c]} + \int_{[c, b]} f_{|[c, b]}$ est un majorant de de $\left\{\int_{[a, b]}\varphi ~~|~~ \varphi \in \mathcal E^-(f) \right\}$.

Donc il est plus grands que sa borne supérieure ($\int_{[a, b]} f$).
Ce qui donne

$$
\int_{[a, b]} f \leq \int_{[a, c]} f_{|[a, c]} + \int_{[c, b]} f_{|[c, b]}
$$

En applique les mêmes étapes pour $-f$


Soit $\varphi \in \mathcal E^-(-f)$ (une fonction en escalier plus petite que $-f$).

On a $\varphi_{|[a, c]} \in \mathcal E^-(-f_{|[a, c]})$ et $\varphi_{|[c, b]} \in \mathcal E^-(-f_{|[c, b]})$.

Par suite 

$$
\begin{aligned}
\int_{[a, b]}\varphi &=& \int_{[a, c]} \varphi_{|[a, c]} + \int_{[c, b]} \varphi_{|[c, b]} \\ \\
&\leq& \int_{[a, c]} -f_{|[a, c]} + \int_{[c, b]} -f_{|[c, b]}
\end{aligned}
$$


Le reel $\int_{[a, c]} -f_{|[a, c]} + \int_{[c, b]} -f_{|[c, b]}$ est un majorant de de $\left\{\int_{[a, b]}\varphi ~~|~~ \varphi \in \mathcal E^-(-f) \right\}$.

Donc il est plus grands que sa borne supérieure ($\int_{[a, b]} -f$).
Ce qui donne

$$
\int_{[a, b]} -f \leq \int_{[a, c]} -f_{|[a, c]} + \int_{[c, b]} -f_{|[c, b]}
$$

Et d'après la linéarité de l'intégrale nous avons

$$
\int_{[a, b]} f \geq \int_{[a, c]} f_{|[a, c]} + \int_{[c, b]} f_{|[c, b]}
$$


En fin

$$
\int_{[a, b]} f = \int_{[a, c]} f_{|[a, c]} + \int_{[c, b]} f_{|[c, b]}
$$
```

**Remarque**:

Soient $f$ une fonction continue par morceaux sur $[a, b]$, et $u=(x_i)_{i\in\{1,\ldots,n\}}$ une subdivision adaptée à $f$. Pour $i \in \{1,\ldots,n\}$, notons $f_i$ la fonction continue sur $[x_{i-1}, x_i]$ tel que $\forall x \in ]x_{i-1}, x_i[, f_i(x) = f(x)$. Alors d'après la relation de Chasles :

$$
\int_{[a, b]} f = \sum_{i=1}^n \int_{[x_{i-1}, x_i]}f = \sum_{i=1}^n \int_{[x_{i-1}, x_i]}f_i
$$

## Quelques inégalités


```{admonition} Proposition
- Une fonction positive et continue par morceaux à une intégrale positive.
- Si $f$ et $g$ sont deux fonctions continues par morceaux sur $[a, b]$ alors:

$$
f \leq g \Rightarrow \int_{[a, b]}f \leq \int_{[a, b]}g 
$$

```

```{admonition} Démonstration
:class: dropdown
- Si $f$ est une fonction continue par morceaux et positive alors la fonction nulle (qui constante donc en escalier) appartient à $\mathcal E^-(f)$. Donc son intégrale (qui vaut 0) est inférieure à l'intégrale de $f$. Par suite $\int_{[a, b]} f \geq 0$.
- On applique le résultat précèdent à $g-f$ puis on utilise la linéarité de l'intégrale.
```

```{admonition} Théorème

Si $f$ est continue par morceaux sur $[a, b]$, alors $|f|$ est continue par morceaux sur $[a, b]$ et:

$$
\left |\int_{[a, b]}f \right | \leq \int_{[a, b]}|f|
$$

```
```{admonition} Démonstration
:class: dropdown
 
Soient $f$ une fonction continue par morceaux sur $[a, b]$ et $u=(x_i)_{i=0}^n$ une subdivision adaptée à $f$. Alors, pour tout $i \in \{1, \ldots, n\}$ la restriction de $f$ sur chacun des intervalles $]x_{i-1}, x_i[$ est continue et admet des limites finies en $x_{i-1}$ et $x_i$. Il en est de même pour $|f|$ d'après les propriétés des limites. Donc $|f|$ est une fonction continue par morceaux sur $[a, b]$.


Nous avons $-|f| \leq f \leq |f|$ donc

$$
- \int_{[a, b]}|f| \leq \int_{[a, b]}f \leq \int_{[a, b]}|f|  
$$

Ce qui veut dire 

$$
\left| \int_{[a, b]}f \right | \leq \int_{[a, b]}|f|  
$$

```

```{admonition} Proposition (Inégalité de la moyenne)
Si $f$ et $g$ sont deux fonctions continues par morceaux sur $[a, b]$, alors:

$$
\left |\int_{[a, b]}fg \right | \leq \sup_{[a, b]} |f| \int_{[a, b]}|g|
$$

```

```{admonition} Démonstration
:class: dropdown
Soit $M = sup_{[a,b]}|f|$.
Nous avons 

$$
\forall x \in [a, b], |f(x)g(x)|=|f(x)||g(x)| \leq M |g(x)|
$$

Donc 

$$
\left |\int_{[a, b]}fg \right | \leq \int_{[a, b]}|fg| \leq \int_{[a, b]}M|g| =M\int_{[a, b]}|g|
$$
```


```{admonition} Corollaire

Si $f$ est une fonction continue par morceaux sur $[a, b]$, alors:

$$
\left |\int_{[a, b]}f \right | \leq (b-a)  \sup_{[a, b]}|f|
$$

```

```{admonition} Démonstration
:class: dropdown
 
En pose $g=1$ est on applique l'inégalité de la moyenne.
```

```{admonition} Théorème (Inégalité de Cauchy-Schwarz)
Si $f$ et $g$ sont deux fonctions continues par morceaux sur $[a, b]$, alors:

$$
\left (\int_{[a, b]}fg \right ) ^2 \leq \int_{[a, b]} f^2 \int_{[a, b]}g^2
$$

```

```{admonition} Démonstration
:class: dropdown
 
On pose 

$$
P(\lambda) = \int_{[a, b]} (f+\lambda g)^2 = \lambda^2 \int_{[a, b]} g^2 + 2\lambda \int_{[a, b]} fg + \int_{[a, b]} f^2
$$


$P$ est donc une fonction polynomiale de degré au plus égale à 2 qui est positive pour tout $\lambda \in \mathbb R$.

- Si $\int_{[a, b]} g^2 = 0$, alors la fonction $P$ ne peut pas changer de signe (car elle est positive) donc ne peut pas être de degré 1. On en déduit $\int_{[a, b]} fg = 0$

Donc $\left (\int_{[a, b]} fg\right)^2 = 0=\int_{[a, b]} f^2 \int_{[a, b]} g^2$

- Sinon, $P$ est polynôme de degré 2 qui positif pour tout $\lambda \in \mathbb R$. Son discriminent 

$$
\Delta = 4 \left (\left (\int_{[a, b]} fg\right)^2- \int_{[a, b]} f^2 \int_{[a, b]} g^2 \right)
$$
est donc negatif. Ce donne

$$
\left (\int_{[a, b]} fg\right)^2 \leq \int_{[a, b]} f^2 \int_{[a, b]} g^2
$$

```

On peut écrire l'inégalité de Cauchy-Schwarz comme suit :

$$
\left |\int_{[a, b]}fg \right | \leq \left (\int_{[a, b]} f^2 \right)^{\frac{1}{2}}  \left (\int_{[a, b]}g^2\right)^{\frac{1}{2}} 
$$


## Cas des fonctions continues

```{admonition} Théorème
Une fonction **continue et positive** sur $[a, b]$ est nulle si, et seulement si, son intégrale sur $[a, b]$ est nulle.
```

```{admonition} Démonstration
:class: dropdown

Soit $f$ une fonction continue et positive sur $[a, b]$.

Si $f$ est nulle alors son intégrale est nulle.

Montrons maintenant, que si l'intégrale de $f$ est nulle alors $f$ est la fonction nulle.

Par absurde, on suppose que $f$ n'est pas nulle. Donc il existe (au moins) $c \in [a, b]$ tel que $f(c) \neq 0$ et puisque $f$ est positive $f(c) > 0$.

1- Si $c \in ]a, b[$. Puisque la fonction est continue en $c$ alors pour tout $\epsilon >0$ il existe $\alpha > 0$ tel que $\forall x \in [a, b],~~ |x-c| \leq \alpha \Rightarrow |f(x) - f(x)|\leq \epsilon$.

On pose $\epsilon = \dfrac{f(x)}{2}$

alors il existe $\alpha>0$ tel que pour tout $x\in [a, b], ~~ x \in ]c-\alpha, c +\alpha[ \Rightarrow f(x)\leq f(c)-\epsilon > 0$.

On pose $\beta = max(\dfrac{a+c}{2}, c-\alpha), \gamma = max(\dfrac{b+c}{2}, c+\alpha)$. On a

$$
\begin{aligned}
\int_{[a, b]}f &= \int_{[a, \beta]}f + \int_{[\beta, \gamma]}f + \int_{[\gamma, b]}f \\ \\
&\geq  \int_{[\beta, \gamma]}f \\ \\
&\geq  (\gamma -\beta )\dfrac{f(c)}{2}> 0
\end{aligned}
$$

2- Si $c =a$ ou $c=b$. La fonction $f$ est continue en $c$ et $f(c)>0$. Donc elle est strictement positive au voisinage de $c$. Ceci dit, il existe un réel $d \in ]a, b[$ tel f(d)>0. On répète les mêmes étapes précédentes mais cette fois avec $d$ et on aboutit a $\int_{[a, b]}f >0$

Ce qui est absurde.

Donc $f$ est nulle.


```

```{warning} 
 
Les deux hypothèses (continuité et positivité) sont nécessaires pour que le résultat soit vrai.


```

```{admonition} Corollaire
Si $f$ et $g$ sont deux fonctions continues sur $[a, b]$, alors:

$$
\left (\int_{[a, b]}fg \right ) ^2 = \int_{[a, b]} f^2 \int_{[a, b]}g^2
$$

Si et seulement si, $f$ et $g$ sont proportionnelles.
```

```{admonition} Démonstration
:class: dropdown

- Si $f$ et $g$ sont proportionnelles, donc il existe $\lambda \in \mathbb R$ tel que $f=\lambda g$ où  $g=\lambda f$. Supposons par exemple que $f=\lambda g$.

Alors, 

$$
\left(\int_{[a, b]} fg \right)^2 = \lambda^2\left(\int_{[a, b]} g^2\right)^2 = \int_{[a, b]} f^2\int_{[a, b]} g^2
$$

Supposons maintenant que 

$$
\left (\int_{[a, b]}fg \right ) ^2 = \int_{[a, b]} f^2 \int_{[a, b]}g^2
$$

On pose 

$$
P(\lambda) = \int_{[a, b]}(f+\lambda g)^2 = \lambda^2\int_{[a, b]}g^2 + 2\lambda \int_{[a, b]}fg + \int_{[a, b]}f^2
$$

* $si \int_{[a, b]}g^2 = 0$ alors $g^2$ est nulle (puisqu'elle est continue est positive avec intégrale nulle) donc $g$ est nulle. Donc $g= 0\times f$. Par suite $f$ et $g$ sont proportionnelles.

* sinon, le polynôme $P$ a un discriminent nul. Donc il existe $\lambda_0$ tel que $P(\lambda_0)=0$.

Donc $P(\lambda_0) = \int_{[a, b]}(f+\lambda_0 g)^2 = 0$. La fonction $(f+\lambda_0 g)^2$ est continue et positive avec intégrale nulle donc elle est nulle. Par suite $f=\lambda_0 g$. Les deux fonctions sont proportionnelles.
```
## Invariance par translation 


```{admonition} Proposition
Soient $f$ une fonction continue par morceaux sur $[a, b]$ et $\alpha$ un réel.
La fonction $f_\alpha$ définie sur $[a+\alpha, b+\alpha]$ par $f_\alpha(x)f(x-\alpha)$ est continue par morceaux sur $[a+\alpha, b+\alpha]$. De plus :


$$
\int_{[a, b]}f= \int_{[a+\alpha, b+\alpha]} f_{\alpha}
$$

```

```{admonition} Démonstration
:class: dropdown
 
On va dabord montrer le resultat pour une fonction en escalier pouis, pour une fonction continue par morceaux.

- Si $f$ est une fonction en escalier sur $[a, b]$:

soit $u=(x_i)_{i=0}^n$ une subdivision adaptee a $f$. Alors on peut facilement montrer que la famille $(y_i)_{i=0}^n$ avec $y_i = x_i +\alpha$ est une subdivision de $[a+\alpha, b+\alpha]$.

Si $f$ prend la valeur $c_i$ sur $]x_{i-1}, x_i[$ alors $f_\alpha$ vaut aussi $c_i$ sur $]x_{i-1}+\alpha,  x_i+\alpha[$. Donc $f_\alpha$ est une fonction en escalier sur $[a+\alpha, b+\alpha]$.

De plus, 

$$
\int_{[a+\alpha, b+\alpha]} f_\alpha = \sum_{i=1}^n (y_i - y_{i-1})c_i = \sum_{i=1}^n (x_i - x_{i-1})c_i = \int_{[a, b]} f
$$


Maintenant si $f$ est continue par morceaux, 

soit $u=(x_i)_{i=0}^n$ une subdivision adaptee a $f$. La famille $(y_i)_{i=0}^n$ avec $y_i = x_i +\alpha$ est une subdivision de $[a+\alpha, b+\alpha]$.

$f$ est continue sur $]x_{i-1}, x_i[$ est admet des limites finies en $x_{i-1}$ et $x_{i}$. Donc, $f_\alpha$ est continue sur $]y_{i-1}, y_i[=]x_{i-1}+\alpha, x_i+\alpha[$ est admet des limites finies en $y_{i-1}$ et $y_{i}$. Donc  $f_\alpha$ est continue par morceaux sur $[a+\alpha, b+\alpha]$.

si $\varphi \in \mathcal E^-(f)$ donc $\varphi \leq f$ donc $\varphi_\alpha  \leq f_\alpha$

donc $\left\{\varphi_\alpha ~~ | ~~ \varphi \in \mathcal E^-(f) \right\} \subset \mathcal E^-(f_\alpha)$

D'autre part, si $\psi \in  \mathcal E^-(f_\alpha)$ donc il existe $\phi \in  \mathcal E^-(f)$ telle que $\psi = \varphi_\alpha$.

Donc, $\mathcal E^-(f_\alpha)= \left\{\varphi_\alpha ~~ | ~~ \varphi \in \mathcal E^-(f) \right\}$

Par suite

$$
\begin{aligned}
\int_{[a+\alpha, b+\alpha]} f_{\alpha} &= sup \left\{\int_{[a+\alpha, b+\alpha]} \psi ~~| ~~ \psi \in \mathcal E^-(f_\alpha) \right\} \\ \\
&= sup \left\{\int_{[a+\alpha, b+\alpha]} \varphi_\alpha ~~| ~~ \varphi \in \mathcal E^-(f) \right\} \\ \\
&= sup \left\{\int_{[a, b]} \varphi ~~| ~~ \varphi \in \mathcal E^-(f) \right\} = \int_{[a, b]} f
\end{aligned}
$$

```

Soient $T>0$ et $f$ une fonction $T$-périodique et continue par morceaux sur une période et donc sur tout segment de $\mathbb R$. Nous avons :

$$
\forall a \in \mathbb R, \int_{[a, a+ T]} f = \int_{[0, T]}f
$$
