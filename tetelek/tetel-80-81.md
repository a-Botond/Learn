<a name="tetel-80-81"></a>

## 80-81. Polinomiális és Nadaraya-Watson regresszió
[[ Tartalomjegyzék ]](../README.md#tartalomjegyzek) | [[ Előző ]](./tetel-60.md#tetel-60) | [[ Következő ]](./tetel-80-81.md#tetel-80-81)


> A polinomiális regresszió egyetlen rugalmas, de merev szabályoknak engedelmeskedő globális "drótot" (görbét) hajlít rá az egész adathalmazra, míg a Nadaraya-Watson módszer eldobja a képleteket, és minden vizsgált pontban egyszerűen csak a legközelebbi szomszédok eredményeinek lokális, a távolsággal exponenciálisan csökkenő súlyozott átlagát számolja ki.


### TÉTEL:
**1. Polinomiális regresszió:**
Keresünk egy $m$-ed fokú polinomot, ami legjobban illeszkedik az adatokra:
$$\hat{y}_i = \hat{\beta}_0 + \hat{\beta}_1 x_i + \hat{\beta}_2 x_i^2 + \dots + \hat{\beta}_m x_i^m$$
A becsült paramétervektor mátrixos alakja (megegyezik a többszörös lineáris regresszióval): $\hat{\boldsymbol{\beta}} = (\mathbf{X}^T \mathbf{X})^{-1} \mathbf{X}^T \mathbf{y}$, ahol az $\mathbf{X}$ dizájnmátrix oszlopai az $x_i$ értékek hatványai.

**2. Nadaraya-Watson (magfüggvényes/kernel) regresszió:**
Egy nemparaméteres módszer, amely a feltételes várható értéket egy $K$ magfüggvény (kernel) és $h > 0$ sávszélesség (bandwidth) segítségével becsli:
$$\hat{m}_h(x) = \frac{\sum_{i=1}^n K\left(\frac{x - X_i}{h}\right) Y_i}{\sum_{i=1}^n K\left(\frac{x - X_i}{h}\right)}$$



### BIZONYÍTÁS:
* **Kiindulópont:** A két módszer gyökere teljesen más! A polinomiálisnál a kiindulás a standard OLS (legkisebb négyzetek) hibafüggvényének felírása. A Nadaraya-Watsonnál az elméleti regressziós görbe (a feltételes várható érték) matematikai definíciója a rajtkő: $E(Y \mid X=x) = \int y \frac{f(x,y)}{f_X(x)} dy$.
* **A "Trükk":** - *Polinomiálisnál:* A "linearizációs" trükk! Az $x^2, x^3 \dots x^m$ hatványokat egyszerűen elnevezzük új, független változóknak ($z_2, z_3 \dots z_m$). Ezzel a nemlineáris problémát egyetlen elegáns mozdulattal visszaminősítjük egy mezei többszörös lineáris regresszióvá.
    - *N-W esetében:* A Parzen-Rosenblatt-féle **sűrűségfüggvény-becslés (KDE)** bevetése! Mivel a fenti integrálban szereplő $f(x,y)$ együttes és $f_X(x)$ peremsűrűséget nem ismerjük, a "trükk" az, hogy a mintapontok köré rajzolt, $h$ szélességű $K$ magfüggvények (púpok) empirikus átlagával helyettesítjük be őket az integrálba.
* **Lezárás:** A polinomiális esetben a felírt $m$-változós hibafüggvény parciális deriváltjait nullává tesszük, amiből kiesik a jól ismert normálegyenlet-rendszer és az inverz mátrixos megoldás. A Nadaraya-Watsonnál a sűrűségbecslőket visszaírva a várható érték definíciójába, az $y$ szerinti integrálás végrehajtása zseniálisan "kiválogatja" és a felszínre hozza az $Y_i$ pontokat, így a bonyolult analízises képletből másodpercek alatt előáll a tételben szereplő gyönyörű, lokálisan súlyozott átlag.

<br>

> Ha a Nadaraya-Watson regresszióban a sávszélesség paramétert ($h$) elkezded a végtelenbe növelni, az összes adatpont súlya gyakorlatilag egyenlővé válik. Geometriailag mi lesz ekkor a regressziós görbédből, és hogyan mutatja meg ez a véglet a klasszikus "paraméteres" és a "lokális nemparaméteres" megközelítések közötti elvi különbséget?

---