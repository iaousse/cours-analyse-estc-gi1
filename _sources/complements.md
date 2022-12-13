# Complement sur les suites et les fonctions numériques
## Suites et critère de Chauchy
Le très grand intéret du critère de Cauchy provient du fait qu'il caractérise dans $\mathbb{R}$ les suites convergentes, sans que la limite apparaisse. D'où son utilisation dans l'étude des séries par exemple, ou encore pour montrer qu'une suite n'est pas convergente.

Le concept de suite de Cauchy correspond à la propriété que la distance entre deux termes de la suite devient arbitrairement petite (et non de plus en plus petite) quand ces termes sont de rang assez grand.

```{admonition} Définition (suite de chauchy)

Soit $(u_n)$ une suite réelle; on dit que $(u_n)$ est une suite de Cauchy ou vérifie le critère de Cauchy si :

$$
\forall \epsilon>0, \exists N \in \mathbb{N},  \forall p, n \in \mathbb{N}, \left\{
\begin{array}{ll}
 p\geq N\\
n\geq N\\
\end{array}
\right. \Rightarrow |u_p-u_n|<\epsilon
$$

```
```{admonition} Théorème (Critère de Cauchy)

Une suite de réels est convergente dans $\mathbb{R}$ si, et seulement si, c'est une suite de Cauchy.
```
Le critère de Cauchy est utilisé pour montrer qu'une suite $(u_n)$ est convergente (resp divergente) dans les cas où l'on peut obtenir facilement une majoration (resp minoration) de $|u_p−u_n|$ pour $n$ et $p$ assez grands. C'est le cas en particulier pour certaines séries.

## COMPARAISON DES SUITES

```{admonition} Définition
Soient $(u_n)$, $(v_n)$ et $(\epsilon_n)$ trois suites telles qu'à partir d'un certain rang $u_n = v_nε_n$. On dit que :
- $u_n$ est dominée par $v_n$ lorsque la suite $(\epsilon_n)$ est bornée. Notation : $u_n = O(v_n)$.
- $u_n$ est négligeable devant $v_n$ lorsque la suite $(\epsilon_n)$ tend vers 0 ($\lim \epsilon_n =0$). Notation : $u_n = o(v_n)$.
- $u_n$ est équivalente à $v_n$ lorsque la suite $(\epsilon_n)$ tend vers 1 ($\lim \epsilon_n =1$). Notation : $u_n \sim v_n$.

```
```{admonition} Théorème (Caractérisations)
Lorsque la suite $v$ ne s'annule pas à partir d'un certain rang :
- $u_n = O(v_n)$ si et seulement si la suite $\frac{u}{v}$ est bornée.
- $u_n = o(v_n)$ si et seulement si $\lim \frac{u_n}{v_n}= 0$.
- $u_n \sim v_n$ si et seulement si $lim \frac{u_n}{v_n}= 1$.
```

```{admonition} Exemple

On a: 

- $n =o(n^2)$ (on prend $\epsilon = \frac{1}{n} \to 0$).
- $ln(n) = o(n)$ car$\frac{ln(n)}{n} \to 0$.
- $n\sin(n) = O(n)$ car $\frac{n\sin(n)}{n}=sin(n)$ bornée.
- $\sin(n) = O(1)$ car $\frac{\sin(n)}{1}=sin(n)$ bornée.
- $\frac{n}{n^2+1} \sim \frac{1}{n}$ car $\dfrac{\frac{n}{n^2+1}}{\frac{1}{n}} = \frac{n^2}{n^2 +1} \to 1$.
- $(1+\frac{1}{n})^n \sim e$ car $\dfrac{(1+\frac{1}{n})^n}{e} \to 1$.
```

