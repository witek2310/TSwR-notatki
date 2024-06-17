#### Przykład 1
$$ \dot{x} = -x $$
Propozycja f. Lapunova:
$$ V(x) = x^2 $$
Sprawdzenie:
$$ \dot{V}(x) = \frac{\partial V}{\partial x}\dot{x} = 2x\cdot(-x) = -2x^2<0 $$

Czyli układ jest [[stabilność w sensie Lapunova|stabilny i.s.L.]] co więcej jest [[Stabilność asymptotyczna|stabilny asymptotycznie]]
co jeszcze więcej, można zapisać:
$$ \dot{V}(x) = -2x^2=-2V(x) $$
czyli jest [[Stabilność wykładnicza|stabilny wykładniczo]]

#### Przykład 2
$$ \dot{x}=-x+x^3 $$
Propozycja f. Lapunova:
$$ V(x) = x^2 $$
Sprawdzenie:
$$ \dot{V}(x) = 2x(-x+x^3) = -2x^2+2x^4=2x^2(x^2-1) $$
system nie ma globalnej stabilności ale:
można zapisać:
$$ \dot{V}(x) = \begin{cases} 0 & \text{dla $x\in \{0, 1, -1\}$} \\ 
							  >0 & \text{dla $|x| > 1$} \\
							 <0 & \text{dla $|x| < 1 \land x\neq 0$} \end{cases} $$
Czyli dla $|x|<1$ system jest stabilny w sensie Lapunova