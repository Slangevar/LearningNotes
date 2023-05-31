# GTM 45 Probability Theory I

## Chapter 1 Exercise

The measurable sets belong to a fixed $\sigma$-field on which the set functions and limits of their sequences are defined. Unless otherwise stated and with or without affixes, $A, B, ...$ denote sets, $\mu$ denotes a measure, $\varphi$ denotes a signed measure. Notice that a signed measure is $\sigma$-additive.

A nonnegative additive set function is called a content or a measure according as it is finitely additive or $\sigma$-additive. Signed measures are differences of two measures of which one at least is finite. 

------

### Exercise 1 (Discussion)

If $\varphi$ is $\sigma$-finite, then there are only countably many disjoint sets for which $\varphi \neq 0$ in every class.

*Note: A set function $\varphi$ is defined on a nonempty class $\mathcal{C}$ of sets in a space $\Omega$ by assigning to every set $A \in \mathcal{C}$ a single number $\varphi(A)$, finite or infinite, the value of $\varphi$ at $A$. If all values of $\varphi$ are finite, $\varphi$ is said to be finite, and we write $|\varphi|<\infty$. If every set in $\mathcal{C}$ is a countable union of sets in $\mathcal{C}$ at which $\varphi$ is finite, $\varphi$ is said to be $\sigma $-finite.*

**Solution**	

We only considering a $\sigma$-field $\mathfrak{a}$ over the space $\Omega$. The proof is as follows. 

According to the given condition, we could write
$$
\Omega = \bigcup_{i=1}^\infty A_i
$$
where $0 \le \left|\varphi(A_i)\right| < \infty$. Based on the definition of signed measure, one of $\varphi^+$ and $\varphi^-$ should be finite. Therefore, we know that $0 \le \varphi^+(A_i) < \infty$ and $0 \le \varphi^-(A_i) < \infty$.

Now, assume that there are uncountably many disjoint sets for which $\varphi\ne 0$. Then there must be uncountably many disjoints set for which $\varphi^+ \ne 0$ or $\varphi^- \ne 0$ (or both).  Without loss of generality, assume $\varphi^+ \ne 0$ (the following will be the same for the case where $\varphi^- \ne 0$). Denote these uncountably many sets as $B_u, u \in \mathcal U$ where $\mathcal U$ is some index set. We will show that it is impossible and so the proposition for this exercise is correct.

For an arbitrary $i$, denote $B_{u,i} = B_u \cap A_i$. Then clearly $A_i \supset \cup_{\mathcal U} B_{u, i}$. Without loss of generality, assume $\varphi^+(A_i) = M < \infty$. For any $N \in Z_+$, we argue that 
$$
|C_N| \le NM, \ \text{where } C_N = \left\{B_{u, i}: \varphi^+(B_{u,i}) > \frac{1}{N}\right\}
$$
Otherwise, take an arbitrary countable subset $\widetilde C_N$ of $C_N$, by the additivity,
$$
\varphi^+\left(\bigcup_{\widetilde B_{u, i}\in \widetilde C_N} \widetilde B_{u, i}\right) > \frac{1}{N}NM = M = \varphi^+(A_i)
$$
This is contradictory since 
$$
\bigcup_{\widetilde B_{u, i}\in \widetilde C_N} \widetilde B_{u, i} \subset  \cup_{\mathcal U} B_{u, i} \subset A_i \implies \varphi^+\left(\bigcup_{\widetilde B_{u, i}\in \widetilde C_N} \widetilde B_{u, i}\right) \le \varphi^+(A_i).
$$
Therefore, since countably union of countable sets are countable, and that $\varphi^+(B_{u}) > 0$ if there exists an $i$ such that $\varphi^+(B_{u, i}) > 0$,
$$
\left|\left\{B_u: \varphi^+(B_u) \right\}\right| = \left|\bigcup_{i=1}^\infty\left\{B_{u, i}: \varphi^+(B_{u,i}) > 0\right\}\right| = \left|\bigcup_{i=1}^\infty\bigcup_{N=1}^\infty C_N \right| = \aleph_0,
$$
which means there has to be only countably many $B_u$'s such that $\varphi^+(B_u) >0$. 	$\square$ 

------

### Exercise 2

For every $A$ there exists a $B\subset A$ such that $\bar{\varphi}(A)\le 2|\varphi(B)|$.

*Note 1: Let $\varphi$ be an additive function on a field $\mathcal{c}$ and define $\varphi^{+}$and $\varphi^{-}$on $\mathcal c$ by*
$$
\varphi^{+}(A)=\sup _{B \subset A} \varphi(B), \quad \varphi^{-}(A)=-\inf _{B \subset A} \varphi(B), \quad A, B \in \mathcal{C} .
$$
*The set functions $\varphi^{+}, \varphi^{-}$and $\bar{\varphi}=\varphi^{+}+\varphi^{-}$are called the upper, lower, and total variation of $\varphi$ on $\mathcal{C}$, respectively. Since $\varphi(\emptyset)=0$, these variations are nonnegative.* 

*Note 2: **Jordan-Hahn decomposition theorem***

*If $\varphi$ on a $\mathfrak{a}$-feld $\mathfrak{a}$ is $\sigma$-additive, then there exists a set $D$ such that, for every $A \in \mathfrak{a}$,*
$$
-\varphi^{-}(A)=\varphi(A D), \quad \varphi^{+}(A)=\varphi\left(A D^c\right) .
$$
*$\varphi^{+}$and $\varphi^{-}$are measures and $\varphi=\varphi^{+}-\varphi^{-}$is a signed measure.*

**Solution** 	

Notice that $\varphi(A) = \varphi(AD) + \varphi(AD^c)$ by additivity so that it will always be true that $\varphi = \varphi^+ - \varphi^-$.

Based on Jordan-Hahn decomposition theorem, we could always find a $D\in \mathfrak{a}$ such that for any $T\in \mathfrak{a}$, $-\varphi^-(T) = \varphi(TD)$ and $\varphi^+(T) = \varphi(TD^c)$. 

Now if $\varphi^-(A) \le \varphi^+(A)$, we let $B = AD^c$. Then we know that $\varphi^+(B) = \varphi^+(A)$ since $AD^c\cap D^c = AD^c$. On the other hand, we have $\varphi^-(B) = -\varphi(AD^c\cap D) = -\varphi(\empty) = 0$. Therefore, 
$$
2|\varphi(B)| = 2|\varphi^+(B) - \varphi^-(B)| = 2\varphi^+(B) = 2\varphi^+(A)
$$
On the other hand,
$$
\bar \varphi(A) = \varphi^+(A) + \varphi^-(A) \le 2 \varphi^+(A)
$$
So $B$ satisfies the result. 

Things are completely an analogy when $\varphi^-(A) > \varphi^+(A)$, just let $B = AD$.	$\square$ 

------

### Exercise 3 

If $\varphi_1 \le \varphi_2$, then $\varphi_1^{+} \le \varphi_2^{+}, \varphi_1^{-} \ge \varphi_2^{-}$. If $\varphi=\varphi_1 \pm \varphi_2$, then $\varphi^{\pm} \le \varphi_1 ^\pm+\varphi_2 ^\pm$.

**Solution**	

The first two inequalities are very obvious since $\sup_{B\subset A} \varphi_1 \le \sup_{B\subset A} \varphi_2$ and $\inf_{B\subset A} \varphi_1 \le \inf_{B\subset A} \varphi_2 $ (then taking the negation will change the direction of the inequality).  

For the third inequality, first consider the case when $\varphi = \varphi_1 + \varphi_2$, then we know that 
$$
\sup_{B\subset A} \varphi_1(B) + \varphi_2(B) \le  \sup_{B_1\subset A} \varphi(B_1) + \sup_{B_2\subset A} \varphi(B_2)
$$
 and 
$$
-(\inf_{B\subset A} \varphi_1(B) + \varphi_2(B)) \ge  -\inf_{B_1\subset A} \varphi(B_1) - \inf_{B_2\subset A} \varphi(B_2)
$$
Therefore, the inequality to prove is correct. For the case when $\varphi = \varphi_1 - \varphi_2$, we also have 
$$
\sup_{B\subset A} \varphi_1(B) - \varphi_2(B) \le  \sup_{B_1\subset A} \varphi(B_1) - \inf_{B_2\subset A} \varphi(B_2)
$$
and 
$$
\inf_{B\subset A} \varphi_1(B) - \varphi_2(B) \ge  \inf_{B_1\subset A} \varphi(B_1) - \sup_{B_2\subset A} \varphi(B_2)
$$
$\square$ 

------

### Exercise 4

**Minimality of the Jordan-Hahn decomposition.**  If $\varphi=\mu^{+}-\mu^{-}$, then $\varphi^{\pm} \le \mu^{\pm}$

**Solution**

It follows the same logic as that in the previous exercise!	$\square$ 

------

We say that $A$ is a $\varphi$-null set, if $\varphi=0$ on $\left\{A A^{\prime}, A^{\prime} \in \mathfrak{a}\right\}$. We say that $A$ and $B$ are $\varphi$-equivalent, if they coincide up to a $\varphi$-null set. We say that a nonempty set is a $\varphi$-atom, if every measurable subset of $A$ is $\varphi$-equivalent either to $\emptyset$ or to $A$.

### Exercise 5

The $\varphi$-null sets form a $\sigma$-ring; the $\varphi$-null sets of $\varphi$ and of $\bar{\varphi}$ are the same. The $\varphi$-equivalence is an equivalence relation (reflexive, transitive, and symmetric), and $\mathfrak{a}$ splits into $\varphi$-equivalence classes.

*Note: Let $\mathcal{R}$ be a nonempty collection of sets. Then $\mathcal{R}$ is a $\sigma$-ring if:*

1. *Closed under countable unions: $\bigcup_{n=1}^{\infty} A_n \in \mathcal{R}$ if $A_n \in \mathcal{R}$ for all $n \in \mathbb{N}$*
2. *Closed under relative complementation: $A \backslash B \in \mathcal{R}$ if $A, B \in \mathcal{R}$*

**Solution**

For $\sigma$-ring, just verify the two properties. First of all, we let $A_n$'s' be $\varphi$-null sets, denote the collection of them as $\mathcal R$. Then for any $A^\prime \in \mathfrak{a}$,  we can construct a sequence $B_n = A_n - \cup_{i=1}^{n-1} A_i$. Since $\cup_{i=1}^{n-1} A_i\in\mathfrak{a}$, we have to have for any $A^\prime \in \mathfrak{a}$, 
$$
\begin{aligned}
\varphi(B_nA^\prime) 
& = \varphi(A_nA^\prime) - \varphi\left(\left(\cup_{i=1}^{n-1} A_i \cap A\right) A^\prime\right) \\
&=  \varphi(A_nA^\prime) - \varphi\left(A\cap\left(\cup_{i=1}^{n-1} A_i \cap  A^\prime\right)\right) \\
&= 0 - 0 = 0
\end{aligned}
$$
Therefore


$$
\begin{aligned}
\varphi\left(\left(\bigcup_{n=1}^\infty A_n\right)A^\prime\right) 
&= \varphi\left(\bigcup_{n=1}^\infty\left(A_nA^\prime\right)\right) \\
&=   \varphi\left(\bigcup_{n=1}^\infty\left(B_nA^\prime\right)\right) \\
& = \sum_{n=1}^\infty\varphi(B_nA^\prime) = 0
\end{aligned}
$$

So we prove that the first property holds. For the second propery, if $A_1, A_2 \in \mathcal R$, then for any $A^\prime\in \mathfrak{a}$,
$$
\begin{aligned}
\varphi((A_1 - A_2) A^\prime) &= \varphi(A_1 A^\prime) - \varphi(A_1\cap(A_2\cap A^\prime)) = 0 - 0 = 0
\end{aligned}
$$
which means it also holds. Therefore, $\varphi$-null sets for a $\sigma$-ring.