```{admonition} Remarque 
- $u_n = O(1)$ signifie que la suite $(u_n)$ est bornée.
- $u_n = o(1)$ signifie que $u_n\to 0$.
- Si $u_n = o(v_n)$ alors $u_n = O(v_n)$.
- Si $u_n \sim v_n$ alors $u_n = O(v_n)$.
- Si $u_n = o(v_n)$ et $v_n = o(w_n)$, alors $u_n = o(w_n)$ (transitivité).
- Si $u_n = O(v_n)$ et $v_n = O(w_n)$, alors $u_n = O(w_n)$ (transitivité).
- $u_n \sim v_n \Leftrightarrow u_n − v_n = o(v_n)$.
- si $l \in \mathbb{R}$ et si $u_n \sim l$ alors $u_n \to l$ (réciproque vraie lorsque $l \neq 0$).
- Si $u_n = o(v_n)$ alors $\forall \lambda \in \mathbb{R}, \lambda u_n + v_n \sim v_n$.
```

```{admonition} Théorème (croissances comparées)

Soient $\alpha, \beta > 0$:
- si $\alpha < \beta$ alors $n^\alpha = o(n^\beta)$ et $ \frac{1}{n^\beta} = o(\frac{1}{n^\alpha})$.
- $ln(n)^\alpha = o(n^\beta)$.
- $n^\alpha =o(e^{n\beta})$ et $n^\alpha =o(e^{n^\beta})$.
- $\forall a \in \mathbb{R}, a^n =o(n!)$ et $n^\alpha = o(n!)$.
- $n! = o(n^n)$.
```



```{admonition} Théorème (les équivalents usuels)

Soit $(u_n)$ une suite de limite nulle ($\lim u_n =0$).

On a:

- Si $f : ]− a;a[\to \mathbb{R}$ (avec $a > 0$) est dérivable en $0$, et si $f'(0) \neq 0$, alors on a $f(u_n)− f(0) ∼ f'(0)u_n$.
- $\sin(u_n) \sim u_n$, $e^{u_n} - 1 \sim u_n$, $ln(1+u_n)\sim u_n$, $\tan(u_n) \sim u_n$, $(1+u_n)^\alpha -1 \sim \alpha u_n$.
- Soit $P(x) = \sum_{k=0}^{p} a_kx^k$ une fonction polynomiale avec $a_p \neq 0$, alors $P(n) \sim a_pn^p$ (équivalence avec le
terme de plus haut degré).
- Soit $Q(x) =\frac{P(x)}{R(x)}$ une fraction rationnelle avec $a_px^p$ le terme de plus haut degré de $P$ ($a_p \neq 0$) et $b_rx^r$ celui de $R$ ($b_r \neq 0$), alors $Q(n) ∼ \frac{a_p}{b_r}n^{p−r}$ (équivalence avec le rapport des termes de plus haut degré).

```

```{admonition} Théorème 
Soient $u$ et $v$ deux suites,
- Si $u_n ∼ v_n$ et si $\lim v_n = l \in \mathbb{R}\cup \{+\infty, -\infty\}$, alors $\lim u_n = l$.
- Si $u_n ∼ v_n$ et si $a_n ∼ b_n$, alors $u_na_n ∼ v_nb_n$ (compatibilité avec la multiplication).
- Si $u_n ∼ v_n$ et si $v$ ne s’annule pas à partir d’un certain rang, alors $\frac{1}{u_n} ∼ \frac{1}{v_n}$ (compatibilité avec le
passage à l’inverse).
- Si $u_n ∼ v_n$ et si $v_n > 0$ ne s’annule pas à partir d’un certain rang, alors $u_n^\alpha ∼ v_n^\alpha$ pour tout réel $\alpha$
(compatibilité avec les puissances constantes).

```

```{warning}
- Il n’y a pas compatibilité avec l’addition en général, par exemple : $n+\frac{1}{n} ∼ n$ et $−n ∼ 1−n$, mais $\frac{1}{n}$
n’est pas équivalent à $1$.
- Ces propriétés sont utiles pour les calculs de limites qui ne peuvent pas être faits directement : on essaie de se
ramener à un équivalent plus simple (s’il y en a ...) dont on sait calculer la limite.
```

