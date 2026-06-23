<a name="tetel-56-57"></a>

## 56-57. Kétmintás u- és t-próbák
[[ Tartalomjegyzék ]](../README.md#tartalomjegyzek) | [[ Előző ]](./tetel-66.md#tetel-66) | [[ Következő ]](./tetel-61.md#tetel-61)


> A kétmintás próbák azt vizsgálják, hogy két teljesen különálló csoport (például egy új gyógyszert kapó és egy kontrollcsoport) átlagai közötti megfigyelt különbség valódi, rendszerszintű eltérésre utal-e, vagy csupán a véletlen mintavétel okozta zaj játékáról van szó.


### TÉTEL:
**Feltételek:** Legyen $X_1, \dots, X_{n_1}$ és $Y_1, \dots, Y_{n_2}$ két *független*, normális eloszlású minta, $m_1$ és $m_2$ ismeretlen várható értékekkel.

**Nullhipotézis ($H_0$):** A két sokaság átlaga megegyezik ($m_1 = m_2$, azaz a különbségük $m_1 - m_2 = 0$).

**1. Kétmintás u-próba (Ismert szórások esetén):**
Ha a populációk $\sigma_1$ és $\sigma_2$ szórásai ismertek, a próbastatisztika:
$$u = \frac{\overline{X} - \overline{Y}}{\sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}}$$
Eloszlás $H_0$ esetén: $u \sim \mathcal{N}(0, 1)$.

**2. Kétmintás t-próba (Ismeretlen, de azonos szórások esetén):**
Ha a szórások ismeretlenek, de feltesszük, hogy megegyeznek ($\sigma_1 = \sigma_2 = \sigma$), a közös szórást a két minta korrigált tapasztalati szórásnégyzeteiből ($s_X^{*2}, s_Y^{*2}$) "összevonva" becsüljük: $s_p = \sqrt{\frac{(n_1-1)s_X^{*2} + (n_2-1)s_Y^{*2}}{n_1+n_2-2}}$. A próbastatisztika:
$$t = \frac{\overline{X} - \overline{Y}}{s_p \sqrt{\frac{1}{n_1} + \frac{1}{n_2}}}$$
Eloszlás $H_0$ esetén: $t \sim t_{n_1+n_2-2}$ (Student-féle t-eloszlás).



### BIZONYÍTÁS:
* **Kiindulópont:** A szóbeli vizsgán a fókusz a számláló, azaz a mintaátlagok különbségének ($D = \overline{X} - \overline{Y}$) eloszlásán van. Mivel $X$ és $Y$ normális változók, a lineáris kombinációjuk is normális eloszlású lesz. Ha a $H_0$ igaz, akkor a különbség várható értéke pontosan nulla: $E(\overline{X} - \overline{Y}) = m_1 - m_2 = 0$.
* **A "Trükk":** A függetlenség miatti szórásnégyzet-additivitás! Itt vérzik el a legtöbb hallgató: hiába vonjuk ki a változókat egymásból, a bizonytalanságuk (szórásnégyzetük) mindig *összeadódik*. A szorzó konstans kiemelésének szabálya szerint $D^2(A - B) = D^2(A) + (-1)^2 D^2(B)$. Ezt alkalmazva az átlagokra a teljes szórásnégyzet: $D^2(\overline{X} - \overline{Y}) = \frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}$.
* **Lezárás:** Standardizáljuk az átlagok különbségét! Vonjuk le a várható értékét (ami $0$), és osszuk el a gyökvonással kapott szórásával. Ismert szórásoknál ez közvetlenül a standard normális $u$-statisztikát adja. Ismeretlen, de azonos szórásnál az elméleti $\sigma$-t az $s_p$ egyesített becsléssel helyettesítjük. Mivel az egyesített szórásnégyzet egy $\chi^2$-eloszlású változóból származik, a t-eloszlás definíciója értelmében megkapjuk a Student-eloszlást, ahol a szabadságfokok száma logikusan a két minta szabadságfokának összege: $(n_1-1) + (n_2-1) = n_1+n_2-2$.

<br>

> Ha a próbastatisztika számlálójában a két csoport átlagát *kivonjuk* egymásból, miért diktálja a valószínűségszámítás vastörvénye azt, hogy a nevezőben (a bizonytalanság kiszámításakor) a két minta szórásnégyzetét kötelezően *összeadni* kell, és miért lenne elvi hiba ott is a különbségüket venni?

---