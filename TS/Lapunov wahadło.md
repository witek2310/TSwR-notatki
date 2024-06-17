Mając równanie dynamiki takie jak dla [[Wahadło#Równanie dynamiki wahadła| tutaj]]
Załóżmy, ze funkcja Lapunova przyjmie postać Energi systemu:
$$ E = E_k + E_p= \frac{1}{2}ml^2\dot{\theta} -mgl\cos(\theta) + mgl$$
To jest energia wahadła, gdzie 0 energii potencjalnej jest w pozycji poziomej na dole. Czyli dla $\dot{\theta}=0$ tylko tam E = 0 w pozostałych przypadkach jest dodatnia.
Pochodna:
$$ \frac{d}{dt} E(x) = \frac{\partial E}{\partial x} \dot{x} = \frac{\partial E}{\partial \theta}\dot{\theta} + \frac{\partial E}{\partial \dot{\theta}} \ddot{\theta} = \dot{\theta} mgl\sin\theta + ml^2\dot{\theta}\ddot{\theta} = \dot{\theta}(mgl\sin\theta + ml^2\ddot{\theta})$$
z równania dynamiko można wyznaczyć ( zakładając u=0):
$$ mgl\sin\theta + ml^2\ddot{\theta} = -b\dot{\theta} $$
wstawiając to do poprzedniego równania:
$$ \dot{\theta}(mgl\sin\theta + ml^2\ddot{\theta}) = \dot{\theta}(-b\dot{\theta})=-b\dot{\theta}^2 \leq 0$$
ale:
$$ -b\dot{\theta}^2 <0 \quad \underset{\dot{\theta}}{\forall} $$
czyli spełniamy założenie od półujemnookreśloności pochodnej 