Dla [[Wahadło#Równanie dynamiki wahadła|równiania wahadła]] (bez tarcia) chcemy zaproponować funkcję, która rozkręci wahadło tak, żeby znalazło się na górze, gdzie regulator zmienni się na inny (np. [[LQR c.d.#Przykład LQR dla wahadła| LQR]]). 

Energia którą chcemy osiągnąć:
$$ E^d = mgl $$
Zaproponujmy [[stabilność w sensie Lapunova#Definicja|funkcje lapunova]] postaci:
$$ V(x) = \frac{1}{2}(\underbrace{E(x) - E^d(x)}_{\tilde{E}(x)})^2 $$
$$ V(x) = \frac{1}{2}\tilde{E}(x)^2 $$
$$ \dot{\tilde{E}}=\dot{E} $$
$$ \dot{E} = \frac{\partial E}{\partial x}\dot{x}= \frac{\partial E}{\partial \theta}\dot{\theta} + \frac{\partial E}{\partial \dot{\theta}}\ddot{\theta} = \dot{\theta}mgl\sin\theta + ml^2 \dot{\theta}\ddot{\theta} = \dot{\theta}u $$
$$ \dot{V}(x) = \dot{\tilde{E}} = \dot{E} $$
Jak dobrać u, żeby $\dot{V}<0$ ?
$$ u = -k\dot{\theta}\tilde{E}^2 $$
Sprawdzenie:
$$ \dot{V}(x)=\dot{\theta}(-k\dot{\theta}\tilde{E}^2 )= -k\dot{\theta}^2\tilde{E}^2  $$
czyli wybierając taki sterownik, system jest stabilny [[stabilność w sensie Lapunova| i.s.L.]]
co więcej można zapisać:
$$ \dot{V}(x) = -k2\dot{\theta}^2\underbrace{\frac{1}{2}\tilde{E}^2}_{V(x)} $$
czyli układ jest [[Stabilność wykładnicza| stabilny wykładniczo]]
