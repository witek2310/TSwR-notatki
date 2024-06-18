#### Podejście 1
Normalnie licząc [[Approximate PD|aproksymację LQR]] wykorzystywaliśmy:
 $$ J_i^d = \underset{j}{min}[l_{ij} + \hat{J_\alpha}(x_{ij}')] $$
 jednak liczenie tego jest nieoptymalne obliczeniowo.
 Dlaczego?
 Bo musimy testować wiele wymuszeń i wybierać najlepsze.
 Rozwiązanie:
 Od razu użyć $u^*$
 Skąd je wziąć?
 z LQR'a
 czyli dla systemów casu ciągłego:
 $$ u^* = -Kx = -R^{-1}B^TSx $$
i casu dyskretnego:
 $$ u^* = -Kx = -(R+B^TSB)^{-1}B^TSAx $$
Dzięki temu można pominąć [[Approximate PD#Step 1| krok pierwszy ]] i od razu przejść do [[Approximate PD#Step 2 | kroku 2]].

Czyli wykorzystujemy [[losowanie x i u#Sposób 2|losowe x i optymalne u]]
#### Podejście 2

###### Systemy dyskretne:
$J^d$ możemy liczyć troszkę lepiej tzn. zamiast licząc je normalnie można rozpisać jednokrokowy koszt na dwie składowe:
$$ l(x,u) = l_x(x) + u^TRu $$
czyli składową związaną ze stanem oraz ze sterowaniem. Co pozwoli pominąć składową związaną ze stanem i zapisać $J^d$ jako:
 $$ J_i^d = \underset{u}{min}[u^TRu + \hat{J_i}(f(x,u))] $$

###### Systemy ciągłe:
Tutaj można zrobić więcej:
- można zastosować rozbicie koszy na dwie składowe
- dla systemów afinicznych można rozbić obiekt na dwie składowe:
	$$ f(x,u) = f_1(x) + f_2(x) \cdot u $$
- pochodna $\frac{\partial \hat{J_\alpha}}{\partial x}$ łatwo się liczy
- można też policzyć optymalne u:
	$$ u^* = -\frac{1}{2}R^{-1}f_2^T(x) \frac{\partial J_\alpha^T}{\partial x}|_{x=x_i} $$