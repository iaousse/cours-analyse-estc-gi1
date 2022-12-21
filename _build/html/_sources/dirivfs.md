
# Dérivabilité d'une fonction numérique

Soit $I$ un intervalle ouvert de $\mathbb{R}$ et $f:I\rightarrow\mathbb{R}$ une fonction. Soit $x_0 \in I.$

```{admonition} Definition
$f$ est dérivable en $x_0$ si le taux d'accroissement $\frac{f(x)-f(x_0)}{x-x_0}$ a une limite finie lorsque $x$ tend vers $x_0.$ La limite s'appelle alors le nombre dérivé de $f$ en $x_0$ et est noté $f'(x_0).$ Ainsi

$$
f'(x_0)=\lim\limits_{\substack{x\rightarrow x_0}}\frac{f(x)-f(x_0)}{x-x_0}
$$

```
```{admonition} Définition
$f$ est dérivable sur $I$ si $f$ est dérivable en tout point $x_0\in I.$ La fonction $x\mapsto f'(x)$ est la fonction dérivée de $f,$ elle se note $f'$ ou $\frac{df}{dx}.$
```
```{admonition} Exemple 
: class: warning
La fonction définie par $f(x)=x^2$ est dérivable en tout point $x_0\in \mathbb{R}.$ En effet,


$$
\frac{f(x)-f(x_0)}{x-x_0}=\frac{x^2-x_{0}^{2}}{x-x_0}=\frac{(x-x_0)(x+x_0}{x-x_0}=x+x_0\underset{x\to x_0}{\longrightarrow}2x_0
$$

On a même montré que le nombre dérivé de $f$ en $x_0$ est $2x_0.$ Autrement dit: $f'(x)=2x,$ pour tout $x\in \mathbb{R}.$
```

De même, on peut montrer que la fonction $f(x)=x^3$ est dérivable sur $\mathbb{R}$ et que $f'(x)=3x^2,\,\forall x\in \mathbb{R}.$

```{admonition} Définition
-  Soit $f$ une fonction définie sur un intervalle de type $[x_0,x_0+\varepsilon[.$ On dit que $f$ est dérivable en $x_0$ à droite si

$$
\lim\limits_{\substack{x_{0}^{+}}}\frac{f(x)-f(x_0)}{x-x_0}=\ell\in \mathbb{R}
$$

Dans ce cas le nombre $\ell$ est appelé dérivé de $f$ à droite en $x_0$ et est noté par $f'_d (x_0).$

-  Soit $f$ une fonction définie sur un intervalle de type $]x_0-\varepsilon,x_0].$ On dit que $f$ est dérivable en $x_0$ à gauche si

$$
\lim\limits_{\substack{x_{0}^{-}}}\frac{f(x)-f(x_0)}{x-x_0}=\ell\in \mathbb{R}
$$

Dans ce cas le nombre $\ell$ est appelé dérivé de $f$ à gauche en $x_0$ et est noté par $f'_g (x_0).$
```
```{admonition} Exemple 
: class: warning
La fonction $f(x)=\sqrt{x}$ n'est pas dérivable à droite en $x_0=0.$ En effet, on a

$$
\lim\limits_{\substack{x \rightarrow 0 \\ x>0}}\frac{f(x)-f(0)}{x-0}=\lim\limits_{\substack{x \rightarrow 0 \\ x>0}}\frac{\sqrt{x}}{x}=\lim\limits_{\substack{x \rightarrow 0 \\ x>0}}\frac{1}{\sqrt{x}}=+\infty
$$
```
```{admonition} Proposition 
:class: important
$f$ est dérivable en $x_0\Leftrightarrow f'_d(x_0)=f'_g(x_0).$
```
# Opérations sur les fonctions dérivables
```{admonition} Proposition 
:class: important
Soient $f,g:I\rightarrow \mathbb{R}$ deux fonctions dérivables sur $I.$ Alors pour tout $x\in I:$

-  $(f+g)'(x)=f'(x)+g'(x),$

-  $(\lambda f)'(x)=\lambda f'(x)$ où $\lambda$ est un réel fixé,

-  $(f\times g)'(x)=f'(x)g(x)+f(x)g'(x),$

-  $(\frac{1}{f})'(x)=-\frac{f'(x)}{(f(x))^2}$ (si $f(x)\neq0$),

-  $(\frac{f}{g})'(x)=\frac{f'(x)g(x)-f(x)g'(x)}{(g(x))^2}$ (si $g(x)\neq 0$)
```

