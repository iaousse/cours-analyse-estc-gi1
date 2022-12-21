# Calcul intégral
## Intégrale de Riemann
**a) Subdivision**

Soit $[a,b]$ un intervalle de $\mathbb{R},\,a<b.$ Divisons $[a,b]$ en $n$ intervalles à l'aide d'une suite strictement croissante de réels $x_i\,(1\leq i\leq n)$ tel que:

$$
a=x_0<x_1<x_2<...<x_{n-1}<x_n=b
$$

La suite finie $d=\{x_0,x_1,...,x_n\}$ est appelée subdivision de $[a,b].$

Le nombre $\delta(d)=\sup_{1\leq k\leq n}|x_k-x_{k-1}|$ s'appelle module ( ou le pas) de la subdivision $d.$

**b) Sommes de Darboux**

Soit $f$ une fonction réelle définie et bornée sur $[a,b]$

Si $d$ est la subdivision $\{x_0,x_1,...,x_n\},$ la restriction de $f$ sur $[x_{k-1},x_k]$ (est aussi bornée pour tout $k\in\{1,2,...,n\}$), on note $M_k=\sup _{[x_{k-1},x_k]}f$ et $m_k=\inf_{[x_{k-1},x_k]}f$

On pose $S(f,d)=\sum_{k=1}^{n}M_k (x_k-x_{k-1})$ et $s(f,d)=\sum_{k=1}^{n}m_k (x_k-x_{k-1})$

$S(f,d)$ (resp. $s(f,d)$) s'appelle somme de Darboux supérieure (resp. inférieure) de $f$ relativement à la subdivision $d.$

On a les propriétés suivantes:

i) $s(f,d)\leq S(f,d)$ pour toute subdivision $d$ de $[a,b],$

ii) Si $d$ et $d'$ sont deux subdivisions quelconques de $[a,b]$ alors $s(f,d)\leq S(f,d').$

```{admonition} Remarque

Si $\delta(d)$ est assez petit, la différence $S-s$ peut être rendue aussi petite que l'on veut.
```

**c) Fonctions intégrables:**

Soit $f$ une fonction bornée sur $[a,b].$ On note $M=\sup_{x\in [a,b]}f(x)$ et $m=\inf_{x\in [a,b]}f(x).$

```{admonition} Lemme
Soit $D$ l'ensemble des subdivisions de $[a,b].$ Alors $\mathcal{S}=\{S(f,d)\,\mbox{\,où\,}d\in D\}$ est minorée par $m(b-a)$ et on note $I(f)=\inf_{d\in D}S(f,d)$

$\mathcal{S}=\{S(f,d)\,\mbox{\,où\,}d\in D\}$ est majorée par $M(b-a)$ et on note $i(f)=\sup_{d\in D}s(f,d).$ On a :$i(f)\leqslant I(f)$

```

```{admonition} Théorème (Theorem de Darboux)

Soient $d$ une subdivision de $[a,b]$ et $\delta(d)$ son module. Alors:

(i) $\forall\varepsilon >0,\, \exists\eta >0$ tel que $(\delta(d)<\eta)\Rightarrow (I(f)\leq S(f,d)<I(f)+\varepsilon)$

(ii) $\forall\varepsilon >0,\exists \eta>0$ tel que $(\delta(d)<\eta)\Rightarrow i(f)-\varepsilon<s(f,d)\leq i(f)$
```

```{admonition} Corollaire  
Soit $(d_k)$ une suite de subdivisions de $[a,b]$ telle que
 
 $$
 \lim\limits_{\substack{k \rightarrow +\infty}}\delta(d_k)=0
 $$

Alors $\lim\limits_{\substack{k \rightarrow +\infty}}S(f,d_k)=I(f)$ et $\lim\limits_{\substack{k \rightarrow +\infty}}s(f,d_k)=i(f)$

```

On a alors la définition suivante:

