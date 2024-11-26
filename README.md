# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

# My Answer, Maxie, M. 
## Definition of Big-O Notation 
- $T(n) \in O(f(n)) \iff \exists c > 0, n_0 > 0 : T(n) \leq c \cdot f(n) \forall n \geq n_0$
- prove asymptotic complexity of $log_2(n)$ is the same as $log_5(n)$
  - $O(log_2 n) = O(log_5 n)$
## Prove $O(log_2 n) \subset O(log_2 n)$
- Will utilize chaqnge of base formula for logarithms:
  - $log_2 n = \frac{log_5 n}{log_5 2}$
- Assume $T(n) \in O(log_2 n)$
  - By the definition, there exist constants $c_1 > 0$ and $n_1 > 0$ such that:
    - $T(n) \leq c_1 \cdot log_2 n \forall \geq n_1$
  - **Substitute** $log_2 n = \frac{log_5 n}{log_5 2}$:
    - $T(n) \leq c_1 \cdot \frac{log_5 n}{log_5 2} \forall \geq n_1$
  - **Let** $c_2 = \frac{c_1}{log_5 2}$, this is a constant, then:
    - $T(n) \leq c_2 \cdot log_5 n \forall \geq n_1$
- **This Demonstrates:** $T(n) \in O(log_5 n)$
## Prove $O(log_5 n) \subset O(log_2 n)$
- Will similarly use the change of base formula:
  - $log_5 n = \frac{log_2 n}{log_2 5}$
- Assume $T(n) \in O(log_5 n)$
  - By the definition, there exist constants $c_3 > 0$ and $n_2 > 0$ such that:
    - $T(n) \leq c_3 \cdot log_5 n \forall \geq n_2$
  - **Substitute** $log_5 n = \frac{log_2 n}{log_2 5}$:
    - $T(n) \leq c_3 \cdot \frac{log_2 n}{log_2 5} \forall n \geq n_2$
  - **Let** $c_4 = \frac{c_3}{log_2 5}$, this is a constant, then:
    - $T(n) \leq c_4 \cdot log_2 n \forall n \geq n_2$
- **This Demonstrates:** $T(n) \in O(log_2 n)$
## Conclusion 
- $O(log_2 n) \subset O(log_5 n)$ and $O(log_5 n) \subset O(log_2 n)$
  - **Therefore:** $O(log_2 n) = O(log_5 n)
## Plagiarism Statement:
I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
## Resources: 
- https://www.onlinemathlearning.com/logarithms-properties.html
