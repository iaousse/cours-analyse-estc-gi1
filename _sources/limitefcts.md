# Fonctions numérique: Définitions générales
```{admonition} Définition
Une fonction d'une variable réelle à valeurs réelles est une application $f:D\rightarrow\mathbb{R},$ où $D$ est une partie de $\mathbb{R}.$ En général, $D$ est un intervalle ou une réunion d'intervalles. On appelle $D$ le domaine de définition de la fonction $f$ et on le note souvent par $D_f$ et on a

$$
D_f:=\{x\in \mathbb{R};\;f(x)\in \mathbb{R}\}
$$

```
```{admonition} Exemple
:class: warning
Le domaine de définition de la fonction $f(x)=\dfrac{\sqrt{x}}{x-2}$ est $D_f=[0,2[\cup]2,+\infty[.$
```

Soient $f:D\rightarrow \mathbb{R}$ et $g:D\rightarrow\mathbb{R}$ deux fonctions définies sur une même partie $D$ de $\mathbb{R}.$

-  La somme de $f$ et $g$ est la fonction $f+g:D\rightarrow \mathbb{R}$ définie par $(f+g)(x)=f(x)+g(x)$ pour tout $x\in D.$

-  Le produit de $f$ et $g$ est la fonction $f\times g:D\rightarrow \mathbb{R}$ définie par $(f\times g)(x)=f(x)\times g(x)$ pour tout $x\in D.$

-  La multiplication par un scalaire $\lambda\in \mathbb{R}$ de $f$ est la fonction $\lambda.f:D\rightarrow \mathbb{R}$ définie par $(\lambda.f)(x)=\lambda.f(x)$ pour tout $x\in D.$

