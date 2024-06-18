regulator do systemów liniowych z kwadratową funkcją kosztu
$$ \underbrace{linear}_{\dot{x} = Ax+Bu} \quad \underbrace{quadratic}_{l(x,u) = x^T Q X + u^TRu} \quad regulator $$
założenia:
- $Q = Q^T \geq 0$
- $R=R^T>0$
- funkcja kosztu:  $l(x,u) = x^T Q X + u^TRu$


$$ J^* = x^TSx $$
$$ \frac{\partial J^*}{\partial x} = 2x^TS$$
$$ u^* =?$$

podstawiając funkcję kosztu do  [[Ciągłe PD#Równanie HJB |równania HJB]] otrzymamy:
$$ 0=\underset{u}{min}[ x^T Q x + u^TRu + 2x^TS(Ax+Bu) ] $$
$$ 0=\underset{u}{min}[\underbrace{u^TRu + 2x^TSBu}_{C} ] $$
szukamy minimalnego u:
$$ \frac{\partial C}{\partial u} = 0 $$
czyli:
$$ 2u^TR + 2x^TSB = 0 $$
$$ u^TR = -x^TSB $$
$$ u^T = -x^TSBR^{-1} $$
$$ u^* = -R^{-1}B^TSx$$
$$ u^*=-kx $$
sprawdźmy czy to na pewno jest optymalne podstawiając do równania HJB:
$$ 0=x^TQx + (R^{-1}B^TSx)^TRR^{-1}B^TSx + 2x^TS(Ax-BR^{-1}B^TSx) $$
$$ 0=x^T(\underbrace{Q + SBR^{-1}B^TS + 2SA - 2SBR^{-1}B^TS}_{=0})x $$

czyli:
$$ 0 = Q - SBR^{-1}B^TS + SA + A^TS $$
to równanie to CARE (**continous algebraic ricatti equation**)

jak wyliczyć S?

nie da się analitycznie ale są świetne rozwiązania numeryczne

plusy LQR:
- ciągła dynamika
minusy:
- liniowa dynamika
- tylko kwadratowa funkcja kosztu

[[LQR c.d.| przykład]]