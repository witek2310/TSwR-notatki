Mając dane [[Wahadło#Równanie dynamiki wahadła|równanie dynamiki wahadła]] musimy je zdyskretyzować:

$$\dot{x} = \begin{bmatrix}
\dot{\theta} \\
\frac{1}{ml^2(u-b\dot{\theta-mgl\sin\theta})}
\end{bmatrix}$$

policzmy A i B dla dyskretnych równań:
$$ A = \frac{\partial f}{\partial x}|_{\theta = \theta_0} = \begin{bmatrix}
0  & 1 \\
-\frac{g}{l}\cos\theta_0 & -\frac{b}{ml^2}
\end{bmatrix} \qquad B =  \frac{\partial f}{\partial u} = \begin{bmatrix}
0 \\
\frac{1}{ml^2}
\end{bmatrix}$$ 
$$ \dot{\hat{x}} = A\hat{x}  + B\hat{u}$$

założenia:
- m=1
- l=1
- b= 0
- q= 10


dla $\theta = \pi$
$$ A = \begin{bmatrix}
0  & 1 \\
10 & 0
\end{bmatrix} \qquad B = \begin{bmatrix}
0   \\
1
\end{bmatrix} $$

dla $u\approx 0$ możemy wyznaczyć wektory i wartości własne:
$$ det(A-I\lambda)=0 $$
czyli: 
$$ \lambda_1 = \sqrt{10}\qquad \lambda_2 = -\sqrt{10}$$
oraz i ich wektory własne:
$$ v_1 = \begin{bmatrix} 1 \\ \sqrt{10} \end{bmatrix} \qquad v_2 = \begin{bmatrix} -1 \\ \sqrt{10} \end{bmatrix}$$

Na tej podstawie można napisać:
$$ \hat{x} = \alpha_1 v_1 + \alpha_2 v_2 $$
$$ \dot{\hat{x}} =Ax - \lambda_1 \alpha_1 v_1 + \lambda_2 \alpha_2 v_2 $$
kolejno można narysować obraz fazowy:
![[linearized pendulum.png]]
czarne to zlinearyzowane wahadło, a fioletowe to zwykłe
WNIOSEK:
w okolicy $\theta = 0$ wykresy są podobne, czyli linearyzacja dobrze oddaje dynamikę wahadła. Im dalej, tym przybliżenie jest gorsze.