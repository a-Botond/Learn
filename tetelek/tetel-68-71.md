<a name="tetel-68-71"></a>

## 68-71. Fisher-információ
[[ Tartalomjegyzék ]](/README.md#tartalomjegyzek) | [[ Előző ]](./tetel-79.md#tetel-79) | [[ Következő ]](./tetel-72.md#tetel-72)


> A Fisher-információ azt a "képélességet" méri, hogy a megfigyelt adataink mennyire határolják be egyértelműen az ismeretlen paramétert: ha ez az érték magas, a valószerűségi görbénknek tűhegyes csúcsa van, így szinte lehetetlen mellélőni a becslésnél.


### TÉTEL:
Legyen $X$ egy véletlen minta, amelynek sűrűségfüggvénye (vagy diszkrét eloszlása) $f(x; \theta)$, ahol $\theta$ a becslendő ismeretlen paraméter. 
A **Fisher-információ** definíciója az úgynevezett *score-függvény* (a log-likelihood első deriváltja) négyzetének várható értéke:
$$I(\theta) = E\left[ \left( \frac{\partial}{\partial \theta} \ln f(X; \theta) \right)^2 \right]$$

Megfelelő regularitási feltételek (kétszeres deriválhatóság és az integrálással/szummázással való felcserélhetőség) mellett a vizsgán is gyakrabban használt, számoláskönnyítő alternatív alak:
$$I(\theta) = -E\left[ \frac{\partial^2}{\partial \theta^2} \ln f(X; \theta) \right]$$

Több ($n$ darab) független, azonos eloszlású (i.i.d.) mintaelem esetén az információ lineárisan additív: $I_n(\theta) = n \cdot I(\theta)$.



### BIZONYÍTÁS:
* **Kiindulópont:** A szóbeli vizsgán a tétel lelke a két fenti formula egyenértékűségének (a második alaknak a) levezetése. Induljunk ki a sűrűségfüggvény legfundamentálisabb axiómájából: a teljes téren vett integrálja mindig $1$, azaz $\int f(x; \theta) dx = 1$.
* **A "Trükk":** Deriváljuk le ezt az egyenletet $\theta$ szerint az integráljel alatt! A zseniális lépés a logaritmikus derivált trükkjének "visszafelé" történő alkalmazása: a láncszabály miatt $\frac{\partial f}{\partial \theta} = f \cdot \frac{\partial \ln f}{\partial \theta}$. Ez az első deriválás megmutatja, hogy a score-függvény várható értéke egzaktan nulla. Az igazi trükk itt jön: **deriváljuk le még egyszer** az egyenletet $\theta$ szerint, most már a szorzatszabályt használva!
* **Lezárás:** A második deriválás után az integrálon belül két tag keletkezik: az egyikben a log-likelihood második deriváltja áll (szorozva $f$-fel), a másikban pedig a log-likelihood első deriváltjának a négyzete (szintén szorozva $f$-fel). Mivel a jobb oldalon a konstans $1$ második deriváltja továbbra is $0$, az integrálokat várható értékként kiolvasva megkapjuk a következőt: $E\left[\frac{\partial^2}{\partial \theta^2} \ln f \right] + E\left[ \left(\frac{\partial}{\partial \theta} \ln f\right)^2 \right] = 0$. Ezt algebrailag átrendezve hajszálpontosan kiadódik az alternatív, negatív előjeles képlet.

<br>

> Ha a Fisher-információ alternatív képlete negatív előjellel veszi a log-likelihood függvény második deriváltjának (vagyis a görbületének) a várható értékét, miért teljesen logikus az, hogy egy extrém "hegyes" és gyorsan zuhanó maximumhely hatalmas Fisher-információt jelent, és hogyan diktálja ez a puszta tény a becslésünk statisztikai bizonytalanságát?

---