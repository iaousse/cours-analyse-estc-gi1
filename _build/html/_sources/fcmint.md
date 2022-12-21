# Fonctions continue par morceaux sur un intervalle

Dans cette partie, $I$ désigne un intervalle de $\mathbb R$.

```{admonition} Définition

Soit $f$ une fonction définie sur $I$. On dit que $f$ est continue par morceaux sur $I$ si elle est continue par morceaux sur tout segment de $I$ ($[a, b]$ avec $a, b \in I$ et $a<b$).
```


```{admonition} Exemples

1- Une fonction continue sur $I$ est continue par morceaux sur $I$.
2- La fonction $ x \to x-E(x) $ est continue par morceaux sur $\mathbb R$.
3- La fonction $f$ définie sur $\mathbb R$ par :

$$f(0)=0 \mbox{  et  } \forall x \in [-1, 1] \setminus \{0\}, f(x)=\dfrac{1}{x}
$$

n'est pas continue morceaux sur $\mathbb R$ puisque elle n'est pas continue par morceaux sur $[-1, 1]$. Cependant, elle est continue par morceaux sur $\mathbb R^*_+$ et $\mathbb R^*_-$ car elle continue sur chacun de ces intervalles.

```


**Notations**

Soient $f$ une fonction continue par morceaux sur un intervalle $I$, ainsi que $a$ et $b$ deux éléments de $I$ ( a partir de maintenant, on a pas nécessairement $a<b$) On adopte les notations suivantes:

- si $a<b$, $\int_a^b f(x)dx = \int_{[a,b]} f$

- si $a>b$, $\int_a^b f(x)dx = -\int_{[b,a]} f$
- si $a = b$, $\int_a^b f(x)dx =0$

```{warning}
Le résultat :

$$
f \leq g \Rightarrow \int_a^b f(x)dx \leq \int_a^b g(x)dx
$$
n'est pas valide que lorsque $a\leq b$. 

```

```{admonition} Proposition (Relation de Chasles)

Si $f$ est continue par morceaux sur un intervalle I, alors :


$$
\forall a, b, c \in I, ~~ \int_a^b f(x)dx = \int_a^c f(x)dx + \int_c^b f(x)dx
$$

```

```{admonition} Démonstration
:class: dropdown
Nous allons traiter le cas ou $a=b=c$, $a<c<b$ et $a<b<c$. Les autres casd ($b<a<c$, $b<c<a$, $c<a<b$ et $c<b<a$) sont similaire aux deux premiers cas.

- si $a=b=c$ chaque intégrale vaut 0, le résultat est donx trivial.

- si $a<c<b$, c'est le cas qu'on a vu dans la proposition de la Relation de Chasles pour le cas d'une fonction continue par morceaux sur $[a, b]$.

- si $a<b<c$, on applique la même proposition (Relation de Chasles) pour $f$ qui est continue par morceaux sur  $[a, c]$.

Donc

$$
\int_a^c f(x)dx = \int_a^b f(x)dx + \int_b^c f(x)dx
$$
 Or $\int_b^c f(x)dx = - \int_c^b f(x)dx$. Donc

$$
\int_a^c f(x)dx = \int_a^b f(x)dx - \int_b^c f(x)dx
$$


Et par suite 

$$
\int_a^b f(x)dx = \int_a^c f(x)dx + \int_c^b f(x)dx
$$

```


```{admonition} Proposition

Si $f$ est continue par morceaux et bornée sur $I$, on :

$$
\forall a, b \in I, ~~ \left|\int_a^b f(x)dx\right| \leq |b-a| sup_{I} |f|
$$

```

```{admonition} Démonstration
:class: dropdown
Nous avons 3 cas : $a=b$, $a<b$ et $a>b$.

1- si $a=b$ alors $\left|\int_a^b f(x)dx\right| = 0|, le résultat est immédiat.

2- si $a<b$, la fonction $f$ est continue par morceaux sur $[a, b]$. Donc, nous avons $\left|\int_{[a, b]}f \right| \leq (b-a)sup_{[a, b]}|f|$

Donc $\left|\int_{a}^bf(x)dx \right| \leq (b-a)sup_{[a, b]}|f|$

Or $sup_{[a, b]}|f| \leq sup_{I}|f|$

Donc, $\left|\int_{a}^bf(x)dx \right| \leq (b-a)sup_{I}|f|$

3- si $a>b$, en applique les mêmes étapes précédentes pour la fonction $f$ est continue par morceaux sur $[a, b]$ et on reçoit $\left|\int_{b}^af(x)dx \right| \leq (b-a)sup_{I}|f|$

Et puisque $\int_a^b f(x)dx = - \int_b^a f(x)dx$ donc $\left|\int_a^b f(x)dx\right| = \left|- \int_b^a f(x)dx\right| = \left| \int_b^a f(x)dx\right|$.

En fin, $\left|\int_{a}^bf(x)dx \right| \leq (b-a)sup_{I}|f|$

```