```{admonition} Exemple 
: class: warning
1. Soit $f:\mathbb{R}\rightarrow \mathbb{R}$ la fonction définie par $f(x)=x+\mbox{exp}(x).$ $f$ est dérivable sur $\mathbb{R}$ car $f$ est la somme de deux fonctions dérivables sur $\mathbb{R}.$ De plus, on a $f'(x)=1+\mbox{exp}(x),$ pour tout $x\in \mathbb{R}.$

2. Soit $g$ la fonction définie sur $\mathbb{R}-\{1/2\}$ par $g(x)=\frac{x^2+3x-1}{2x-1}.$ La fonction $g$ est dérivable sur son domaine de définition et, pour tout $x\in \mathbb{R}-\{1/2\},$ on a 

$$
g'(x)=\frac{(2x+3)(2x-1)-2(x^2+3x-1)}{(2x-1)^2}=\frac{2x^2-2x-1}{(2x-1)^2}
$$

```
```{admonition} Proposition 
:class: important
Si $f$ est dérivable en $x$ et $g$ est dérivable en $f(x)$ alors $g\circ f$ est dérivable en $x$ de dérivée: 

$$
(g\circ f)'(x)=g'(f(x)).f'(x)
$$

```
```{admonition} Corollaire  
:class: important
Soit $I$ un intervalle ouvert. Soit $f:I\rightarrow J$ dérivable et bijective dont on note $f^{-1}:J\rightarrow I$ la bijection réciproque. Si $f'$ ne s'annule pas sur $I$ alors $f^{-1}$ est dérivable et on a pour tout $x\in J:$

$$
(f^{-1})'(x)=\frac{1}{f'(f^{-1}))}
$$

```

Le tableau suivant résume les principales formules à connaître où $x$ est une variable réelle;

| Fonction      | Dérivée                                         |
|---------------|-------------------------------------------------|
| $x^n$         | $n x^{n-1}$                                     |
| $\frac{1}{x}$ | $-\frac{1}{x^2}$                                |
| $\sqrt{x}$    | $\frac{1}{2}\frac{1}{\sqrt{x}}$                 |
| $x^{\alpha}$  | $\alpha x^{\alpha-1}\; (\alpha \in \mathbb{R})$ |
| $e^{x}$       | $e^{x}$                                         |
| $\ln x$       | $\frac{1}{x}$                                   |
| $\cos x$      | $-\sin x$                                       |
| $\sin x$      | $\cos x $                                       |
| $\tan x$       | $1+\tan^2 x=\frac{1}{\cos^2 x}$                 |


Le tableau suivant résume les principales formules à connaître de la composée des fonctions dérivable où $u$ est une fonction dérivable;