Soit $f$ une fonction réelle définie et bornée sur $[a,b],$ on dit que $f$ intégrable (au sens de Riemann) sur $[a,b]$ si, et seulement si, $I(f)=i(f)=\int_{a}^{b}f(x)dx$ (c'est un réel).

```{admonition} Exemple  
1. Si $f$ est constante sur $[a,b],\;f(x)=c,\;\forall x\in [a,b]$

On aura $M_k=c=m_k$ pour tout $k\in \{1,2,...,n\}$ et

$$
S(f,d)=s(f,d)=\sum\limits_{k=1}^{n}c(x_k-x_{k-1})=c(b-a)
$$

ceci pour toute subdivision $d.$

d'où $I(f)=i(f)$ soit encore  $\int_{a}^{b}f(x)dx=c(b-a)$

2. Soit $f$ définie sur $[a,b]$ par:

$f(x)=1$ si $x$ est rational

$f(x)=-\frac{1}{2}$ si $x$ est irrationnel

Tout segment $[x_{k-1},x_k]$ contient des points rationnels et des points irrationnels, on a donc

$$
M_k=1\quad\mbox{et}\quad m_k=-\frac{1}{2}\quad\mbox{pour tout}\;k\in \{1,2,...,n\}
$$

$$
S(f,d)=\sum\limits_{k=1}^{n}M_k(x_k-x_{k-1})=b-a
$$

$$
s(f,d)=\sum\limits_{k=1}^{n}m_k(x_k-x_{k-1})=\frac{a-b}{2}
$$

d'où $I(f)=b-a$ et $i(f)=\frac{a-b}{2}$ et $f$ n'est pas intégrable sur $[a,b]$. Il existe donc des fonctions bornées, non intégrables.
```

\subsubsection{Sommes de Riemann}

Soit $f$ une fonction réelle définie et bornée sur $[a,b].$

Soit $d=\{x_0,x_1,...,x_n\}$ une subdivision de $[a,b].$

La somme $\sigma(f,d)=\sum\limits_{k=1}^{n}f(\xi_k)(x_k-x_{k-1})$ où $\xi_k\in [x_{k-1},x_k]$ est appelée somme de Riemann relative à la fonction $f$ et à la subdivision $d.$

on a $s(f,d)\leq\sigma(f,d)\leq S(f,d)$

```{admonition} Théorème 
Soient $f$ une fonction intégrable sur $[a,b]$ et $(d_k)$ une suite de subdivision de $[a,b]$ telles que $\lim\limits_{\substack{k \rightarrow +\infty}}\delta(d_k)=0$ alors $\lim\limits_{\substack{k \rightarrow +\infty}}\sigma(f,d_k)=\int_{a}^{b}f(x)dx$
```

Ce théorème est suite $(u_n)$ définie par $u_n=\frac{n}{n^2+1^2}+\frac{n}{n^2+2^2}+...+\frac{n}{n^2+n^2}$

Alors $u_n=\frac{1}{n}[\frac{1}{1+(\frac{1}{n})^2}+\frac{1}{1+(\frac{2}{n})^2}+...+\frac{1}{1+(\frac{n}{n})^2}]$

on a une somme de Riemann relative à la fonction $f(x)=\frac{1}{1+x^2}$ et la subdivision $d=\{0,\frac{1}{n},\frac{2}{n},...,\frac{n}{n}\}$

$x_{k}-x_{k-1}=\frac{1}{n}$ pour $k\in\{1,2,...,n\}$

et 

$$
\lim\limits_{\substack{n \rightarrow +\infty}}u_n=\lim\limits_{\substack{n \rightarrow +\infty}}\frac{1}{n}\sum\limits_{k=1}^{n}f(\frac{k}{n^2})=\int_{0}^{1}\frac{dx}{1+x^2}=\frac{\pi}{4}
$$


## Propriétés remarquables des fonctions intégrables
\subsubsection{Critère d'intégrabilité}
```{admonition} Théorème 
Soit $f$ définie et bornée sur $[a,b]$ si, et seulement si, pour toute suite $(d_n)$ de subdivisions de $[a,b]$ telle que

$$
\lim\limits_{\substack{n \rightarrow +\infty}}\delta(d_n)=0,\,\lim\limits_{\substack{n \rightarrow +\infty}}(S(f,d_n)-s(f,d_n))=0
$$

Ce qui équivalent à la proposition:

pour tout $\varepsilon>0$ il existe une subdivision $d$ de $[a,b]$ telle que $|S(f,d)-s(f,d)|<\varepsilon$
```

```{admonition} Théorème 
Toute fonction continue (resp. monotone) sur $[a,b]$ est intégrable sur $[a,b].$
```

On pose $\int_{a}^{a}f(x)dx=0$ et $\int_{a}^{b}f(x)dx=-\int_{b}^{a}f(x)dx$

```{admonition} Théorème (relation de Chasles)

i) Si $f$ est l'intégrale sur $[a,b]$ elle l'est sut tout sous intervalle fermé de $[a,b]$

ii) Soit $c\in [a,b],$ si $f$ est intégrable sur $[a,c]$ et sur $[c,b]$ alors $f$ est intégrable sur $[a,b]$ et

$$
\int_{a}^{b}f(x)dx=\int_{a}^{c}f(x)dx+\int_{c}^{b}f(x)dx
$$ 


```
\subsubsection{Structure d'espace vectoriel}
```{admonition} Théorème 
Si $f$ et $g$ sont intégrables sur $[a,b]$ et $\lambda\in \mathbb{R}$ alors $f+g,\,fg$ et $\lambda f$ sont intégrables sur $[a,b]$ et

$$
\int_{a}^{b}(f+g)(x)dx=\int_{a}^{b}f(x)dx+\int_{a}^{b}g(x)dx,\,\int_{a}^{b}(\lambda f(x))dx=\lambda \int_{a}^{b}f(x)dx
$$

```

L'ensemble $\mathcal{E}([a,b])$ des applications définies sur $[a,b],$ muni de l'addition et de la multiplication par un scalaire possède une structure d'espace vectoriel.
\subsubsection{Quelques propriétés d'inégalités}
```{admonition} Proposition   
Soit $f$ une fonction intégrable sur $[a,b],$ alors:

$f(x)\geq 0,\forall x\in [a,b]\Rightarrow \int_{a}^{b}f(x)dx\geq0$

$f(x)> 0,\forall x\in [a,b]\Rightarrow \int_{a}^{b}f(x)dx>0$
```
La réciproque de cette proposition est en général fausse.

```{admonition} Corollaire  

i) Soient $f$ et $g$ deux fonctions intégrables sur $[a,b]$ telles que $\forall x\in [a,b],\;f(x)\leq g(x),$ alors $\int_{a}^{b}f(x)dx\leq \int_{a}^{b}g(x)dx$

ii) Si $f$ est intégrable sur $[a,b]$ et si $m$ et $M$ sont des réels tels que

$m\leq f(x)\leq M$ pour tout $x\in [a,b]$ alors $m(b-a)\leq \int_{a}^{b}f(x)dx \leq M(b-a)$

```
```{admonition} Théorème 
Si $f$ est intégrable sur $[a,b]$ alors $|f|$ est intégrable sur $[a,b]$ et $|\int_{a}^{b}f(x)dx|\leq \int_{a}^{b}|f(x)|dx$

Soit $f$ une fonction continue et positive sur $[a,b]$ alors

$f$ est identiquement nulle sur $[a,b]$ si, et seulement si, $\int_{a}^{b}f(x)dx=0$
```

**Inégalité de Schwarz**

Si $f$ et $g$ sont intégrables sur $[a,b]$ alors

$$
\int_{a}^{b}f(x)g(x)dx\leq (\int_{a}^{b}(f(x))^2dx)^{1/2}(\int_{a}^{b}(g(x))^2dx)^{1/2}
$$

**Formule de la moyenne**

```{admonition} Théorème 
Soient $f$ et $g$ deux fonctions intégrables sur $[a,b]$ telles que $g$ ait un signe constant dans $[a,b].$ Si $m$ (resp. $M$) est la borne inférieure (resp. supérieure) de $f$ alors il existe $\mu\in [m,M]$ tel que

$$
\int_{a}^{b}f(x)g(x)dx=\mu\int_{a}^{b}g(x)dx
$$


Si $g=1$ sur $[a,b]$ alors $\mu=\frac{1}{b-a}\int_{a}^{b}f(x)dx$

$\mu$ est appelée la valeur moyenne de $f$ sur $[a,b]$
```
```{admonition} Corollaire   (Formule de la moyenne)

Si $f$ est continue sur $[a,b]$ alors il existe $c\in [a,b]$ tel que

$$
\int_{a}^{b}f(x)dx=(b-a)f(c)
$$

```