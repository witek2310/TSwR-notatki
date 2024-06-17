### Dynamika wahadła
##### Wyprowadzenie
Równania na model wahadła matematycznego zostaną wyprowadzone wykorzystując formalizm Lagranga

- Energia kinetyczna:
	$$ T = \frac{1}{2} mV^2 = \frac{1}{2} ml^2\dot{\theta}^2$$
- Energia potencjalna:
	$$V = -mgl \cos \theta $$
następnie policzyć Lagrangian
$$ \mathcal{L} = T - V $$

$$\frac{d}{dt}(\frac{\partial \mathcal{L}}{\partial \dot{q}}) - \frac{\partial \mathcal{L}}{\partial q} = Q $$

po policzeniu otrzymamy:
$$ ml^2 \ddot{\theta} + mgl\sin\theta = Q = \tau - b\dot{\theta} $$
##### Równanie dynamiki wahadła
$$ ml^2 + b\dot{\theta} + mgl\sin\theta = u$$

### Obraz fazowy:
zakładając:
$$x = \begin{bmatrix}
\theta \\
\dot{\theta}
\end{bmatrix}$$
zapisując równania wahadła w ten sposób:
$$\dot{x} = \begin{bmatrix}
\dot{\theta} \\
\frac{1}{ml^2(u-b\dot{\theta-mgl\sin\theta})}
\end{bmatrix}$$
![[pend_undamped_phase.svg]]



Specjalny przypadek:
[[Overdamped pendulum]]