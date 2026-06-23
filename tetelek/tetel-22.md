<a name="tetel-22"></a>

## 22. Poisson eloszlás
[[ Tartalomjegyzék ]](../README.md#tartalomjegyzek) | [[ Előző ]](./tetel-18.md#tetel-18) | [[ Következő ]](./tetel-28.md#tetel-28)


> A Poisson-eloszlás azt mutatja meg, mekkora eséllyel következik be pontosan egy adott számú ritka, egymástól teljesen független esemény (például beérkező hívások, sajtóhibák egy könyvben vagy meteorok felvillanása) egy fix időtartam vagy terület alatt, ha csak a hosszútávú átlagukat (a rátát) ismerjük.


### TÉTEL:
Egy $X$ diszkrét valószínűségi változó Poisson-eloszlású $\lambda$ ($\lambda > 0$) paraméterrel – jelölése $X \sim \text{Poisson}(\lambda)$ –, ha a lehetséges értékei a nemnegatív egész számok ($k = 0, 1, 2, \dots$), és a valószínűség-eloszlása:
$$P(X = k) = \frac{\lambda^k}{k!} e^{-\lambda}$$

*Legfontosabb jellemzői (szóbeli vizsgán szinte biztosan rákérdeznek az egybeesésre):*
* Várható értéke: $E(X) = \lambda$
* Szórásnégyzete: $D^2(X) = \lambda$



### BIZONYÍTÁS:
* **Kiindulópont:** (A Poisson-féle határeloszlás-tétel levezetése) Induljunk ki a binomiális eloszlásból ($n$ kísérlet, $p$ siker-esély). Vizsgáljuk azt a ritka eseményekre vonatkozó határesetet, amikor a kísérletek száma tart a végtelenbe ($n \to \infty$), a siker esélye tart a nullához ($p \to 0$), de az átlagos eseményszám (várható érték) végig egy fix konstans marad: $n \cdot p = \lambda$. Írjuk fel a binomiális képletet az ebből adódó $p = \frac{\lambda}{n}$ helyettesítéssel: 
    $P(X=k) = \binom{n}{k} \left(\frac{\lambda}{n}\right)^k \left(1 - \frac{\lambda}{n}\right)^{n-k}$.
* **A "Trükk":** Bontsuk fel a kifejezést olyan tényezők szorzatára, amelyeknek külön-külön könnyen vehetjük a határértékét az analízis szabályai szerint! Fejtsük ki a binomiális együtthatót ($\frac{n(n-1)\dots(n-k+1)}{k!}$), és csoportosítsuk át a kifejezést úgy, hogy ügyesen leválasszuk belőle a nevezetes $(1 - \frac{\lambda}{n})^n$ határérték-formulát.
* **Lezárás:** Képezzük az $n \to \infty$ határértéket! A felbontott törtek szorzata ($\frac{n}{n} \cdot \frac{n-1}{n} \dots \frac{n-k+1}{n}$) mind $1$-hez tart. Az $(1 - \frac{\lambda}{n})^{-k}$ rész szintén $1$-hez tart (mivel $k$ egy fix, véges szám). A gondosan leválasztott $(1 - \frac{\lambda}{n})^n$ tag pedig definíció szerint az Euler-féle szám hatványához, $e^{-\lambda}$-hoz tart. A maradék konstanst ($\frac{\lambda^k}{k!}$) leírva, a szorzat pontosan kiadja a Poisson-eloszlás bizonyítandó képletét.

<br>

> Ha egy telefonos ügyfélszolgálatra átlagosan óránként 20 hívás fut be, miért tökéletes és jól működő modell a Poisson-eloszlás a hívások számának becslésére egy "sima" kedd délelőtt, de miért omlik össze teljesen a modell logikája, ha a cég mondjuk egy pontban délben induló, betelefonálós nyereményjátékot hirdet meg a rádióban?

---