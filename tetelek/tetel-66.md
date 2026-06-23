<a name="tetel-66"></a>

## 66. Erősen konzisztens becslések
[[ Tartalomjegyzék ]](../README.md#tartalomjegyzek) | [[ Előző ]](./tetel-50.md#tetel-50) | [[ Következő ]](./tetel-56-57.md#tetel-56-57)


> A konzisztencia azt a megnyugtató statisztikai ígéretet jelenti, hogy ha a végtelenségig növeljük a gyűjtött adatok (a minta) mennyiségét, akkor a becslésünk hibája nemcsak szimplán csökken, hanem 100%-os bizonyossággal, tévedhetetlenül "rácuppan" a keresett, valódi elméleti értékre.


### TÉTEL:
Legyen $X_1, X_2, \dots, X_n$ egy minta, és $\hat{\theta}_n = \hat{\theta}_n(X_1, \dots, X_n)$ egy becslőfüggvény-sorozat az ismeretlen $\theta$ paraméterre. 

A $\hat{\theta}_n$ becslés **erősen konzisztens**, ha a becslések sorozata $1$ valószínűséggel (majdnem biztosan) konvergál a valódi paraméterértékhez:
$$P\left( \lim_{n \to \infty} \hat{\theta}_n = \theta \right) = 1$$

*(Vizsgás mentőöv: Nagyon fontos hangsúlyozni, hogy ez szigorúbb, mint a "sima" vagy gyenge konzisztencia, ami csak sztochasztikus konvergenciát követel meg: $\lim_{n \to \infty} P(|\hat{\theta}_n - \theta| > \varepsilon) = 0$)*.



### BIZONYÍTÁS:
* **Kiindulópont:** Mivel általános becslésre nehéz bizonyítani, a vizsgán tipikusan a tapasztalati átlag (vagy momentumok) erős konzisztenciáját kell levezetni. Írjuk fel a **Nagy számok erős törvényét (Kolmogorov-féle törvény)**! Ez az axióma garantálja, hogy ha a minta i.i.d. és létezik várható értéke ($m$), akkor a mintaátlag $1$ valószínűséggel tart oda: $P(\lim \overline{X}_n = m) = 1$.
* **A "Trükk":** A **folytonos leképezési tétel (Continuous Mapping Theorem)** bevetése! A gyakorlatban a bonyolultabb becsléseink (pl. a momentummódszernél) a mintaátlagok *folytonos függvényeiként* ($g$) állnak elő: $\hat{\theta}_n = g(\overline{X}_n)$. A trükk az, hogy a folytonos függvények "átengedik magukon" a határértéket, azaz a limesz és a függvény sorrendje felcserélhető.
* **Lezárás:** "Vigyük be" a határértéket a függvény belsejébe! $1$ valószínűséggel teljesül, hogy $\lim_{n \to \infty} g(\overline{X}_n) = g(\lim_{n \to \infty} \overline{X}_n)$. Mivel a NSET miatt a belső limesz maga az $m$ elméleti várható érték, így az eredmény $g(m)$ lesz. Mivel a mi függvényünket pont úgy alkottuk meg, hogy $g(m) = \theta$ legyen, azonnal megkapjuk, hogy a becslőfüggvény limesze is $1$ valószínűséggel $\theta$, azaz erősen konzisztens.

<br>

> Ha egy becslőfüggvény-sorozat erősen konzisztens (azaz a végtelenben garantáltan eltalálja a pontos célt), matematikailag lehetséges-e, hogy közben minden véges $n$ elemű mintára folyamatosan, szisztematikusan *torzított* marad, és ha igen, miért fogadják el a statisztikusok mégis zseniális becslésként?

---