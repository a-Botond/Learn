<a name="tetel-79"></a>

## 79. Lineáris regresszió (Legkisebb négyzetek módszere)
[[ Tartalomjegyzék ]](/README.md#tartalomjegyzek) | [[ Előző ]](./tetel-62.md#tetel-62) | [[ Következő ]](./tetel-68-71.md#tetel-68-71)


> A legkisebb négyzetek módszere azt a "tökéletes" egyenest keresi egy ponthalmazban, amelyik úgy feszül ki a pontok között, hogy ha minden pontból húzunk egy függőleges vonalat az egyenesig, akkor ezeknek a hibaszakaszoknak a területre emelt (négyzetes) összege a lehető legkisebb lesz.


### TÉTEL:
Adott egy $n$ elemű megfigyeléssorozat: $(x_1, y_1), (x_2, y_2), \dots, (x_n, y_n)$.
Keressük azt az $\hat{y} = ax + b$ regressziós egyenest, amely minimalizálja a megfigyelt értékek és a becsült értékek közötti eltérések négyzetösszegét (célfüggvény):
$$Q(a,b) = \sum_{i=1}^{n} (y_i - (ax_i + b))^2 \rightarrow \min$$

A minimumhelyet az úgynevezett **normálegyenlet-rendszer** megoldása adja (vizsgán ezt kérik):
1. $\sum_{i=1}^n y_i = a \sum_{i=1}^n x_i + n \cdot b$
2. $\sum_{i=1}^n x_i y_i = a \sum_{i=1}^n x_i^2 + b \sum_{i=1}^n x_i$



### BIZONYÍTÁS:
* **Kiindulópont:** A szóbeli vizsgán a levezetés azzal indul, hogy felírod a fenti $Q(a,b)$ minimalizálandó hibafüggvényt. Fontos tudatosítani (és mondani), hogy itt most a megfigyelt pontok ($x_i, y_i$) a konstansok, és az egyenes paraméterei ($a, b$) a mi változóink, amiket finomhangolunk.
* **A "Trükk":** A többváltozós analízis szélsőérték-tétele! Ahhoz, hogy a $Q(a,b)$ "hibagödörnek" megtaláljuk az alját (a minimumát), a függvény mindkét változó ($a$ és $b$) szerinti parciális deriváltját ki kell számolnunk, és azokat szigorúan egyenlővé kell tennünk nullával: $\frac{\partial Q}{\partial a} = 0$ és $\frac{\partial Q}{\partial b} = 0$. Ezen az egyetlen analízis-lépésen múlik a teljes tétel.
* **Lezárás:** Végezzük el a deriválásokat a láncszabály alapján. A $b$ szerinti derivált: $\sum 2(y_i - ax_i - b) \cdot (-1) = 0$. Az $a$ szerinti derivált (itt a belső függvény deriváltja $-x_i$ lesz): $\sum 2(y_i - ax_i - b) \cdot (-x_i) = 0$. Mindkét egyenletet azonnal osszuk el a zavaró $-2$-es szorzóval. Ezután egyszerűen bontsuk fel a szummákat, és rendezzük át az egyenleteket úgy, hogy a paramétereket ($a, b$) tartalmazó tagok átkerüljenek a jobb oldalra. Ezzel az egyszerű algebrai rendezéssel hajszálpontosan megkapjuk a fent kimondott két normálegyenletet.

<br>

> Miért pont a hibák *négyzetét* (és nem mondjuk a sima abszolút értéküket) akarjuk minimalizálni, és miért szigorúan csak a *függőleges* távolságokat mérjük a pontok és az egyenes között, ahelyett, hogy a legrövidebb, geometriailag merőleges távolságot vennénk alapul?

---