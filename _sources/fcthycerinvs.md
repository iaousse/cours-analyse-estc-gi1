# Fonctions circulaires inverses
## Arccosinus
Considérons la fonction cosinus $\cos : \mathbb{R}\rightarrow[−1,1], x \mapsto\cos x.$ Pour obtenir une bijection à partir de
cette fonction, il faut considérer la restriction de cosinus à l'intervalle $[0,\pi].$ Sur cet intervalle la
fonction cosinus est continue et strictement décroissante, donc la restriction

$$
\cos:[0,\pi]\rightarrow[-1,1]
$$



est une bijection. Sa bijection réciproque est la fonction **arccosinus:**

$$
\arccos :[-1,1]\rightarrow[0,\pi]
$$


```{figure} sinconsinv.png
---
height: 150px
name: directive-fig
---
fonctions sin cos et leurs inverse
```


On a donc, par définition de la bijection réciproque:

$$
\cos(\arccos(x)=x \quad\forall x \in [−1,1]
$$

$$
\arccos(\cos(x)=x \quad x \in [0,\pi]
$$

Autrement dit:

$$
\mbox{Si}\quad x \in[0,\pi] \cos(x) =y \Leftrightarrow x = \arccos y
$$

Notons finalement que la fonction arccosinus est dérivable sur l'intervalle $]-1,1[$ et

$$
\forall x\in ]-1,1[,\quad \arccos'(x)=\frac{-1}{\sqrt{1-x^2}}
$$

**Démonstration:**


On a l'égalité $\cos(\arccos x) = x$ que l'on dérive :

\begin{eqnarray*}
\cos(\arccos x)=x
&\Rightarrow& −\arccos'(x)\times\sin(\arccos x) = 1\\
&\Rightarrow&  \arccos'(x)=-\frac{1}{\sin(\arccos x)}\\
&\Rightarrow& \arccos'(x)=-\frac{1}{\sqrt{1-\cos^2(\arccos x)}}\\
&\Rightarrow& \arccos'(x)=-\frac{1}{\sqrt{1-x^2}}
\end{eqnarray*}


## Arcsinus
La restriction

$$
\sin:[-\frac{\pi}{2},\frac{\pi}{2}]\rightarrow [-1,1]
$$

est une bijection. Sa bijection réciproque est la fonction **arcsinus** définie par

$$
\sin(\arcsin(x))=x,\;\forall x\in [-1,1]
$$


$$
\arcsin(\sin(x))=x,\;\forall x\in[-\frac{\pi}{2},\frac{\pi}{2}] 
$$

On a alors: $\forall x\in[-\frac{\pi}{2},\frac{\pi}{2}] , \sin (x)=y\Leftrightarrow x=\arcsin(y).$

La fonction arcsinus est dérivable sur l'intervalle $]-1,1[$ et

$$
\forall x\in ]-1,1[,\quad \arcsin'(x)=\frac{1}{\sqrt{1-x^2}}
$$

## Arctangente
La restriction $\tan:]-\frac{\pi}{2},\frac{\pi}{2}[\rightarrow\mathbb{R}$ est une bijection. Sa bijection réciproque est la fonction arctangente:

$$
\arctan:\mathbb{R}\rightarrow]-\frac{\pi}{2},\frac{\pi}{2}[
$$

Ainsi

$$
\tan(\arctan(x))=x,\forall x\in \mathbb{R}
$$

$$
\arctan(\tan(x))=x, \forall x\in]-\frac{\pi}{2},\frac{\pi}{2}[
$$

Et si $x\in ]-\frac{\pi}{2},\frac{\pi}{2}[,$ alors $\tan(x)=y\Leftrightarrow x=\arctan y.$

# Fonctions hyperboliques et hyperboliques inverses
## Cosinus hyperbolique et son inverse
Pour $x\in \mathbb{R},$ le cosinus hyperbolique est :

$$
ch(x)=\frac{e^x+e^{-x}}{2}
$$

La restriction $ch: [0,+\infty[\rightarrow[1,+\infty[$ est une bijection. Sa bijection réciproque est $argch:[1,+\infty[\rightarrow[0,+\infty[$
## Sinus hyperbolique et son inverse

Pour $x\in \mathbb{R},$ le sinus hyperbolique est:

$$
sh(x)=\frac{e^x-e^{-x}}{2}
$$

$sh:\mathbb{R}\rightarrow\mathbb{R}$ est une fonction continue, dérivable, strictement croissante vérifiant $\lim\limits_{\substack{x\rightarrow-\infty}}shx=-\infty$ et $\lim\limits_{\substack{x\rightarrow+\infty}}shx=+\infty,$  c'est donc une bijection. Sa bijection réciproque est $argsh:\mathbb{R}\rightarrow \mathbb{R}.$

```{admonition} Proposition 
:class: important

- $ch^2 x - sh^2 x=1.$

- $ch'x = shx, \;sh'x = chx.$

- argsh est dérivable et $argsh'x=\frac{1}{\sqrt{x^2+1}}$

- $argshx = \ln(x+\sqrt{x^2 +1}).$

```


```{figure} sh-ch.png
---
height: 150px
name: directive-fig
---
fonctions sh, ch, argch et argsh
```


# Tangente hyperbolique et son inverse

Par définition la **tangente hyperbolique** est :

$$
th x=\frac{sh x}{ch x}
$$

La fonction $th :\mathbb{R}\rightarrow]-1,1[$ est une bijection, on note $argth :]-1,1[\rightarrow\mathbb{R}$ sa bijection réciproque.





```{figure} th-argth.png
---
height: 150px
name: directive-fig
---
fonctions th et argth
```

## Trigonométrie hyperbolique

$$
ch^2 a-sh^2 a=1
$$

$$
ch(a+b)=ch a. chb+sh a.shb
$$

$$
ch(2a)= ch^2 a+sh^2 a=2 ch^2 a-1=1+2sh^2 a
$$

$$
sh(a+b)=sh a. chb+sh b. ch a
$$

$$
sh(2a)=2sha. cha
$$

$$
th(a+b)=\frac{tha+thb}{1+tha.thb}
$$

**Dérivées de fonctions hyperboliques et leurs inverses**

$$
ch'x=shx
$$

$$
sh'x=chx
$$

$$
th'x=1-th^2 x=\frac{1}{ch^2 x}
$$

$$
argch'x=\frac{1}{\sqrt{x^2-1}},\:|x|>1
$$

$$
argsh'x=\frac{1}{\sqrt{x^2+1}}
$$

$$
argth'x=\frac{1}{1-x^2},\:|x|<1
$$

$$
argch(x)=\ln(x+\sqrt{x^2-1}),\:|x|\leq 1
$$

$$
arhsh(x)=\ln(x+\sqrt{x^2+1}),\,(x\in\mathbb{R})
$$

$$
argthx=\frac{1}{2}\ln(\frac{1+x}{1-x}),\,(-1<x<1)
$$



## formules trigonometriques

### Rapel: 
- les fonctions $\sin$ et $\cos$ sont definies sur $\mathbb{R}$ et a valeurs dans $[-1, 1]$, $2\pi$-periodiques. 
- La fonction $\tan$ est definie sur $\mathbb{R}\setminus \{\frac{\pi}{2} +k\pi, k\in \mathbb{Z}$ a valeurs dans $\mathbb{R}$, $\pi$-periodiques.
- $\cos^2(x) + \sin^2(x) = 1$
- $\tan(x) = \frac{\sin(x)}{\cos(x)}$
- $\sin(-x) = -\sin(x)$
- $\cos(-x) =\cos(x)$
- $\tan(-x) = - \tan(x)$
- $ 1 + \tan^2(x) = \frac{1}{\cos^2(x)}$
- $\sin(\pi - x) = \sin(x)$
- $\cos(\pi - x) = - \cos(x)$
- $\tan(\pi - x) = - \tan(x)$
- $\sin(\frac{\pi}{2} - x)  = \cos(x)$
- $\cos(\frac{\pi}{2} - x)  = \sin(x)$
- $\tan(\frac{\pi}{2} - x)  = \frac{1}{\tan(x)}$
- $\sin(2x) = 2\sin(x)\cos(x)$
- $\cos(2x) = \cos^2(x) - \sin^2(x) = 2\cos^2(x) -1 = 1 - 2\sin^2(x)$
- $\tan(2x) = \frac{2\tan(x)}{1-\tan^2(x)}$
- $\sin(x) = \frac{2t}{1+t^2}, \mbox{ avec } t=\tan(\frac{x}{2})$
- $\cos(x) = \frac{1-t^2}{1+t^2} , \mbox{ avec } t=\tan(\frac{x}{2})$
- $\tan(x) = \frac{2t}{1-t^2} , \mbox{ avec } t=\tan(\frac{x}{2})$



### Conditions pour lesquelles cos(x) est égal à une valeur donnée $y$ :
- En général, pour une valeur donnée $y$, $cos(x) = y$ si $x = arccos(y) + 2\pi k$ ou $x = -arccos(y) + 2\pi k$, pour tout entier $k$.
- Remarque spéciale : $cos(x) = 0$ lorsque $x = \frac{\pi}{2} + \pi k$, pour tout entier $k$.

### Conditions pour lesquelles sin(x) est égal à une valeur donnée $y$ :
- En général, pour une valeur donnée $y$, $sin(x) = y$ si $x = arcsin(y) + 2\pi k$ ou $x = \pi - arcsin(y) + 2\pi k$, pour tout entier $k$.
- Remarque spéciale : $sin(x) = 0$ lorsque $x = \pi k$, pour tout entier $k$.

### Conditions pour lesquelles tan(x) est égal à une valeur donnée $y$ :
- En général, pour une valeur donnée $y$, $tan(x) = y$ si $x = arctan(y) + \pi k$, pour tout entier $k$.
- Remarque spéciale : $tan(x) = 0$ lorsque $x = \pi k$, pour tout entier $k$.





### table des valeurs
Voici une table des valeurs remarquables pour les fonctions sinus ($\sin$), cosinus ($\cos$) et tangente ($\tan$) en degrés et en radians


| Angle (degrés) | Angle (radians) | sin        | cos         | tan            |
| -------------- | --------------- | ---------- | ----------- | -------------- |
| 0°             | 0               | 0          | 1           | 0              |
| 30°            | $\frac{\pi}{6}$ | $\frac{1}{2}$ | $\frac{\sqrt{3}}{2}$ | $\frac{1}{\sqrt{3}}$ |
| 45°            | $\frac{\pi}{4}$ | $\frac{\sqrt{2}}{2}$ | $\frac{\sqrt{2}}{2}$ | 1              |
| 60°            | $\frac{\pi}{3}$ | $\frac{\sqrt{3}}{2}$ | $\frac{1}{2}$       | $\sqrt{3}$   |
| 90°            | $\frac{\pi}{2}$ | 1          | 0           | Non définie    |
| 120°           | $\frac{2\pi}{3}$ | $\frac{\sqrt{3}}{2}$ | -$\frac{1}{2}$      | -$\sqrt{3}$  |
| 135°           | $\frac{3\pi}{4}$ | $\frac{\sqrt{2}}{2}$ | -$\frac{\sqrt{2}}{2}$ | -1             |
| 150°           | $\frac{5\pi}{6}$ | $\frac{1}{2}$       | -$\frac{\sqrt{3}}{2}$ | -$\frac{1}{\sqrt{3}}$ |
| 180°           | $\pi$           | 0          | -1          | 0              |
| 210°           | $\frac{7\pi}{6}$ | -$\frac{1}{2}$      | -$\frac{\sqrt{3}}{2}$ | $\frac{1}{\sqrt{3}}$  |
| 225°           | $\frac{5\pi}{4}$ | -$\frac{\sqrt{2}}{2}$ | -$\frac{\sqrt{2}}{2}$ | 1              |
| 240°           | $\frac{4\pi}{3}$ | -$\frac{\sqrt{3}}{2}$ | -$\frac{1}{2}$      | $\sqrt{3}$   |
| 270°           | $\frac{3\pi}{2}$ | -1         | 0           | Non définie    |
| 300°           | $\frac{5\pi}{3}$ | -$\frac{\sqrt{3}}{2}$ | $\frac{1}{2}$       | -$\sqrt{3}$  |
| 315°           | $\frac{7\pi}{4}$ | -$\frac{\sqrt{2}}{2}$ | $\frac{\sqrt{2}}{2}$ | -1             |
| 330°           | $\frac{11\pi}{6}$ | -$\frac{1}{2}$      | $\frac{\sqrt{3}}{2}$ | -$\frac{1}{\sqrt{3}}$ |
| 360°           | $2\pi$          | 0          | 1           | 0              |

