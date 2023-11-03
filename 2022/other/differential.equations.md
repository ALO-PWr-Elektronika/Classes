## Dodatek I – Przykłady wyprowadzeń z równań różniczkowych i rachunku całkowego

Poniższy dodatek prezentuje wyprowadzenia dla kilku podstawowych wzorów fizycznych.

### Równanie prędkości i położenia jako funkcji czasu w ruchu przyspieszonym - Całkowanie

Wyprowadzenie prędkości jako funkcji czasu $v(t)$ z przyspieszenia $a$:

$v\left(t\right)=\int{a\ dt}=at+C$

Przyjmijmy warunek początkowy $v\left(0\right)=v_0$:

$v\left(0\right)=a\cdot0+C=C=v_0$

Wyprowadzenie położenia jako funkcji czasu $x(t)$ z prędkości i przyspieszenia:
$x\left(t\right)=\int v d t=\int\left(\int a d t\right)dt=\int{(at+v_0)dt}=\frac{1}{2}at^2+v_0t+C$
Przyjmijmy warunek początkowy $x\left(0\right)=x_0$:

$x\left(0\right)=\frac{1}{2}a\cdot0+v_0\cdot0+C=C\Longrightarrow C=x_0$

$x\left(t\right)=\frac{1}{2}at^2+v_0t+x_0$

### Siła oporu proporcjonalna do prędkości, prędkość ciała – RR I Stopnia

Siła wypadkowa działająca na ciało (Z drugiej zasady dynamiki Newtona):

$F=ma$

Wiemy, że $a=\frac{dv}{dt}$, zatem:

$F=m\frac{dv}{dt}$

Załóżmy równocześnie, że na ciało działa siła proporcjonalna do prędkości ciała:

$F$ ~ $v$

Przyjmijmy współczynnik proporcjonalności $k$, wtedy:

$kv=m\frac{dv}{dt}$
$\frac{k}{m}dt=\frac{1}{v}dv\ \Longrightarrow\int{\frac{k}{m}dt}=\int{\frac{1}{v}dv}\Rightarrow\frac{k}{m}t+C=\ln{\left(v\right)}$

$\log_e{v}=\frac{k}{m}t+C$

$v(t)=e^{\frac{k}{m}t+C}=e^{\frac{k}{m}t}\cdot e^C=e^{\frac{k}{m}t}\cdot C$

### Położenie jako funkcja czasu w ruchu harmonicznym – RR II Stopnia

Wyprowadzenie $x(t)$ w ruchu drgającym:

$F=-kx$

$ma=-kx$

$m\frac{d^2x}{dt^2}=-kx$

W równaniu różniczkowym drugiego stopnia postuluje się rozwiązanie w postaci funkcji $x\left(t\right)={Ae}^{rt}$, gdzie $A,r$ to dowolne liczby $\in\mathbb{C}$. Następnie udowadnia się jego prawdziwość. Zauważmy następujące zależności:

Jeśli $x\left(t\right)=e^{rt}$, to:
- $\frac{dx}{dt}=\left(e^{rt}\right)^\prime=r\cdot e^{rt}$
- $\frac{d^2x}{dt^2}=\left(e^{rt}\right)^{\prime\prime}=\left(r\cdot e^{rt}\right)^\prime=r\cdot\left(e^{rt}\right)^\prime=r^2\cdot e^{rt}$
  
Wobec tego równanie różniczkowe przyjmuje postać:

$\frac{d^2x}{dt^2}=-\frac{kx}{m}\Rightarrow\frac{d^2x}{dt^2}+\frac{kx}{m}=0$

$r^2\cdot{Ae}^{rt}+\frac{k}{m}{\ Ae}^{rt}=0\Rightarrow{Ae}^{rt}\left(r^2+\frac{k}{m}\right)=0$

Równanie jest prawdziwe, gdy:

$Ae^{rt}=0$

Lub gdy:

$r^2+\frac{k}{m}=0\Longrightarrow r^2=-\frac{k}{m}\Rightarrow r=\pm\sqrt{-\frac{k}{m}}\Rightarrow r=\pm i\sqrt{\frac{k}{m}}$

Dokonujemy podstawienia r do postaci funkcji $x\left(t\right)=Ae^{rt}$, otrzymując:

$x\left(t\right)={Ae}^{rt}\ oraz\ r=\pm i\sqrt{\frac{k}{m}}$

$x\left(t\right)={Ae}^{i\sqrt{\frac{k}{m}}t}=Acos{\left(\sqrt{\frac{k}{m}}t\right)}+isin\left(\sqrt{\frac{k}{m}}t\right)$

Sens fizyczny ruchu harmonicznego tkwi w rzeczywistej części rozwiązania, zatem:

$x\left(t\right)=A\cos{\left(\sqrt{\frac{k}{m}}t\right)}=A\cdot cos(\omega t+\varphi)$
