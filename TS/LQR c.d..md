dla [[Linearyzacja wahadła|zlinearyzowanego wahadła]] można zapisać:
$$ \dot{\hat{x}} = A\hat{x} + B\hat{u} $$
zakładając funkcje kosztu jak w [[LQR]] musimy wyliczyć:
$$[k, S] = LQR(A,B,Q,R)$$
i sterowanie:
$$u^* = -k\hat{x}$$

Co zrobiliśmy?
Zmieniliśmy problem wybierania macierzy K na macierz Q i R.
Czyli nic nam to nie dało?
DAŁO!   bo:
$\underset{Q \geq0 , R>0}{\forall}\dot{\hat{x}}=(A-Bk)\hat{x}$ jest stabilny jeżeli $\dot{\hat{x}} = A\hat{x} + B\hat{u}$ jest [[stabilizowalność|stabilizowalny]]
![[K_Q_R_stabilizowalny.png]]



#### Przykład LQR dla wahadła
przykład wartości dla [[Linearyzacja wahadła|zlinearyzowanego wahadła]]
$$ Q=\begin{bmatrix} 10 & 0 \\0 & 1\end{bmatrix} R = [1] $$

Dlaczego takie wartości?
Bo chcemy żeby obydwa koszty były w podobnej skali. 
Czyli:
możemy rozpisać funkcje kosztu:
$$ L = 10\theta^2 + 1\dot{\theta}^2 + u^2 $$
dla wahadła bez tłumienia można zapisać:
$$\omega = \sqrt{\frac{g}{l}}\approx \sqrt{10}$$
$$ q= \sin(\omega t) $$
$$ \dot{q}=\omega \cos(\omega t) $$

podstawiając otrzymamy:
$$ L = 10\sin(\omega t) + (\omega \cos(\omega t))^2 + u^2 $$
$$ L = 10\sin(\omega t) + \omega^2 \cos(\omega t)^2 + u^2 $$
$$ L = 10\sin(\omega t) + 10  \cos(\omega t)^2 + u^2 $$
czyli tak samo ważymy obydwa stany