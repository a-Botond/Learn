<a name="tetel-46"></a>

## 46. Csebisev-egyenlőtlenség
[[ Tartalomjegyzék ]](/README.md#tartalomjegyzek) | [[ Előző ]](./tetel-30.md#tetel-30) | [[ Következő ]](./tetel-47.md#tetel-47)


> A Csebisev-egyenlőtlenség univerzálisan garantálja, hogy bármilyen furcsa is legyen egy eloszlás, az adatok túlnyomó többsége mindig az átlag közelében tömörül, és minél messzebb megyünk az átlagtól, annál drasztikusabban (négyzetesen) csökken az esélye annak, hogy ott kiugró értéket találunk.


### TÉTEL:
Legyen $X$ egy tetszőleges valószínűségi változó, amelynek létezik és véges a várható értéke ($E(X) = m$) és a szórásnégyzete ($D^2(X) = \sigma^2$). Ekkor bármely $\varepsilon > 0$ valós számra érvényes:
$$P(|X - m| \ge \varepsilon) \le \frac{\sigma^2}{\varepsilon^2}$$

*(Gyakori alternatív alak a vizsgán: ha az eltérést a szórás $k$-szorosában mérjük ($\varepsilon = k\sigma$), akkor a képlet $P(|X - m| \ge k\sigma) \le \frac{1}{k^2}$ formára egyszerűsödik).*



### BIZONYÍTÁS:
* **Kiindulópont:** Írjuk fel a szórásnégyzet alapdefinícióját a táblára (könnyebb folytonos esetben, integrállal demonstrálni, de szummával is tökéletes):
    $\sigma^2 = \int_{-\infty}^{\infty} (x-m)^2 \cdot f(x) dx$.
* **A "Trükk":** Az integrál tartományának csonkítása és alulbecslése! Vágjuk ketté az integrált: egyrészt azokra az $x$-ekre, amik $\varepsilon$-nál messzebb vannak az átlagtól ($|x-m| \ge \varepsilon$), és az összes többire. A "többi" részt egyszerűen elhagyjuk. Mivel a sűrűségfüggvény és a négyzet is pozitív, elhagyással garantáltan egy *kisebb vagy egyenlő* kifejezést kapunk. A megmaradt tartományon pedig tudjuk, hogy $(x-m)^2 \ge \varepsilon^2$, így a változó tagot lecserélhetjük a konstans $\varepsilon^2$ alsó korlátra.
* **Lezárás:** A becslésünk most így néz ki: $\sigma^2 \ge \int_{|x-m| \ge \varepsilon} \varepsilon^2 \cdot f(x) dx$. Emeljük ki az $\varepsilon^2$ konstanst az integrál elé! Ami az integráljelen belül marad ($\int f(x) dx$ a kritikus tartományon), az definíció szerint pontosan a $P(|X - m| \ge \varepsilon)$ valószínűség. Végül osszuk el mindkét oldalt $\varepsilon^2$-tel, és már kész is vagyunk.

<br>

> A Csebisev-egyenlőtlenség a valószínűségszámítás egyik legfontosabb elméleti tartópillére (ezen múlik a Nagyok törvénye is), de a gyakorlati életben mégis sokszor "haszontalannak" és túl pesszimistának tartjuk. Miért ad ez az egyenlőtlenség nevetségesen gyenge becslést akkor, ha történetesen pontosan tudjuk az adatainkról, hogy normális eloszlásúak?

---