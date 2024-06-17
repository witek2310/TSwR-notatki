optymalizacja wypukła -> minimum lokalne = globalne

#### Sposoby rozwiązywania
Im niżej tym trudniejszy problem, ale bardziej ogólny
O -> objective
C -> constrains
##### Linear programming (LP)
$$ O: c^tx \qquad C: AX \leq b $$
##### Quadratic programming (QP)
$$ O: x^TCx + c^Tx \qquad C: AX \leq b $$
##### Second-order cone programming (SOCP)
$$ O: f^Tx \qquad C:||Ax+b||\leq c^Tx+d $$
##### Semi-definite programming SDP
$$ O: f^Tx \quad C: Ax\leq b  \lor \text{PSD matrix constrain}$$