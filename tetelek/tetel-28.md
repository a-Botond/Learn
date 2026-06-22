<a name="tetel-28"></a>

## 28. Exponenciális eloszlás (és örökifjú tulajdonsága)
[[ Tartalomjegyzék ]](/README.md#tartalomjegyzek) | [[ Előző ]](./tetel-22.md#tetel-22) | [[ Következő ]](./tetel-30.md#tetel-30)


> Az exponenciális eloszlás a "várakozási idők" eloszlása: azt modellezi, mennyi ideig kell várnunk a következő teljesen véletlenszerűen, de egy fix átlagos rátával bekövetkező eseményre (például egy rádióaktív részecske elbomlására), méghozzá úgy, hogy a rendszernek nincsen "memóriája" az eltelt időről.


### TÉTEL:
**Definíció:** Egy $X$ folytonos valószínűségi változó exponenciális eloszlású $\lambda$ ($\lambda > 0$) paraméterrel, ha a sűrűségfüggvénye:
$$f(x) = \begin{cases} \lambda e^{-\lambda x}, & \text{ha } x \ge 0 \\ 0, & \text{ha } x < 0 \end{cases}$$

Eloszlásfüggvénye (integrálással kapjuk, a vizsgán ezt használjuk többet): 
$$F(x) = 1 - e^{-\lambda x} \quad (x \ge 0)$$

*(Fontos jellemzők: $E(X) = \frac{1}{\lambda}$ és $D^2(X) = \frac{1}{\lambda^2}$)*

**Az "Örökifjú" (emlékezet nélküli) tulajdonság tétele:** Minden $s, t > 0$ esetén a rendszer elfelejti, mennyit vártunk már eddig:
$$P(X > s+t \mid X > s) = P(X > t)$$



### BIZONYÍTÁS:
* **Kiindulópont:** A szóbeli vizsgán a definíció felírása után a legfontosabb tételét, az **örökifjú tulajdonságot** kell levezetned. Indulj ki a bal oldalból, és írd fel a feltételes valószínűség alapképletét:
    $P(X > s+t \mid X > s) = \frac{P(X > s+t \cap X > s)}{P(X > s)}$.
* **A "Trükk":** Egyszerűsítsd a számlálóban lévő metszetet puszta logikával! Ha valami tovább tart, mint $s+t$ idő, akkor az *automatikusan* tovább tart, mint $s$ idő (hiszen $t > 0$). A két esemény metszete tehát egyszerűen a szigorúbb feltétel, maga a $P(X > s+t)$. 
* **Lezárás:** Használjuk a komplementer eloszlásfüggvényt (annak esélyét, hogy az érték *nagyobb* valaminél): $P(X > x) = 1 - F(x) = e^{-\lambda x}$. Helyettesítsük be ezt a számlálóba és a nevezőbe is:
    $\frac{e^{-\lambda(s+t)}}{e^{-\lambda s}}$.
Bontsuk fel a kitevőt a számlálóban, és egyszerűsítsünk az $e^{-\lambda s}$ taggal: $\frac{e^{-\lambda s} \cdot e^{-\lambda t}}{e^{-\lambda s}} = e^{-\lambda t}$. Ami maradt, az pontosan $P(X > t)$, vagyis megkaptuk a jobb oldalt, befejezve a bizonyítást.

<br>

> Ha egy busz érkezési ideje exponenciális eloszlású, és te már 20 perce vársz a megállóban a tűző napon, miért állítja ez a kegyetlen matematikai modell azt, hogy a várható *hátralévő* várakozási időd hajszálpontosan ugyanannyi, mintha most ebben a pillanatban érkeztél volna ki a megállóba?

---