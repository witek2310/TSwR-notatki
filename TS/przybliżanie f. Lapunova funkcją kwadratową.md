Proponowana funkcja Lapunova ma postać:
$$ V(x) = \Phi^T(x)G\Phi(x), \qquad G\geq 0$$
$\Phi$ to wektor [[funkcje bazowe|funkcji bazowych]].
skoro $G\geq0$ [[stabilność w sensie Lapunova#Funkcja musi być dodatnio określona|pierwszy warunek]] jest spełniony dla wszystkich x.
Co z [[stabilność w sensie Lapunova#Pochodna musi być ujemnie półokreślona|drugim warunkiem]] ?
$$ \dot{V}(x) = \frac{\partial V}{\partial x}f(x) = F(x) $$
zakładamy, że $F(x)$ jest wielomianem (funkcji bazowych) i 
$$ F(x) =-\Phi^TG_2\Phi $$
większość wielomianów p można rozłożyć na SOS (Sum of squares) i nakładając ograniczenie $G_2>0$ gwarantujemy, że $\dot{V}(x)$ jest prawdziwa dla każdego x. Dobre rozwiązanie jest dla funkcji bazowych będących wielomianami(1, $x$, $x^2$)

[[przybliżanie f. Lapunova funkcją kwadratową przykład|przykład]]
