<a name="tetel-74"></a>

## 74. Elégséges statisztikai függvény
[[ Tartalomjegyzék ]](/README.md#tartalomjegyzek) | [[ Előző ]](./tetel-72.md#tetel-72) | [[ Következő ]](./tetel-77-78.md#tetel-77-78)


> Az elégséges statisztika úgy sűríti össze az összes nyers adatunkat egyetlen értékbe vagy vektorba, hogy közben egyetlen csepp információt sem veszítünk el az ismeretlen paraméterről; ha ezt a "kivonatot" ismered, az eredeti adathalmaz már semmi újat nem tudna mondani neked.


### TÉTEL:
Egy $T(\mathbf{X}) = T(X_1, \dots, X_n)$ statisztika **elégséges** a $\theta$ paraméterre, ha a minta feltételes eloszlása adott $T$ ismeretében már független $\theta$-tól.

A vizsgán a definíció helyett a gyakorlatban használt **Fisher–Neyman faktorizációs tételt** kell kimondani: 
$T(\mathbf{X})$ pontosan akkor elégséges statisztikája $\theta$-nak, ha a minta együttes sűrűségfüggvénye (a likelihood-függvény) felbontható a következő szorzatra:
$$f(\mathbf{x}; \theta) = g(T(\mathbf{x}), \theta) \cdot h(\mathbf{x})$$
ahol $g$ egy függvény, ami *csak* a statisztikán és a paraméteren keresztül függ a mintától, a $h$ függvény pedig *csak* a mintától függ, de $\theta$-t egyáltalán nem tartalmazza.



### BIZONYÍTÁS:
* **Kiindulópont:** A szóbeli vizsgán a diszkrét eset levezetését kérik, mert az nagyon elegáns. Írjuk fel az elégségesség eredeti definícióját a feltételes valószínűség Bayes-szabályával: $P(\mathbf{X} = \mathbf{x} \mid T(\mathbf{X}) = t) = \frac{P(\mathbf{X} = \mathbf{x} \text{ és } T(\mathbf{X}) = t)}{P(T(\mathbf{X}) = t)}$. Vegyük észre, hogy mivel $\mathbf{x}$ konkrét értéke automatikusan meghatározza a $t$-t, a számláló simán csak a minta együttes eloszlása: $f(\mathbf{x}; \theta)$.
* **A "Trükk":** A nevező átírása és a faktorizáció behelyettesítése! A nevező (a $T$ eloszlása) nem más, mint a számlálók összege az összes olyan lehetséges $\mathbf{y}$ mintára, amelyre $T(\mathbf{y}) = t$. Helyettesítsük be a törtbe a Fisher-Neyman felbontást: a számláló $g(t, \theta) \cdot h(\mathbf{x})$ lesz, a nevező pedig a szumma: $\sum g(t, \theta) \cdot h(\mathbf{y})$.
* **Lezárás:** Mivel a szummázás $\mathbf{y}$-on fut, a $g(t, \theta)$ tag konstansként viselkedik az összegzés szempontjából, így simán kiemelhető a szumma elé! A törtünk tehát így néz ki: $\frac{g(t, \theta) \cdot h(\mathbf{x})}{g(t, \theta) \cdot \sum h(\mathbf{y})}$. A zseniális befejezés: a $\theta$-t tartalmazó $g(t, \theta)$ kifejezés a számlálóból és a nevezőből maradéktalanul kiejti egymást. A megmaradt tört, $\frac{h(\mathbf{x})}{\sum h(\mathbf{y})}$ már nyomokban sem tartalmazza a $\theta$ paramétert, amivel matematikailag is bebizonyítottuk a definíció feltételét.

<br>

> Ha bebizonyítjuk, hogy a mintaátlag tökéletes "elégséges statisztika" egy normális eloszlás várható értékének becsléséhez, vajon nyugodt szívvel bedarálhatjuk-e a nyers adatokat a papírzúzóban abban a hitben, hogy később sem fog hiányozni, mondjuk ha a főnökünk hirtelen a folyamat ingadozására (szórására) is kíváncsi lesz?

---