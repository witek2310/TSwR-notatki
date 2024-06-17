równanie
$$ \ddot{q} = u $$
funkcja kosztu:
$$ l_c(q, \dot{q}, u) = q^2 + \dot{q}^2 + u^2 $$
stan:
$$x = \begin{bmatrix}
q \\
\dot{q}
\end{bmatrix}$$
##### zadanie
sprawdź czy podana funkcja kosztu i sterowanie są optymalne
$$ u = -q - \sqrt{3} \dot{q} $$
$$ J^* = \sqrt{3} q^2 + 2 q\dot{q} + \sqrt{3}\dot{q}^2 $$

##### rozwiązanie
Trzeba udowodnić, że [[Ciągłe PD#Równanie HJB|rówanie HJB]] jest prawdziwe tzn.:
$$ 0=  \underset{u}{min}[l_c(x[n] +\frac{\partial J^*}{\partial x} f_c(x,u)]$$
najpierw wyznaczmy $\frac{\partial J}{\partial x} f_c(x,u)$ :  

$$\frac{\partial J}{\partial x} f_c(x,u) = \begin{bmatrix}
\frac{\partial J}{\partial q} & \frac{\partial J}{\partial \dot{q}}
\end{bmatrix}\cdot\begin{bmatrix}
\dot{q} \\
\ddot{q}=u
\end{bmatrix} = (2\sqrt{3}q + 2\dot{q})\dot{q} + (2q+2\sqrt{3}\dot{q})u$$
podstawiając to do HJB:
$$0 = \underset{u}{min}[q^2 + \dot{q}^2 + u^2 + (2\sqrt{3}q + 2\dot{q})\dot{q} + (2q+2\sqrt{3}\dot{q})u]  $$
redukując składniki niezależne od u:
$$0 = \underset{u}{min}[\underbrace{u^2 +(2q+2\sqrt{3}\dot{q})u}_{C}]  $$
trzeba znaleźć najmniejsze u, w tym celu musimy obliczyć minimum z u:
$$ \frac{\partial C}{\partial u} = 2u + 2q + 2\sqrt{3}\dot{q} = 0$$
na tej podstawie możemy napisać:
$$ u = -q - \sqrt{3}\dot{q} $$
następnie musimy sprawdzić, czy to u jest optymalne, w tym celu trzeba je podstawić do równania:
$$0 = \underset{u}{min}[q^2 + \dot{q}^2 + u^2 + (2\sqrt{3}q + 2\dot{q})\dot{q} + (2q+2\sqrt{3}\dot{q})u]  $$
i zobaczyć czy rzeczywiście równa się zero, jeżeli tak to znaczy, że podana funkcja kosztu i sterowanie są optymalne.