| Fonction      | Dérivée                                            |
|---------------|----------------------------------------------------|
| $u^n$         | $n u' u^{n-1}\, n\in \mathbb{Z}$                   |
| $\frac{1}{u}$ | $-\frac{u'}{u^2}$                                  |
| $\sqrt{u}$    | $\frac{1}{2}\frac{u'}{\sqrt{u}}$                   |
| $u^{\alpha}$  | $\alpha u' u^{\alpha-1}\; (\alpha \in \mathbb{R})$ |
| $e^{u}$       | $u' e^{u}$                                         |
| $\ln u$       | $\frac{u'}{u}$                                     |
| $\cos u$      | $-u' \sin u$                                       |
| $\sin u$      | $u' \cos u $                                       |
| $\tan u$       | $u' (1+\tan^2 u) =\frac{u'}{\cos^2 u}$             |


```{admonition} Remarque  
:class: tip
Si vous voulez dériver une fonction avec un exposant dépendant de $x$ il faut absolument repasser à la forme exponentielle. Par exemple si $f(x)=2^x$ alors on réécrit d'abord $f(x)=e^{x\ln 2}$ pour pouvoir calculer $f'(x)=\ln 2. e^{x\ln 2}=\ln 2 . 2^x.$
```
# Quelques applications de la dérivabilité
## Etude de sens de variation d'une fonction
```{admonition} Proposition (Dérivée et monotonie d'une fonction)
:class: important
Soit $f:[a,b]\rightarrow\mathbb{R}$ une fonction continue sur $[a,b]$ et dérivable sur $]a,b[.$

1. $\forall x\in ]a,b[,\;f'(x)\geq 0 (\mbox{resp.}f'(x)>0)\Rightarrow f$ est croissante (resp. $f$ est strictement croissante).

2. $\forall x\in ]a,b[,\;f'(x)\leq 0 (\mbox{resp.}f'(x)<0)\Rightarrow f$ est décroissante (resp. $f$ est strictement décroissante).

3. $\forall x\in ]a,b[,\;f'(x)=0\Leftrightarrow f$ est constante.

```
```{admonition} Exemple 
: class: warning
Soit $g$ la fonction définie sur $\mathbb{R}$ par $g(x)=(1-x)e^x.$ On a

$$
\forall x\in \mathbb{R}:\;g'(x)=-e^x+(1-x)e^x=(-1+1-x)e^x=-xe^x
$$

Donc $g'(x)=0\Leftrightarrow x=0$ et $g'(x)>0\Leftrightarrow x<0.$ En déduit que $g$ est strictement décroissante sur $]0,+\infty[$ et est strictement croissante sur $]-\infty,0[.$
```
## Etude d'extremums d'une fonction
```{admonition} Définition
On dit que $f$ admet un maximum (resp. un minimum) en un point $x_0\in D_f$ si

$$
\forall x\in D_f,\; f(x)\leq f(x_0)\quad (\mbox{resp.}\, f(x)\geq f(x_0))
$$

On dit que $f$ admet un maximum (resp. un minimum) local en un point $x_0$ s'il existe un voisinage $I\subset D_f$ de $x_0$ tel que

$$
\forall x\in I,\;f(x)\leq f(x_0)\quad (\mbox{resp.}\, f(x)\geq f(x_0))
$$

On dit que $f$ admet un extremum (resp. un extremum local) si $f$ admet un maximum ou un minimum (resp. un maximum local ou un minimum local).
```
```{admonition} Proposition (Dérivée et extremums locaux d'une fonction)
:class: important

Soit $f$ une fonction dérivable sur un intervalle $I$ et soit $x_0$ un point dans l'interieur de $I$ tel que $f'(x_0)=0.$

$\diamond$ S'il existe $h>0$ tel que $]x_0 -h,x_0 +h[\subset I$ avec $f'>0$ sur $]x_0-h,x_0[$ et $f'<0$ sur $]x_0,x_0+h[,$ alors $f$ admet un maximum local en $x_0.$

$\diamond$ S'il existe $h>0$ tel que $]x_0 -h,x_0 +h[\subset I$ avec $f'<0$ sur $]x_0-h,x_0[$ et $f'>0$ sur $]x_0,x_0+h[,$ alors $f$ admet un minimum local en $x_0.$

```
```{admonition} Exemple 
: class: warning
Considérons la fonction $g$ définie dans l'exemple précédent $g(x)=(1-x)e^x.$ D'après le tableau de variation de $g,$ elle admet un maximum global en $x_0=0$ puisque 

$$
\forall x\in \mathbb{R};\; g(x)\leq g(0)
$$

La fonction $g$ n'admet pas de minimum (ni global ni local)
```
# Théorème de Rolle-Théorème des accroissements finis
```{admonition} Théorème(Théorème de Rolle) 
:class: important
Soit $f:[a,b]\rightarrow\mathbb{R}$ telle que

$\diamond$ $f$ est continue sur $[a,b],$

$\diamond$ $f$ est dérivable sur $]a,b[,$

$\diamond$ $f(a)=f(b).$

Alors il existe $c\in ]a,b[$ tel que $f'(c)=0.$
```
```{admonition} Exemple 
: class: warning
Soit $f(x)=x^3-x.$ On a $f(-1)=f(1).$ De plus, $f$ est continue et dérivable sur $\mathbb{R}.$ En particulier, $f$ est continue sur $[-1,1]$ et est dérivable sur $]-1,1[.$ D'après le Théorème de Rolle, il existe $c\in ]-1,1[$ tel que $f'(c)=0.$
```

```{admonition} Théorème (Théorème des accroissements finis) 
:class: important
Soit $f:[a,b]\rightarrow \mathbb{R}$ une fonction continue sur $[a,b]$ et dérivable sur $]a,b[.$ Il existe $c\in ]a,b[$ tel que 

$$
f(b)-f(a)=f'(c)(b-a)
$$

```
```{admonition} Corollaire (Inégalité des accroissements finis)
:class: important
Soit $f:I\rightarrow\mathbb{R}$ une fonction dérivable sur un intervalle $I$ ouvert. S'il existe une constante $M$ telle que pour tout $x\in I,\,|f'(x)|\leq M$ alors 

$$
|f(x)-f(y)|\leq M|x-y|,\;\forall x,y\in I
$$

```
```{admonition} Exemple  
:class: warning
En utilisant le théorème des accroissements finis, on va montrer que

$$
x<e^x -1<xe^x,\;\forall x>0
$$

Fixons donc $x$ tel que $x>0$ et considérons la fonction $f(t)=e^t$ sur l'intervalle $[0,x].$ $f$ est continue sur $[0,x]$ et est dérivable sur $]0,x[.$ Donc, d'après le théorème des accroissements finis, il existe $c\in ]0,x[$ tel que 

$$
f'x)-f(0)=f'(c)(x-0)
$$

C-à-d: $\exists c\in ]0,x[:\;e^x-1=xe^c,$ or, $0<c<x$ implique $1<e^c<e^x,$ donc puisque $x>0,$ on a $x<xe^c<xe^x.$ Ainsi $x<e^x-1<xe^x.$
```


```{admonition} Proposition (Règle de l'Hospital)
:class: important 
Soient $f,g:I\rightarrow \mathbb{R}$ deux fonctions dérivables et soit $x_0\in I.$ On suppose que

-  $f(x_0)=g(x_0)=0,$

-  $\forall x\in I\setminus\{x_0\},\;g'(x)\neq0.$

Si $\lim\limits_{\substack{x\rightarrow x_0}}\frac{f'(x)}{g'(x)}=\ell \,(\ell\in \mathbb{R})$ alors $\lim\limits_{\substack{x\rightarrow x_0}}\frac{f(x)}{g(x)}=\ell.$
```
```{admonition} Exemple 
: class: warning
Calculer la limite en 1 de $\frac{\ln(x^2+x-1)}{\ln(x)}.$ On vérifie que:

-  $f(x)=\ln(x^2+x-1),\, f(1)=0,\,f'(x)=\frac{2x+1}{x^2+x-1},$

-  $g(x)=\ln(x),\,g(1)=0,\,g'(x)=\frac{1}{x},$

-  Prenons $I=]0,1],\,x_0=1,$ alors $g'$ ne s'annule pas sur $I\setminus\{x_0\}.$

$$
\frac{f'(x)}{g'(x)}=\frac{2x+1}{x^2+x-1}\times x=\frac{2x^2+x}{x^2+x-1}\rightarrow 3,\,qd \,x\rightarrow 1
$$

Donc, $\frac{f'(x)}{g'(x)}\rightarrow 3,\,qd x\rightarrow 1.$
```