To show that the $\varphi$-null sets of $\varphi$ and of $\bar{\varphi}$ are the same, we again use the Jordan-Hahn decomposition theorem. For any $\bar\varphi$-null set $A$, we have there exists a $D\in\mathfrak{a}$, for any $A^\prime \in \mathfrak{a}$
$$
\psi(AA^\prime D^c) + \psi(AA^\prime D) = 0 \Rightarrow \psi(AA^\prime) = 0
$$
Therefore, we take $A^\prime = A^\prime D$ and $A^\prime = A^\prime D^c$ to get $\varphi(AA^\prime D^c) = \varphi(AA^\prime D) = 0$ which means $A$ is also $ \varphi$-null. 

On the other hand, if $A$ is $\varphi$-null, then
$$
\psi(AA^\prime D^c) - \psi(AA^\prime D) = 0 \Rightarrow\psi(AA^\prime D^c ) = \psi(AA^\prime D)
$$
Take $A^\prime = A^\prime D$ we will have that $\varphi(\empty) = \varphi(AA^\prime D) = 0$ and take $A^\prime = A^\prime D^c$ we will have $\varphi(AA^\prime D^c) = \varphi(\empty) = 0$. Therefore, we must have $A$ is also $\bar\varphi$-null.

The reflexitivity and the symmetry of $\varphi$-equivalence are trivial. We only need to show for the transitivity of it. Suppose $A$ and $B$ are $\varphi$-equivalent, and $B$ and $C$ are $\varphi$-equivalent. 
$$
\begin{aligned}
A - C &= (A - B) - (C-B) \cup (A\cap (B - C))
\end{aligned}
$$
Since $\varphi$-null sets form a $\sigma$-ring, we know that $(A - B) - (C -B)$ is also $\sigma$-null since the two parenthesized terms are both $\sigma$-null. On the other hand, Then for any $A^\prime \in \mathfrak{a}$
$$
\varphi(A\cap(B-C)A^\prime) = \varphi((B-C)\cap(AA^\prime)) = 0
$$
Therefore, by the property of a $\sigma$-ring, we can conclude that $A-C$ is also $\sigma$-null, which leads to transitivity.	

For the last statement, for every set in $\mathfrak{a}$, we could always categorize it into some class where sets in that class are $\varphi$-equivalent. It itself could form such a class without any other members, otherwise if it is $\varphi$-equivalent to some set in other $\varphi$-equivalence class, then by transitivity, it is $\varphi$-equivalence to all the other sets in this class, then the two classes could be merged.	$\square$

------

### Exercise 6

Every $\varphi$-null set and every measurable set consisting of one point is a $\varphi$-atom; $\bar{\varphi}(A)=|\varphi(A)|$ for every $\varphi$-atom $A$. Atoms of $\varphi$ and $\bar{\varphi}$ are the same; atoms of $\varphi$ are atoms of $\varphi^{+}$and $\varphi^{-}$, but the converse is not necessarily true.

If $A$ is a $\varphi$-atom, then $\varphi=0$ or $\varphi(A)$ on $A \cap \mathfrak{a} ;$ if $\varphi$ is finite, then the converse is true. What if $\varphi$ is $\sigma$-finite? What about $\varphi=\infty$ except for $\emptyset$ ?

**Solution** 

For measurable set consisting of one point, the conclusion is trivial -- its measurable subsets could only be $\empty$ and itself! For a $\varphi$-null set $A$, consider its measurable subset $B$, then we have for any $A^\prime$ in $\mathfrak{a}$, 
$$
\varphi((A - B)A^\prime) = \varphi(AA^\prime) - \varphi((A\cap B)A^\prime) = \varphi(AA^\prime) - \varphi(A\cap(B\cap A^\prime)) = 0-0 = 0
$$
Therefore, its subset is always $\varphi$-equivalent with $A$ itself and so $A$ is a $\varphi$-atom.

For the second statement, based on Jordan-Hahn decomposition theorem, we want to show that 
$$
\psi(AD) + \psi(AD^c) = |\psi(AD) - \psi(AD^c)|
$$
Since $A$ is a $\varphi$-atom, we have that either $A - AD^c = AD$ is $\varphi$-null or $AD^c$ is $\varphi$-null. For the former case, we have $\forall A^\prime \in \mathfrak{a}$
$$
\psi(A^\prime AD) = 0 \Rightarrow \psi(AD) = 0.
$$
For the latter case, we have $\forall A^\prime\in \mathfrak{a}$,
$$
\psi(A^\prime AD^c) = 0 \Rightarrow \psi(AD^c) = 0
$$
For both cases, it is easy to check that the aforementioned equality (17) holds.

For the third statement, from the solution for exercise 5, we know that a $\varphi$-null set is also $\varphi^+$ and $\varphi^-$-null. Therefore, atoms of $\varphi$ will be the atoms of $\varphi^+$ and $\varphi^-$. But there is no such relationship conversely.

If $A$ is a $\varphi$-atom, then of course $\varphi=0$ when $A$ is $\varphi$-null. In general, for any $B\in A\cap \mathfrak{a}$, we have $B$ being $\varphi$-equivalent to $\emptyset$ or $A$. For the former case, we pick $A^\prime = B$, then 
$$
\varphi((B-\emptyset)B) = 0 \Rightarrow \varphi(B) = 0.
$$
For the latter case, we consider $B^c = A - B$ and pick $A^\prime = A - B$, then 
$$
\varphi(A - B) = 0
$$
Since $\varphi(A) = \varphi(A-B) + \varphi(B)$, we have $\varphi(B) = \varphi(A)$.

If $\varphi$ is finite, we need to show that $A$ is a $\varphi$-atom given  $\varphi=0$ or $\varphi(A)$ on $A\cap \mathfrak{a}$. For any measurable subset $B \in A$, we know that $\varphi(B) = 0 \text{ or } \varphi(A)$. 

For the former case, we know that for every $A^\prime \in \mathfrak{a}$,  $(B - \empty)A^\prime  = BA^\prime \subset A$ so that $\varphi(BA^\prime) = 0 \text{ or } \varphi(A)$. On the other hand, we know that $\varphi(BA^\prime) = \varphi(B) - \varphi(B(A^\prime)^c)$. What is more, following the same argument, $\varphi(B(A^\prime)^c) = 0 \text{ or } \varphi(A)$. Therefore, we must have $\varphi(BA^\prime) = 0$ so that $B$ is $\varphi$-equivalent to $\empty$.  

For the latter case, $\varphi(B) = \varphi(A)$. Consider the set $A - B$. $\forall A^\prime \in \mathfrak{a}$, $(A - B)A^\prime \subset A$ , we want to show that $\varphi((A - B)A^\prime) = 0 $. Suppose not, then we must have $\varphi((A-B)A^\prime) = \varphi(A)$. On the other hand, we know that $\varphi(A - B) = \varphi(A) - \varphi(B) = 0$ and $\varphi((A-B)(A^\prime)^c) = 0 \text{ or } \varphi(A)$. Since 
$$
\varphi((A-B)A^\prime) + \varphi((A-B)(A^\prime)^c) = \varphi(A-B) 
$$
The supposed case will lead to contradictory result. In consequence, we must have $\varphi((A-B)A^\prime) = 0$. Which means that $B$ is $\varphi$-equivalent to $A$. Hence, $A$ is a $\varphi$-atom.

If $\varphi$ is $\sigma$-finite, then our previous argument for the case when $\varphi(B) = 0$ is still valid. When $\varphi(B) = \varphi(A)$, it is possible that $\varphi(B) = \varphi(A) = \infty$, only for this case can't we use the previous arguments.  But this is impossible. Based on the definition of $\sigma$-finite, let us decompose $A$ into $\sum_{i=1}^\infty A_i$ where $\varphi(A_i) < \infty, \forall i$, which means, $\varphi(A_i) = 0$. This means that $\varphi(A)$ = 0 which is contradictory. Hence, $A$ is a $\varphi$-atom.

If $\varphi = \infty$ except for $\empty$, then the conclusion is not true since it could only be true when $\varphi(BA^\prime) \text{ or } \varphi((A-B)A^\prime)$ is always $0$, which means $BA^\prime$ or $(A-B)A^\prime$ will always be $\empty$, which is clearly impossible. $\square$

------

### Exercise 7 (Discussion)

If $\mu$ is finite, then $\Omega=\sum A_j+A$ where the $A_j$ or $A$ may be absent but, if present, then the $A_j$ are $\mu$-atoms of positive measure and, for every $B \subset A$ of positive measure, $\mu$ takes every value $c$ between 0 and $\mu B$ for measurable subsets of $B$. This decomposition of $\Omega$ is determined up to $\mu$-null sets. Can $\mu$ be replaced by $\varphi$ ?

