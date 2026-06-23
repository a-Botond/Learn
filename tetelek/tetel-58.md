<a name="tetel-58"></a>

## 58. Welch-próba (Kétmintás t-próba nem egyenlő szórások esetére)
[[ Tartalomjegyzék ]](/README.md#tartalomjegyzek) | [[ Előző ]](./tetel-31.md#tetel-31) | [[ Következő ]](./tetel-60.md#tetel-60)


> A Welch-próba a klasszikus kétmintás t-próba "megengedőbb" nagytesója: azt vizsgálja, hogy két csoport átlaga azonos-e, de nem kényszeríti rájuk azt az a priori (és sokszor irreális) feltételt, hogy a természetes ingadozásuk (szórásuk) is milliméterre pontosan megegyezzen, hanem a "szabadságfok" ravasz lecsökkentésével kompenzálja ezt a plusz bizonytalanságot.


### TÉTEL:
**Feltételek:** Legyen $X_1, \dots, X_{n_1}$ és $Y_1, \dots, Y_{n_2}$ két független, normális eloszlású minta, ismeretlen és *nem feltétlenül egyenlő* ($\sigma_1^2 \neq \sigma_2^2$) szórásnégyzetekkel. 
**Nullhipotézis ($H_0$):** A két sokaság átlaga megegyezik ($m_1 = m_2$).

A próbastatisztika:
$$t_w = \frac{\overline{X} - \overline{Y}}{\sqrt{\frac{s_1^{*2}}{n_1} + \frac{s_2^{*2}}{n_2}}}$$
*(ahol $s_1^{*2}$ és $s_2^{*2}$ a korrigált tapasztalati szórásnégyzetek).*

**Eloszlás:** $H_0$ fennállása esetén a statisztika eloszlása *közelítőleg* Student-féle t-eloszlást követ az alábbi, úgynevezett **Welch–Satterthwaite-féle effektív szabadságfokkal** ($df$):
$$df = \frac{\left(\frac{s_1^{*2}}{n_1} + \frac{s_2^{*2}}{n_2}\right)^2}{\frac{(s_1^{*2}/n_1)^2}{n_1-1} + \frac{(s_2^{*2}/n_2)^2}{n_2-1}}$$



### BIZONYÍTÁS:
* **Kiindulópont:** A t-eloszlás definíciójához egy standard normális eloszlású változót kell elosztanunk egy független $\chi^2$ (Khí-négyzet) eloszlású változó gyökével. A statisztikánk számlálója rendben van: $H_0$ esetén $\overline{X} - \overline{Y}$ normális eloszlású, várható értéke $0$, valódi varianciája pedig $\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}$.
* **A "Trükk":** A momentumok illesztése (Satterthwaite-approximáció)! Mivel a szórások eltérőek, a minták szórásnégyzeteiből képzett nevezőt nem tudjuk tisztán egyetlen, egzakt $\chi^2$ eloszlássá összevonni (mint a sima t-próbánál). A trükk az, hogy ezt a lineáris kombinációt egy fiktív, $df$ szabadságfokú $\chi^2$ eloszlással *közelítjük*. Ezt úgy érjük el, hogy a fiktív eloszlás szórásnégyzetét (ami $2 \cdot df$) algebrailag egyenlővé tesszük a mi két különálló kifejezésünk szórásnégyzetének összegével. Ebből a mesterséges egyenlőségből fejezzük ki a $df$-et.
* **Lezárás:** A fenti algebrai átrendezésből pontosan a tételben kimondott, robusztus, tört alakú $df$ képlet "göngyölődik" ki. Ezzel az illesztéssel a standard normális számláló és a fiktív $\chi^2$-tel közelített nevező hányadosa a matematikai statisztika szabályai szerint egy $df$ paraméterű (ami így nem is feltétlenül egész szám!) t-eloszlásként fog viselkedni.

<br>

> Ha a két megfigyelt csoportod elemszáma hajszálpontosan megegyezik ($n_1 = n_2$), és a mintákból kiszámolt tapasztalati szórásaik is teljesen azonosak ($s_1^{*2} = s_2^{*2}$), vajon összeomlik-e ez a borzalmasnak tűnő Welch-féle szabadságfok-képlet a klasszikus t-próba egyszerű $(n_1 + n_2 - 2)$ képletévé – és ha igen, mit árul el ez arról, hogy valójában melyik próba tekinthető a másik speciális esetének?

---