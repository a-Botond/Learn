<a name="tetel-47"></a>

## 47. Nagy számok törvénye (Gyenge törvény)
[[ Tartalomjegyzék ]](../README.md#tartalomjegyzek) | [[ Előző ]](./tetel-46.md#tetel-46) | [[ Következő ]](./tetel-51.md#tetel-51)


> A nagy számok törvénye a statisztika legfontosabb ígérete: garantálja, hogy ha egy kísérletet nagyon sokszor, egymástól függetlenül megismételsz (például kockadobás, mérés), akkor a kapott eredmények átlaga szinte biztosan hajszálpontosan beáll a valódi elméleti átlagra (a várható értékre).


### TÉTEL:
Legyenek $X_1, X_2, \dots, X_n$ független, azonos eloszlású (i.i.d.) valószínűségi változók, amelyeknek létezik közös várható értéke ($E(X_i) = m$) és véges szórásnégyzete ($D^2(X_i) = \sigma^2$). Legyen ezen változók számtani közepe (a mintaátlag) $\overline{X}_n = \frac{1}{n} \sum_{i=1}^n X_i$. 

Ekkor tetszőleges (bármilyen kicsi) $\varepsilon > 0$ hibahatár esetén érvényes:
$$\lim_{n \to \infty} P(|\overline{X}_n - m| \ge \varepsilon) = 0$$
*(Szakszóval: az átlag sztochasztikusan tart a várható értékhez. Egyenértékű megfogalmazása: $\lim_{n \to \infty} P(|\overline{X}_n - m| < \varepsilon) = 1$).*



### BIZONYÍTÁS:
* **Kiindulópont:** Oktatóként látni akarom, hogy érted az átlagolás matematikáját. Először számoljuk ki a táblán az $\overline{X}_n$ mintaátlag saját várható értékét és szórásnégyzetét! A linearitás miatt a várható érték marad az eredeti: $E(\overline{X}_n) = m$. A függetlenség miatt a szórásnégyzetek összeadódnak ($n \cdot \sigma^2$), de az $\frac{1}{n}$ szorzó négyzetesen emelődik ki: így a mintaátlag szórásnégyzete $D^2(\overline{X}_n) = \frac{1}{n^2} \cdot n\sigma^2 = \frac{\sigma^2}{n}$. 
* **A "Trükk":** Mivel az előző tételben épp bizonyítottuk, szabadítsuk rá közvetlenül erre az $\overline{X}_n$ változóra a **Csebisev-egyenlőtlenséget**! Nem kell új módszert kitalálni, az előző tétel adja a kulcsot.
* **Lezárás:** A Csebisev-egyenlőtlenség szerint $P(|\overline{X}_n - m| \ge \varepsilon) \le \frac{D^2(\overline{X}_n)}{\varepsilon^2}$. Helyettesítsük be ide a frissen kiszámolt szórásnégyzetet, így a felső korlát $\frac{\sigma^2}{n \cdot \varepsilon^2}$ lesz. Képezzük az $n \to \infty$ határértéket: mivel $n$ a nevezőben van és tart a végtelenbe ($\sigma^2$ és $\varepsilon^2$ pedig konstansok), a tört értéke tart a nullához. A valószínűség így alulról $0$, felülről egy $0$-hoz tartó sorozat közé van szorítva (Rendőr-elv), tehát pontosan $0$, és a tételt bebizonyítottuk.

<br>

> Ha egy szabályos érmét nagyon sokszor feldobsz, a nagy számok törvénye garantálja, hogy a fejek *aránya* (relatív gyakorisága) 50%-hoz fog tartani. De vajon ez egyben azt is jelenti-e, hogy a fejek és írások *darabszámának abszolút különbsége* is biztosan el fog tűnni (nullához tart) ahogy a végtelen felé haladunk, vagy épp ellenkezőleg történik?

---