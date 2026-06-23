<a name="tetel-55"></a>

## 55. t-próba (Egymintás t-próba)
[[ Tartalomjegyzék ]](../README.md#tartalomjegyzek) | [[ Előző ]](./tetel-54.md#tetel-54) | [[ Következő ]](./tetel-20.md#tetel-20)


> A t-próba az u-próba óvatosabb testvére: azt méri, hogy a mintaátlag mennyire tér el a célétrendtől, de mivel itt az alapsokaság eredeti ingadozását (szórását) sem ismerjük és azt is a mintából kell "megtippelnünk", a rendszer ezt a bizonytalanságot egy megengedőbb, szélesebb (t-eloszlású) hibahatárral bünteti, különösen pici minták esetén.


### TÉTEL:
**Feltételek:** Legyen $X_1, X_2, \dots, X_n$ egy normális eloszlású populációból vett minta, amelynek **mind a várható értéke ($m$), mind a szórása ($\sigma$) ismeretlen**. 

**Nullhipotézis ($H_0$):** A populáció várható értéke megegyezik egy előre megadott $m_0$ értékkel ($m = m_0$).

**A próbastatisztika:**
$$t = \frac{\overline{X} - m_0}{\frac{s_n^*}{\sqrt{n}}}$$
ahol $s_n^*$ a minta korrigált tapasztalati szórása (amivel az ismeretlen $\sigma$-t becsüljük).

**Eloszlás:** Ha a nullhipotézis igaz, akkor a $t$ próbastatisztika Student-féle t-eloszlást követ $f = n-1$ szabadságfokkal: $t \sim t_{n-1}$.



### BIZONYÍTÁS:
* **Kiindulópont:** A t-eloszlás levezetése az egyik legszebb statisztikai bravúr a szóbeli vizsgán! Írjuk fel az ismert standard normális u-statisztikát: $u = \frac{\overline{X} - m_0}{\sigma / \sqrt{n}} \sim \mathcal{N}(0,1)$. Mellé pedig írjuk fel a korrigált tapasztalati szórásnégyzetből képzett, $\chi^2$-eloszlású statisztikát: $y = \frac{(n-1)(s_n^*)^2}{\sigma^2} \sim \chi^2_{n-1}$. (Fontos: Fisher-tétel miatt $\overline{X}$ és $s_n^*$ függetlenek).
* **A "Trükk":** Maga a Student-féle t-eloszlás definíciója! Egy t-eloszlású változót definíció szerint úgy kapunk, hogy egy standard normális változót elosztunk egy tőle független $\chi^2$-változó és a szabadságfokának hányadosából vont négyzetgyökkel. Írjuk fel ezt a csontvázat: $t = \frac{u}{\sqrt{y / (n-1)}}$, és egyszerűen helyettesítsük be a mi $u$ és $y$ képleteinket!
* **Lezárás:** A behelyettesítés után a nevezőben ez áll: $\sqrt{\frac{(n-1)(s_n^*)^2}{\sigma^2} / (n-1)}$. Itt az $(n-1)$ szabadságfokok azonnal kiejtik egymást, a gyök alatt csak $\frac{(s_n^*)^2}{\sigma^2}$ marad, ami a gyökvonás után $\frac{s_n^*}{\sigma}$ lesz. Írjuk ezt vissza a nagy törtünk nevezőjébe: $t = \frac{\frac{\overline{X} - m_0}{\sigma / \sqrt{n}}}{\frac{s_n^*}{\sigma}}$. A legzseniálisabb lépés: a sosem ismert, valódi elméleti $\sigma$ a számlálóból és a nevezőből **kiesik**! Amit kapunk, az hajszálpontosan a $t = \frac{\overline{X} - m_0}{s_n^* / \sqrt{n}}$ próbastatisztika, bizonyítva, hogy ez tényleg $t_{n-1}$ eloszlású.

<br>

> Ha a Student-féle t-eloszlás görbéje nagy mintaelemszám (például 100 felett) esetén szinte tökéletesen rásimul a standard normális eloszlás haranggörbéjére, miért van az, hogy nagyon pici (például 5 elemű) minta esetén a t-eloszlásnak sokkal "vastagabbak a farkai", azaz miért ad jóval nagyobb esélyt az extrém kiugró értékeknek, mint az u-próba?

---