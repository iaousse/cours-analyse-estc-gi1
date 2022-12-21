# Méthodes de calcul des primitives

### Intégration par parties

```{admonition} Proposition

Si $u$ et $v$ sont deux fonctions de classe $\mathcal C^1$ sur le segment $[a, b]$, on a:

$$
\int_a^b u(t)v^{'}(t)dt = u(b)v(b)- u(a)v(a) - \int_a^b u^{'}(t)v(t)dt
$$

```


```{admonition} Démonstration

Si $u$ et $v$ sont deux fonctions de classe $\mathcal C^1$, alors $uv$ est aussi de classe $\mathcal C^1$.

Donc 

$$
u(b)v(b)- u(a)v(a) = \int_a^b (uv)^{'}(t)dt = \int_a^b u(t)v^{'}(t)dt + \int_a^b u^{'}(t)v(t)dt
$$

```

**Remarque**: Dans un calcul de primitive, la formule d'intégration par parties s'écrit:

$$
\int u(x)v^{'}(x)dx = u(x)v(x) - \int v(x)u^{'}(x)dx
$$

La formule d'intégration par parties est en général utilisée pour:

- éliminer une fonction transcendantes dont la dérivée est plus simple comme par exemple les fonctions $\ln, \arcsin, \arctan,\ldots$

- calculer une intégrale par récurrence.

```{admonition} Exemples

1- sur $\mathbb R_+^*$ on a :

$$
\int \ln x dx = \int (x)^{'}\ln x dx = x\ln x - \int x\dfrac{1}{x} = x\ln x = x + Cst 
$$

2- Sur $\mathbb R$ on a:

$$
\int \arctan x dx = x \arctan x - \int \dfrac{x}{1+x^2} dx = x \arctan x - \dfrac{1}{2}\ln (1+x^2) + Cst
$$


3 - Pour calculer $\int x^2 e^x dx$, on peut intégrer l'exponentielle et dériver le polynôme:

$$
\int x^2 e^x dx = x^2e^x - 2\int xe^x dx
$$

puis recommencer:


$$
\int xe^x dx = xe^x - \int e^x dx
$$

ce qui donne:

$$
\int x^2 e^x dx = x^2e^x - 2(xe^x - \int e^x dx) = x^2e^x - 2xe^x + 2e^x + Cst
$$

```


### Changement de variable

```{admonition} Proposition
Soient $I$ et $J$ deux intervalle de $\mathbb R$, ainsi que $f$ une fonction continue de $I$ dans $\mathbb R$ et $\varphi$ une fonction de classe $\mathcal C^1$ de $J$ dans $I$. Si $\alpha$ et $\beta$ sont deux éléments de $J$, on a :

$$
\int_{\varphi(\alpha)}^{\varphi(\beta)} f(t)dt = \int_\alpha^\beta f(\varphi(u)) \varphi^{'}(u)du
$$


```

```{admonition} Démonstration

Comme $f$ est continue sur $I$, elle possède une primitive $F$ et l'on a:

$$
\int_{\varphi(\alpha)}^{\varphi(\beta)} f(t)dt = F(\varphi(\beta)) - F(\varphi(\alpha)) = F \circ\varphi(\beta) - F \circ\varphi(\alpha)
$$

D'autre part, puisque les deux fonctions $F$ et $varphi$ sont de classe $\mathcal C^1$ donc $F \circ\varphi$ est aussi de classe $\mathcal C^1$

Donc on peut écrire : $ F \circ\varphi(\beta) - F \circ\varphi(\alpha) = F(\varphi(\beta)) - F(\varphi(\alpha)) = \int_\alpha^\beta  (F \circ\varphi)^{'}(u) du$.

Par suite :

$$
\begin{aligned}
F(\varphi(\beta)) - F(\varphi(\alpha)) &= \int_\alpha^\beta  (F \circ\varphi)^{'}(u) du \\ \\
& = \int_\alpha^\beta  F^{'}(\varphi(u)) \varphi^{'}(u) du \\ \\
& = \int_\alpha^\beta f(\varphi(u)) \varphi^{'}(u)du
\end{aligned}
$$

````

**Remarques**: 

- la formule de changement de variable n'est que la formule de dérivation d'une fonction composée lue à l'envers.

- Quand on utilise la formule de changement de variable avec les notations vues dans la proposition, on dit que l'on effectue le changement de variable $t=\varphi(u)$ (d'où l'appellation changement de variable). On remplace alors $t$ par $\varphi(u)$ et $dt$ par la différentielle $\varphi^{'}(u)du$, ce qui rend le calcul assez naturel.

-  il faut faire attention lors de l'application de cette méthode, les bornes de l'intégral doivent être changées.


```{admonition} Exemples
1- Pour calculer l’intégrale :

$$
\int_0^{\frac{\pi}{2}} \sin^2 u \cos u du
$$

On pose $t = \sin u$, donc 

$$
\int_0^{\frac{\pi}{2}} sin^2 u \cos u du = \int_0^{1} t^2 dt = \dfrac{1}{3}
$$

2- Pour calculer l'intégrale 

$$
\int_{-1}^2 \sqrt{4-u^2} u du
$$

On pose $t = u^2$, donc :

$$
\int_{-1}^2 \sqrt{4-u^2} u du = \dfrac{1}{2}\int_1^4 \sqrt{4-t}dt = [-\dfrac{1}{3}(4-t^2)^{\frac{3}{2}}]_1^4 = \sqrt{3}
$$

```
