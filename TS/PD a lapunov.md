Do [[Ciągłe PD#Równanie HJB|równania HJB]] wstawiając optymalne sterowanie otrzymamy:
$$ 0=l(x,u^*) + \underbrace{\frac{\partial J^*}{\partial x}f(x,u)}_{\frac{\partial J}{\partial x}\dot{x}=\frac{dJ}{dt}} $$
czyli można napisać:
$$ \dot{J} = -l(x,u^*) $$

Podobne jest to do [[stabilność w sensie Lapunova#Pochodna musi być ujemnie półokreślona| drugiego warunku]]
Czyli funkcja cost to go (J) jest szczególnym przypadkiem funkcji Lapunova.
Właśnie dlatego łatwiejsze jest szukanie funkcji Lapunova (których może być nieskończenie wiele) niż optymalnego J (który jest tylko 1)