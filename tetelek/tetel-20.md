<a name="tetel-20"></a>

## 20. Geometriai eloszlás
[[ Tartalomjegyzék ]](/README.md#tartalomjegyzek) | [[ Előző ]](./tetel-55.md#tetel-55) | [[ Következő ]](./tetel-24.md#tetel-24)


> A geometriai eloszlás azt a mindennapi, olykor bosszantó "meddig kell próbálkoznom, amíg végre sikerül" helyzetet írja le, és pontosan megadja annak az esélyét, hogy a várva várt első siker hajszálpontosan a $k$-adik kísérletünkre fog összejönni.


### TÉTEL:
Egy $X$ diszkrét valószínűségi változó geometriai eloszlású $p$ ($0 < p < 1$) paraméterrel (jelölése: $X \sim \text{Geo}(p)$), ha azt méri, hogy egy független kísérletsorozatban hányadik próbálkozásra következik be a legelső "siker".

Valószínűség-eloszlása:
$$P(X = k) = (1-p)^{k-1} \cdot p \quad \text{ahol } k \in \{1, 2, 3, \dots\}$$

*(Szóbeli vizsgán rögtön rákérdezhetnek a legfontosabb jellemzőkre is)*:
* Várható értéke: $E(X) = \frac{1}{p}$
* Szórásnégyzete: $D^2(X) = \frac{1-p}{p^2}$



### BIZONYÍTÁS:
* **Kiindulópont:** (A képlet levezetése) Vizsgáljuk meg logikailag a konkrét eseménysorozatot! Ahhoz, hogy a legelső siker hajszálpontosan a $k$-adik lépésben történjen meg, az kell, hogy az ezt megelőző $k-1$ darab kísérlet kivétel nélkül "kudarc" legyen, majd legvégül a $k$-adik "siker".
* **A "Trükk":** A kísérletek **függetlenségének** kihasználása (szorzástétel)! Mivel a próbálkozások nem hatnak egymásra, ennek a konkrét láncolatnak (metszetnek) a valószínűsége egyszerűen a független események valószínűségeinek szorzata lesz: $1-p$ a kudarcnak, $p$ a sikernek. Szorzatként felírva: $(1-p) \cdot (1-p) \cdots (1-p) \cdot p$.
* **Lezárás:** Összevonva a tényezőket azonnal adódik a tétel alapképlete: $(1-p)^{k-1} \cdot p$. *(Oktatói bónusz: Ha a vizsgán megkérdezem, honnan tudod, hogy ez egy "szabályos" eloszlás, azaz az esélyek összege 1, mutass rá, hogy ez egy végtelen mértani sor $q = 1-p$ hányadossal. Az összegképlet alapján $\sum P(X=k) = \frac{p}{1-(1-p)} = \frac{p}{p} = 1$.)*

<br>

> Ha egy teljesen szabályos dobókockával addig dobálunk, amíg ki nem jön a hatos, miért mondja azt a geometriai eloszlás (és a kíméletlen matematika is), hogy a legelső siker bekövetkezésének a legvalószínűbb időpontja már rögtön az *első* dobásnál van ($k=1$), miközben a várható érték ($1/p$) alapján átlagosan 6 dobást kellene várnunk a sikerre?

---