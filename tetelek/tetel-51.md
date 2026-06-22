<a name="tetel-51"></a>

## 51. Momentummódszer (Becsléselmélet)
[[ Tartalomjegyzék ]](/README.md#tartalomjegyzek) | [[ Előző ]](./tetel-47.md#tetel-47) | [[ Következő ]](./tetel-52.md#tetel-52)


> A momentummódszer logikája végtelenül egyszerű: feltételezzük, hogy a vizsgált sokaság elméleti "átlagai" (várható értéke, szórása) pontosan megegyeznek a kezünkben lévő konkrét minta ténylegesen kiszámolt átlagaival, és ebből az egyenlőségből visszafejtjük az ismeretlen paramétereket.


### TÉTEL:
Legyen $X_1, X_2, \dots, X_n$ egy független, azonos eloszlású minta, amelynek eloszlása $k$ darab ismeretlen paramétertől ($\theta_1, \theta_2, \dots, \theta_k$) függ. 

Az eloszlás $j$-edik **elméleti momentuma**: $\mu_j(\theta_1, \dots, \theta_k) = E(X^j)$
A minta $j$-edik **empirikus (tapasztalati) momentuma**: $M_j = \frac{1}{n} \sum_{i=1}^n X_i^j$

A momentummódszer szerinti $\hat{\theta}_1, \dots, \hat{\theta}_k$ becsléseket az alábbi $k$ ismeretlenes egyenletrendszer megoldása adja meg:
$$\mu_j(\hat{\theta}_1, \dots, \hat{\theta}_k) = M_j \quad \text{minden } j = 1, 2, \dots, k \text{ esetén.}$$



### BIZONYÍTÁS:
* **Kiindulópont:** (Ennél a tételnél klasszikus értelemben vett bizonyítás helyett az eljárás elvi **jogosultságát** várja az oktató). Írjuk fel a táblára, hogy hány ismeretlen paraméterünk van ($k$ darab). Ebből tudjuk, hogy pontosan $k$ darab egyenletre lesz szükségünk, tehát az első $k$ darab elméleti és empirikus momentumot kell felírnunk.
* **A "Trükk":** A hivatkozási alap a **Nagy számok törvénye**! Ez a törvény garantálja számunkra, hogy ha a mintaelemszám elég nagy ($n \to \infty$), akkor a minta alapján számolt átlagok (empirikus momentumok, $M_j$) majdnem biztosan tartanak az eloszlás valódi elméleti átlagaihoz ($\mu_j$). Emiatt teljesen racionális és statisztikailag megalapozott lépés a kettőt egyenlővé tenni egymással.
* **Lezárás:** Miután felírtuk az egyenletrendszert (legtöbbször $k=1$ vagy $k=2$, tehát csak a várható érték és a szórásnégyzet játszik szerepet), pusztán algebrai átrendezéssel kifejezzük az ismeretlen $\theta$ paramétereket a minta konkrét értékeinek ($X_i$) függvényében. Amit kapunk, az maga a keresett pontbecslés.

<br>

> Mivel a momentummódszer "vakul" csak az elméleti és a tapasztalati átlagok gépies egyenlővé tételén alapul, miért fordulhat elő a gyakorlatban (kisebb minták vagy furcsa eloszlások esetén), hogy a módszerrel kiszámolt becslés matematikailag teljesen képtelenség lesz (például egy paraméterre, aminek valószínűséget kellene jelölnie, 1-nél nagyobb értéket, vagy egy szórás paraméterre negatív számot kapunk)?

---