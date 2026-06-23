<a name="tetel-38"></a>

## 38. Szorzat (Műveletek valószínűségi változókkal)
[[ Tartalomjegyzék ]](../README.md#tartalomjegyzek) | [[ Előző ]](./tetel-34.md#tetel-34) | [[ Következő ]](./tetel-41.md#tetel-41)


> Ha két bizonytalan dolgot összeszorzunk (például egy téglalap véletlenszerű oldalhosszait, hogy megkapjuk a területet), a szorzatuk átlagos értéke csak akkor egyenlő a külön-külön vett átlagaik szorzatával, ha a két dolog teljesen független egymástól; ha van köztük kapcsolat, akkor az "együttmozgásuk" (kovarianciájuk) el fogja torzítani a végeredményt.


### TÉTEL:
Legyen $X$ és $Y$ két valószínűségi változó. A szorzatuk várható értékére vonatkozó összefüggések:

**Általános eset (kovarianciával kifejezve):**
$$E(XY) = E(X) \cdot E(Y) + cov(X,Y)$$

**Szorzástétel független esetre:**
Ha $X$ és $Y$ **független** valószínűségi változók, akkor a kovarianciájuk nulla ($cov(X,Y) = 0$), így a szorzatuk várható értéke pontosan a várható értékek szorzata:
$$E(XY) = E(X) \cdot E(Y)$$



### BIZONYÍTÁS:
* **Kiindulópont:** A szóbeli vizsgán a független esetre vonatkozó szorzástétel levezetése a klasszikus feladat (érdemes folytonos esetre mutatni, kettős integrállal). Írjuk fel a szorzat várható értékének definícióját a kétdimenziós együttes sűrűségfüggvény ($f_{X,Y}(x,y)$) segítségével:
    $E(XY) = \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} x \cdot y \cdot f_{X,Y}(x,y) \,dx\,dy$.
* **A "Trükk":** A függetlenség definíciójának bevetése az analízisben! Mivel a tétel feltétele szerint $X$ és $Y$ függetlenek, az együttes sűrűségfüggvényük maradéktalanul szétesik a peremsűrűség-függvények szorzatára: $f_{X,Y}(x,y) = f_X(x) \cdot f_Y(y)$. Helyettesítsük be ezt a szorzatot az integrálba!
* **Lezárás:** Szeparáljuk szét a kettős integrált két darab egydimenziós integrál szorzatára! Mivel a magfüggvény most $x \cdot f_X(x) \cdot y \cdot f_Y(y)$ alakú, a változókat teljesen szét tudjuk válogatni:
    $\left( \int_{-\infty}^{\infty} x \cdot f_X(x) \,dx \right) \cdot \left( \int_{-\infty}^{\infty} y \cdot f_Y(y) \,dy \right)$.
Ezen a ponton az oktató felé fordulva csak annyit kell mondani: az első zárójel definíció szerint pontosan $E(X)$, a második pedig $E(Y)$. A kettő szorzata adja a tételt, a bizonyítás kész.

<br>

> Ha egy számolás során bebizonyítod, hogy $E(XY) = E(X)E(Y)$ (vagyis a kovariancia nulla, a változók "korrelálatlanok"), miért óriási logikai hiba ebből azonnal arra következtetni, hogy a két változó a való életben is teljesen *független* egymástól?

---