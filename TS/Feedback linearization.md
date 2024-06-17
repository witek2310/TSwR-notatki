Feedback linearization (linearyzacja przez sprzężenie zwrotne) - wykorzystuje model do sterowania
dla systemów:
$$ \dot{x} = f_{1}(x) + u \cdot f_{2}(x) $$ 

jeżeli układ jest w pełni [[Niedosterowanie | sterowalny]] możemy przyjąć:
$$ u = \frac{1}{f_2(x)}(v - f_1(x))$$
podstawiając to do równania dynamiki otrzymamy:
$$ \dot{x} = f_1(x) + f_2(x) \cdot \frac{1}{f_2(x)} (v-f_1(x)) $$
$$ \dot{x} = v $$

otrzymana dynamika to intergrator

Problemy:
- wpływ niedokładności modelowania
- $f_2 = 0$
- w przypadku manipulatora $M^{-1}B$ musi istnieć
- brak pętli sprzężenia zwrotnego