(There is only a countable number of $\mu$-equivalence classes of such $A_j$ 's. Select representatives $A_j$ of these classes and let $B \subset A=\Omega-\sum A_j$. Select inductively sets $C_n \in \mathcal{C}_n$ such that $\mu C_n>\sup \mu C-\frac{1}{n}$ for all $C \in \mathcal{C}_n$, where $\mathcal{C}_n$ is the class of all $C \subset B-\left(C_1 \cup C_2 \ldots \cup C_{n-1}\right)$ for which $\mu C \leqq c-$ $\mu\left(C_1 \cup C_2 \cup \ldots \cup C_{n-1}\right)$. Then $\mu C=c$ for $\left.C=\bigcup C_{n .}\right)$

**Solution**

According to the statement, only $A$ could be non-atomic. $\Omega=\sum A_j+A$ is given so we do not prove that $A_j$ is $\mu$-atoms.  Now suppose we have such $A_j$'s, then clearly there are only coutably many of $\mu$-equivalent classes of them. Otherwise, uncountable sum of positive values will lead to infinite value of $\mu(\Omega)$ which is contradictory. Select representatives $A_j$ of these classes and let $B \subset A=\Omega-\sum A_j$. 

We now actually wants to show that $A$ could be "infinitely divided" into sets with smaller measures. Based on the hint, we can inductively select sets. Let $n = 1$, then can we select a set $C_1$ from $B$ such that $C_1 \in \mathcal{C}_1$ such that $\mu C_1>\sup \mu C-1$ for all $C \in \mathcal{C}_1$, where $\mathcal{C}_1$ is the class of all $C \subset B$ for which $\mu C \le c$. We only need to show that there are sets satisfying $\mu C \le c$ and the rest is obvious since we could always select the that $C_1$ based on the definition of $\sup$. 

If there is no $C\subset B$ such that $\mu C \le c$, then it will lead to a contradiction since it means that there is also no sets $D\subset$ satisfying $\mu D \ge \mu B - c$. We can take a sequence $D_n \to B$, so that $B-D_n \to \emptyset$ while $\mu(B-D_n) \ge \mu B -c > 0$, which is impossible since $\mu$ is continuous (*CONTINUITY THEOREM FOR ADDITIVE SET FUNCTIONS*). So that we can always find $C$'s with $\mu C \le c$. 

Similarly, we could find $C_2$, $C_3$, $\dots$ We know that $\mu\left(\bigcup_{i=1}^n C_n\right)$ is an increasing sequence. Moreover, by the construction we know that $\mu\left(\bigcup_{i=1}^n C_n\right) > c - \frac{1}{n}$ since $\sup \mu C \ge c - \mu\left(C_1 \cup C_2 \cup \ldots \cup C_{n-1}\right)$. (Actually each $C_i$ is disjoint with each other, and this inequality follows from the non-atomic property of $B$ as we argue previously. Otherwise, if $\sup \mu C <c - \mu\left(C_1 \cup C_2 \cup \ldots \cup C_{n-1}\right)$, then denote $\delta = c - \mu\left(C_1 \cup C_2 \cup \ldots \cup C_{n-1}\right) - \sup \mu C$. There will be no set $C^\prime$ in $B-\left(C_1 \cup C_2 \ldots \cup C_{n-1}\right)$  satisfying $\mu C^\prime < \delta$, which leads to the same contraction in the previous paragraph). Therefore, by the continuity, $\lim_{n\to\infty} \mu\left(\bigcup_{i=1}^n C_n\right) = \mu\left(\lim_{n\to\infty}\bigcup_{i=1}^n C_n\right) = c$. Then $\mu C=c$ for $C=\bigcup C_{n .}$ 

Can $\mu$ be replaced by $\varphi$? Is it possible for $\varphi$ to take every value $c$ between some values? 

We may show that $\varphi$ could take any value between $-\varphi^-$ and $\varphi^+$. Since $\varphi = \varphi^+ - \varphi^-$, $\varphi$ being an additive function, it can not take values outside the aforementioned range within a measurable $B \subset A$.  By Jordan-Hahn decomposition theorem, there exists $BD \subset B$ such that $\varphi(BD) = \varphi^+(B)$ and $BD^c \subset B$ such that $\varphi(BD^c) = -\varphi^-(B)$. So that $\varphi$ could take values at the edge. How about the in-between values? Again, by Jordan-Hahn decomposition theorem, we know that $\varphi+$ and $\varphi^-$ are measures, which means that, based on the conclusion for $\mu$,  for any values $c^+$ between $0$ and $\varphi^+(B)$, there exists $C^+ \subset B$ such that $\varphi^+(C^+) = c^+$ and so $C^+D \subset B$ satisfies $\varphi(C^+D) = c^+$. Similarly, we have for any values $c^-$ between $\varphi^-(B)$ and 0 such that there is $C^- D \subset B$ and $\varphi(C^-D) = c^-$. So the conclusion also works for the signed measure. $\square$

------

### Exercise 8 

If $\varphi$ is finitely additive, $\mu$ is finite, and $\mu A_n \rightarrow 0$ implies $\varphi A_n \rightarrow 0$, then $\varphi$ is $\sigma$-additive. *We say that $\varphi$ is $\varphi_0$-continuous if $\varphi_0 A=0$ implies $\varphi A=0$*.

**Solution**

Consider a sequence of disjoint sets $B_i$ and define $A_n = \sum_{i=1}^n B_i$ and $A = \sum_{i=1}^\infty B_i$. Clearly $A_n \uparrow A$ for some $A$ as $n\to \infty$.  Since $\varphi$ is finitely addtive, for any $n$ we have 
$$
\varphi\left(\sum_{i=1}^n B_i \right) = \sum_{i=1}^n \varphi(B_i)
$$
 Now, using the same technique in the textbook, for any $m < \infty$
$$
\varphi\left(\sum_{i=1}^\infty B_i\right) = \sum_{i=1}^m \varphi(B_i) + \varphi\left(\sum_{i = m+1}^\infty B_i\right).
$$
Since $\sum_{i = m+1}^\infty B_i = A - A_{m} \to \emptyset$, $\mu\left(\sum_{i = m+1}^\infty B_i\right) \to 0$ by the its $\sigma$-additivity (by *CONTINUITY THEOREM FOR ADDITIVE SET FUNCTIONS*). Hence, by assumption, we have $\varphi\left(\sum_{i = m+1}^\infty B_i\right) \to 0$ as $m\to \infty$. As a result,
$$
\varphi\left(\sum_{i=1}^\infty B_i\right) = \lim_{m\to \infty} \sum_{i=1}^m \varphi(B_i) = \sum_{i=1}^\infty \varphi(B_i),
$$
which means $\sigma$-addtivity. $\square$

------

### Exercise 9 (Discussion)

If $\mu A_n \rightarrow 0$ implies $\varphi A_n \rightarrow 0\left(\bar{\varphi} A_n \rightarrow 0\right)$, then $\varphi$ is $\mu$-continuous. If $\varphi$ is finite, then the converse is true.
(Assume the contrary of the converse; there exist $\epsilon>0$ and $A_n$ such that $\mu A_n<\frac{1}{2^n}$ and $\bar{\varphi} A_n \geqq \epsilon$. Then $\mu B=0$ and $\bar{\varphi} B \geqq \epsilon$ for $B=\lim \sup A_n$.)
What if $\varphi$ is $\sigma$-finite? What about $\mathfrak{a}$ consisting of all subsets of a denumerable space of points $\omega_n$, and $\mu\left\{\omega_n\right\}=\frac{1}{2^n}, \varphi\left\{\omega_n\right\}=n$. What about $\mu$ replaced by $\varphi_0$ ?

**Solution**

Based on the previous definition, the contrary of the converse case is that:

*$\mu A$ = 0 implies $\varphi A = 0$ $\nRightarrow$ $\mu A_n \rightarrow 0$ implies $\varphi A_n \rightarrow 0$*

Then by the given hint, the contrary of the converse is possible, then there exists $\epsilon > 0$ and $A_n \downarrow$ (We can always find such a sequence. The most extreme case is that for all $n$, $\mu A_n = 0$) such that $\mu A_n<\frac{1}{2^n}$ and $\varphi A_n \ge \epsilon$. Take $B = \lim \sup A_n = \cap_{n=1}^\infty\cup_{k=n}^\infty A_k$. Then $\mu B = \mu(\lim \sup A_n ) = 0$ by continuity. Since for any $\delta >0$, there is always an $n_0 > 0$ such that $\frac{1}{2^{n_0-1}} < \delta$. Then,
$$
\mu\left(\bigcup_{k=n_0}^\infty A_k\right) \le \sum_{k = n_0}^\infty \mu(A_k) \le \frac{1}{2^{n_0-1}} < \delta
$$
As a result, $0 \le \mu(B) < \mu\left(\bigcup_{k = k_0}^\infty A_k\right)$ for any $k_0$ so $\mu(B) = 0$.

On the other hand $\varphi(B) = \varphi(\lim \sup A_n) \ge \varphi(\lim A_n) = \lim \varphi A_n \ge  \epsilon$, by continuity of the finite measure $\varphi$. which is contradictory to the assumption. 

The given example is a case when $\varphi$ is $\sigma$-finite. In this case, the converse is not true. This is because if we let $A_n = \cup_{k = n}^\infty \{w_k\}$, then $\mu A_n = \sum_{k = n}^\infty \frac{1}{2^k} < \frac{1}{2^{n-1}} \to 0$ as $n\to \infty$ while $\varphi A_n = \sum_{k=n}^\infty k = \infty$. Yet, we still have $\mu(\emptyset) = \varphi(\emptyset) = 0$.

What is the role of finiteness? With finiteness assumed, we will have continuity from above at $\emptyset$ for the monotone set sequence, but for $\sigma$-finite measure we can't guarantee it because the measure of a monotone decreasing sequence could be always infinity, yet the limit of the sets is the empty set! 

If $\mu$ is replaced by a signed measure $\varphi_0$. Then we consider the same argument by taking the absolute value of the signed measure. $\square$

------

### Exercise 10 

If the $\mu_j$ are finite measures, then there exists a $\mu$ such that all the $\mu_j$ are $\mu$-continuous. (Take $\mu=\sum \mu_j / 2^j \mu_j \Omega$.) What about $\mu_j$ 's replaced by $\varphi_j$ 's?

**Solution**

Take $\mu=\sum \mu_j / 2^j \mu_j \Omega$. Since it is the linear combination of $\mu_j$'s, it is a measure. If $\mu = 0$, by the nonnegativity of measures, we must have all $\mu_j$'s being zero.

If $\mu_j$'s are replaced by signed measures $\varphi_j$'s. Let's consider $\varphi_j^+$ and $\varphi_j^-$'s. Following the same manner we can construct $\varphi^\pm$ such that $\varphi^\pm = 0 \implies \varphi_j^\pm = 0$. If we consider $\bar \varphi$, then $\bar\varphi = 0$ iff $\varphi^\pm = 0$.  Therefore, 
$$
\bar\varphi = 0\iff \varphi^\pm = 0 \implies \varphi_j^{\pm} = 0 \implies \varphi_j = 0
$$
 $\square$

------

Let $\mathfrak B \subset \mathfrak{a}$ be a $\sigma$-field such that the measurable subsets of elements of $\mathfrak B$ belong to $\mathfrak B$. Let $\mathfrak B(\varphi)$ be the class of sets such that their subsets which belong to $\mathfrak B$ are $\varphi$-null. Call the sets of $\mathfrak B$ "singular," and the sets of $\mathfrak B(\varphi)$ "regular." Call $\varphi$ regular (singular) if every singular (regular) set is $\varphi$-null.
Let $\varphi_r=\varphi_r^{+}-\varphi_r^{-}, \varphi_s=\varphi_s^{+}-\varphi_s^{-}$, defined by
$$
\begin{array}{ll}
\varphi_r{ }^{ \pm}(A)=\sup \varphi^{ \pm}(B) & \text { for all regular } \quad B \subset A, \\
\varphi_{\star}^{ \pm}(A)=\sup \varphi^{ \pm}(B) & \text { for all singular } \quad B \subset A .
\end{array}
$$

### Exercise 11 (Undone)

*Decomposition theorem*. $\varphi_r$ is regular, $\varphi_s$ is singular, and $\varphi=\varphi_r+\varphi_{\mathrm{s}}$. If $\varphi$ is finite, then the decomposition of $\varphi$ into a regular and a singular part is unique. What if $\varphi$ is $\sigma$-finite? What if $\mathfrak a$ consists of all subsets of a noncountable space, and $\varphi(A)$ equals the number of points of $A$ ? (Proceed as follows:

1. $B(\varphi)=B(\bar{\varphi})=B\left(\varphi^{+}\right) \cap B\left(\varphi^{-}\right)$is a $\sigma$-field.
2. $\varphi_r\left(\varphi_s\right)$ is a regular (singular) signed measure.
3. Every $A$ contains disjoint $A_r$ regular and $A_s$ singular such that $\varphi_r \pm(A)$ $=\varphi^{ \pm}\left(A_r\right), \varphi_s^{ \pm}(A)=\varphi^{ \pm}\left(A_s\right)$.
4.  If $A=A^{\prime}{ }_r+A^{\prime}$, with $A^{\prime}$, regular and $A^{\prime}$, singular, then we can take $A_r=A^{\prime}{ }_r$ and $A_s=A^{\prime}{ }_s$.
5.  If $\varphi$ is finite, every $A$ can be so decomposed.)

**Solution**

### Exercise 12 (Undone)

We can take for singular sets:

1. the $\mu$-null sets-regular (singular) becomes $\mu$-continuous ( $\mu$-discontinuous);
2. the countable measurable sets-regular (singular) becomes continuous (purely discontinuous);
3.  the countable sums of atoms-regular (singular) becomes nonatomic (atomic).

In each case investigate the regular and singular parts.

------

### Exercise 13 (Discussion)

*Intermediate-value theorem* (compare with continuous function on a connected set). If $A$ is nonatomic and $A_n \uparrow A$ with $\varphi A_n$ finite, then $\varphi$ takes every value between $-\varphi^-A$ and $+\varphi^{+} A$ for measurable subsets in $A$. (See 7.) What if $\mathfrak a$ consists of all sets in a noncountable space, $\varphi(A)=0$ or $\infty$ according as $A$ is countable or not?

**Solution**

For countable $A$'s the results is still the same, $\varphi(A)$ could only be $0$. For uncountable $A$'s, since they always have countable subsets, and it is impossible for $\varphi$ to take values other than $0$ and $\infty$, the conclusion therefore does not hold.

------

In what follows, the $\varphi_n$ are $\sigma$-additive but, unless otherwise stated, $\lim \varphi_n$ is not assumed to be $\sigma$-additive. 

*Page 86 c. If $\varphi$ on a $\sigma$-field $\mathfrak a$ is $\sigma$-additive, then there exist sets $C$ and $D$ of $a$ such that $\varphi(C)=\sup \varphi$ and $\varphi(D)=\inf \varphi$.*

### Exercise 14

If $\varphi_n \rightarrow \varphi$ $\sigma$-addtive, then $\varphi ^\pm \le \lim \inf \varphi_n ^\pm$. If, moreover, $\varphi_n \uparrow$ or $\varphi_n \downarrow$, then $\varphi^{ \pm}=\lim \varphi_n ^\pm$.

**Solution**

$\forall A \in \mathfrak a$, recall that 
$$
\varphi^+(A) = \sup_{B\subset A}\varphi(B); \quad \varphi^-(A) = -\inf_{B\subset A} \varphi(B).
$$
We first show for $\varphi^+$. Let $B_0 \subset A$ be such that $\varphi(B_0) = \varphi^+(A)$ and $B_n \subset A$ such that $\varphi_n(B_n) = \varphi_n^+(A)$ （this is possible because of c. on page 86, where $\sigma$-additivity plays the role,) then $\forall \epsilon > 0$, $\exists N_1 > 0$ such that $\forall n > N_1$,
$$
\varphi^+(A) = \varphi(B_0) < \varphi_n(B_0) + \frac{\epsilon}{2} \le \varphi_n(B_n)+ \frac{\epsilon}{2} = \varphi_n^+(A)+ \frac{\epsilon}{2}.
$$
On the other hand, $\forall N_1 > 0$, $\exists n_2 > N_1$ such that
$$
\lim\inf \varphi_{n}^+(A) + \frac{\epsilon}{2} > \varphi_{n_2}^+(A).
$$
Therefore, $\forall \epsilon > 0, A\in \mathfrak a$, 
$$
\varphi^+(A) < \lim\inf\varphi_n^+(A) + \epsilon \implies \varphi^+ \le \lim\inf \varphi^+_n.
$$
Same techniques apply to $\varphi^-$.

