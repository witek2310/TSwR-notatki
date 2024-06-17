### Założenie programowania dynamicznego
- dyskretne stany $s_i \in S$
- dyskretne sterowania/akcje $a_i \in A(s)$
- dyskretny czas $s[n+1]=f(s[n] + a[n])$
- jednokrokowa funkcja kosztu $l_d(s,a)$ (koszt krawędzi)
- koszt całkowity $\underset{l=1}{\overset{n|\infty}{\sum}}l_d(s,a)$
- [[optymalna podstruktura]]

Na podstawie tych informacji można utworzyć graf gdzie krawędzie będą funkcjami kosztu, a węzły stanami.
Taki graf można przeszukiwać różnymi metodami (BFS, DFS, $A^*$ )

### Funkcja kosztu
Cost to go 
ogónie
$$ J^*(s) = \underset{a[\cdot]}{min}\underset{i=0}{\overset{n|\infty}{\sum}} l(s[i], a[i])$$
dla konkretnego s:
$$ J^*(s_0) = \underset{a_0}{min}[l(s_0[i], a_o[i]) + J^*(f(s_0, a_0))]$$

### Polityka
$$ \Pi(s) = \underset{a}{argmin}[l(s_0[i], a_o[i]) + J^*(f(s_0, a_0))] $$


### Algorytm
Value iteration
1. Zaczynamy z jakimś J
3. dla każdego stanu znajdujemy politykę (sterowanie) dla którego funkcja kosztu jest najmniejsza$$ \underset{s}{\forall} J(s) := \underset{a_0}{min}[l(s_0[i], a_o[i]) + J(f(s_0, a_0))] $$
4. Obserwuj jak z $J\rightarrow J^*+C$


### Ograniczenia
- artefakty (mała dokładność, błędy dyskretyzacji)
- dokładna dyskretyzacja jest droga obliczeniowo
- skalowalność metody "przekleństwo/klątwa" wymiarowości
- konieczność znajomości pełnego stanu