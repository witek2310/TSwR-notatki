#### Postać [[stabilność w sensie Lapunova|funkcji Lapunova]]
Proponowana funkcja Lapunova ma postać:
$$ V(x) = \sum_i \alpha_i \phi = \alpha^T\Phi(x)$$
więc jej pochodna:
$$ \dot{V}(x)=\frac{\partial V}{\partial x}f(x)=(\alpha^T\frac{\partial \Phi}{\partial x})f(x) $$

Wylosuj $x_i$ tak, że $\underset{i}{\forall}$ :
$$ V(x_i) \geq 0$$
$$ \dot{V}(x_i) \leq 0$$


Wrzuć do [[optymalizacja|optymalizatora]] i odbierz wyniki.

Co to $\Phi$?
To macierz [[funkcje bazowe |funkcji bazowwych]]

Problem:
Czy jeżeli już znajdzie się $\alpha$ to czy mamy pewność, że dla WSZYSTKICH x (nie tylko tych wylosowanych) wyrażenie $\alpha^T\Phi(x)$ spełnia [[stabilność w sensie Lapunova#Warunki na V(x)|warunki]] ?
NIE 
Rozwiązanie:
Inna [[przybliżanie f. Lapunova funkcją kwadratową|metoda przybliżania]]