If $\varphi_n\uparrow$, we know that $\varphi \ge \varphi_n$ and so
$$
\varphi^+_n(A) = \varphi_n(B_n) \le \varphi(B_n) \le \varphi(B_0) = \varphi^+(A).
$$
$\forall \epsilon > 0$, $\forall N_1 > 0$, $\exists n_3 > N_1$, such that
$$
\lim\sup \varphi_n^+(A) - \epsilon < \varphi_{n_3}^+(A)\le \varphi^+(A).
$$
Therefore, $\forall \epsilon > 0, A\in \mathfrak a$, 
$$
\varphi^+(A) > \lim\sup\varphi_n^+(A)  - \epsilon \implies \varphi^+ \ge \lim\sup\varphi_n^+.
$$
To wrap up,
$$
\lim\sup\varphi_n^+ \le \varphi^+\le \lim\inf_n\varphi^+ \implies \varphi^+ = \lim\varphi_n^+.
$$
If $\varphi_n \downarrow$, then $\forall \epsilon > 0, A\in\mathfrak a$, $\exists N_4 > 0$, such that $\forall n > N_4$
$$
\varphi_n(A) < \varphi(A) + \frac{\epsilon}{2} \implies \varphi_n^+(A) = \varphi_n(B_n) < \varphi(B_n) + \frac{\epsilon}{2} \le \varphi(B_0) + \frac{\epsilon}{2}
$$
On the other hand, $\forall \epsilon > 0$, $\forall N_4 > 0$, $\exists n_4 > N_4$, such that 
$$
\varphi_{n_4}^+(A) > \lim\sup \varphi_n^+(A) - \frac{\epsilon}{2}
$$
The rest remains the same. Same techniques apply for $\varphi^-$. $\square$

------

### Exercise 15 (Check)

If $\varphi_n \uparrow(\downarrow)$ and $\varphi_1>-\infty(<+\infty)$, then $\varphi_n \rightarrow \varphi$ $ \sigma$-additive.

**Solution**

Consider $\varphi_n \uparrow$. It is easier to show that $\varphi$ is $\sigma$-subadditive. $\forall \epsilon > 0$, $\exists N > 0$ such that $\forall n > N$, for arbitrary disjoint $A_k$'s,
$$
\begin{aligned}
\varphi\left(\sum_{k=1}^\infty A_k\right) < \varphi_n\left(\sum_{k=1}^\infty A_k\right) + \epsilon = \sum_{k=1}^\infty \varphi_n\left(A_k\right) + \epsilon \le  \sum_{k=1}^\infty\varphi\left(A_k\right) + \epsilon
\end{aligned}
$$
Therefore, $\varphi\left(\sum_{k=1}^\infty A_k\right) \le \sum_{k=1}^\infty\varphi\left(A_k\right)$.

On the other hand, by the monotonicity of $\varphi_n$. $\forall \epsilon > 0$, there exists $N_1$, such that $\forall n > N_1$, $\varphi_{n}(A_1) > \varphi(A_1) - \frac{\epsilon}{2}$... In general, we can always have $N_k > N_{k-1} > \dots > N_1$,  $\varphi_{N_k+1}(A_k) > \varphi(A_k) - \frac{\epsilon}{2^k}$. Therefore, 
$$
\sum_{k=1}^K \varphi(A_k) - \epsilon < \sum_{k=1}^K\varphi_{N_k+1}(A_k) = \varphi_{N_K+1}\left(\sum_{k=1}^K A_k \right) \le \varphi\left(\sum_{k=1}^K A_k \right)
$$
Therefore, $\forall \epsilon > 0, K < \infty$, $\sum_{k=1}^K \varphi(A_k) - \epsilon < \varphi\left(\sum_{k=1}^K A_k \right) \implies \sum_{k=1}^K \varphi(A_k) \le \varphi\left(\sum_{k=1}^K A_k \right)$. Since taking limit preserves partial inequality, we must have $\sum_{k=1}^\infty \varphi(A_k) \le \varphi\left(\sum_{i=1}^\infty A_k \right)$.

Hence, $\sum_{k=1}^\infty \varphi(A_k) = \varphi\left(\sum_{i=1}^\infty A_k \right)$. For $\varphi_n \downarrow$, let 
$$
M = \sup_{B \subset \sum_{i=1}^\infty A_k} \varphi_1(B)
$$
Just consider $\varphi_n^\prime = M - \varphi_n \uparrow$. $\square$

------

### Exercise 16 (Check)

If $\varphi_n \rightarrow \varphi$ uniformly on $\mathfrak a$ and $\varphi>-\infty$ or $\varphi<+\infty$, then $\varphi$ is $\sigma$-additive.

**Solution**

The uniform convergence means that $\forall A\in \mathfrak a, \epsilon > 0$, $\exists N > 0$ such that when $n > N$, $|\varphi_n(A) - \varphi(A)| < \epsilon$. 

For arbitrary disjoint $A_k$'s, $\forall \epsilon > 0, K \in \mathbb Z_+$, there exsits $N_K > 0$ such that when $n > N_K$, 
$$
\varphi\left(\sum_{k=1}^K A_k\right) < \varphi_n\left(\sum_{k=1}^K A_k\right) + \frac{\epsilon}{K+1} = \sum_{k=1}^K\varphi_n\left( A_k\right) + \frac{\epsilon}{K+1} < \sum_{k=1}^K\varphi\left( A_k\right) + \epsilon,
$$
and 
$$
\varphi\left(\sum_{k=1}^K A_k\right) > \varphi_n\left(\sum_{k=1}^K A_k\right) - \frac{\epsilon}{K+1} = \sum_{k=1}^K\varphi_n\left( A_k\right) - \frac{\epsilon}{K+1} > \sum_{k=1}^K\varphi\left( A_k\right) - \epsilon,
$$
Therefore, $\forall \epsilon > 0, \forall K \in \mathbb Z_+$
$$
\sum_{k=1}^K\varphi\left( A_k\right) - \epsilon < \varphi\left(\sum_{k=1}^K A_k\right) < \sum_{k=1}^K\varphi\left( A_k\right) + \epsilon \implies \sum_{k=1}^K\varphi\left( A_k\right) \le \varphi\left(\sum_{k=1}^K A_k\right) \le \sum_{k=1}^K\varphi\left( A_k\right)
$$
which means that (the partial inequality is preserved)
$$
\sum_{k=1}^\infty \varphi\left( A_k\right) \le  \varphi\left(\sum_{k=1}^\infty A_k\right)  \le \sum_{k=1}^\infty\varphi\left( A_k\right) \implies \varphi\left(\sum_{k=1}^\infty A_k\right) = \sum_{k=1}^\infty \varphi\left( A_k\right)
$$
and $\sigma$-addtivity is proved. $\square$

------

*If $d\left(x_m, x_n\right) \rightarrow 0$ implies that $x_n \rightarrow$ some $x$, then the mutual convergence criterion is valid, and we say that the space is complete.*

### Exercise 17 (Discussion)

To a measure space $(\Omega, \mathfrak a, \mu)$ associate a complete metric space $(\mathcal{X}, d)$ as follows: $\mathcal X$ is the space of all sets $A, B$ of finite measure, $d$ is a metric defined by $d(A, B)=\mu\left(A B^c+A^c B\right)$. Prove that the metric space is complete.
(If $A_n$ is a mutually convergent sequence in $\mathcal X$, then the sequence $I_{A_n}$ mutually converges in measure and hence converges in measure - see Page 116 6.3.)

If $\nu$ on $\mathfrak a$ is a finite $\mu$-continuous measure, then $\nu$ is defined and continuous on $(\mathcal{X}, d)$.

**Solution**

Consider a set sequence $A_n$ such that $\forall \epsilon > 0$, $\exists N > 0$, such that if $n_1,n_2 > N$, $d(A_{n_1}, A_{n_2}) < \epsilon$.  This means that 
$$
\mu\left(A_{n_1}A_{n_2}^c+A_{n_1}^cA_{n_2}\right) < \epsilon \implies \mu\left(\{x: x\in A_{n_1}\Delta A_{n_2}\}\right) < \epsilon \implies \mu\left(\left|I_{A_{n_1}} - I_{A_{n_2}}\right| > 0 \right) < \epsilon
$$
This means, since convergence in measure and mutually convergence in measure is equivalent, that there exists a set $A$ such that 
$$
\mu\left(\left|I_{A_{n}} - I_{A}\right| > 0 \right) \to 0 \implies I_{A_{n_1}} \xrightarrow{\mu} I_A
$$
Then $\{x: x\in A_{n_1}\Delta A\} \to \emptyset$ and so $d(A_n, A) \to 0$. Hence $A_n\to A$ and this metric space is complete. 

The last statement comes from that, by Exercise 9 (the converse is true),
$$
A_n \to A \implies d(A_n, A) \to 0 \implies \mu(A \Delta A_n) \to 0 \implies v(A \Delta A_n) \to 0 \implies v(A_n) \to v(A)
$$
The last step follows from the fact that 
$$
A_n = A - (A - A_n) + (A_n - A) 
$$
and $v(A_n\Delta A) = v(A - A_n) + v(A_n - A) \to 0$. $\square$

------

We say that the $\varphi_n$ are uniformly $\mu$-continuous if $\mu A_m \rightarrow 0$ implies $\varphi_n A_m \rightarrow 0$ uniformly in $n$, as $m \rightarrow \infty$.

*A set $A$ is nowhere dense if the complement of $\bar{A}$ is dense in the space, or, equivalently, if $\bar{A}$ contains no spheres, that is, if the interior of $\bar{A}$ is empty. A set is of the first category if it is a countable union of nowhere dense sets, and it is of the second category if it is not of the first category.*

***Baire's category theorem** Every complete metric space is of the second category.*

### Exercise 18 

Let $\mu$ be $\sigma$-finite. If the finite $\varphi_n$ are $\mu$-continuous and $\lim \varphi_n$ exists and is finite, then the $\varphi_n$ are uniformly $\mu$-continuous and $\lim \varphi_n=\varphi$ is $\mu$-continuous and $\sigma$-additive. 

