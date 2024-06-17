- ogólny zapis systemów:
 $$\dot{x} = f (x,u) $$
 $$y = g(x) $$
 x - wektor stanu
 u - sterowanie
w ogólności *f* i *g* są nieliniowymi funkcjami

- systemu drugiego rzędu

$$ x = \begin{bmatrix}
q \\
\dot{q}
\end{bmatrix} $$ 

czyli możemy zapisać:
$$ \ddot{q} = f(q, \dot{q}, u)$$
następnie taką dynamikę możemy dalej podzielić na:
$$ \ddot{q} = f_{1}(q, \dot{q}) + u \cdot f_{2}(q, \dot{q})$$
gdzie:
- *$f_1$* - dryf układu
- *$f_2$* - sterowanie


