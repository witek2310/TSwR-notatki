Przeniesienie [[Programowanie dynamiczne|programowania dynamicznego]] na ciągłą przestrzeń.
$$ x_i \in X_s \subset X \qquad u_j \in U_s \subset U $$

czyli z całego zbioru stanów i wymuszeń wybieramy sobie podzbiory z których losujemy stany i akcje ($x_i$ to wylosowana akcja)

Czyli wykorzystujemy [[losowanie x i u#Sposób 1.| losowe x i u]]

### Algorytm

$J_\alpha$ to aktualnie najlepsza funkcja kosztu
#### Step 1
$$ \underset{i,j}{\forall} x_{ij}' = f(x_i, u_j) $$
$$ \underset{i,j}{\forall} l_{ij} = l(x_i, u_j) $$
 i liczymy:
 $$ J_i^d = \underset{j}{min}[l_{ij} + \hat{J_\alpha}(x_{ij}')] $$
 czyli dla każdego ze wylosowanych stanów wybieramy najlepszą akcję 
 
 #### Step 2
 $$ \underset{\alpha}{argmin} \sum_i [\hat{J_\alpha}(x_1) - J^d_i]^2 $$

szukamy takich $\alpha$ że $J_\alpha$  będzie jak najbliższy temu co wyszło z obliczenia kosztów

I wykonujemy krok 1 i 2 naprzemiennie
#### Można połączyć te dwa kroki w jeden
 $$ \underset{\alpha}{argmin} \sum_i [\hat{J_\alpha}(x_1) - \underset{j}{min}[l_{ij} + \hat{J_\alpha}(x_{ij}')]]^2 $$
Problem jest taki, że to nie musi być stabilne.
Rozwiązanie:
 $$ \underset{\alpha}{argmin} \sum_i [\hat{J_\alpha}(x_1) - \underset{j}{min}[l_{ij} + \hat{J_\beta}(x_{ij}')]]^2 $$
 gdzie 
 $J_\beta$ to target network
 $\beta=LPF(\alpha)$             
LPS - low pass filter
dlaczego?
żeby nie zmieniać zbyt gwałtowanie tych parametrów. 



### Kiedy ADP zbiega?
Dla liniowych sieci neuronowych:
$$ \hat{J_\alpha} = \alpha^T \Phi (x) $$

### Przybliżenie LQR
Liniowa sieć neuronowa może być aproksymacją [[LQR]]
$$ J^*(x) = x^TSx $$
$$ tr(x^TSx) = tr(Sxx^T) $$

ostatecznie musimy minimalizować loss
$$ loss = \sum_{i}[x^T\hat{S}x - J^d_i] $$

$$ \hat{S} = \hat{S} - \eta\frac{\partial loss}{\partial \hat{S}} $$

takie podejście nie zadziała bo domyślnie LQR realizuje zadanie w nieskończonym horyzoncie czasowym, czyli lokalnie jesteśmy daleko od stabilności ^71bef6

Rozwiązanie:
Discounting - zmieniamy funkcję kosztu:
$$ \sum^{\infty}_{n=0} \lambda ^nl(x[n], u[n]) \qquad \lambda \in (0, 1>$$

Można też wykorzystać [[lepsza aproksymacja LQR|lepszą aproksymację LQR]]
