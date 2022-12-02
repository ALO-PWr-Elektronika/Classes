### Dioda

- Dioda to element elektroniczny posiadający dwa wyprowadzenia:<br/>
    $(+)$ Anoda --> Katoda $(-)$
- Podstawowy model diody to idealna dioda prostownicza:<br/>
    - Prąd może płynąć przez idealną diodę tylko w jednym kierunku.
    - Dioda służy wobec tego do ustalania kierunku płynięcia prądu
    - Idealna dioda w kierunku przewodzenia jest idealnym przewodnikiem. W praktyce w wyniku oddziaływań międzycząsteczkowych w warstwie zaporowej PN dochodzi do spadku napięcia $V_D$. Dla krzemu $V_{Krzemu}=0.7V$
    - Idealna dioda w kierunku zaporowym jest idealnym izolatorem. W praktyce występuje tzw. prąd upływu $I_L$ (leakage current) 
- Pozostałe typy diód to również:
    - Dioda LED - Źródło światła
    - Dioda Zenera - Stabilizacja napięcia
    - Dioda Schottky'ego - Działająca na wysokich częstotliwościach

![](semiconductor-graph.png)

Do przewodzenia dochodzi poprzez ustawienie powłoki przewodzenia w atomie:
- W przewodnikach typu **miedź** powłoka przewodzenia praktycznie pokrywa się z powłoką walencyjną, dzięki czemu elektrony mogą swobodnie odrywać się i przesuwać dalej
- W izolatorach typu **styropian** powłoka przewodzenia jest zbyt odległa oraz elektronów na powłoce walencyjnej jest zbyt dużo żeby mogły się one oderwać. Nie są w stanie wobec tego opuścić atomu
- Półprzewodnik typu **krzem** działa jak izolator, natomiast powłoka przewodzenia jest na tyle blisko, że przy dostarczeniu relatywnie niewielkiej energii jesteśmy w stanie przesunąć niektóre elektrony powyżej powłoki walencyjnej 

Tworzenie warstw półprzewodnikowych (Doping):

![](dopingPN.png)

**TYP N** Czysty krzem nie ma wielu wolnych elektronów, dlatego w procesie tworzenia półprzewodnika dodaje się do niego niewielką ilość materiału z wieloma wolnymi elektronami tworząc warstwę wzbogacaną. Np poprzez dodanie fosforu (który ma 5 zamiast 4 elektronów walencyjnych)
<br/>
**TYP P** Poprzez dodanie innego materiału, który ma bardzo mało wolnych elektronów tworzy się tzw. warstwę zubożałą. Na przykład przez dodanie glinu (który ma tylko 3 elektrony walencyjne)
<br/>

![](depletion-region.png)

Łączymy **typ P** oraz **typ N**. W wyniku tego, wskutek dyfuzyjnego przepływu elektronów, powstaje warstwa PN, która nazywana jest warstwą zaporową (Depletion Region). 

O elektronach mówi się że mają ładunek ujemny, a o ich braku (dziurach) że mają ładunek dodatni.
W wyniku dyfuzji powstaje pole elektryczne, które nie pozwala poruszać się w tym samym kierunku pozostałym elektronom. W krzemie różnica potęcjałów między tymi rejonami wynosi około $U_{Krzemu}=0.7V$

**Napięcie** przyłożone w **kierunku przewodzenia** powyżej spadku napięcia na diodzie sprawi, że **popłynie prąd**.

$U>U_{Spadku\space na\space didodzie} \implies$ Przewodzenie<br/>

**Napięcie** przyłożone w **kierunku zaporowym** sprawi, że warstwa zaporowa powiększy się, a prąd **nie popłynie**.
Jeżeli zostanie przekroczone napięcie zaporowe, to dioda ulegnie zniszczeniu.

$U>U_{Zaporowe} \implies$ Uszkodzenie diody 

![](diode-VI-characteristics.png)

Parametry diody:
- Maksymalne napięcie zaporowe
- Napięcie przewodzenia
- Maksymalne natężenie płynące przez diodę

![](full-bridge-rectifier.png)

Zastosowania:
- Dioda jest w stanie prostować napięcie. Zmieniać prąd AC w DC:
    - Mostek Pojedyńczy - 1 dioda - Prostowanie połowy okresu<br/>
    $U(t) = U_0 sin(\omega t)\implies$
    $
    \begin{cases}
    U = 0\text{, jeśli}\space sin(\omega t)<0 \implies \frac{2\pi n + \pi}{\omega} < t < \frac{2\pi n}{\omega}\\
    U = U_0 sin(\omega t)\text{, jeśli}\space sin(\omega t)\geq 0 \implies \frac{2\pi n}{\omega} \leq t \leq \frac{2\pi n + \pi}{\omega}
    \end{cases}
    $
    - Mostek Graetza (na schemacie) - 4 diody - Prosotwanie pełnego okresu (full bridge rectifier)<br/>
    $U(t) = U_0 sin(\omega t)\implies$
    $
    U = | U_0 sin(\omega t) |
    $
- Dioda zabezpiecza układ przed podłączeniem napięcia w sposób odwrotny (nieprawidłowy)

Woltomierz:
- Test diody pozwala testować diodę w kierunku przewodzenia i zaporowym.

### Tranzystor

![](NPNtransistor.png)

Tranzystor służy głównie jako:
- Łącznik
- Wzmacniacz sygnału

Tranzystor bipolarny (BJT - Bipolar Junction Transistor) to element elektroniczny z trzema wyprowadzeniami:
- (B) Baza
- (C) Kolektor
- (E) Emiter

Strzałka na symbolu wskazuje konwencjonalny przepływ prądu.

**Wzmocnienie Tranzystora**<br/>
$\beta=\frac{I_c}{I_b}$

Warstwy półprzewodnikowe w tranzystorze NPN

![](NPNdepletion-region.png)

Poprzez podanie wystarczającego napięcia między bazą a emiterem zajdzie przewodzenie prądu z bazy do emitera, jak w normalnej diodzie.<br/>

Gdy $V_{Bazy}>U_{Diody BE}$ to $I_{BE}>0$ 

Przez bazę płynie mały prąd, ponieważ w procesie wzbogacania baza jest wzbogazana znacznie mniej niż emiter i kolektor, dzięki czemu niewiele elektronów jest w stanie poruszać się z emiter do bazy.

Poprzez podanie wystarczającego napięcia między bazą a emiterem i podanie napięcia między bazą a kolektorem dochodzi do przewodzenia między kolektorem a emiterem. Niewielka liczba elektronów przechodzi wówczas z emitera do bazy, a wielka liczba elektronów przechodzi z emitera do kolektora.

Gdy $V_{Kolektora}>V_{Emitera}$ oraz $I_{BE}>0$ to $I_{CE}>0$

![](transistorNPN-open.png)

W stanie przeowdzenia $I_B>0$<br/>
Z zasady zachowania łudnku<br/>
$I_E = \frac{q}{t}$ oraz $q_E=q_B+q_C \implies$
$I_E = I_C + I_B \implies I_E>I_C $

### Podstawowe układy na tranzystorze

- Switch
- Bramki logiczne (System TTL (Bipolar Junction Transistor), CMOS (Field Effect Transistor))