```{admonition} Définition
Soit $f:D\rightarrow \mathbb{R}$ une fonction. On dit que:

-  $f$ est majorée sur $D$ si $\exists M\in \mathbb{R},\;\forall x\in D;\; f(x)\leq M;$

-  $f$ est minorée sur $D$ si $\exists m\in \mathbb{R},\,\forall x\in D,\, f(x)\geq m;$

-  $f$ est bornée sur $D$ si $f$ est à la fois majorée et minorée sur $D,$ c'est-à-dire si $\exists M\in \mathbb{R}_{+},\forall x\in D,\,|f(x)|\leq M.$
```
```{admonition} Définition
Soit $f:D\rightarrow \mathbb{R}$ une fonction. On dit que:

-  $f$ est croissante sur $D$ si: pour tout $x$ et $y$ dans $D$ on a $x\leq y\Rightarrow f(x)\leq f(y).$

-  $f$ est strictement croissante sur $D$ si: pour tout $x$ et $y$ dans $D$ on a $x < y\Rightarrow f(x)< f(y)$

-  $f$ est décroissante sur $D$ si: pour tout $x$ et $y$ dans $D$ on a $x\leq y\Rightarrow f(x)\geq f(y).$

-  $f$ est strictement décroissante sur $D$ si: pour tout $x$ et $y$ dans $D$ on a $x < y\Rightarrow f(x)> f(y).$

-  $f$ est monotone (resp. strictement monotone) sur $D$ si $f$ est croissante ou décroissante (resp. strictement croissante ou strictement décroissante) sur $D.$


```
```{admonition} Définition
On dit que:

-  $f$ est paire si $\forall x\in D_f:$ $-x\in D_f$ et $\forall x\in D_f$ $f(-x)=f(x),$

-  $f$ est impaire si $\forall x\in D_f:$ $-x\in D_f$ et $\forall x\in D_f$ $f(-x)=-f(x),$
```
```{admonition} Définition
Soit $f:\mathbb{R}\rightarrow \mathbb{R}$ une fonction et $T$ un nombre réel, $T>0.$ La fonction $f$ est dite périodique de période $T$ si $\forall x\in \mathbb{R}$ $f(x+T)=f(x).$
```
```{admonition} Exemple
:class: warning
Les fonctions sinus et cosinus sont $2\pi$-périodique. La fonction tangente est $\pi$-périodique.
```
# Limite d'une fonction numérique
## Limite en un point en l'infini
Soit $f$ une fonction définie sur un ensemble de la forme $]a,x_0[\cup ]x_0,b[,\,x_0\in \mathbb{R}.$
```{admonition} Définition
Soit $l\in \mathbb{R}.$ On dit que $f$ a pour limite en $x_0$ si

$\forall \varepsilon>0,\quad \exists \delta>0, \quad x\in D_f:\quad |x-x_0|<\delta\Rightarrow |f(x)-l|<\varepsilon.$

On dit aussi que $f(x)$ tend vers $l$ lorsque $x$ tend vers $x_0.$ On note alors $\lim_{x\rightarrow x_0}f(x)=l$ ou bien $\lim_{x_0}f(x)=l.$
```
```{admonition} Définition
On dit que $f$ a pour limite $+\infty$ en $x_0$ si

$\forall A>0, \quad \exists \delta>0, \quad x\in I:\quad |x-x_0|<\delta\Rightarrow f(x)>A.$

On note alors $\lim_{x\rightarrow x_0}f(x)=+\infty.$

On dit que $f$ a pour limite $-\infty$ en $x_0$ si

$\forall A>0, \quad \exists \delta>0, \quad x\in I:\quad |x-x_0|<\delta\Rightarrow f(x)<-A.$

On note alors $\lim_{x\rightarrow x_0}f(x)=-\infty.$

```
Soit $f:I\rightarrow\mathbb{R}$ une fonction définie sur un intervalle de la forme $I=]a,+\infty[.$

```{admonition} Définition
-  Soit $l\in \mathbb{R}.$ On dit que $f$ a pour limite $l$ en $+\infty$ si

$\forall \varepsilon>0,\quad \exists B>0, \quad x\in I:\quad x> B\Rightarrow |f(x)-l|<\varepsilon.$

On note alors $\lim_{x\rightarrow +\infty}f(x)=l$ ou $\lim_{+\infty}=l.$

-  On dit que $f$ a pour limite $+\infty$ en $+\infty$ si

$\forall A>0,\quad \exists B>0, \quad x\in I:\quad x> B\Rightarrow f(x)>A.$

On note alors $\lim_{x\rightarrow +\infty}f(x)=+\infty$

On définirait de la même manière la limite en $-\infty$ pour des fonctions définies sur les intervalles de type $]-\infty,a[.$
```
```{admonition} Exemple
:class: warning
On a les limites classiques suivantes pour tout $n\geq 1:$

-  $\lim_{x\rightarrow +\infty}x^n=+\infty$ et $\lim_{x\rightarrow-\infty}x^n=\left\{
\begin{array}{ll}
+\infty \quad\mbox{si} \;n\;\mbox{est pair}\\
-\infty \quad\mbox{si}\;n\;\mbox{est impair}
\end{array}
\right.$

-  $\lim_{x\rightarrow \pm\infty}(\dfrac{1}{x^n})=0$

-  Soient $P(x)=a_n x^n+a_{n-1}x^{n-1}+...+a_1 x+a_0$ et $Q(x)=b_m x^m+b_{m-1}^{m-1}+...+b_1 x+b_0$ deux polynômes ($a_n\neq0$ et $b_m\neq 0$). On a

$\lim_{x\rightarrow\pm\infty}P(x)=\lim_{x\rightarrow\pm\infty}a_n x^n$ et $\lim_{x\rightarrow\pm\infty}\dfrac{P(x)}{Q(x)}=\left\{
\begin{array}{ll}
\pm\infty \quad\mbox{ si } \; n>m\\
\dfrac{a_n}{b_m} \quad\mbox{si}\;n=m\\
0 \quad\mbox{si} n<m
\end{array}
\right.$

-  Les fonctions sin et cos n'admettent pas de limite ni en $+\infty$ ni en $-\infty.$
```
## Limite à gauche et à droite en un point
```{admonition} Définition
Soit $f$ une fonction définie sur un intervalle $]x_0,b[$ (resp. $]a,x_0[$). On dit que $f$ admet une limite $\ell\in \mathbb{R}$ à droite (resp. à gauche) en $x_0$ si

$\forall \varepsilon>0,\quad \exists\delta>0,\quad \forall x\in D_f:\quad x_0< x<x_0+\delta$ (resp. $x_0-\delta< x< x_0)\Rightarrow |f(x)-l|<\varepsilon.$

On écrit alors $\lim\limits_{\substack{x \rightarrow x_0 \\ x>x_0}} f(x)=l$ (resp. $\lim\limits_{\substack{x \rightarrow x_0 \\ x<x_0}} f(x))=l.$

On note aussi $\lim\limits_{\substack{x_{0}^{+}}}f$ pour la limite à droite et $\lim\limits_{\substack{x_{0}^{-}}}f$ pour la limite à gauche.
```
```{admonition} Proposition
Soit $\ell\in \mathbb{R}.$ On a $\lim\limits_{\substack{x \rightarrow x_0}}f(x)=\ell\Leftrightarrow \lim\limits_{\substack{x \rightarrow x_{0}^{+}}}f=\lim\limits_{\substack{x \rightarrow x_{0}^{-}}}f=\ell.$
```
```{admonition} Exemple
:class: warning
Considérons la fonction $f(x)=\left\{
\begin{array}{ll}
x-2 \quad\mbox{si} \;x\geq 1,\\
x+1 \quad\mbox{si}\;x<1.
\end{array}
\right.$

On a $\lim\limits_{\substack{x \rightarrow 1^{-}}}f(x)=\lim\limits_{\substack{x \rightarrow 1^{-}}}(x+1)=2$ et $\lim\limits_{\substack{x \rightarrow 1^{+}}}f(x)=\lim\limits_{\substack{x \rightarrow 1^{+}}}(x-2)=-1.$

Comme $\lim\limits_{\substack{x \rightarrow 1^{-}}}f(x)\neq\lim\limits_{\substack{x \rightarrow 1^{+}}}f(x),$ on en déduit que $f$ n'a pas de limite en 1.
```
## Propriétés
```{admonition} Proposition
:class: important
Si une fonction admet une limite, alors cette limite est unique.
```
Soient deux fonctions $f$ et $g.$ On suppose que $x_0$ est un réel, ou que $x_0=\pm\infty.$
```{admonition} Proposition
:class: important
Si $\lim\limits_{\substack{x_{0}}}f=\ell\in \mathbb{R}$ et $\lim\limits_{\substack{x_{0}}}g=\ell'\in \mathbb{R},$ alors:

-  $\lim\limits_{\substack{x_{0}}}(\lambda. f)=\lambda.\ell$ pour tout $\lambda\in \mathbb{R}$

-  $\lim\limits_{\substack{x_{0}}}(f+g)=\ell+\ell'$

-  $\lim\limits_{\substack{x_{0}}}(f\times g)=\ell\times \ell'$

-  Si $\ell\neq0,$ alors $\lim\limits_{\substack{x_{0}}}\dfrac{1}{f}=\dfrac{1}{\ell}$

-  Si $\lim\limits_{\substack{x_{0}}}f=\pm\infty,$ alors $\lim\limits_{\substack{x_{0}}}\dfrac{1}{f}=0.$
```
Voici une liste de formes indeterminées:

$$
+\infty-\infty,\quad0\times\infty,\quad\dfrac{\infty}{\infty},\quad\dfrac{0}{0},\quad 1^{\infty},...
$$

```{admonition} Proposition
:class: important
-  Si $f\leq g$ et si $\lim\limits_{\substack{x_{0}}}f=\ell\in \mathbb{R}$ et $\lim\limits_{\substack{x_{0}}}g=\ell'\in \mathbb{R},$ alors: $\ell\leqslant\ell'.$

-  Si $f\leq g$ et si $\lim\limits_{\substack{x_{0}}}f=+\infty,$ alors $\lim\limits_{\substack{x_{0}}}g=+\infty.$

-  Si $f\leq g\leq h$ et si $\lim\limits_{\substack{x_{0}}}f=\lim\limits_{\substack{x_{0}}}h=\ell\in \mathbb{R},$ alors $g$ a une limite en $x_0$ et $\lim\limits_{\substack{x_{0}}}g=\ell.$
```
# Continuité d'une fonction numérique
```{admonition} Définition

-  Soit $f$ une fonction définie en un voisinage de $x_0.$ On dit que $f$ est continue en $x_0$ si $\lim\limits_{\substack{x\rightarrow x_{0}}}f(x)=f(x_0).$

-  Soit $f$ une fonction définie en un intervalle de type $]x_0-\varepsilon, x_0].$ On dit que $f$ est continue à droite en $x_0$ si $\lim\limits_{\substack{x\rightarrow x_{0}^{+}}}f(x)=f(x_0).$

-  Soit $f$ une fonction définie en un intervalle de type $[x_0,x_0+\varepsilon[.$ On dit que $f$ est continue à gauche en $x_0$ si $\lim\limits_{\substack{x\rightarrow x_{0}^{+}}}f(x)=f(x_0).$
```
```{admonition} Définition
Soit $f$ une fonction définie en un voisinage de $x_0.$ On a
$f$ est continue en $x_0\Leftrightarrow\lim\limits_{\substack{x\rightarrow x_{0}^{+}}}f(x)=\lim\limits_{\substack{x\rightarrow x_{0}^{-}}}f(x)=f(x_0)$
```
```{admonition} Définition

-  Une fonction $f$ est dite continue sur un intervalle ouvert $I\subset D_f$ si elle est continue en tout point de $I.$

-  Une fonction $f$ est dite continue sur un intervalle $[a,b]\subset D_f$ si elle est continue sur $]a,b[$ et continue à droite en $a$ et à gauche en $b.$

-  Une fonction $f$ est dite continue sur un intervalle $[a,b[\subset D_f$ si elle est continue sur $]a,b[$ et continue à droite en $a.$

De même, on définit la continuité d'une fonction sur un intervalle $]a,b],$ sur $]-\infty,a],$ sur $[a,+\infty[,$...
```
```{admonition} Exemple
:class: warning
-  La fonction racine carrée $x\mapsto \sqrt{x}$ est continue sur $[0,+\infty[.$

-  Les fonctions sin et cos sont continues sur $\mathbb{R}.$

-  La fonction valeur absolue $x\mapsto |x|$ est continue sur $\mathbb{R}.$
```

```{admonition} Proposition
:class: important
Soient $f,\,g:I\rightarrow\mathbb{R}$ deux fonctions continues en un point $x_0\in I.$ Alors

-  $\lambda.f$ est continue en $x_0$ (pour tout $\lambda\in \mathbb{R}$),

-  $f+g$ est continue en $x_0.$

-  $f\times g$ est continue en $x_0.$

-  Si $f(x_0)\neq0,$ alors $\dfrac{1}{f}$ est continue en $x_0.$
```

```{admonition} Exemple
:class: warning
Les polynômes sont continues sur $\mathbb{R}.$

Toute fraction rationnelle $x\mapsto\dfrac{P(x)}{Q(x)}$ est continue sur son domaine de définition.


```

La composition conserve la continuité (mais il faut faire attention en quels points les hypothèse s'appliquent)

```{admonition} Proposition
:class: important
Soient $f:I\rightarrow\mathbb{R}$ et $g:J\rightarrow\mathbb{R}$ deux fonctions telles que $f(I)\subset J.$ Si $f$ est continue en un point $x_0\in I$ et si $g$ est continue en $f(x_0),$ alors $g\circ f$ est continue en $x_0.$
```

# Prolongement par continuité
```{admonition} Définition
Soit $I$ un intervalle, $x_0$ un point de $I$ et $f:I\setminus\{x_0\}\rightarrow\mathbb{R}$ une fonction.

-  On dit que $f$ est prolongeable par continuité en $x_0$ si $f$ admet une limite finie en $x_0.$ Notons alors $\ell=\lim\limits_{\substack{x_{0}}}f.$

-  On définit alors la fonction $\widetilde{f}:I\rightarrow\mathbb{R}$ en posant pour tout $x\in I$

$\widetilde{f}(x)=\left\{
\begin{array}{ll}
f(x) \quad\mbox{si} \;x\neq x_0\\
\ell \quad\mbox{si}\;x=x_0.
\end{array}
\right.$

Alors $\widetilde{f}$ est continue en $x_0$ et on l'appelle le prolongement par continuité de $f$ en $x_0.$
```
```{admonition} Exemple
:class: warning
Considérons la fonction $f$ définie sur $\mathbb{R}-\{1\}$ par $f(x)=\dfrac{x^2+x-2}{x-1}.$ Etudions le prolongement par continuité de $f$ en 1. On a

$$
\lim\limits_{\substack{x\rightarrow1}}f(x)=\lim\limits_{\substack{x\rightarrow1}}\dfrac{(x-1)(x+2)}{x-1}=\lim\limits_{\substack{x\rightarrow1}} x+2=3
$$

Donc $f$ est prolongeable par continuité en 1. Le prolongement par continuité de $f$ en 1 est donc
$\widetilde{f}(x)=\left\{
\begin{array}{ll}
f(x) \quad\mbox{si} \;x\neq 1\\
3 \quad\mbox{si}\;x=1.
\end{array}
\right.$
```



# Théorème des valeurs intermédiaires

```{admonition} Théorème (Théorème des valeurs intermédiaires) 
:class: important
Soit $f:[a,b]\rightarrow\mathbb{R}$ une fonction continue sur un segment. Pour tout réel $y$ compris entre $f(a)$ et $f(b),$ il existe $c\in [a,b]$ tel que $f(c)=y.$

```

Voici la version la plus utilisée du théorème des valeurs intermédiaires.

```{admonition} Corollaire 
:class: important
Soit $f:[a,b]\rightarrow\mathbb{R}$ une fonction continue sur un segment. Si $f(a).f(b)<0,$ alors il existe $c\in ]a,b[$ tel que $f(c)=0.$
```

```{admonition} Exemple
:class: warning
Tout polynôme de degré impair possède au moins une racine réelle. En effet, un tel polynôme s'écrit $P(x)=a_n x^n+...+a_1 x+a_0$ avec $n$ un entier impair. On peut supposer que le coefficient $a_n$ est strictement positif. Alors on a $\lim\limits_{\substack{x\rightarrow-\infty}}P(x)=-\infty$ et $\lim\limits_{\substack{x\rightarrow+\infty}}P(x)=+\infty.$ En particulier, il existe deux réel $a$ et $b$ tels que $P(a)<0$ et $P(b)>0$ et on conclut grâce au corollaire précédent qu'il existe au moins $c\in \mathbb{R}$ tel que $P(c)=0.$
```

Voici une formulation théorique du théorème des valeurs intermédiaires

```{admonition} Corollaire 
:class: important
Soit $f:I\rightarrow\mathbb{R}$ une fonction continue sur un intervalle $I.$ Alors $f(I)$ est un intervalle.
```

Attention! Il serait faux de croire que l'image par une fonction $f$ de l'intervalle $[a,b]$ soit l'intervalle $[f(a), f(b)]$. Cependant, on a le théorème suivant

```{admonition} Théorème 
:class: important
Soit $f:[a,b]\rightarrow\mathbb{R}$ une fonction continue sur un segment. Alors il existe deux réels $m$ et $M$ tels que $f([a,b])=[m,M].$ Autrement dit, l'image d'un segment par une fonction continue est un segment.
```

Comme on sait déjà par le théorème des valeurs intermédiaires que $f([a,b])$ est un intervalle, le théorème précédent signifie que si $f$ est continue sur $[a,b],$ alors $f$ est bornée sur $[a,b],$ et elle atteint ses bornes: $m$ est le minimum de la fonction sur l'intervalle $[a,b]$ alors que $M$ est bon maximum sur $[a,b].$
# Théorème de la bijection

```{admonition} Définition
Soit $f:E\rightarrow F$ une fonction, où $E$ et $F$ sont des parties de $\mathbb{R}.$

-  $f$ est injective $\forall x,x'\in E,\; f(x)=f(x')\Rightarrow x=x';$

-  $f$ est surjective si $\forall y\in F,\exists x\in E,\;y=f(x);$

-  $f$ est bijective si $f$ est à la fois injective et surjective, c'est-à-dire si $\forall y\in F,\,\exists! x\in E:\;y=f(x).$
```
```{admonition} Proposition
:class: important
Si $f:E\rightarrow F$ est une fonction bijective alors il existe une unique application $g:F\rightarrow E$ telle que $g\circ f=\mbox{Id}_E$ et $f\circ g=\mbox{Id}_F.$ La fonction $g$ est la bijection réciproque de $f$ et se note $f^{-1}.$

$\diamond$ On rappelle que l'identité, Id$_E:E\rightarrow E$ est simplement définie par $x\mapsto x.$

$\diamond$ $g\circ f=$Id$_E$ se reformule ainsi: $\forall x\in E,\quad g(f(x))=x.$

$\diamond$ Alors que $f\circ g=\mbox{Id}_F$ s'écrit: $\forall y\in F\quad f(g(y))=y.$
```

Le théorème suivant est un outil très utile dans la pratique pour montrer qu'une fonction est bijective.
```{admonition} Théorème (Théorème de la bijection)
:class: important
Soit $f:I\rightarrow\mathbb{R}$ une fonction définie sur un intervalle $I$ de $\mathbb{R}.$ Si $f$ est continue et strictement monotone sur $I,$ alors

1. $f$ établit une bijection de l'intervalle $I$ dans l'intervalle $J=f(I),$

2. La fonction réciproque $f^{-1}:J\rightarrow I$ est continue et strictement monotone sur $J$ et elle a le même sens de variation que $f.$

```
```{admonition} Exemple
:class: warning
Considérons la fonction carrée définie sur $\mathbb{R}$ par $f(x)=x^2.$ La fonction $f$ est continue et est strictement croissante sur $I=[0,+\infty[,$ donc $f$ établit une bijection de $I$ dans $J=f([0,+\infty[)=[0,+\infty[.$ Déterminons sa fonction réciproque: Soit $x$ et $y$ dans $\mathbb{R}_{+},$ on a

$$
f^{-1}(x)=y\Leftrightarrow x=f(y)\Leftrightarrow x=y^2 \Leftrightarrow y=\sqrt{x}
$$

Donc $f^{-1}(x)=\sqrt{x},$ pour tout $x\in \mathbb{R}_{+}.$
```

Généralisons en partie l'exemple précédent;
```{admonition} Exemple
:class: warning
Soit $n\geq 1.$ Soit $f:[0,+\infty[\rightarrow [0,+\infty[$ définie par $f(x)=x^n.$ On a $f$ est continue et strictement croissante. Donc $f$ admet sur $I=[0,+\infty[$ une fonction réciproqie $f^{-1}$ définie sur $J=f([0,+\infty[)=[0,+\infty[.$

$f^{-1}$ est notée: $x\mapsto x^{\frac{1}{n}}$ ou aussi $x\mapsto \sqrt[n]{x};$ c'est la fonction racine $n-$ième. Elle est continue et strictement croissante sur $[0,+\infty[.$
```
# Application: Fonctions Logarithme et exponentielle

```{admonition} Proposition
:class: important
Il existe une unique fonction, notée $\ln:]0,+\infty[\rightarrow\mathbb{R}$ telle que:

$$
\ln'(x)=\dfrac{1}{x}\quad\mbox{pour tout}\,x>0\qquad\mbox{et}\qquad \ln(1)=0
$$

De plus, cette fonction vérifie (pour tout $a,b>0$):

1. $\ln(a\times b)=\ln(a)+\ln(b).$

2. $\ln(\dfrac{1}{a})=-\ln a,$

3. $\ln (a^n)=n\ln(a),$ (pour tout $n\in \mathbb{N}$).

4. $\ln$ est une fonction continue, strictement croissante et définit une bijection de $]0,+\infty[$ sur $\mathbb{R}.$

5. $\lim\limits_{\substack{x\rightarrow0}}\dfrac{\ln(1+x)}{x}=1.$
```
```{admonition} Définition
La bijection réciproque de $\ln:]0,+\infty[\rightarrow\mathbb{R}$ s'appelle la fonction exponentielle, notée exp$:\mathbb{R}\rightarrow]0,+\infty[.$
```
```{admonition} Proposition
:class: important
La fonction exponentielle vérifie les propriétés suivantes:

1. exp$(\ln (x))=x$ pour tout $x>0$ et $\ln(\mbox{exp}(x))=$ pour tout $x\in \mathbb{R}$

2. exp$(a+b)=\mbox{exp}(a)\times \mbox{exp}(b)$

3. exp$(nx)=(\mbox{exp}(x))^n$

4. exp$:\mathbb{R}\rightarrow]0,+\infty[$ est une fonction continue, strictement croissante vérifiant $\lim\limits_{\substack{x\rightarrow-\infty}}\mbox{exp}(x)=0$ et $\lim\limits_{\substack{x\rightarrow+\infty}}\mbox{exp}(x)=+\infty$

5. La fonction exponentielle est dérivable et $\mbox{exp}'(x)=\mbox{exp}(x),$ pour tout $x\in \mathbb{R}.$
```
```{admonition} Remarque 
:class: tip
La fonction exponentielle est l'unique fonction qui vérifie exp$'(x)=$exp$(x)$ (pour tout $x\in \mathbb{R}$) et exp$(1)=e,$ où $e\simeq2.718...$ est le nombre qui vérifie $\ln (e)=1.$

Par définition, pour $a>0$ et $b\in \mathbb{R},\,$ $a^b=\mbox{exp}(b\ln (a))$
``` 
```{admonition} Remarque 
:class: tip
$\sqrt{a}=a^{\dfrac{1}{2}}=\mbox{exp}(\dfrac{1}{2}\ln (a))$

$\sqrt[n]{a}=a^{\dfrac{1}{n}}=\mbox{exp}(\dfrac{1}{n}\ln (a))$ ( la racine $n$-ième de $a$)

On note aussi $\mbox{exp}(x)$ par $e^x$ ce qui se justifie par le calcul: $e^x=\mbox{exp}(x\ln (e))=\mbox{exp}(x).$
``` 
Les fonctions $x\mapsto a^x$ s'appellent aussi des fonctions exponentielles et se ramènent systématiquement à la fonction exponentielle classique par l'égalité $a^x=\mbox{exp}(x\ln (a)).$ Il ne faut surtout pas les confondre avec les fonctions puissances $x\mapsto x^a.$ On a les propriété suivantes;

```{admonition} Proposition
:class: important
Soient $x,y>0$ et $a,\,b\in \mathbb{R}.$

1. $x^{a+b}=x^a x^b$

2. $x^{-a}=\dfrac{1}{x^a}$

3. $(xy)^a=x^a y^a$

4. $(x^a)^b=x^{ab}$

5. $\ln(x^a)=a\ln (x)$
```

Comparons les fonctions $\ln (x),\,\mbox{exp}(x)\,$ avec $x:$

```{admonition} Proposition
:class: important

$$
\lim\limits_{\substack{x\rightarrow+\infty}}\dfrac{\ln (x)}{x}=0\qquad \mbox{et}\quad \lim\limits_{\substack{x\rightarrow+\infty}}\dfrac{\mbox{exp}x}{x}=+\infty
$$

```