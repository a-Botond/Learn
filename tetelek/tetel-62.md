<a name="tetel-62"></a>

## 62. Függetlenségvizsgálat (Khí-négyzet próba kontingenciatáblákra)
[[ Tartalomjegyzék ]](../README.md#tartalomjegyzek) | [[ Előző ]](./tetel-61.md#tetel-61) | [[ Következő ]](./tetel-79.md#tetel-79)


> A függetlenségvizsgálat azt ellenőrzi, hogy két tulajdonság (például a nem és a politikai preferencia) között van-e bármilyen valós kapcsolat, méghozzá úgy, hogy összehasonlítja a táblázatunkban lévő tényleges adatokat azokkal a "kikevert" darabszámokkal, amiket akkor látnánk, ha a két dolog teljesen vak lenne egymásra.


### TÉTEL:
**Feltételek:** Két diszkrét (vagy kategóriába sorolt) ismérvet vizsgálunk. Az $X$ ismérvnek $r$ darab, az $Y$ ismérvnek $c$ darab kategóriája van. Az adatokat egy $r \times c$-s kontingenciatáblázatba foglaljuk.
Jelölje a megfigyelt gyakoriságot a cellákban $\nu_{ij}$, a sorösszegeket $\nu_{i.}$, az oszlopösszegeket $\nu_{.j}$, a teljes elemszámot pedig $n$.

**Nullhipotézis ($H_0$):** A két ismérv független egymástól, azaz minden $(i,j)$ párra $P(X=x_i, Y=y_j) = P(X=x_i) \cdot P(Y=y_j)$.

**A próbastatisztika:**
$$\chi^2 = \sum_{i=1}^{r} \sum_{j=1}^{c} \frac{\left( \nu_{ij} - \frac{\nu_{i.} \cdot \nu_{.j}}{n} \right)^2}{\frac{\nu_{i.} \cdot \nu_{.j}}{n}}$$

**Eloszlás:** Ha $H_0$ igaz (és a cellák elvárt gyakorisága elegendően nagy, tipikusan $\ge 5$), a statisztika aszimptotikusan Khí-négyzet eloszlást követ $f = (r-1)(c-1)$ szabadságfokkal.



### BIZONYÍTÁS:
* **Kiindulópont:** Építsünk az előző tételre, az illeszkedésvizsgálatra! A táblázat $r \cdot c$ darab cellája felfogható egyetlen nagy, több kimenetelű kísérletnek. Írjuk fel a standard Pearson-féle képletet: $\sum \frac{(\text{Tapasztalati} - \text{Elvárt})^2}{\text{Elvárt}}$. 
* **A "Trükk":** Hogyan számoljuk ki a cellák elméletileg *elvárt* gyakoriságát, ha a valódi valószínűségeket nem ismerjük? Itt vetjük be a függetlenség definícióját ($P(A \cap B) = P(A) \cdot P(B)$)! Az ismeretlen peremvalószínűségeket magából a mintából becsüljük: a sor valószínűsége $\hat{p}_i = \frac{\nu_{i.}}{n}$, az oszlopé $\hat{p}_j = \frac{\nu_{.j}}{n}$. A függetlenség miatt a cella valószínűsége ezek szorzata. Ezt beszorozva a teljes $n$ elemszámmal pontosan megkapjuk a nevezőben lévő $\frac{\nu_{i.} \cdot \nu_{.j}}{n}$ formulát.
* **Lezárás:** Helyettesítsük be ezeket az elvárt értékeket a Pearson-képletbe, amivel a statisztikát meg is kaptuk. A szabadságfok ($f$) meghatározásához a teljes cellaszámból ($r \cdot c - 1$) le kell vonni a mintából becsült paraméterek számát. Mivel a valószínűségek összege 1, a soroknál $(r-1)$, az oszlopoknál $(c-1)$ független paramétert becsültünk. Az algebrai kivonás: $(r c - 1) - (r - 1) - (c - 1) = r c - r - c + 1$, ami elegánsan szorzattá alakítható: $(r-1)(c-1)$.

<br>

> Ha egy $2 \times 2$-es kontingenciatáblázatban a peremösszegek (a sorok és oszlopok végén lévő szummák) már előre kőbe vannak vésve, miért van az, hogy elég egyetlenegy belső cella értékét megadni, és abból a maradék három cella tartalma már egyértelműen, automatikusan kiszámítható – és hogyan adja meg ez a tény a kézzelfogható magyarázatot a fenti $(r-1)(c-1)$ szabadságfokra?

---