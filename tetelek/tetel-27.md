<a name="tetel-27"></a>

## 27. Gamma-eloszlás
[[ Tartalomjegyzék ]](../README.md#tartalomjegyzek) | [[ Előző ]](./tetel-77-78.md#tetel-77-78) | [[ Következő ]](./tetel-29.md#tetel-29)


> A Gamma-eloszlás az exponenciális eloszlás "türelmes bátyja": míg az exponenciális azt mondja meg, meddig kell várnod az *első* buszra (vagy az első meghibásodásra), a Gamma-eloszlás azt modellezi, mennyi teljes időt fogsz a megállóban tölteni, amíg pontosan az *$\alpha$-adik* busz meg nem érkezik.


### TÉTEL:
Egy folytonos $X$ valószínűségi változó Gamma-eloszlású $\alpha > 0$ (alakparaméter) és $\lambda > 0$ (skála/intenzitás paraméter) esetén, ha a sűrűségfüggvénye:
$$f(x) = \begin{cases} \frac{\lambda^\alpha}{\Gamma(\alpha)} x^{\alpha-1} e^{-\lambda x}, & \text{ha } x > 0 \\ 0, & \text{ha } x \le 0 \end{cases}$$

*(Ahol a nevezőben lévő $\Gamma(\alpha) = \int_0^\infty t^{\alpha-1} e^{-t} dt$ a matematikai Gamma-függvény, ami egész $\alpha$ esetén egyszerűen $(\alpha-1)!$ faktoriális).*

Legfontosabb jellemzők (vizsgán kötelező felírni):
* Várható érték: $E(X) = \frac{\alpha}{\lambda}$
* Szórásnégyzet: $D^2(X) = \frac{\alpha}{\lambda^2}$



### BIZONYÍTÁS:
* **Kiindulópont:** Egy szóbeli vizsgán a sűrűségfüggvény helyességét túl hosszú integrálni, a *várható érték* levezetése viszont egy gyönyörű, elvárt minifeladat. Írjuk fel a folytonos várható érték definícióját: $E(X) = \int_0^\infty x \cdot \frac{\lambda^\alpha}{\Gamma(\alpha)} x^{\alpha-1} e^{-\lambda x} dx$.
* **A "Trükk":** "Alakítsunk ki egy új sűrűségfüggvényt" az integrálon belül! Először isvonjuk össze az $x$-eket: $x \cdot x^{\alpha-1} = x^\alpha$. Célunk, hogy a magfüggvényből egy $(\alpha+1)$ paraméterű Gamma-eloszlás sűrűségfüggvényét varázsoljuk elő. Ehhez szorozzuk be és osszuk is el a kifejezést $\lambda$-val, a nevezőt pedig a jól ismert $\Gamma(\alpha+1) = \alpha \cdot \Gamma(\alpha)$ azonosság alapján manipuláljuk (az $\alpha$-t kiemelve a nevezőből).
* **Lezárás:** Ha a "felesleges" $\frac{\alpha}{\lambda}$ konstansokat kiemeljük az integráljel elé, ami bent marad, az hajszálpontosan egy új, $\alpha+1$ és $\lambda$ paraméterű Gamma-eloszlás teljes sűrűségfüggvénye lesz. Mivel a sűrűségfüggvények görbe alatti területe (a teljes tartományon vett integrálja) a valószínűségszámítás axiómái szerint szigorúan $1$, a borzalmas integrál egyszerűen köddé válik, és a táblán tiszta eredményként csak a kiemelt $\frac{\alpha}{\lambda}$ marad.

<br>

> Ha az $\alpha = 1$ paraméterű Gamma-eloszlás (ami valójában a sima exponenciális eloszlás) bizonyítottan "örökléktelen", azaz nem emlékszik a múltra, miért veszíti el ezt a különleges, memórianélküli tulajdonságát a rendszer abban a pillanatban, ahogy $\alpha > 1$ lesz (például ha egy gépben a 3. alkatrész meghibásodására várunk)?

---