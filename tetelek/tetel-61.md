<a name="tetel-61"></a>

## 61. Illeszkedésvizsgálat (Pearson-féle Khí-négyzet próba)
[[ Tartalomjegyzék ]](/README.md#tartalomjegyzek) | [[ Előző ]](./tetel-56-57.md#tetel-56-57) | [[ Következő ]](./tetel-62.md#tetel-62)


> Az illeszkedésvizsgálat azt ellenőrzi, hogy a valóságban megfigyelt adataink mennyire passzolnak egy előre kitalált elméleti modellhez; ezt úgy teszi, hogy a tényleges és az elvárt darabszámok közötti eltéréseket összegzi, és ha a kapott "hibapontszám" gyanúsan nagy, akkor az elméleti modellt egyszerűen kidobjuk.


### TÉTEL:
**Feltételek:** Legyen $n$ a mintaelemszám, amelyet $r$ darab diszjunkt (egymást kizáró) kategóriába (osztályba) sorolunk. Jelölje a megfigyelt gyakoriságokat a kategóriákban $\nu_1, \nu_2, \dots, \nu_r$ (ahol $\sum \nu_i = n$). 

**Nullhipotézis ($H_0$):** A kísérlet kimenetelei egy előre megadott $p_1, p_2, \dots, p_r$ elméleti valószínűség-eloszlást követnek (ahol a várható gyakoriság az $i$-edik osztályban: $n \cdot p_i$).

**A próbastatisztika:**
$$\chi^2 = \sum_{i=1}^{r} \frac{(\nu_i - n \cdot p_i)^2}{n \cdot p_i}$$

**Eloszlás:** Ha a nullhipotézis igaz és a minta elég nagy (ökölszabály: $n \cdot p_i \ge 5$ minden osztályra), akkor a statisztika aszimptotikusan $\chi^2$-eloszlást követ $f = r - 1 - c$ szabadságfokkal (ahol $c$ a mintából becsült paraméterek száma; tiszta illeszkedésnél $c=0$, így a szabadságfok $r - 1$).



### BIZONYÍTÁS:
* **Kiindulópont:** A szóbeli vizsgán a levezetés alapja a megfigyelt $\nu_i$ gyakoriságok együttes eloszlásának felírása. Mivel visszatevéses (vagy végtelen populációból vett) független mintáról beszélünk $r$ lehetséges kimenetellel, a rendszer egy **multinomiális eloszlást** követ.
* **A "Trükk":** A többdimenziós Centrális Határeloszlás-tétel (konkrétan a de Moivre–Laplace-tétel lokális alakjának) alkalmazása! Ahogy $n \to \infty$, a binomiális/multinomiális eloszlás többdimenziós normális eloszláshoz közelít. A trükk az, hogy a sűrűségfüggvényt közelítő többdimenziós normális eloszlás exponenciális kitevőjében hajszálpontosan a $\sum \frac{(\nu_i - np_i)^2}{np_i}$ alak (a Pearson-statisztika) jelenik meg az algebrai átrendezés után!
* **Lezárás:** Mivel a statisztikánk lényegében aszimptotikusan standardizált normális valószínűségi változók négyzeteinek összege, definíció szerint $\chi^2$-eloszláshoz tart. A szabadságfok pedig azért nem a kategóriák száma ($r$), hanem $r - 1$, mert a megfigyelt gyakoriságok nem teljesen szabadok: van egy kőbe vésett lineáris kényszerfeltételük, miszerint az összegüknek kötelezően ki kell adnia a fix $n$ mintaelemszámot ($\sum \nu_i = n$), ami pontosan egy dimenziót "megeszik" a térből.

<br>

> A $\chi^2$ képletében miért osztunk elméleti osztályonként külön-külön a várható gyakorisággal ($n \cdot p_i$)? Vagyis logikailag miért bünteti a statisztika sokkal brutálisabban mondjuk egy 10 darabos abszolút eltérést akkor, ha az egy nagyon ritka kategóriában történik, mintha egy nagyon gyakori kategóriában történt volna?

---