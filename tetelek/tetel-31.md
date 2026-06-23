<a name="tetel-31"></a>

## 31. Weibull-eloszlás
[[ Tartalomjegyzék ]](/README.md#tartalomjegyzek) | [[ Előző ]](./tetel-29.md#tetel-29) | [[ Következő ]](./tetel-58.md#tetel-58)


> A Weibull-eloszlás a megbízhatóságelmélet "jokere": rugalmasan képes leírni egy alkatrész (vagy élőlény) élettartamát, függetlenül attól, hogy a meghibásodás esélye az idővel egyre nő (kopás, öregedés), folyamatosan csökken (bejáratódási szakasz), vagy éppen teljesen állandó.


### TÉTEL:
Egy $X$ folytonos valószínűségi változó Weibull-eloszlású $k > 0$ (alakparaméter) és $\lambda > 0$ (skála/élettartam paraméter) esetén, ha az eloszlásfüggvénye (mivel ez zárt alakú, vizsgán gyakran ebből indulunk):
$$F(x) = \begin{cases} 1 - e^{-(x/\lambda)^k}, & \text{ha } x \ge 0 \\ 0, & \text{ha } x < 0 \end{cases}$$

A sűrűségfüggvénye (deriválással):
$$f(x) = \begin{cases} \frac{k}{\lambda} \left(\frac{x}{\lambda}\right)^{k-1} e^{-(x/\lambda)^k}, & \text{ha } x \ge 0 \\ 0, & \text{ha } x < 0 \end{cases}$$

*(A vizsgán az egyik legfontosabb elvárt képlet)* a várható érték:
$$E(X) = \lambda \cdot \Gamma\left(1 + \frac{1}{k}\right)$$



### BIZONYÍTÁS:
* **Kiindulópont:** Egy szóbeli vizsgán a sűrűségfüggvényt általában nem kell fejből tudni, de a várható érték levezetése klasszikus vizsgafeladat. Írjuk fel a folytonos várható érték definícióját: $E(X) = \int_0^\infty x \cdot \frac{k}{\lambda} \left(\frac{x}{\lambda}\right)^{k-1} e^{-(x/\lambda)^k} dx$. Ránézésre ez egy reménytelenül csúnya integrál.
* **A "Trükk":** Az integrálhelyettesítés! Vezessünk be egy új változót a teljes kitevőre: legyen $t = (x/\lambda)^k$. Fejezzük ki ebből az eredeti változót: $x = \lambda \cdot t^{1/k}$. Ha megnézzük a differenciálokat, egy zseniális dolog történik: az eredeti sűrűségfüggvény bonyolult első fele pontosan a $dt$ differenciált adja meg (hiszen $f(x)dx$ nem más, mint a $1-e^{-t}$ deriváltja), így a borzalmas $f(x)dx$ csomag egyszerűen $e^{-t} dt$-vé szelídül!
* **Lezárás:** Helyettesítsük be ezeket az integrálba. Az $x$ helyére bekerül a $\lambda \cdot t^{1/k}$, a maradék pedig $e^{-t} dt$ lesz. Az integrálunk így néz ki: $\lambda \int_0^\infty t^{1/k} e^{-t} dt$. Emeljük ki a $\lambda$-t, és vegyük észre a bent maradó részt: ez hajszálpontosan a matematikai Gamma-függvény definíciója! A $t$ kitevője alapján (mivel a formula $\int t^{z-1} e^{-t} dt = \Gamma(z)$), a belső rész pontosan $\Gamma(1 + 1/k)$ lesz. A $\lambda$-val beszorozva meg is kaptuk a tétel végeredményét.

<br>

> Ha a Weibull-eloszlás $k$ alakparamétere pontosan $1$, a képlet egy jól ismert, "memórianélküli" eloszlássá (az exponenciálissá) omlik össze – de vajon logikailag mit jelent az "öregedés" szempontjából az, ha $k < 1$ (például $0,5$), és a való életben milyen műszaki berendezésekre vagy folyamatokra lehet ez igaz a kicsomagolás utáni legelső napokban?

---