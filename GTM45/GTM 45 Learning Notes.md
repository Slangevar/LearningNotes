# GTM 45 Probability Theory I

## Chapter 1 Exercise

The measurable sets belong to a fixed $\sigma$-field on which the set functions and limits of their sequences are defined. Unless otherwise stated and with or without affixes, $A, B, ...$ denote sets, $\mu$ denotes a measure, $\varphi$ denotes a signed measure. Notice that a signed measure is $\sigma$-additive.

A nonnegative additive set function is called a content or a measure according as it is finitely additive or $\sigma$-additive. Signed measures are differences of two measures of which one at least is finite. 

------

### Exercise 1

If $\varphi$ is $\sigma$-finite, then there are only countably many disjoint sets for which $\varphi \neq 0$ in every class.

*Note: A set function $\varphi$ is defined on a nonempty class $\mathcal{C}$ of sets in a space $\Omega$ by assigning to every set $A \in \mathcal{C}$ a single number $\varphi(A)$, finite or infinite, the value of $\varphi$ at $A$. If all values of $\varphi$ are finite, $\varphi$ is said to be finite, and we write $|\varphi|<\infty$. If every set in $\mathcal{C}$ is a countable union of sets in $\mathcal{C}$ at which $\varphi$ is finite, $\varphi$ is said to be $\sigma $-finite.*

**Solution**	

If we let every class we are considering be a $\sigma$-field $\mathfrak{a}$ over the space $\Omega$, then the proof is as follows. 

Based on the definition of signed measure, one of $\varphi^+$ and $\varphi^-$ should be finite. Therefore, every set in $\mathfrak{a}$ is also a countable union of sets in $\mathfrak{a}$ at which $\varphi^+$ and $\varphi^-$ is finite (so that there is no set with infinite value of $\varphi$). 

According to the given condition, the space $\Omega$ could be expressed as a countable union of subsets of itself, i.e. $\cup_{n=1}^\infty A_n$ or $\cup_{n=N}^\infty A_n$ where each $A_n$ has finite value of $\varphi$, which also means that $\varphi^+$ and $\varphi^-$ has finite value over these sets.