(For every $\epsilon>0$, set $A_k=\bigcap_{m=k}^{\infty} \bigcap_{n=k}^{\infty}\left[A \in \mathcal X ;\left|\varphi_m A-\varphi_n A\right|\right.\left.\le \frac{\epsilon}{3}\right]$. By (17), every $A_k$ is closed. By Baire's category theorem, there exists $k_0, d_0$ and $A_0 \in \mathcal X$ such that $\left[A \in \mathcal X ; d\left(A, A_0\right)<d_0\right] \subset A_{k_0}$. Let $0<\delta_0<d_0$ such that $\left|\varphi_n A\right|<\epsilon$ whenever $\mu A<\delta_0$ and $n \le k_0$. If $\mu A<\delta_0$, then $d\left(A_0-A, A_0\right)<d_0,  d\left(A_0 \cup A, A_0\right)<d_0,$ and $\left|\varphi_n A\right| \le\left|\varphi_{k_0} A\right|+\left.\left|\varphi_n\left(A_0 \cup A\right)-\varphi_{k_0}\left(A_0 \cup A\right)\right|+\left|\varphi_n\left(A_0-A\right)-\varphi_{k_0}\left(A_0-A\right)\right|.\right)$

**Solution**

Why is every $A_k$ closed? 

Consider a sequence $\{B_{j}: B_j\in A, d(B_{j_1}, B_{j_2}) \to 0 \text{ as } j_1, j_2 \to \infty\}$. This is a mutually convergence sequence in $A_k$. We know from Exercise 17 that this sequence has a limit in $\mathcal X$, namely $B$ and $d(B_j, B) \to 0$ as $j \to \infty$. Now we need to show that $B\in A_k$, i.e., $\forall m, n \ge k$, $|\varphi_m(B) - \varphi_n(B)| \le \frac{\epsilon}{3}$. 

$\forall \delta > 0$, based on the $\mu$-continuity, since $\varphi_n$'s are finite, based on exercise 9, $\exists J$ such that if $j > J$, then for given $m, n > k$,  $|\varphi_m(B_j) - \varphi_m(B)|= |\varphi_m(B_jB^c) + \varphi_m(BB_j^c)| < \frac{\delta}{2}$ and $|\varphi_n(B_j) - \varphi_n(B)|  < \frac{\delta}{2}$. This is because the symmetric difference goes to $\emptyset$ and $\varphi_m$ as well as $\varphi_n$ are finite and $\sigma$-additive (so that we will have continuity at $\emptyset$).  Therefore, 
$$
|\varphi_m(B) - \varphi_n(B)| \le |\varphi_m(B_j) - \varphi_m(B)| + |\varphi_m(B_j) - \varphi_n(B_j)| + |\varphi_n(B_j) - \varphi_n(B)| = \frac{\epsilon}{3} + \delta.
$$
Since $\delta$ could be arbitrarily small, we must have $|\varphi_m(B) - \varphi_n(B)| \le \frac{\epsilon}{3}$. This means that $A_k$ is closed.

By Baire's category theorem, there exists $k_0, d_0$ and $A_0 \in \mathcal X$ such that $\left[A \in \mathcal X ; d\left(A, A_0\right)<d_0\right] \subset A_{k_0}$. Why?  

First of all, for any set $A \in \mathcal X$, given $\varphi_n \to \varphi$, we know that there exists some $\tilde k$ such that whenever $m, n > \tilde k$, 
$$
\left|\varphi_m\left(A\right) - \varphi_n\left(A\right)\right| < \frac{\epsilon}{3}.
$$
Therefore, we have 
$$
\mathcal X = \bigcup_{k=1}^\infty A_k
$$
If there does not exists $k_0$, $d_0$ and $A_0 \in \mathcal X$ such that $\left[A \in \mathcal X ; d\left(A, A_0\right)\right]\subset A_{k_0}$, then for any $k$, $A_k$ contains no spheres. This means that $\mathcal X$ is a countable union of nowhere dense sets $A_k$'s and so $\mathcal X$ is of the first category. However, we have shown in exercise 17 that $\mathcal X$ is a complete metric space and so it should be of the second category. This contradiction tells us that there must exists  some  $k_0$, $d_0$ and $A_0 \in \mathcal X$ such that $\left[A \in \mathcal X ; d\left(A, A_0\right)\right]\subset A_{k_0}$.

By $\mu$-continuity, $\exists \delta_0$ such that when $\mu A(\text{ or some }A_m) < \delta_0$, $|\varphi_n A| < \frac{\epsilon}{3}$ where $n \le k_0$ (finite $n$'s). This could always be done based on exercise 9, i.e., $\mu \to 0$ implies $\varphi_n \to 0$ because of finiteness. If $\mu A<\delta_0$, then 
$$
d\left(A_0-A, A_0\right) = \mu\left((A_0 - A)^c A_0 + (A_0 - A)A_0^c\right) = \mu(A_0\cap A) \le \mu(A) < \delta_0 < d_0,
$$

$$
d\left(A_0 \cup A, A_0\right) = \mu((A_0\cup A)^c A_0 + (A_0\cup A)A_0^c) = \mu(A - A_0) < \mu(A) < \delta_0 < d_0.
$$

This means that $A_0 - A$ and $A_0 \cup A$ are elements in $A_{k_0}$. Which means that when $n > k_0$, 
$$
\left|\varphi_n\left(A_0 \cup A\right)-\varphi_{k_0}\left(A_0 \cup A\right)\right|\le \frac{\epsilon}{3}, \quad \left|\varphi_n\left(A_0-A\right)-\varphi_{k_0}\left(A_0-A\right)\right| \le \frac{\epsilon}{3}
$$
Since $|\varphi_n A| < \frac{\epsilon}{3}$ is certain when $n \le k_0$, we only need to consider the case when $n > k_0$. When $n> k_0$, by the definition of $A_{k_0}$,
$$
\begin{aligned}
\left|\varphi_n A\right| & \le 
|\varphi_{k_0}A| + \left|\varphi_n\left(A_0 \cup A\right)-\varphi_{k_0}\left(A_0 \cup A\right)\right|+\left|\varphi_n\left(A_0-A\right)-\varphi_{k_0}\left(A_0-A\right)\right| \\
& < \frac{\epsilon}{3} + \frac{\epsilon}{3} + \frac{\epsilon}{3} = \epsilon
\end{aligned}
$$
Hence, as long as $\mu A < \delta_0$ we will have $\forall n > 0$, $|\varphi_n A| < \epsilon $. This means uniform $\mu$-continuity. The definition of $A_{k_0}$ guarantees that $|\varphi A| \le \epsilon$ as well because the argument would be the same as that for $\varphi_{n}$ based on the fact that taking the limit will preserve the inequality condition for $A_{k_0}$. As a result, we prove for the $\mu$-continuity for $\varphi$ as well.

By exercise 8, we know that if $\mu$ is finite, $\varphi$ being $\mu$-continuous and finitely additive, then $\varphi$ is $\sigma$-additive. The finite addtivity is obvious since the limit of the finite sum is the finite sum of the limit. On the other hand, in this exercise, we know that $\mu$ is $\sigma$-finite, which means that if we ignore trivialities, there is at least one finite value for $\mu$. This means that $\mu(\emptyset) = 0$. Based on the continuity of $\sigma$-additive function, i.e., $\mu(\lim A_n) = \lim \mu(A_n)$, and using the same argument of exercise 8, we can claim that $\varphi$ is $\sigma$-additive. Here we don't have the special case in exercise 9 since $\varphi$ is guaranteed to be finite.

 $\square$

------

### Exercise 19

If finite $\varphi_n \rightarrow \varphi$ finite, then $\varphi$ is $\sigma$-additive. (If $\left|\varphi_n\right| \le c_n$, set $\mu A=\sum \frac{1}{2^n c_n}\left|\varphi_n A\right|$ and apply 18.)

**Solution**

If $\left|\varphi_n\right| \le c_n$, set $\mu A=\sum \frac{1}{2^n c_n}\left|\varphi_n A\right|$ . Then $\varphi_n$'s are $\mu$-continuous, i.e. $\mu A = 0 \implies \varphi_n A = 0$. By exercise 18, $\varphi_n$ are uniformly $\mu$-continuous and $\lim \varphi_n=\varphi$ is $\mu$-continuous and $\sigma$-additive. $\square$

## Chapter 2 Exercise

**Notation.** Unless otherwise stated, the measure space $(\Omega,\mathfrak a, \mu)$ is fixed, the (measurable) sets $A, B, ...,$ with or without affixes, belong to $\mathfrak a$, and the functions $X, Y, \dots$ with or without affixes, are finite measurable functions.

*In the proof of Measurability Theorem, we have that* 

*The constructive and descriptive definitions are equivalent, and the class of measurable functions is closed under the usual operations of analysis.*

*Let $X_n$ be functions measurable (D), that is, measurable according to (D) or, equivalently, $\left(D^{\prime}\right)$. Then all sets*
$$
\left[\text { inf } X_n<x\right]=\bigcup\left[X_n<x\right], \quad\left[-X_n<x\right]=\left[X_n>-x\right]
$$
*are measurable and, hence, the functions*
$$
\begin{aligned}
\sup X_n= & -\inf \left(-X_n\right), \lim \inf X_n=\sup _n\left(\inf _{k \geqq n} X_k\right), \\
& \lim \sup X_n=-\liminf \left(-X_n\right)
\end{aligned}
$$
*are measurable (D).*

### Exercise 1 

The set $C$ of convergence of a sequence $X_{n}$ (to a finite or inlinite limit function) is measurable.
$$
(C=\left[\operatorname*{lim}\,\operatorname{inf}X_{n}=\operatorname*{lim}\,\operatorname*{sup}\,X_{n}\right].)
$$

**Solution**

To be specific, we could write 
$$
C = \left[\omega\in \Omega: \lim\inf X_n(\omega) = \lim\sup X_n(\omega)\right]
$$
Consider the function $Y_1 = \lim \inf X_n$ and $Y_2 = \lim\sup X_n$, then according to the *MEASURABILITY THEOREM*, they are measurable. If we define $Y = Y_1 - Y_2$, then it is the result of an arithmetic operation of $Y_1$ and $Y_2$ so that it is also measurable. Notice that 
$$
C = Y^{-1}(0).
$$
Since it is a inverse image of a Borel set $\{0\}$ in $\mathbb R$, $C$ is a measurable set. $\square$

------

A countably valued function $X=\sum x_j I_{A_j}$ where the sets $A_j$ are measurable is called an elementary measurable function or, simply, an *elementary function*; if the number of distinct values of $X$ is finite, then $X$ is also called a *simple function*.

### Exercise 2 

If $\mu$ is finite, then given $X$, for every $\epsilon > 0$ there exists $A$ such that $\mu A<\epsilon$ and $X$ is bounded on $A^{c}.$ If $X$ is bounded, then there exists a sequence of simple functions which converges uniformly to $X.$ Combine both propositions.

We say that a sequence $X_n$ converges almost uniformly (a.u.) to $X$, and write $X_n \stackrel{\text { a.u. }}{\longrightarrow} X$, if, for every $\epsilon>0$, there exists a set $A$ with $\mu A<\epsilon$ such that $X_n \stackrel{\mathrm{u}}{\longrightarrow} X$ on $A^c$.

**Solution**

For the first statement, since $\mu$ is finite, we have that $\mu(\emptyset) = 0$. If the statement is not true, then there exists $\epsilon_0 > 0$ such that there does not exist a set $A$ satisfying $\mu A < \epsilon_0$ and $X$ is bounded on $A^c$. (Notice that finiteness does not mean boundedness, consider $f(x) = x$. ) 

There are two possible situations, the first is that $\forall B \ne \emptyset, B \in \mathfrak a$, $\mu B \ge \epsilon_0$ or $\mu B = 0$. Since $\mu$ is finite, we can write $\mu \Omega = M < \infty$.  This means that the number of disjoint sets such that its measure is greater than $\epsilon_0$ is at most $\frac{M}{\epsilon_0}$, which is a finite number. For any one these set, say $C$, it is possible to claim that for each single element subset  $\{\omega\} \subset C$ is either $\mu$-null or with $\mu$-value no less than $\epsilon_0$. This further leads to the fact that there are at most $\frac{M}{\epsilon_0}$ single element set with $\mu$-value no less than $\epsilon_0$ subsets. It is possible to find the maximum of $|X|$, say $x_0$, over these finite number of single elements and so on a set with $\mu$-value $M$, we have $|X| < x_0$, which means the statement is actually true. 

The second possible situation is the one that does not belong to the first. If the first statement is not true, then there exists $\epsilon_0$ such that for any $x_0 > 0$, $\mu(A_0 = \{\omega: |X(\omega)| \le x_0\}) <= M - \epsilon_0$. But this means that over a non-empty set $A_0^c$ with measure at least $\epsilon_0$, for any $x_0 > 0$, $|X| > x_0$ which means $|X| = \infty$, and it is contradictory. Therefore, the first statement has to be true.

For the second statement, this is proposition C'' of measurability theorem. Since $X$ is bounded, we can assume that $|X| < x_0$. On the other hand, since $X$ is a measurable function, the set $\{\omega:  \frac{k-1}{2^n} \le X(\omega) < \frac{k}{2^n}\}$ is measurable for any $n\in \mathbb N$ and $k \in \mathbb Z$(, and so the indicator function is measurable as well).  As a result, we can consider a sequence of simple function $\{X_n\}$ such that 
$$
X_n = \sum_{k = \lceil -x_02^n\rceil }^{\lceil x_0 2^n \rceil } \frac{k-1}{2^n} \mathbb I_{\{\frac{k-1}{2^n} \le X < \frac{k}{2^n}\}}. 
$$
It is true that $|X_n - X| < \frac{1}{2^n}$ everywhere, which means that $X_n \xrightarrow{u} X$. 

Finally we could see that it is very natural to define almost-uniform convergence. $\square$

------

### Exercise 3

If $X_n \stackrel{\text { a.u. }}{\longrightarrow} X$, then $X_n \stackrel{\text { a.e. }}{\longrightarrow} X$ and $X_n \stackrel{\mu}{\longrightarrow} X$. (For the first assertion, form $A_n$ where $A_n$ is the $A$ of the foregoing definition with $\epsilon=\frac{1}{n}$.)

**Solution**

For the first assertion, we consider a sequence of set $\{A_n\}$ where $\mu(A_n) < \frac{1}{n}$ and on $A_n^c$ we have $X_n\xrightarrow{u} X$ and so $X_n \to X$. As a result, if we define $A = \cap_{n=1}^\infty A_n$, then on $A^c$ we have  $X_n\to X$ . However, if we consider the measure of $A$ we will see that 
$$
\mu A = \mu\left( \bigcap_{n=1}^\infty A_n \right) \le \inf \mu(A_n) = 0.
$$
This means that $X_n \xrightarrow{\text{a.e.}} X$.

We don't have $\mu$ being finite, so we cannot use the Comparison of Convergence Theorem. We may need to proof for convergence in measure directly. Notice that for any $\delta > 0$,  $\epsilon > 0$, there exists $A$ with $\mu(A) < \epsilon$ and $X_n \xrightarrow{u} X$ on $A^c$. This means that $\exist N_\delta$ such that when $n > N_{\delta}$,  
$$
\mu\left(|X_n - X| > \delta\right) \le \mu(A) < \epsilon \implies \forall \delta,\ \mu\left(|X_n - X| > \delta\right) \to 0
$$
This is just the definition of $X_n \xrightarrow{\mu} X$. $\square$

------

### Exercise 4

If $X_n \stackrel{\mu}{\longrightarrow} X$, then there exists a subsequence $X_{n^{\prime}} \stackrel{\text { a.u. }}{\longrightarrow} X$.

**Solution**

Based on the definition of convergence by measure, we know that there exists $N_1$ such that when $n_1 > N_1$, 
$$
\mu\left(|X_{n_1} - X| \ge 1 \right) := \mu(A_1) < 2^{-1}
$$
Similarly, we can have $n_2 > \max\{N_2, n_1\}$ such that 
$$
\mu\left(|X_{n_2} - X| \ge \frac{1}{2} \right):= \mu(A_2) < 2^{-2}.
$$
In general, for $k \in \mathbb N$, $n_k > \max\{N_{k}, n_{k-1}\}$ and 
$$
\mu\left(|X_{n_k} - X| \ge \frac{1}{k} \right):= \mu(A_k) < 2^{-k}.
$$
In this way, we construct a sequence $\{X_{n^\prime}\} = \{X_{n_1}, X_{n_2}, \dots\}$. Now for any $\epsilon > 0$, let $N_{\epsilon} = \lceil 1 - \log_2 \epsilon\rceil + 1$, then consider the set 
$$
A_{\epsilon} = \bigcup_{n^\prime=N_{\epsilon}}^\infty A_{n^\prime}, \ \mu(A_{\epsilon}) \le \sum_{n^\prime = N_\epsilon}^\infty \mu (A_{n^\prime}) < \sum_{i = 1}^\infty \frac{\epsilon}{2^{-i}} < \epsilon.
$$
$\forall \delta > 0$, on $A_\epsilon^c$, we have that as long as $n^\prime > \max\left\{\left\lceil \frac{1}{\delta}\right\rceil + 1, N_{\epsilon}\right\}$, 
$$
|X_{n^\prime} - X| < \delta \implies X_{n^\prime} \xrightarrow{\text u} X.
$$
Then this is the subsequence we are looking for.

------

### Exercise 5

*Egoroff's theorem.* If $\mu$ is finite, then $X_n \stackrel{\text { a.e. }}{\longrightarrow} X$, implies that $X_n \stackrel{\text { a.u. }}{\longrightarrow} X$. Compare with 3. (Neglect the null set of divergence, and form $A=\bigcup_{m=1}^{\infty} A_m$ with $A_m=\bigcup_{k \ge n(m)}\left[\left|X_k-X\right| \ge \frac{1}{m}\right]$ and $n(m)$ such that $\mu A_m<\frac{\epsilon}{2^m}$.)

**Solution**

If $\mu$ is finite, then by the convergence a.e. criterion (page 116), we have 
$$
\mu \bigcup_\nu\left[\left|X_{n+\nu}-X\right| \ge \epsilon\right] \rightarrow 0
$$
Therefore, $\forall \epsilon$, based on the given hint, for any $m \in \mathbb N$, $\exists n(m)$ such that when $k = n + v \ge n(m)$, 
$$
\mu \left(\bigcup_{k \ge n(m)}\left[\left|X_{k}-X\right| \ge \frac{1}{m}\right]\right) := \mu (A_m) < \frac{\epsilon}{2^m}
$$
As a result, if we define $A=\bigcup_{m=1}^{\infty} A_m$, then $\mu(A) < \epsilon$. Furthermore, on $A^c$, $\forall \delta > 0$, as long as $n \ge n\left(\left\lceil \frac{1}{\delta}\right\rceil\right)$, we have 
$$
|X_n - X| < \frac{1}{\left\lceil \frac{1}{\delta}\right\rceil} < \delta \implies X_n \xrightarrow{\text u} X
$$
Combine the previous statement together, we have $X_n \xrightarrow{\text{a.u.}} X$. 

The finiteness gives us a nice property that gets rid of the intersection regarding $n$. Actually, finiteness will give us continuity from above, which further ensures that conditions in (70) could be satisfied. 

Notice that 
$$
\bigcap_n \bigcup_\nu\left[\left|X_{n+\nu}-X\right| \geqq \epsilon\right] = \lim_{n\to \infty }\bigcup_\nu\left[\left|X_{n+\nu}-X\right| \geqq \epsilon\right]
$$
becaues $\bigcup_\nu\left[\left|X_{n+\nu}-X\right| \geqq \epsilon\right]$ is a monotonic decreasing sequence as $n \uparrow$.  Therefore, the a.e. criterion is equivalent to say that when $\mu$ is finite,
$$
\mu\left(\lim_{n\to \infty} \bigcup_\nu\left[\left|X_{n+\nu}-X\right| \geqq \epsilon\right]\right) = 0 \implies \lim \mu \left(\bigcup_\nu\left[\left|X_{n+\nu}-X\right| \geqq \epsilon\right]\right) \to 0.
$$
which is true. We can also refer to exercise 9 of Chapter 1 for this. $\square$

------

### Exercise 6

*Lusin's theorem.* If $\mu$ is $\sigma$-finite, then $X_n \stackrel{\text { a.e. }}{\rightarrow} X$ implies that $X_n \stackrel{\mathrm{u}}{\rightarrow} X$ on every element $A_j$ of some countable partition of $\Omega-N$ where $N$ is some null set. (Neglect the null set of divergence, and start with $\mu$ finite. Use Egoroff's theorem to select inductively sets $A_k$ such that $\mu \bigcap_{k=1}^n A_k<\frac{1}{n}$ and $X_n \stackrel{\mathrm{u}}{\rightarrow} X$ on $A_k^c$ for every $\left.k.\right)$

**Solution**

According to the hint, we start with $\mu$ finite and we only need to consider this case. In fact, $\mu$ being $\sigma$-finite means that we can partition $\Omega$ into countably many $A_j$'s where we have finite value of $\mu$. Since $X_n \xrightarrow{\text{a.e.}} X$ and $\mu$ is finite, we know from Egoroff's theorem that $X_n\xrightarrow{\text{a.u.}} X$. Therefore, we can select set $A_k, k = 1, 2, \dots$ as such that $\mu(A_k) < \frac{1}{k}$ and on $A_k^c$ we have $X_n \xrightarrow{\text{u}} X$. Now consider $A = \cap_{k=1}^\infty A_k$. We must have that for any $n > 0$,
$$
0 \le \mu(A) \le \inf \mu(A_k) < \frac{1}{n} \implies \mu(A) = 0
$$
Therefore, we have that, except for a null set, $X_n\xrightarrow{\text u} X$. Since the countable union of null sets is still null, the general conclusion for $\Omega-N$ holds.

------

### Exercise 7

If $\mu$ is finite, then $X_n \stackrel{\text { a.e. }}{\longrightarrow} X$ implies existence of a set of positive measure on which the $X_n$ are uniformly bounded. What if $\mu$ is $\sigma$-finite?

**Solution**

Based on exercise 2, if $\mu$ is finite, suppose that $\mu(\Omega) =  \mu_0$, then $\exists A, 0 < \epsilon_0 < \frac{\mu_0}{4}$, $\mu(A) < \epsilon_0$, and on $A^c$, there is $x_0 < \infty$ such that $|X| < x_0$. Since $X_n \xrightarrow{\text{a.e.}} X$, according to the convergence a.e. criterion, we have that 
$$
\mu \bigcup_\nu\left[\left|X_{n+\nu}-X\right| \ge \epsilon\right] \rightarrow 0.
$$
Therefore, there exists $N > 0$ such that when $n > N$, 
$$
\mu \bigcup_\nu\left[\left|X_{n+\nu}-X\right| \ge x_0 \right]:= \mu(A^\prime) < \frac{\mu_0}{4}.
$$
As a result, we have that as long as $n > N$, $|X_n| < 2x_0$. For the remaining $N$ elements, $X_1, \dots, X_N$, using the result of exercise 2 again, there exists $A_1, A_2, \dots, A_N$, all with measure $\frac{\mu_0}{4N}$ and on $A_i^c$, $X_i$ is bounded.  Let us denote 
$$
x_1 = \max\left\{2x_0, \max\left\{X_i(\omega): i=1,\dots,N, \omega\in \bigcup_{i=1}^N A_i\right\}\right\}.
$$
If we let
$$
B = \Omega - A - A^\prime - \bigcup_{i=1}^N A_i
$$
then on $B$, $|X_n| < x_1$, and 
$$
\mu(B) > \mu_0 - \epsilon_0 - \frac{\mu_0}{4} - N\cdot\frac{\mu_0}{4N} > \frac{\mu_0}{4} = 0.
$$
Therefore, $B$ is the set we are looking for. If $\mu$ is $\sigma$-finite, then just look at one of its finite partition and everything will be the same. $\square$

------

### Exercise 8

If $\mu$ is finite, then $X_{m n} \stackrel{\text { a.e. }}{\longrightarrow} X_m$ as $n \rightarrow \infty$ and $X_m \stackrel{\text { a.e. }}{\longrightarrow} X$ as $m \rightarrow \infty$ imply that there exists subsequences $m_k, n_k$ such that $X_{m_k n_k} \stackrel{\text { a.e. }}{\longrightarrow} X$ as $k \rightarrow \infty$. What if $\mu$ is $\sigma$-finite?
(Neglect the null sets of divergence. Select $A_k$ and $m_k$ such that $\mu A_k<\frac{1}{2^k}$ and $\left|X_{m_k}-X\right|<\frac{1}{2^k}$ on $A_k^c$. Select $B_k \subset A_k$ and $n_k$ such that $\mu B_k<\frac{1}{2^k}$ and $\left|X_{m_k n_k}-X_{m_k}\right|<\frac{1}{2^k}$ on $A_k-B_k$.)

**Solution**

If $\mu$ is finite, then using egoroff's theorem, we know that $X_{mn} \xrightarrow{\text{a.u.}} X_m$ and $X_m\xrightarrow{\text{a.u.}} X$. Now we begin the construction, for $k = 1, 2, \dots$, $\exists A_k$ such that $\mu(A_k) < \frac{1}{2^{k+1}}$ and $X_m \xrightarrow{\text{a.u.}} X$ on $A_k^c$. Therefore, $\exists M_1 >0$, when $m > M_1$, on $A_1^c$, $|X_m - X| < \frac{1}{2^2}$.  Take $X_{m_1} = X_{M_1+1}$. $\exists M_2 >0$, when $m_2 > M_2$,  on $A_2^c$, $|X_m - X| < \frac{1}{2^3}$.  Take $X_{m_2} = X_{\max\{m_1+1, M_2+1\}}$, etc. So we have selected $A_k$ and $m_k$ such that $\mu A_k<\frac{1}{2^{k+1}}$ and $\left|X_{m_k}-X\right|<\frac{1}{2^{k+1}}$ on $A_k^c$. 

Similarly, we can select $B_k$ and $n_k$ such that $\mu B_k<\frac{1}{2^{k+1}}$ and $\left|X_{m_k n_k}-X_{m_k}\right|<\frac{1}{2^{k+1}}$ on $B_k^c$. As a result, we know that on $C_k^c = A^c_k \cap B_k^c$, $\left|X_{m_k n_k}-X\right|<\frac{1}{2^{k}}$ by the triangular inequality. And we can derive that
$$
\mu\left(C_k\right) = \mu\left((A^c_k \cap B_k^c)^c\right) = \mu(A_k \cup B_k) < \frac{1}{2^k}
$$


As a result, since $\mu$ is finite, we can use the a.e. criterion, $\forall \epsilon > 0, \delta > 0$, let $k = \left\lceil 1 - \log_2\left(\min\{\epsilon, \delta\}\right)\right\rceil$ + 1, then
$$
\begin{aligned}
\mu\left(\bigcup_{v=0}^\infty \left[\left|X_{m_kn_k+v} - X\right|\ge \epsilon \right] \right) 
& \le \mu \left(\bigcup_{v=0}^\infty \left[\left|X_{m_kn_k+v} - X\right|\ge \frac{1}{2^{k+v}} \right] \right) \\
& = \sum_{v = 0}^{\infty} \frac{1}{2^{k+v}} = \frac{1}{2^{k-1}} < \delta
\end{aligned}
$$
This is equivalent to say that 
$$
\mu\left(\bigcup_{v=0}^\infty \left[\left|X_{m_kn_k+v} - X\right|\ge \epsilon \right] \right), \ k \to \infty
$$
And so $X_{m_kn_k}\xrightarrow{\text{a.e.}} X$.

If $\mu$ is $\sigma$-finite, we can prove the same conclusion on every $\mu$-finite partitions and then combine them together. Since the countable union of null set is still null, the a.e. condition holds for the universe $\Omega$ as well. $\square$

------

### Exercise 9 (Undone)

Let $X_n \stackrel{\mu}{\rightarrow} X, Y_n \stackrel{\mu}{\rightarrow} Y$. Do $a X_n+b Y_n \stackrel{\mu}{\rightarrow} a X+b Y,\left|X_n\right| \stackrel{\mu}{\rightarrow}|X|, X_n{ }^2 \stackrel{\mu}{\rightarrow}$ $X^2, X_n Y_n \stackrel{\mu}{\rightarrow} X Y$ ? What about $1 / X_n$ ? Let $\mu$ be finite and let $g$ on $\mathbb R$ or on $\mathbb R \times \mathbb R$ be continuous. What about the sequences $g\left(X_n\right)$ and $g\left(X_n, Y_n\right)$ ?

**Solution**

This is, in some sense, a combination of Slutsky Thoerem and continuous mapping theorem... I don't want to reinvent the wheel.

------

### Exercise 10 (Undone)

Let the functions $X_n, X$ on the measure space be complex-valued or vector-valued or, more generally, let them take their values in some fixed Banach space. Denote the norm of $X$ by $|X|$, and denote $\left|X_n-X\right| \rightarrow 0$ by $X_n \rightarrow X$.

Transpose the constructive definitions of measurability and the definitions of various types of convergence. Investigate the validity of the transposed of the corresponding properties established in the text, as well as of those stated above.

**Solution**

They work. Not interesting.

------

### Exercise 11

Examples and counterexamples of mutual implications of types of convergence. Investigate convergences of the sequences defined below:

1. The measure space is the Borel line with Lebesgue measure, $X_n=1$ on $[n, n+1]$ and $X_n=0$ elsewhere.
2. The measure space is the Borel interval $(0,1)$ with Lebesgue measure, $X_n=1$ on $\left(0, \frac{1}{n}\right)$ and $X_n=0$ elsewhere.
3. The measure space is the Borel interval $[0,1]$ with Lebesgue measure, the sequence is $X_{11}, X_{21}, X_{22}, X_{31}, X_{32}, X_{33}, \cdots$ with $X_{n k}=1$ on $\left[\frac{k-1}{n}, \frac{k}{n}\right]$ and $X_{n k}=0$ elsewhere.
4. $\mathfrak a$ consists of all subsets of the set of positive integers, $\mu A$ is the number of points of $A, X_n$ is indicator of the set of the $n$ first integers.

**Solution**

**For 1**, the limiting function could only be that $X = 0$. Therefore, it is not convergence in measure (the measure for deviating from 0 will always be 1). If we consider a.e. convergence, then we should investigate 
$$
\begin{aligned}
\mu \bigcap_n \bigcup_\nu\left[\left|X_{n+\nu}-X\right| \geqq \epsilon\right]
& = \mu \bigcap_n \bigcup_\nu\left[\left|X_{n+\nu}\right| \geqq \epsilon\right] \\ 
& = \mu \bigcap_n [n, \infty) \\
& = 0
\end{aligned}
$$
This is that for any $r < \infty, r\in \mathbb R$, there always exists $n > r$ so that $r$ is not in the intersection. Therefore, $X_n \xrightarrow{\text{a.e.}} X$. 

**For 2**, the limiting function should be $X = 0$ and for any $\epsilon > 0, \delta > 0$, we know that as long as $n > \frac{1}{\delta}$,
$$
\mu\left(\left[ |X_n - 0|\right] > \epsilon \right) \le \frac{1}{n} < \delta.
$$
Hence, $X_n \xrightarrow{\mu} X$.

On the other hand, since $\mu$ is finite on $(0, 1)$, we can use a simplified a.e. criterion. $\forall \epsilon$, consider 
$$
\begin{aligned}
\mu \bigcup_\nu\left[\left|X_{n+\nu}-X\right| \geqq \epsilon\right]
&= \mu\left(\left(0, \frac{1}{n}\right)\right) \to 0, \text{ as }n \to \infty.
\end{aligned}
$$
Hence, $X_n \xrightarrow{\text{a.e.}} X$ as well.

**For 3**, the limiting funtion here is still $X = 0$. The sequence $X_n \xrightarrow{\mu} X$ since $\forall \epsilon, \delta > 0$, as long as $n > \frac{1}{\delta}$,
$$
\mu\left(\left[ |X_n - 0|\right] > \epsilon \right) \le \frac{1}{n} < \delta.
$$
$\mu$ is still finite on $[0, 1]$ so we can consider the simplied criterion for a.e. convergence. Notice that 
$$
\begin{aligned}
\mu \bigcup_\nu\left[\left|X_{n+\nu}-X\right| \geqq \epsilon\right]
&= \mu\left(\left[0, 1\right]\right) = 1 \not\to 0, \text{ as }n \to \infty,
\end{aligned}
$$
We have no a.e. convergence here.

**For 4**, the limiting function $X$ could be either $0$ or $1$. For any finite $n$, $\mu\left(|X_n - 1| > \epsilon\right) > \infty - n$ and $\mu\left(|X_n| > \epsilon\right) = n$, this indicates the failure of convergence in measure. For a.e. convergene, if $X = 1$, then
$$
\begin{aligned}
\mu \bigcap_n \bigcup_\nu\left[\left|X_{n+\nu}-X\right| \geqq \epsilon\right]
& = \mu \bigcap_n \bigcup_\nu\left[\left|X_{n+\nu}\right| = 0 \right] \\ 
& = \mu \bigcap_n \bigcup_\nu \{A: A\subset \mathfrak a, A \ne \{1, \dots, n+\nu\}\} \\
& = \mu \bigcap_n \Omega > 0.
\end{aligned}
$$
If $X = 0$, then 
$$
\begin{aligned}
\mu \bigcap_n \bigcup_\nu\left[\left|X_{n+\nu}-X\right| \geqq \epsilon\right]
& = \mu \bigcap_n \bigcup_\nu\left[\left|X_{n+\nu}\right| = 1 \right] \\ 
& = \mu \bigcap_n \bigcup_\nu \{1, \dots, n+\nu\} \\
& = \mu \bigcap_n \Omega > 0.
\end{aligned}
$$
So failing to converge a.e. is obvious. $\square$

------

### Exercise 12 (Discussion)

If $X$ is integrable, then the set $[X \neq 0]$ is of $\sigma$-finite measure. What if $\int X$ exists? ($\mu[|X| \geqq c] \leqq \frac{1}{c} \int|X|$)

**Solution**

If $X$ is integrable, then $\int |X|$ is finite. Based on the hint, $\forall c \in \mathbb Z_+$, 
$$
\begin{aligned}
	\mu\left[|X| \ge c \right] 
	& = \int \mathbb I_{\{|X| \ge c\}} d\mu \\ 
	& \le \frac{1}{c}\left[\int c \mathbb I_{\{|X| \ge c\}} d\mu + \int |X| I_{\{|X| < c\}} d\mu\right] \\
	& \le \frac{1}{c}\int |X| d\mu = \frac{1}{c}\int |X| < \infty.
\end{aligned}
$$
Therefore, since 
$$
[X \ne 0] = \bigcup_{c=0}^\infty\left[ |X| > c \right],
$$
we know that $[X \ne 0]$ is of $\sigma$-finite measure.

If only $\int X$ exists, then we cannot say something like the previous part. Consider the case when there is $c_0$ such that $\{X > c_0\}$ with $\mu = \infty$. The negative part could still be finite. Notice that if $X$ is integrable, then sets like $\{X > c_0\}$ cannot have infinite $\mu$.  $\square$

------

### Exercise 13 (Undone)

Let $(T, \mathfrak T, \tau)$ be a measure space, to every point $t$ of which is assigned a measure $\mu_t$ on $\mathfrak a$. Let the function on $T$ defined by $\mu_t A$ for any fixed $A$ be $\mathfrak T$-measurable.

The relation $\mu A=\int_T \mu_t A d \tau(t)$ defines a measure $\mu$ on $\mathfrak a$. If $\int_{\Omega} X(\omega) d \mu(\omega)$ exists, then the function defined on $T$ by $U(t)=\int_{\Omega} X(\omega) d \mu_t(\omega)$ exists and is $\mathfrak T$-measurable, and $\int_{\Omega} X(\omega) d \mu(\omega)=\int_T U(t) d \tau(t)$.

------

### Exercise 14

Let $\varphi$ be the indefinite integral of $X$. Express $\varphi^{+}, \varphi^{-}, \bar{\varphi}$ in terms of $X$.

**Solution**
$$
\varphi(\cdot) = \int_{\cdot} X d\mu
$$
Based on the definition of $\varphi^+$, we know that for $A, B \in \mathfrak a$
$$
\varphi^+(A) = \sup_{B\subset A} \varphi(B) = \sup_{B\subset A} \int_{B} X d\mu = \int_A X^+ d\mu
$$
Similarly, we know that 
$$
\varphi^-(\cdot) = \int_{\cdot} X^- d\mu
$$
And so 
$$
\bar\varphi(\cdot) = \int_{\cdot} (X^+ + X^-) d\varphi = \int_{\cdot} |X| d\mu.
$$
$\square$

------

### Exercise 15

If $\int_A X_n \rightarrow 0$ uniformly in $n$ as $\mu A \rightarrow 0$ or as $A \downarrow \emptyset$, then the same is true of $\int_A\left|X_n\right| ;$ and conversely. Interpret in terms of signed measures.
$$
\left(\int_A\left|X_n\right|=\int_{A\left[X_n \geqq 0\right]} X_n-\int_{A\left[X_n<0\right]} X_n .\right)
$$
**Solution**

This is closely related to the previous question. If $\varphi_n(A)\to 0$ uniformly, then
$$
\begin{aligned}
 & \varphi_n^+(A) = \sup_{B\subset A} \varphi_n(A) \xrightarrow{\text u} 0,\quad \varphi_n^-(A) = -\inf_{B\subset A} \varphi_n(A)\xrightarrow{\text u} 0  \\
 \implies & \bar\varphi_n(A) = \varphi_n^+(A) + \varphi_n^-(A) \xrightarrow{\text u} 0\\
 \implies & \int _A |X_n| \xrightarrow{\text u} 0.
 \end{aligned}
$$
The converse is obvious since  $|\int_A  X_n| \le \int_A |X_n| $. $\square$

------

***Dominated convergence theorem**. If $\left|X_n\right| \leqq Y$ a.e. with $Y$ integrable and if $X_n \stackrel{\text { a.e. }}{\rightarrow} X$ or $X_n \stackrel{\mu}{\rightarrow} X$, then $\int X_n \rightarrow \int X$. In fact, $\int_A X_n-\int_A X \rightarrow 0$ uniformly in $A$ or, equivalently, $\int\left|X_n-X\right| \rightarrow 0$.*

### Exercise 16

If finite $\int_A X_n \rightarrow \int_A X$ finite, uniformly in $A(\in \mathfrak a)$, then $\int_{\Omega}\left|X_n-X\right| \rightarrow 0$  ; and conversely.

**Solution**

This is related to the proof of dominated convergence theorem. By the given condition, uniformly in $A\in \mathfrak a$,
$$
\int_A (X_n - X) \xrightarrow{\text u } 0.
$$
This gives us the right to choose $A$ aribitrarily. And $\forall \epsilon > 0, A\in \mathfrak a$, $\exists N$ such that when $n > N$, 
$$
\left|\int_A (X_n - X)\right| < \frac{\epsilon}{2}
$$
Now for each $n$, let $A_{n_1} = [X_n \ge X], A_{n_2} = [X_n < X]$, then as long as $n > N$, we will have 
$$
\int_\Omega (X_n - X)^+ = \left|\int_{A_{n_1}} (X_n - X)\right|, \quad \int_\Omega (X_n - X)^- = \left|\int_{A_{n_1}} (X_n - X)\right|
$$
And so
$$
\int_\Omega |X_n - X| = \int_\Omega (X_n - X)^+ + \int_\Omega (X_n - X)^- < \epsilon
$$
which means $\int_{\Omega}\left|X_n-X\right| \rightarrow 0$.

The converse is true since $\forall$ $A \in \mathfrak a$
$$
\left|\int_A (X_n - X)\right| \le \int_A |X_n- X| \le \int_{\Omega} |X_n - X| \to 0
$$
Therefore, $\forall \epsilon > 0$, $\exists N$ such that when $n > N$,
$$
0 \le \left|\int_A (X_n - X)\right| \le \int_A |X_n- X| \le \int_{\Omega} |X_n - X| < \epsilon.
$$
Since this applies to all $A$'s, we have uniform convergence here.

------

### Exercise 17

If $0 \leqq X_n \stackrel{\mu}{\rightarrow} X$, then finite $\int_{\Omega} X_n \rightarrow \int_{\Omega} X$ finite implies that $\int_A X_n \rightarrow$ $\int_A X$ uniformly in $A$ (also if $\stackrel{\mu}{\longrightarrow}$ is replaced by $\stackrel{\text { a.e. }}{\longrightarrow}$ )
$\left(0 \leqq\left(X-X_n\right)^{+} \leqq X\right.$ integrable, and $\left.\int\left(X-X_n\right)^{+}-\int\left(X-X_n\right) \rightarrow 0.\right)$

**Solution**

According to exercise 16, if we could show that 
$$
\int_{\Omega} |X_n - X| \to 0,
$$
then the uniform convergence is true. 

Then it is equivalent to show that 
$$
\int_{\Omega} (X - X_n)^+ + \int (X - X_n)^- \to 0.
$$
Because $(X - X_n)^+ \le |X - X_n|$, by the definition of convergence in measure, $X_n \xrightarrow{\mu} X$ implies $(X_n - X)^+ \xrightarrow{\mu} 0$. Since $0 \le (X - X_n)^+ \le |X|$ integrable, by the dominated convergence theorem, 
$$
\int_{\Omega} |(X - X_n)^+| = \int_{\Omega} (X - X_n)^+ \to 0
$$
On the other hand, we know from the given condition that
$$
\int_{\Omega} (X - X_n) \to 0
$$
As a result, 
$$
\int_{\Omega} (X_n - X)^ - = \int_{\Omega} (X - X_n)^+ - \int_{\Omega} (X - X_n) \to 0 \implies \int_{\Omega} |X_n - X| \to 0,
$$
and so by exercise 16, we know that $\int_A X_n \rightarrow$ $\int_A X$ uniformly in $A$. Changing $\mu$ to $\text{a.e.}$ will not affect our application of dominated convergence theorem here so the conclusion still holds. $\square$

------

### Exercise 18 (Undone)

Rewrite in terms of integrals as many as possible of the complements and details of Chapter I.

------

***RADON-NIKODYM THEOREM** If, on $\mathfrak a$, the measure $\mu$ and the $\sigma$-additive set function $\varphi$ are $\sigma$-finite and $\varphi$ is $\mu$-continuous, then $\varphi$ is the indefinite integral of a finite function determined up to an equivalence.*

***An interesting fact.***

*If a random variable $Y > 0$ is integrable, then for $n \in \mathbb Z_+$*,  
$$
\int_{\{Y > n\}} Y  \to 0 \text{ as } n\to \infty.
$$
*This is because we can construct a sequence $Y_n = Y\mathbf{1}\{Y \le n\}$, then we know that $0\le Y_n \uparrow Y$. By monotone convergence theorem, we know that* 
$$
\int Y_n \to \int Y \implies \int_{Y >n} Y = \int Y - \int Y_n \to 0.
$$

### Exercise 19 (Discussion)

If the $X_n$ are integrable and $\lim \int_A X_n$ exists and is finite for every $A$, then the $\int\left|X_n\right|$ are uniformly bounded, $\int_A\left|X_n\right| \rightarrow 0$ uniformly in $n$ as $\mu A \rightarrow 0$ and as $A \downarrow \emptyset$, and there exists an integrable $X$, determined up to an equivalence, such that $\int_A X_n \rightarrow \int_A X$ for every $A$. (Use 18.)

**Solution**

Is it about uniformly integrability?

Using the conclusion of 14, we can define $\varphi_n(A) = \int_A X_n$. With the condition $\mu A \to 0$ and $A \downarrow \empty$,  we have that $\varphi_n \to 0$. Conditioned on $A\downarrow 0$, $\varphi_n A \to 0$ as $\mu A \to 0$.  Then, with the same logic for exercise 18 of chapter 1, we know that $\varphi_n A \to 0$ uniformly as $\mu A \to 0$ and $A \downarrow \emptyset$  and $\varphi = \lim \varphi_n$ is $\mu$-continuous and $\sigma$-additive.

The question here is why we need $A\downarrow\emptyset$. Maybe because we try to avoid things like Dirac function? But in the next question, it seems that this condition could be suppressed when $\mu$ is finite. 

The fact that $\varphi_n A \to 0$ uniformly as $\mu A \to 0$ and $A \downarrow \emptyset$, plus the conclusion in exercise 15 implies that $\int_A\left|X_n\right| \rightarrow 0$ uniformly in $n$ as $\mu A \rightarrow 0$ and as $A \downarrow \emptyset$ (since $\varphi_n$'s are all finite, then by exercise 9 of chapter 1 it is true).  The $\mu$-continuity and the $\sigma$-additivity of $\varphi$, along with the Radon-Nikodym theorem tells us that $\varphi$ is an indefinite integral of some $X$ up to an equivalence and 
$$
\varphi_n \to \varphi \implies \text{ for every A, } \int_A X_n \to \int_A X.
$$
The only thing that remains to prove is that $\int |X_n|$ are uniformly bounded. 



### Exercise 20 (Discussion)

If integrable $X_n \rightarrow X$ integrable, then existence and finiteness of $\lim \int_A X_n$ for every $A$ are equivalent to the following properties:

(1)	$\int_A X_n \rightarrow \int_A X$ uniformly in $A$.

(2)	$\int_A X_n \rightarrow 0$ uniformly in $n$ as $\mu A \rightarrow 0$ and as $A \downarrow \emptyset$.

If $\mu$ is finite, then "as $A \downarrow \emptyset$ " can be suppressed. (Use the preceding propositions and the relations
$$
\begin{gathered}\int_A\left|X_n\right| \leqq \int_A\left|X_n-X\right|+\int_A|X|, \\ \int_A\left|X_n-X\right| \leqq \epsilon+\int_{A\left[\left|X_n-X\right| \geqq \epsilon\right]}\left(\left|X_n\right|+|X|\right)\end{gathered}
$$
)

**Solution**

This seems to be a continuation of the discussion of uniform integrability.

Similarly to exercise 17. We will have that $X_n^+ \to X^+$ and $X_n^- \to X^-$ on $\Omega$. On the other hand, $0 \le (X^+ - X_n^+)^+ \le X^+$ integrable. By dominated convergence theorem, we know that
$$
\int (X^+ - X_n^+)^+ \to 0
$$
On the other hand, we know that 
$$
\int (X^+ - X_n^+) \to 0
$$
And so following the same logic in exercise 17,
$$
\int |X^+ - X_n^+| \to 0.
$$
Similarly, we will have 
$$
\int |X^- - X_n^-| \to 0.
$$
Therefore,
$$
\int_{\Omega} |X_n - X| \le \int_{\Omega} |X^+ - X_n^+| + \int_\Omega |X^- -  X_n^-| \to 0,
$$
which means that $\int_A X_n \rightarrow \int_A X$ uniformly in $A$.

Without the condition that $\mu$ is finite, proposition (2) is proved in the exercise 19.

But what happens when $\mu$ is finite?

------

### Exercise 21

The differential formalism applies to Radon-Nikodym derivatives:
Let $\mu, \nu$ be finite measures on $\mathfrak a$ and $\varphi, \varphi^{\prime}$ be $\sigma$-finite signed measures on $\mathfrak a$. Let $\varphi$ be $\nu$-continuous and $\nu, \varphi, \varphi^{\prime}$ be $\mu$-continuous. Then
$$
\begin{gathered}
\frac{d\left(\varphi+\varphi^{\prime}\right)}{d \mu}=\frac{d \varphi}{d \mu}+\frac{d \varphi^{\prime}}{d \mu} \quad \mu \text {-a.e. } \\
\frac{d \varphi}{d \mu}=\frac{d \varphi}{d \nu} \frac{d \nu}{d \mu} \quad \mu \text {-a.e. }
\end{gathered}
$$
(For the second assertion, it suffices to consider $\varphi \geqq 0, X=\frac{d \varphi}{d \nu} \geqq 0$ $Y=\frac{d \nu}{d \mu} \geqq 0$. Take simple $X_n$ with $0 \leqq X_n \uparrow X$ so that
$$
\int_A X d \nu \leftarrow \int_A X_n d \nu=\int_A X_n Y d \mu \rightarrow \int_A X Y d \mu 
$$
)

**Solution**

https://math.stackexchange.com/questions/4384565/additivity-of-radon-nikodym-derivatives-of-signed-measures

For the first statement, for any set $A$,
$$
\int_A\frac{d(\varphi+\varphi^\prime)}{d\mu} d\mu = \varphi + \varphi^\prime = \int_A \frac{d\varphi}{d\mu} d\mu + \int_A \frac{d\varphi^\prime}{d\mu} d\mu = \int_A \frac{d\varphi}{d\mu} + \frac{d\varphi^\prime}{d\mu} d\mu
$$
The last equality comes from the additivity property stated on page 124. Therefore, $\frac{d\left(\varphi+\varphi^{\prime}\right)}{d \mu}=\frac{d \varphi}{d \mu}+\frac{d \varphi^{\prime}}{d \mu} \quad \mu \text {-a.e. }$. Otherwise, there will be a set with positive measure such that the left-hand side is greater than the right-hand side, which means that the equality will not hold for this particular set.

 
