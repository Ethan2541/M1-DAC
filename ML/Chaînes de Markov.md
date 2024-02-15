

## Modèles de Markov

<hr>

Une chaîne de Markov est dite d'ordre $k$ si $p(x_t|x_0, ..., x_t) = p(x_t | x_{t-k+1}, ..., x_t)$.

Les paramètres d'une chaîne de Markov sont :
- Les états initiaux $\Pi$
- La matrice de transition $A = (a_{ij})_{i,j}$ stochastique (somme des lignes égale à 1) où $a_{i,j} = p(x_{t+1}=q_j | x_t=q_i)$

Une chaîne de Markov est ergodique si elle est irréductible (fortement connexe) et apériodique (PGCD des cycles égal à 1). 

Dans ce cas, $\Pi A^n$ converge indépendamment du choix de $\Pi$. Pour trouver cette loi stationnaire, on peut chercher le vecteur propre de $A^T$ associé à $1$, ou calculer les puissances de $A$.


## Modèles de Markov Cachés

<hr>

Dans le cas des chaînes de Markov cachées, l'ensemble des observations et les états sont indépendants.

On ajoute également un nouveau paramètre $B = (p(x_t=e_j|s_t=q_i))_{i,j}$

### Algorithme Forward

On cherche à calculer pour $\lambda$ : $p(x_t|\lambda)$ mais la combinatoire explose.

Initialisation :
$$\alpha_1(i) = p(x_1^1, s_1=j|\lambda)$$
Itération :
$$\alpha_t(j) = \left[\sum_{i=1}^N\alpha_{t-1}(i)a_{ij}\right]b_j(x_t)$$
Terminaison :
$$p(x_1^T|\lambda) = \sum_{i=1}^N\alpha_T(i)$$

### Algorithme de Viterbi

L'algorithme de Viterbi nous permet de décoder le chemin d'états optimal à partir d'une séquence d'observations.

Initialisation :
$$
\begin{cases}
	\delta_1(i) = \pi_ib_i(x_1) \\
	\psi_1(i) = 0
\end{cases}
$$
Récursion :
$$
\begin{cases}
	\delta_t(j) = \left[\max_i\delta_{t-1}(i)a_{ij}\right]b_{ij}(x_t) \\
	\psi_t(j) = \arg\max_{1\leq i\leq N}\delta_{t-1}(i)a_{ij}
\end{cases}
$$
Terminaison :
$$S^* = \max_i\delta_T(i)$$
Chemin :
$$
\begin{cases}
	q_T^* = \arg\max_{1\leq i\leq N}\delta_T(i) \\
	q_t^* = \psi_{t+1}(q_{t+1}^*)
\end{cases}
$$