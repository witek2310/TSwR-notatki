### porównanie z [[Programowanie dynamiczne| programowanie dynamiczne]]
- ciągłą dynamika, stan, czas
	$$\dot{x} = f_c(x,u)$$
- koszt całkowity
	$$ l=\int_0^\infty l_c(x(t), u(t))dt $$
- Odpowiednik $J^*(s_0)$
	$$ 0 = \underset{u}{min}[l_c(x,u) + \frac{\partial J^*}{\partial X} f_c(x,u)] $$

### Równanie HJB
równie HJB  czyli równanie Hamiltona-Jakobiego-Bellmana to równanie postaci:
$$ 0=  \underset{u}{min}[l_c(x[n] +\frac{\partial J^*}{\partial x} f_c(x,u)]$$


##### wyprowadzenie
$$ x[n+1] = f_d(x[n], u[n]) $$
używając szeregu Taylora:
$$ x[n+1] \approx x[n] + h f_c(\underbrace{x[n]}_{x[n]=x(n\cdot h)}, u[n]) $$

h-stała czasowa

koszt całkowity:
$$l_d(x,u) \approx h\cdot l_c(x,u)$$ 

funkcja kosztu:
**WARNING**
**PISANE MOCNO NA WYCZUCIE**

$$ J^*(x[n+1]) = J^*(x[n]) - l_d(x,u) $$

koszt kolejnego stanu jest równy aktualnemu kosztowi to go minus koszt przebywania w aktualnym stanie

podstawiając ciągłą funkcje kosztu:
$$ J^*(x[n+1]) \approx J^*(x[n]) - h\cdot l_c(x,u) $$

wiedząc że:
$$ \frac{dJ^*}{dt} = -l_c(x, u^*)$$
można zapisać:
$$ J^*(x[n+1]) \approx J^*(x[n]) + h\underbrace{\frac{dJ^*}{dt}}_{\frac{\partial J}{\partial x}\cdot \frac{dx}{dt} = \frac{\partial J}{\partial x} f_c(x,u)} $$

następnie wracając do podstawowej definicji cost to go:
$$ J^*(x[n]) = \underset{u}{min}[l_d(x[n], u[n]) + J^*(f(x[n], u[n]))]$$
$$ J^*(x[n]) = \underset{u}{min}[h\cdot l_c(x[n], u[n]) + J^*(x[n+1])]$$
$$ J^*(x[n]) = \underset{u}{min}[h\cdot l_c(x[n], u[n]) + J^*(x[n])] +h\cdot \frac{\partial J^*}{\partial x} f_c(x,u)]$$

Jako, że $J^*(x[n])$ nie zależy od u, można je wystawić przed min i skrócić, jednocześnie ze środka min można wyłączyć h i obustronnie przez nie podzielić:
$$ 0=  \underset{u}{min}[l_c(x[n] +\frac{\partial J^*}{\partial x} f_c(x,u)]$$
otrzymujemy równanie HJB

#### Przykład

[[HJB podwójny integrator przykład|Przykład]]