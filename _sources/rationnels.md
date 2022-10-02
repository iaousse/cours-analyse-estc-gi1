# Les nombres rationnels

## L'écriture décimale

Par définition, l'ensemble des nombres rationnels est 

$$
\mathbb{Q}:=\{\frac{p}{q}\mid\, p\in \mathbb{Z},\,q\in \mathbb{N}^{*}\}
$$

Par exemple : $\frac{2}{5},\,\frac{-7}{71},\frac{3}{6}=\frac{1}{2},\,etc...$


Les nombres décimaux, c'est-à-dire les nombres de la forme $\frac{a}{10^{n}},$  avec $a\in \mathbb{Z}$, $n\in \mathbb{N}$ fournissent d'autres exemples:

$$
1,234 = 1234\times 10^{-3} =\frac{1234}{1000}
0,00345 = 345\times 10^{-5}=\frac{345}{100000}
$$

```{admonition} Définition
Un nombre est rationnel si et seulement s'il admet une écriture décimale périodique ou finie.
```

```{admonition} Exemple
le nombre $\frac{3}{5}$ est rationnel car:

$$
\frac{3}{5}=0,6\quad \frac{1}{3}=0,333\ldots
$$

```
Nous n'allons pas donner la démonstration mais le sens direct ( $\Rightarrow$ ) repose sur la division euclidienne. Pour la réciproque ($\Leftarrow$) voyons comment cela marche sur un exemple : Montrons que $x = 12,34 2021 2021\ldots$ est un rationnel.

L'idée est d'abord de faire apparaître la partie périodique juste après la virgule. Ici la période commence deux chiffres après la virgule, donc on multiplie par 100 :

$$
100x=1234,2021 2021 \ldots
$$(100x)

Maintenant on va décaler tout vers la gauche de la longueur d'une période, donc ici on multiplie encore par 10 000 pour décaler de 4 chiffres :

Maintenant on va décaler tout vers la gauche de la longueur d'une période, donc ici on multiplie encore par 10 000 pour décaler de 4 chiffres :

$$
10 000\times 100x= 1234 2021, 2021 \ldots
$$(10000x)

Les parties après la virgule des deux lignes {eq}`100x` et {eq}`10000x` sont les mêmes, donc si on les soustrait en faisant {eq}`10000x` - {eq}`100x` alors les parties décimales s’annulent :

$$
10 000 \times 100x-100x = 12 342 021-1234
$$


Donc $999 900x = 12 340 787$ donc $x=\frac{12 340 787}{999 900},$ $x$ est bien un nombre rationnel.

## $\sqrt{2}$ n'est pas un nombre rationnel

Il existe des nombres qui ne sont pas rationnels, les irrationnels. Les nombres irrationnels apparaissent naturellement dans les figures géométriques : par exemple la diagonale d'un carré de côté 1 est le nombre irrationnel $\sqrt{2}$ ; la circonférence d'un cercle de rayon $\frac{1}{2}$ est $\pi$ qui est également un nombre irrationnel. Enfin $e = exp(1)$ est aussi.

Nous allons prouver que $\sqrt{2}$ n'est pas un nombre rationnel.

```{admonition} Proposition
$\sqrt{2}$ est un nombre irrationnel.
```

Par l'absurde supposons que $\sqrt{2}$ soit un nombre rationnel. Alors il existe des entiers $p\in\mathbb{Z}$ et $q\in \mathbb{N}^{*}$ tels que $\sqrt{2}=\frac{p}{q}$ de plus, ce sera important pour la suite– on suppose que $p$ et $q$ sont premiers entre eux (c'est-à-dire que la fraction $\frac{p}{q}$ est sous une écriture irréductible).

En élevant au carré, l'égalité $\sqrt{2}=\frac{p}{q}$ devient $2q^2=p^2$. Cette dernière égalité est une égalité d'entiers. L'entier de gauche est pair, donc on en déduit que $p^2$ est pair ; en termes de divisibilité 2 divise $p^2$.
Mais si 2 divise $p^2$

Alors 2 divise $p$ (cela se prouve par facilement l'absurde). Donc il existe un entier $p'\in \mathbb{Z}$ tel que $p=2p'$

```{admonition} Démonstration
Repartons de l'égalité $2q^2=p^2$ et remplaçons $p$ par $2p'.$ Cela donne $2q^2=4p'^{2}$. Donc $q^2=2p'^{2}.$
Maintenant cela entraîne que 2 divise $q^2$ et comme avant alors 2 divise $q.$
Nous avons prouvé que 2 divise à la fois $p$ et $q.$ Cela rentre en contradiction avec le fait que $p$ et $q$ sont premiers entre eux. Notre hypothèse de départ est donc fausse : $\sqrt{2}$ n'est pas un nombre rationnel.
```

Comme ce résultat est important en voici une deuxième démonstration, assez différente, mais toujours par l'absurde.
Autre démonstration. Par l'absurde, supposons $\sqrt{2}=\frac{p}{q},$ donc $q\sqrt{2}=p\in \mathbb{N}.$ Considérons l'ensemble

$$
\mathcal{N}:=\{n\in \mathbb{N}^{*}\mid n\sqrt{2}\in \mathbb{N}\}
$$


Cet ensemble n'est pas vide car on vient de voir que $q\sqrt{2}=p\in \mathbb{N}$ donc $q\in \mathcal{N}.$ Ainsi $\mathcal{N}$ est une partie non vide de $\mathbb{N},$
elle admet donc un plus petit élément $n_0 :=\min \mathcal{N}.$

Posons

$$
n_1=n_0 \sqrt{2}-n_0=n_0 (\sqrt{2}-1)
$$

Il découle de cette dernière égalité et de $1 <\sqrt{2} < 2$ que $0 < n_1 < n_0.$

De plus $n_1 \sqrt{2}= (n_0 \sqrt{2}-n_0
)\sqrt{2}= 2n_0-n_0 \sqrt{2}\in \mathbb{N}.$ Donc $n_1\in \mathcal{N}$ et $n_1 < n_0$
: on vient de trouver un élément $n_1$ de
$\mathcal{N}$ strictement plus petit que $n_0$ qui était le minimum. C'est une contradiction.
Notre hypothèse de départ est fausse, donc $\sqrt{2}$ est un nombre irrationnel.

