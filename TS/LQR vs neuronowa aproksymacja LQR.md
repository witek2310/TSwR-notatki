#### Zwykły [[LQR]]:
$$ [k,S] = LQR(A,B,Q,R) $$
#### [[Approximate PD|Aproksymacja LQR]]:
$$ [k,S] = LQRD_{iscounted}(A,B,Q,R,\gamma) $$
można to też zapisać z wykorzystaniem zwykłego [[LQR]]:
$$ [k,S] = LQR(\sqrt{\gamma}A,B,Q,\frac{1}{\gamma}R) $$
Im $\gamma$ bliższa 1 tym system jest bliżej prawdziwemu, jednak jest mniej stabilny.
"Dodanie $\gamma$ spowoduje, że wydaje nam się, że sterujemy układem, który jest bardziej stabilny niż w rzeczywistości"
Zazwyczaj wybiera się $\gamma$ bliskiej 1 (0.99)


 Można też wykorzystać [[lepsza aproksymacja LQR|lepszą aproksymację LQR]]