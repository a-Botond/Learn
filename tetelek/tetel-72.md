<a name="tetel-72"></a>

## 72. Cramér-Rao-egyenlőtlenség
[[ Tartalomjegyzék ]](../README.md#tartalomjegyzek) | [[ Előző ]](./tetel-68-71.md#tetel-68-71) | [[ Következő ]](./tetel-74.md#tetel-74)


> A Cramér-Rao-egyenlőtlenség a statisztika "Heisenberg-féle határozatlansági relációja", amely kimondja: létezik egy matematikai kőfal, egy elméleti alsó határ, ami alá a torzítatlan becslésünk bizonytalansága (szórásnégyzete) sosem csökkenhet, akármilyen zseniális képletet is találunk ki.


### TÉTEL:
Legyen $X_1, X_2, \dots, X_n$ egy $f(x; \theta)$ sűrűségfüggvényű eloszlásból származó független minta, amely eleget tesz a regularitási feltételeknek (pl. az integrál és a deriválás sorrendje felcserélhető). 

Legyen $T = T(X_1, \dots, X_n)$ a $\theta$ paraméter egy **torzítatlan** becslése (azaz $E(T) = \theta$).
Akkor a $T$ becslés szórásnégyzetére (varianciájára) érvényes az alábbi alsó korlát:
$$D^2(T) \ge \frac{1}{n \cdot I(\theta)}$$
ahol $I(\theta)$ a Fisher-információ egyetlen mintaelemre vonatkozóan.

*(Azokat a becsléseket, amelyek elérik ezt az elméleti minimumot, vagyis egyenlőség áll fenn, **hatásos becslésnek** nevezzük).*



### BIZONYÍTÁS:
* **Kiindulópont:** A bizonyításhoz a vizsgált becslőfüggvényt ($T$) és a Fisher-információt generáló *score-függvényt* (a log-likelihood deriváltját, jelöljük $S$-sel: $S = \frac{\partial}{\partial \theta} \ln L(X; \theta)$) kell összeeresztenünk. Írjuk fel az alapokat: tudjuk, hogy $E(S) = 0$, a szórásnégyzete pedig maga a Fisher-információ: $D^2(S) = n \cdot I(\theta)$.
* **A "Trükk":** A **Cauchy–Bunyakovszkij–Schwarz-egyenlőtlenség** bevetése a kovarianciára! Ez a monstrum bizonyítás igazi, gyönyörű szíve. Bármely két valószínűségi változóra igaz, hogy a kovarianciájuk négyzete sosem haladhatja meg a szórásnégyzeteik szorzatát. Írjuk fel ezt $T$-re és $S$-re: 
$[cov(T, S)]^2 \le D^2(T) \cdot D^2(S)$
* **Lezárás:** Már csak ki kell számolni a kovarianciát! Mivel $T$ torzítatlan, az integrálalakban felírt $E(T) = \int T \cdot L \,dx = \theta$ egyenletet ha lederiváljuk $\theta$ szerint, a láncszabály és némi algebra után azt kapjuk, hogy az integrál pont $E(T \cdot S)$-et adja, ami egyenlő a jobb oldal deriváltjával, azaz $1$-gyel. Tehát $cov(T,S) = 1$. Ezt és az $S$ szórásnégyzetét visszahelyettesítve a CBS-egyenlőtlenségbe: $1^2 \le D^2(T) \cdot n \cdot I(\theta)$. Ezt $D^2(T)$-re átrendezve megkapjuk a tételt.

<br>

> Ha egy statisztikai becslés tökéletes, és eléri a Cramér-Rao alsó határt (vagyis a formulában egyenlőség áll fenn), mit árul el ez a helyzet a becslőfüggvény és a score-függvény geometriai/algebrai kapcsolatáról a Cauchy-Schwarz egyenlőtlenség szabályai alapján?

---