Now suppose there are uncountably many disjoint sets for which $\varphi \ne 0$. Denote them as $B_i, i\in \mathcal I$ where $\mathcal I$ is some index set. We know that $\cup_n A_n \supe \cup_i B_i$.  Therefore, at least one of $A_{n_0}$ is a union of uncountably many $B_{i^\prime} \in \{B_i\}$ whose corresponding value of $\varphi$ is finite and nonzero. This means that there should be uncountably many sets $B_{i^{''}} \in \{B_{i^{'}}\}$ over which the value of $\varphi^+$ or $\varphi^-$ is positive. Without loss of generality, assume it is $\varphi^+$. We have that $\cup B_{i^{''}}\sube A_{n_0}$ and so $0 < \varphi^+(\cup {B_{i^{''}}}) < \varphi^+(A_{n_0}) < \infty$. 

Now we only need to prove that only countably many elements in $\cup {B_{i^{''}}}$ is positive, which, by contradiction, will prove our proposition. Suppose $\varphi^+(\cup {B_{i^{''}}}) < M$. Then for an arbitrary positive integer $N$, $\mathcal B_{N} = \{B_{i^{ii}} \subset \mathcal B| \varphi^+(B_{i^{''}}) > \frac{1}{N}\}$ has at most $NM$ elements . Therefore, the set for all ${B_{i^{''}}}$'s such that the corresponding value of $\varphi^+$ is positive is $\cup_{N=1}^\infty\mathcal B_N$. This union is a countable union over finite sets which has countably many members. This means that for $\varphi^+$ and so $\varphi$, it is always true that we can only find countably many disjoint sets whose corresponding function value is finite and nonzero. 

Therefore, we found a contradiction.	$\square$ 

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
2|\varphi(B)| = 2|\psi^+(B) - \psi^-(B)| = 2\psi^+(B) = 2\psi^+(A)
$$
On the other hand,
$$
\bar \varphi(A) = \psi^+(A) + \psi^-(A) \le 2 \psi^+(A)
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

### Exercise 7

If $\mu$ is finite, then $\Omega=\sum A_j+A$ where the $A_j$ or $A$ may be absent but, if present, then the $A_j$ are $\mu$-atoms of positive measure and, for every $B \subset A$ of positive measure, $\mu$ takes every value $c$ between 0 and $\mu B$ for measurable subsets of $B$. This decomposition of $\Omega$ is determined up to $\mu$-null sets. Can $\mu$ be replaced by $\varphi$ ?

(There is only a countable number of $\mu$-equivalence classes of such $A_j$ 's. Select representatives $A_j$ of these classes and let $B \subset A=\Omega-\sum A_j$. Select inductively sets $C_n \in \mathcal{C}_n$ such that $\mu C_n>\sup \mu C-\frac{1}{n}$ for all $C \in \mathcal{C}_n$, where $\mathcal{C}_n$ is the class of all $C \subset B-\left(C_1 \cup C_2 \ldots \cup C_{n-1}\right)$ for which $\mu C \leqq c-$ $\mu\left(C_1 \cup C_2 \cup \ldots \cup C_{n-1}\right)$. Then $\mu C=c$ for $\left.C=\bigcup C_{n .}\right)$

**Solution**

According to the statement, only $A$ could be non-atomic. $\Omega=\sum A_j+A$ is given so we do not prove that $A_j$ is $\mu$-atoms.  Now suppose we have such $A_j$'s, then clearly there are only coutably many of $\mu$-equivalent classes of them. Otherwise, uncountably sum of positive values will lead to infinite value of $\mu(\Omega)$ which is contradictory. Select representatives $A_j$ of these classes and let $B \subset A=\Omega-\sum A_j$. 

We now actually wants to show that $A$ could be "infinitely divided" into sets with smaller measures. Based on the hint, we can inductively select sets. Let $n = 1$, then can we select a set $C_1$ from $B$ such that $C_1 \in \mathcal{C}_1$ such that $\mu C_1>\sup \mu C-1$ for all $C \in \mathcal{C}_1$, where $\mathcal{C}_1$ is the class of all $C \subset B$ for which $\mu C \le c$. We only need to show that there are sets satisfying $\mu C \le c$ and the rest is obvious since we could always select the that $C_1$ based on the definition of $\sup$. 

If there is no $C\subset B$ such that $\mu C \le c$, then it will lead to a contradictory since it means that there is also no sets $D\subset$ satisfying $\mu D \ge \mu B - c$. We can take a sequence $D_n \to B$, so that $B-D_n \to \emptyset$ while $\mu(B-D_n) \ge \mu B -c > 0$, which is impossible since $\mu$ is continuous (*CONTINUITY THEOREM FOR ADDITIVE SET FUNCTIONS*). So that we can always find $C$'s with $\mu C \ge c$. 

Similarly, we could find $C_2$, $C_3$, $\dots$ We know that $\mu\left(\bigcup_{i=1}^n C_n\right)$ is an increasing sequence. Moreover, by the construction we know that $\mu\left(\bigcup_{i=1}^n C_n\right) - \frac{1}{n} > c$ since $\sup \mu C \ge c - \mu\left(C_1 \cup C_2 \cup \ldots \cup C_{n-1}\right)$ (Actually each $C_i$ is disjoint with each other, and this inequality follows from the non-atomic property of $B$ as we argue previously). Therefore, by the continuity, $\lim_{n\to\infty} \mu\left(\bigcup_{i=1}^n C_n\right) = \mu\left(\lim_{n\to\infty}\bigcup_{i=1}^n C_n\right) = c$. Then $\mu C=c$ for $C=\bigcup C_{n .}$ 

Can $\mu$ be replaced by $\varphi$? Is it possible for $\varphi$ to take every value $c$ between some values? 

We may show that $\varphi$ could take any value between $-\varphi^-$ and $\varphi^+$. Since $\varphi = \varphi^+ - \varphi^-$, $\varphi$ being an additive function, it can not take values outside the aforementioned range within a measurable $B \subset A$.  By Jordan-Hahn decomposition theorem, there exists $BD \subset B$ such that $\varphi(BD) = \varphi^+(B)$ and $BD^c \subset B$ such that $\varphi(BD^c) = -\varphi^-(B)$. So that $\varphi$ could take values at the edge. How about the in-between values? Again, by Jordan-Hahn decomposition theorem, we know that $\varphi+$ and $\varphi^-$ are measures, which means that, based on the conclusion for $\mu$,  for any values $c^+$ between $0$ and $\varphi^+(B)$, there exists $C^+ \subset B$ such that $\varphi^+(C^+) = c^+$ and so $C^+D \subset B$ satisfies $\varphi(C^+D) = c^+$. Similarly, we have for any values $c^-$ between $\varphi^-(B)$ and 0 such that there is $C^- D \subset B$ and $\varphi(C^-D) = c^-$. So the conclusion also works for the signed measure. $\square$

------

### Exercise 8

If $\varphi$ is finitely additive, $\mu$ is finite, and $\mu A_n \rightarrow 0$ implies $\varphi A_n \rightarrow 0$, then $\varphi$ is $\sigma$-additive. *We say that $\varphi$ is $\varphi_0$-continuous if $\varphi_0 A=0$ implies $\varphi A=0$*.

**Solution**

Consider a sequence of sets $A_n \uparrow A$ for some $A$ as $n\to \infty$.  we know that $B_i = A - A_i \to \empty$  as $n\to \infty$. Since $\varphi$ is finitely addtive, for any $n$ we have 
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

### Exercise 9

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

If $\mu_j$'s are replaced by signed measures $\varphi_j$'s. Let's consider $\varphi_j^+$ and $\varphi_j^-$'s. Following the same manner we can construct $\varphi^\pm$ such that $\varphi^\pm = 0 \implies \varphi_j^\pm$. If we consider $\bar \varphi$, then $\bar\varphi = 0$ iff $\varphi^\pm = 0$.  Therefore, 
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

### Exercise 11

*Decomposition theorem*. $\varphi_r$ is regular, $\varphi_s$ is singular, and $\varphi=\varphi_r+\varphi_{\mathrm{s}}$. If $\varphi$ is finite, then the decomposition of $\varphi$ into a regular and a singular part is unique. What if $\varphi$ is $\sigma$-finite? What if $\mathfrak a$ consists of all subsets of a noncountable space, and $\varphi(A)$ equals the number of points of $A$ ? (Proceed as follows:

1. $B(\varphi)=B(\bar{\varphi})=B\left(\varphi^{+}\right) \cap B\left(\varphi^{-}\right)$is a $\sigma$-field.
2. $\varphi_r\left(\varphi_s\right)$ is a regular (singular) signed measure.
3. Every $A$ contains disjoint $A_r$ regular and $A_s$ singular such that $\varphi_r \pm(A)$ $=\varphi^{ \pm}\left(A_r\right), \varphi_s^{ \pm}(A)=\varphi^{ \pm}\left(A_s\right)$.
4.  If $A=A^{\prime}{ }_r+A^{\prime}$, with $A^{\prime}$, regular and $A^{\prime}$, singular, then we can take $A_r=A^{\prime}{ }_r$ and $A_s=A^{\prime}{ }_s$.
5.  If $\varphi$ is finite, every $A$ can be so decomposed.)

**Solution**

### Exercise 12

We can take for singular sets:

1. the $\mu$-null sets-regular (singular) becomes $\mu$-continuous ( $\mu$-discontinuous);
2. the countable measurable sets-regular (singular) becomes continuous (purely discontinuous);
3.  the countable sums of atoms-regular (singular) becomes nonatomic (atomic).

In each case investigate the regular and singular parts.

------

### Exercise 13

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
Same techniques apply for $\varphi^-$.

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

### Exercise 15

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
\sum_{k=1}^K \varphi(A_k) - \epsilon < \sum_{k=1}^K\varphi_{N_k+1}(A_k) \le \sum_{k=1}^K\varphi_{N_K+1}(A_k) \le \varphi_{N_K+1}\left(\sum_{k=1}^K A_k \right) \le \varphi\left(\sum_{k=1}^K A_k \right)
$$
Therefore, $\forall \epsilon > 0, K < \infty$, $\sum_{k=1}^K \varphi(A_k) - \epsilon < \varphi\left(\sum_{k=1}^K A_k \right) \implies \sum_{k=1}^K \varphi(A_k) \le \varphi\left(\sum_{k=1}^K A_k \right)$. Since taking limit preserves partial inequality, we must have $\sum_{k=1}^\infty \varphi(A_k) \le \varphi\left(\sum_{i=1}^\infty A_k \right)$.

Hence, $\sum_{k=1}^\infty \varphi(A_k) = \varphi\left(\sum_{i=1}^\infty A_k \right)$. For $\varphi_n \downarrow$, let 
$$
M = \sup_{B \subset \sum_{i=1}^\infty A_k} \varphi_1(B)
$$
Just consider $\varphi_n^\prime = M - \varphi_n \uparrow$. $\square$

------

### Exercise 16

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

### Exercise 17

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

$\forall \delta > 0$, based on the $\mu$-continuity, since $\varphi_n$'s are finite, based on exercise 9, $\exists J$ such that if $j > J$, then for given $m, n > k$,  $|\varphi_m(B_j) - \varphi_m(B)| < \frac{\delta}{2}$ and $|\varphi_n(B_j) - \varphi_n(B)|  < \frac{\delta}{2}$. This is because the symmetric difference goes to $\emptyset$ and $\varphi_m$ as well as $\varphi_n$ are finite and $\sigma$-additive (so that we will have continuity at $\emptyset$).  Therefore, 
$$
|\varphi_m(B) - \varphi_n(B)| \le |\varphi_m(B_j) - \varphi_m(B)| + |\varphi_m(B_j) - \varphi_n(B_j)| + |\varphi_n(B_j) - \varphi_n(B)| = \frac{\epsilon}{3} + \delta.
$$
Since $\delta$ could be arbitrarily small, we must have $|\varphi_m(B) - \varphi_n(B)| \le \frac{\epsilon}{3}$. This means that $A_k$ is closed.

By Baire's category theorem, there exists $k_0, d_0$ and $A_0 \in \mathcal X$ such that $\left[A \in \mathcal X ; d\left(A, A_0\right)<d_0\right] \subset A_{k_0}$. Why?  

First of all, we know that $\mathcal X$ contains a sphere, which is in the form of $\widetilde{\mathcal X} = \left[A \in \mathcal X ; d\left(A, A_0\right) < d_0\right]$. Now, we need to show that there exists $k_0$ such that $\widetilde{\mathcal X} \subset A_{k_0}$. Since by asssumption, $\varphi_n \to \varphi$, for $\widetilde{\mathcal X}$, there exists $N_0 > 0$ such that when $m, n > N_0$ ,  $\left|\varphi_n(\widetilde{\mathcal X}) - \varphi_m(\widetilde{\mathcal X})\right| < \frac{\epsilon}{3}$ (convergence to mutual convergence for real sequence). Take $k_0 = N_0 + 1$ then $\widetilde{\mathcal X} \subset A_{k_0}$.

By $\mu$-continuity, $\exists \delta_0$ such that when $\mu A(\text{ or some }A_m) < \delta_0$, $|\varphi_n A| < \frac{\epsilon}{3}$ where $n \le k_0$ (finite $n$'s). This could always be done based on exercise 9, i.e., $\mu \to 0$ implies $\varphi_n \to 0$ because of finiteness. If $\mu A<\delta_0$, then 
$$
d\left(A_0-A, A_0\right) = \mu\left((A_0 - A)^c A_0 + (A_0 - A)A_0^c\right) = \mu(A_0\cap A) \le \mu(A) < \delta_0 < d_0,
$$

$$
d\left(A_0 \cup A, A_0\right) = \mu((A_0\cup A)^c A_0 + (A_0\cup A)A_0^c) = \mu(A - A_0) < \mu(A) < \delta_0 < d_0.
$$

This means that $A_0 - A$ and $A_0 \cup A$ are elements in $A_{k_0}$.

And so, 
$$
\begin{aligned}
\left|\varphi_n A\right| & = \left|\varphi_{k_0} A + \varphi_n A - \varphi_{k_0} A \right|\\
& \le |\varphi_{k_0} A + \varphi_n (A_0 \cup A - (A_0 - A)) - \varphi_{k_0} (A_0 \cup A - (A_0 - A))|\\
& \le\left|\varphi_{k_0} A\right|+\underbrace{\left|\varphi_n\left(A_0 \cup A\right)-\varphi_{k_0}\left(A_0 \cup A\right)\right|+\left|\varphi_n\left(A_0-A\right)-\varphi_{k_0}\left(A_0-A\right)\right|}_{C_0} \\

\end{aligned}
$$

As we know, since $|\varphi_n A| < \frac{\epsilon}{3}$, we must have $C_0 < \frac{\epsilon}{3}$ otherwise we will have negative $|\varphi_{k_0} A|$.

On the other hand 
$$
\begin{aligned}
|\varphi_{k_0} A| &= |\varphi_n A + \varphi_{k_0}A - \varphi_n A| \\
& \le\left|\varphi_{n} A\right|+\left|\varphi_n\left(A_0 \cup A\right)-\varphi_{k_0}\left(A_0 \cup A\right)\right|+\left|\varphi_n\left(A_0-A\right)-\varphi_{k_0}\left(A_0-A\right)\right| \\
& \le \epsilon + C_0 \le \frac{2\epsilon}{3}
\end{aligned}
$$
Eventually, $t > k_0$, since $A_0 - A$ and $A_0 \cup A$ are elements in $A_{k_0}$,
$$
\begin{aligned}
\left|\varphi_n\left(A_0 \cup A\right)-\varphi_{t}\left(A_0 \cup A\right)\right| & \le \left|\varphi_t\left(A_0 \cup A\right)-\varphi_{k_0}\left(A_0 \cup A\right)\right| + \left|\varphi_n\left(A_0 \cup A\right)-\varphi_{k_0}\left(A_0 \cup A\right)\right| \\
& \le \left|\varphi_n\left(A_0 \cup A\right)-\varphi_{k_0}\left(A_0 \cup A\right)\right| + \frac{\epsilon}{3}
\end{aligned}
$$
Similarly, we will have 
$$
\left|\varphi_n\left(A_0-A\right)-\varphi_{t}\left(A_0-A\right)\right|  \le \left|\varphi_n\left(A_0-A\right)-\varphi_{k_0}\left(A_0-A\right)\right| + \frac{\epsilon}{3}
$$
As a result, 
$$
|\varphi_t A| \le |\varphi_n A|+ C_0 + \frac{\epsilon}{3} \le \frac{4}{3}\epsilon
$$
Hence, as long as $\mu A < \delta_0$ we will have $\forall n > 0$, $\varphi_n A \le \frac{4}{3}\epsilon $. This means uniform $\mu$-continuity. The definition of $A_{k_0}$ guarantees that $|\varphi A| \le \frac{4}{3}\epsilon$ as well because the argument would be the same as that for $\varphi_t$ based on the fact that taking the limit will preserve the inequality condition for $A_{k_0}$. As a result, we prove for the $\mu$-continuity for $\varphi$ as well.

By exercise 8, we know that if $\mu$ is finite, $\varphi$ being $\mu$-continuous and finitely additive, then $\varphi$ is $\sigma$-additive. The finite addtivity is obvious since the limit of the finite sum is the finite sum of the limit. On the other hand, in this exercise, we know that $\mu$ is $\sigma$-finite, which means that if we ignore trivialities, there is at least one finite value for $\mu$. This means that $\mu(\emptyset) = 0$. Based on the continuity of $\sigma$-additive function, i.e., $\mu(\lim A_n) = \lim \mu(A_n)$, and using the same argument of exercise 8, we can claim that $\varphi$ is $\sigma$-additive. Here we don't have the special case in exercise 9 since $\varphi$ is guaranteed to be finite.

 $\square$

### Exercise 19

If finite $\varphi_n \rightarrow \varphi$ finite, then $\varphi$ is $\sigma$-additive. (If $\left|\varphi_n\right| \le c_n$, set $\mu A=\sum \frac{1}{2^n c_n}\left|\varphi_n A\right|$ and apply 18.)

**Solution**

If $\left|\varphi_n\right| \le c_n$, set $\mu A=\sum \frac{1}{2^n c_n}\left|\varphi_n A\right|$ . Then $\varphi_n$'s are $\mu$-continuous, i.e. $\mu A = 0 \implies \varphi_n A = 0$. By exercise 18, $\varphi_n$ are uniformly $\mu$-continuous and $\lim \varphi_n=\varphi$ is $\mu$-continuous and $\sigma$-additive. $\square$

## Chapter 2 Exercise

**Notation.** Unless otherwise stated, the measure space $(\Omega,\mathfrak a, \mu)$ is fixed, the (measurable) sets $A, B, ...,$ with or without affixes, belong to $\mathfrak a$ and the functions $X, Y, \dots$ with or without affixes, are finite measurable functions.

### Exercise 1

The set $C$ of convergence of a sequence $X_{n}$ (to a finite or inlinite limit function) is measurable.
$$
(C=\left[\operatorname*{lim}\,\operatorname{inf}X_{n}=\operatorname*{lim}\,\operatorname*{sup}\,X_{n}\right].)
$$

### Exercise 2

If $\mu$ is finite, then given X, for every $\epsilon > 0$ there exists $A$ such that $\mu A<\epsilon$ and $X$ is bounded on $A^{c}.$ If $X$ is bounded, then there exists a sequence of simple functions which coniverges uniformly to $X.$ Combine both propositions.

We say that a sequence $X_n$ converges almost uniformly (a.u.) to $X$, and write $X_n \stackrel{\text { a.u. }}{\longrightarrow} X$, if, for every $\epsilon>0$, there exists a set $A$ with $\mu A<\epsilon$ such that $X_n \stackrel{\mathrm{u}}{\longrightarrow} X$ on $A^c$.



3. If $X_n \stackrel{\text { a.u. }}{\longrightarrow} X$, then $X_n \stackrel{\text { a.e. }}{\longrightarrow} X$ and $X_n \stackrel{\mu}{\longrightarrow} X$. (For the first assertion, form $A_n$ where $A_n$ is the $A$ of the foregoing definition with $\epsilon=\frac{1}{n}$.)
4. If $X_n \stackrel{\mu}{\longrightarrow} X$, then there exists a subsequence $X_{n^{\prime}} \stackrel{\text { a.u. }}{\longrightarrow} X$.
5. Egoroff's theorem. If $\mu$ is finite, then $X_n \stackrel{\text { a.e. }}{\longrightarrow} X$, implies that $X_n \stackrel{\text { a.u. }}{\longrightarrow} X$. Compare with 3. (Neglect the null set of divergence, and form $A=\bigcup_{m=1}^{\infty} A_m$ with $A_m=\bigcup_{k \geqq n(m)}\left[\left|X_k-X\right| \geqq \frac{1}{m}\right]$ and $n(m)$ such that $\mu A_m<\frac{\epsilon}{2^m}$.)