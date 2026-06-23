<a name="tetel-50"></a>

## 50. Szórásnégyzet torzítatlan becslése
[[ Tartalomjegyzék ]](/README.md#tartalomjegyzek) | [[ Előző ]](./tetel-35-37.md#tetel-35-37) | [[ Következő ]](./tetel-66.md#tetel-66)


> A tapasztalati szórásnégyzet kiszámításakor azért osztunk $n$ helyett $n-1$-gyel, mert a minta elemei matematikailag mindig "közelebb húzódnak" a saját, mintából számolt átlagukhoz, mint a populáció valódi, ismeretlen átlagához; így a sima átlagolás szisztematikusan alábecsülné a tényleges ingadozást, amit ez a némileg kisebb nevező korrigál.


### TÉTEL:
Legyen $X_1, X_2, \dots, X_n$ egy független, azonos eloszlású (i.i.d.) minta, amelynek elméleti várható értéke $E(X_i) = m$, szórásnégyzete pedig $D^2(X_i) = \sigma^2$. 
A **korrigált tapasztalati szórásnégyzet** definíciója:
$$s_n^{*2} = \frac{1}{n-1} \sum_{i=1}^{n} (X_i - \overline{X})^2$$

A tétel kimondja, hogy ez a statisztika a valódi szórásnégyzet torzítatlan becslése, azaz:
$$E(s_n^{*2}) = \sigma^2$$



### BIZONYÍTÁS:
* **Kiindulópont:** Azt kell megvizsgálnunk, hogy mi a várható értéke a szumma résznek. Írjuk fel a táblára: $E\left( \sum_{i=1}^n (X_i - \overline{X})^2 \right)$. Ezt fogjuk kifejteni és algebrailag átalakítani.
* **A "Trükk":** Csempésszük be a képletbe a valódi, de ismeretlen $m$ várható értéket egy ravasz "hozzáadom és kivonom" lépéssel! Írjuk át a belső különbséget így: $(X_i - \overline{X}) = (X_i - m) - (\overline{X} - m)$. Ha ezt a kéttagú kifejezést négyzetre emeljük (az $(a-b)^2 = a^2 - 2ab + b^2$ azonosság alapján) és elvégezzük rajta a szummázást, a borzalmasnak tűnő vegyes szorzat zseniálisan leegyszerűsödik, és az egész összeg erre az alakra esik szét: $\sum_{i=1}^n (X_i - m)^2 - n(\overline{X} - m)^2$.
* **Lezárás:** Szabadítsuk rá a várható érték operátort erre az egyszerűsített alakra! Az első tagban lévő $E((X_i - m)^2)$ pontosan a $\sigma^2$ definíciója, amiből összeadunk $n$ darabot, tehát ez $n\sigma^2$. A második tagban lévő $E((\overline{X} - m)^2)$ pedig nem más, mint a *mintaátlag* szórásnégyzete, amiről egy korábbi tételből tudjuk, hogy pontosan $\frac{\sigma^2}{n}$. Ezt beszorozva az előtte álló $n$-nel sima $\sigma^2$-t kapunk. A kettő különbsége $n\sigma^2 - \sigma^2 = (n-1)\sigma^2$. Mivel a definícióban ott a $\frac{1}{n-1}$ szorzó, a nevező maradéktalanul kiejti az $(n-1)$ tagot, és a táblán megkapjuk a bizonyítandó torzítatlan $\sigma^2$ eredményt.

<br>

> Tegyük fel, hogy egy isteni kinyilatkoztatás folytán pontosan ismered a populáció valódi $m$ várható értékét, és a szórásnégyzet kiszámításakor a képletben nem a mintaátlagot ($\overline{X}$) használod, hanem ezt az igazi $m$-et. Ebben a speciális esetben is $n-1$-gyel kellene osztanod az eltérések négyzetösszegét ahhoz, hogy torzítatlan becslést kapj, vagy itt már matematikailag valami megváltozik?

---