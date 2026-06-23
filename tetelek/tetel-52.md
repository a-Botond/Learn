<a name="tetel-52"></a>

## 52. ML-módszer (Maximum Likelihood becslés)
[[ Tartalomjegyzék ]](../README.md#tartalomjegyzek) | [[ Előző ]](./tetel-51.md#tetel-51) | [[ Következő ]](./tetel-42.md#tetel-42)


> A Maximum Likelihood (legnagyobb valószerűség) módszere "visszafelé" gondolkodik: azt az ismeretlen elméleti paramétert tekinti a legjobb becslésnek, amely mellett a legnagyobb matematikai eséllyel (valószínűséggel) jött volna ki pont az a konkrét adathalmaz, amit a valóságban a kezünkben tartunk.


### TÉTEL:
Legyen $X_1, X_2, \dots, X_n$ egy független, azonos eloszlású (i.i.d.) minta, amelynek eloszlását (sűrűségfüggvényét vagy diszkrét eloszlását) a $f(x; \theta)$ függvény írja le, ahol $\theta$ az ismeretlen paraméter.

A minta együttes eloszlása a **Likelihood-függvény**, ami a peremeloszlások szorzata:
$$L(\theta) = \prod_{i=1}^n f(x_i; \theta)$$

A Maximum Likelihood (ML) becslés ($\hat{\theta}$) az a paraméterérték, amely ezt a függvényt a megfigyelt minta mellett maximalizálja:
$$\hat{\theta} = \arg\max_{\theta} L(\theta)$$

A gyakorlatban szinte mindig a **Log-likelihood függvényt** használjuk:
$$\ell(\theta) = \ln L(\theta) = \sum_{i=1}^n \ln f(x_i; \theta)$$



### BIZONYÍTÁS:
* **Kiindulópont:** Ahogy a momentummódszernél, itt sem klasszikus levezetés, hanem a becslési eljárás algoritmusának felírása a feladat. Kezdjük azzal, hogy felírjuk a táblára a megfigyelt minta együttes eloszlását. Mivel a mintaelemek függetlenek, a valószínűség-szorzási tétel értelmében ez egyszerűen az egyes sűrűségfüggvények szorzata lesz: $L(\theta) = f(x_1;\theta) \cdot f(x_2;\theta) \cdots f(x_n;\theta)$.
* **A "Trükk":** Szorzatot deriválni a végtelenbe nyúló láncszabály miatt kínszenvedés. Használjuk ki, hogy maximalizálni akarunk, és a természetes alapú logaritmus ($\ln$) egy szigorúan monoton növekvő függvény! Ha egy függvénynek valahol maximuma van, ott a logaritmusának is pontosan ugyanott van a maximuma. Ez a zseniális húzás a borzalmas szorzatot azonnal egy tagonként, nagyon könnyen deriválható összeggé alakítja: $\ell(\theta) = \sum \ln f(x_i; \theta)$.
* **Lezárás:** Alkalmazzuk az egyváltozós (vagy vektortérben többváltozós) szélsőérték-számítás klasszikus lépéseit a deriválás-analízisből: deriváljuk a log-likelihood függvényt a keresett $\theta$ paraméter szerint, és a deriváltat tegyük egyenlővé nullával (ezt hívják *likelihood-egyenletnek*: $\frac{\partial \ell(\theta)}{\partial \theta} = 0$). Az ebből kapott egyenletet $\theta$-ra algebrailag megoldva rögtön megkapjuk a keresett $\hat{\theta}$ pontbecslést.

<br>

> Mivel a Maximum Likelihood becslés célja kifejezetten az, hogy a már *meglévő, konkrét* mintánkhoz a legszorosabban "hozzásimítsa" a modellt, miért fordulhat elő az, hogy kis elemszámú minta esetén a módszer torzított (optimista) becslést ad – például a szórásnégyzet ML-becslése miért oszt $n$-nel a statisztikailag "helyesebbnek" tartott $n-1$ helyett?

---