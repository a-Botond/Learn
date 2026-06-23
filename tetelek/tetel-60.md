<a name="tetel-60"></a>

## 60. Nem független t-próba (Párosított t-próba)
[[ Tartalomjegyzék ]](../README.md#tartalomjegyzek) | [[ Előző ]](./tetel-58.md#tetel-58) | [[ Következő ]](./tetel-80-81.md#tetel-80-81)


> A nem független (párosított) t-próba azt a zseniális húzást alkalmazza, hogy két erősen összefüggő adatsort (például ugyanazon betegek vérnyomását egy gyógyszer bevétele "előtt" és "után") nem két különálló sokaságként kezel, hanem egyénenként veszi a változást, így az egész bonyolult összehasonlítást egyetlen, letisztult adatsorrá olvasztja.


### TÉTEL:
**Feltételek:** Adott $n$ darab összefüggő (párosított) megfigyelés: $(X_1, Y_1), \dots, (X_n, Y_n)$. Képezzük az egyéni különbségeket: $D_i = X_i - Y_i$. Feltesszük, hogy a $D_i$ különbségek normális eloszlásúak, ismeretlen $m_D$ várható értékkel és $\sigma_D$ szórással.

**Nullhipotézis ($H_0$):** A kezelésnek nincs hatása, azaz a két állapot várható értéke megegyezik, így a különbségek várható értéke nulla: $m_D = 0$.

A próbastatisztika:
$$t = \frac{\overline{D}}{s_D} \sqrt{n}$$
*(ahol $\overline{D}$ a különbségek tapasztalati átlaga, $s_D$ pedig a különbségek korrigált tapasztalati szórása).*

**Eloszlás:** $H_0$ fennállása esetén a statisztika $t \sim t_{n-1}$ (Student-eloszlást követ $n-1$ szabadságfokkal).



### BIZONYÍTÁS:
* **Kiindulópont:** A szóbeli vizsgán rögtön mondd ki a lényeget: ez valójában nem egy új eljárás, hanem a már jól ismert **egymintás t-próba** alkalmazása egy származtatott változóra! Írjuk fel a táblára az egymintás t-statisztika általános alakját a $D_i$ változóra fókuszálva: $t = \frac{\overline{D} - m_D}{s_D / \sqrt{n}}$.
* **A "Trükk":** A dimenziócsökkentés és a zavaró kovariancia kikerülése! Mivel $X$ és $Y$ nem függetlenek (ugyanazon az emberen mértük), a különbségük elméleti szórásnégyzete $D^2(X-Y) = D^2(X) + D^2(Y) - 2 \cdot cov(X,Y)$ lenne. Ha a két mintát külön vizsgálnánk, ezt a bonyolult együttes ingadozást (a $cov$-t) is becsülnünk kellene. Azzal viszont, hogy rögtön a mérések fizikai szintjén, egyénenként vonjuk ki az értékeket ($D_i = X_i - Y_i$), ezt a belső korrelációt elegánsan "elnyeljük", és a kétdimenziós problémát egy szimpla egydimenziós feladattá butítjuk.
* **Lezárás:** Helyettesítsük be a hipotézist! Mivel a $H_0$ azt mondja ki, hogy az elméleti várható érték $m_D = 0$, a képlet számlálójából a kivonandó rész szimplán eltűnik. Mivel kikötöttük, hogy a $D_i$ értékek normál eloszlásúak, a definíció szerint egy normális eloszlású minta átlagának és a mintából becsült (Khí-négyzet eloszláson alapuló) szórásnak a standardizált hányadosa egzaktan Student-eloszlást ad. A szabadságfok azért $n-1$, mert a különbségekből ($D_i$) álló mintánk elemszáma $n$.

<br>

> Ha egy fogyókúrás tabletta tesztelésekor a párosított (nem független) t-próba masszívan szignifikáns, egyértelmű fogyást mutat, miért történhet meg az, hogy ha teljesen hibásan a független kétmintás t-próbával elemezzük *ugyanezeket* az adatokat, akkor a gyógyszer hirtelen hatástalannak tűnik? Logikailag milyen gigantikus, zavaró tényezőt szűr ki automatikusan a "párosítás" lépése?

---