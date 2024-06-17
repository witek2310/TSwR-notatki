#### Definicja
$$ \underset{\epsilon >0}{\forall} \enspace \underset{\delta>0}{\exists} \enspace||x(0) - x^*|| < \delta \implies \underset{t}{\forall} \enspace||x(t) - x^*|| < \epsilon$$

![[lapunov.png]]
Dla każdego punktu w hiperkuli o promieniu $\delta$ to wiemy, że dla dowolnego czasu nie oddalimy się od tego punktu o więcej niż $\epsilon$

#### Warunki na V(x)
Żeby punku był w stabilny w sensie lapunova musi istnieć funkcja V(x), która spełnia warunki:

###### Funkcja musi być dodatnio określona:
$$V(0) = 0, \quad \underset{x \neq0}{\forall} \ V(x)>0$$
###### Pochodna musi być ujemnie półokreślona:
$$ \dot{V}(0) =0, \quad \underset{x \neq0}{\forall} \dot{V}(x)\leq0 $$


#### Przykład
[[Lapunov wahadło|Przykład dla wahadła]]
