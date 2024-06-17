### Minimum time problem dla podwójnego integratora
#### Równie
$$\ddot{q} = u $$
#### Cel
$$
\underset{u}{argmin}(t) \qquad |u|\leq 1 $$

#### Rozwiązanie
Zakładając sterowanie bang-bang (wartość sterowania jest minimalna lub maxymalna) można zapisać:
$$ \ddot{q} = -1 \qquad  |\int$$
$$ \dot{q} = \dot{q}(0) - t \implies t=\dot{q}(0) - \dot{q}$$
$$ q = q(0) + t\dot{q}(0) + \frac{1}{2}t^2 $$
podstawiając t i upraszając orzymmamy:
$$ q(t) = q(0) - \frac{1}{2} \dot{q}(0)^2 - \frac{1}{2}\dot{q}^2(t) $$
$C=q(0) - \frac{1}{2} \dot{q}(0)^2$ - warunki początkowe
otrzymane równanie jest równaniem paraboli, ale w drugą stronę. 
Robiąc analogicznie dla wymuszenie równego 1 można narysować obraz fazowy:
![[minimum time problem.png]]
Kolor żółty i niebieski oznaczają  przykładowe trajektorie i ich wymuszenie, aby znaleźć się w zerze.