# Rozładowanie układu RC

Weźmy układ składający się z połączenia rezystora o rezystancji $R$ i kondensatora o pojemności $C$. Przyjmując w stanie początkowym napięcie rezystora za $U_R$ oraz napięcie kondensatora za $U_C$ zachodzi (z drugiego prawa Kirchhoffa):

$U_C - U_R = 0$

Wiedząc, że napięcie kondensatora wyraża się wzorem $U_C=\frac{Q}{C}$, mamy:

$\frac{Q}{C}-U_R=0$

Następnie z prawa Ohma zauważmy, że $U_R=I_R\cdot R$

Wartość prądu płynącego przez rezystor $R$ zależy od ładunku, który przepływa przez niego  w czasie $t$. Możemy wobec tego wyrazić $I$ jako $I=\frac{dq}{dt}$

Powstaje następujące liniowe równanie różniczkowe pierwszego stopnia:

$\frac{Q}{C}-R\frac{dq}{dt}=0$

$\frac{Q}{C}=R\frac{dq}{dt}$

$\frac{1}{RC}dt=\frac{1}{q}dq$

Zastosowana metoda separacji zmiennych. Zachodzi całkowanie stronami

$\int \frac{1}{RC} dt = \int \frac{1}{q} dq$

$\frac{t}{RC} = ln(|q|)+K$

Traktujemy ładunek jako jego wartość, wobec tego przyjmuje wartość nieujemną:

$-\frac{t}{RC} = ln(q)+K$

$-\frac{t}{RC}-K = ln(q)$

$q=e^{-\frac{t}{RC}-K}=e^{-\frac{t}{RC}}\cdot e^{-K}=Ae^{-\frac{t}{RC}}$

W celu wyliczenia stałej całkowania $A$ należy wprowadzić warunki początkowe w układzie. Niech rozładowanie kondensatora następuje od stanu naładowania ładunkiem $q_0$, wtedy:

$
\begin{cases}
q(t=0)=q_0\\
q(t=0)=Ae^{-\frac{t}{RC}}=A
\end{cases}
\implies
q_0=A
$

Wyraźmy ładunek $q$ kondensatora jako $q=UC$. Zachodzi:

$q(t)=q_0e^{-\frac{t}{RC}}$

Pojemność kondensatora jest zmienną niezależna od czasu $\frac{\partial C}{\partial t}=0$

$U(t)\cdot C=U_0\cdot C\cdot e^{-\frac{t}{RC}}$

$U(t)=U_0 \cdot e^{-\frac{t}{RC}}$





