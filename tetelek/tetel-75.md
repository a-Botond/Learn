<a name="tetel-75"></a>

## 75. Alapfogalmak (Hipotézisvizsgálat)
[[ Tartalomjegyzék ]](../README.md#tartalomjegyzek) | [[ Előző ]](./tetel-42.md#tetel-42) | [[ Következő ]](./tetel-54.md#tetel-54)


> A hipotézisvizsgálat pontosan olyan, mint egy büntetőper: a vizsgált állítás (a nullhipotézis) ártatlan, amíg a mintából vett bizonyítékok (adatok) annyira extrémek nem lesznek, hogy a véletlen egybeesés esélye egy előre megadott, nagyon pici hibahatár (a szignifikanciaszint) alá csökken.


### TÉTEL (A fogalmi rendszer):
Mivel ez nem egy klasszikus matematikai formula, a vizsgán a döntési rendszer pontos definícióit kérik számon:

* **Nullhipotézis ($H_0$):** A vizsgált alapfeltevés, a "status quo" (általában az "nincs változás", "a paraméter egyenlő egy adott értékkel" állapota).
* **Ellenhipotézis ($H_1$ vagy $H_a$):** Az az állítás, amit bizonyítani szeretnénk (általában az eltérés, a változás).
* **Próbastatisztika ($T$):** A mintából számolt valószínűségi változó, ami egy konkrét eloszlást követ, ha $H_0$ igaz. Ez alapján hozunk döntést.
* **Kritikus tartomány ($K$):** A próbastatisztika azon értékeinek halmaza, amelyeknél elvetjük a $H_0$-t.
* **Elsőfajú hiba ($\alpha$):** Elvetjük $H_0$-t, pedig a valóságban igaz (ártatlanul elítéljük). Ennek az előre rögzített, maximálisan megengedett valószínűségét hívjuk **szignifikanciaszintnek**: 
  $$P(T \in K \mid H_0 \text{ igaz}) = \alpha$$
* **Másodfajú hiba ($\beta$):** Megtartjuk $H_0$-t, pedig $H_1$ igaz (futni hagyjuk a bűnöst). A $1-\beta$ értéket a próba **erejének** nevezzük.



### BIZONYÍTÁS (A döntési mechanizmus logikája):
* **Kiindulópont:** Ennél a tételnél klasszikus bizonyítás helyett a *hipotézisvizsgálat logikáját* (Neyman-Pearson lemma elveit) kell felvázolni. Rajzold fel fejben a döntési mátrixot (Valóság vs. Döntés). Mivel a mintavétel véletlenszerű, sosem lehetünk 100%-ig biztosak, így elvi szinten mindig fennáll az elsőfajú ($\alpha$) és másodfajú ($\beta$) hiba esélye.
* **A "Trükk":** Adott mintaelemszám ($n$) mellett a két hiba egymás rovására megy: ha csökkentem $\alpha$-t, drasztikusan nő $\beta$. A mesterfogás itt az **aszimmetrikus hozzáállás**: a súlyosabbnak ítélt elsőfajú hibát ($\alpha$) kőkeményen lefixáljuk egy kicsi értékre (pl. 0.05 vagy 5%), és ehhez az $\alpha$-hoz határozzuk meg úgy a $K$ kritikus tartományt, hogy az a lehető legkisebb $\beta$-t (legnagyobb erőt) biztosítsa.
* **Lezárás:** Végrehajtjuk a próbát. Kiszámoljuk a mintából a $T$ próbastatisztika konkrét értékét. Ha ez az érték beleesik a rögzített $\alpha$ alapján kijelölt $K$ kritikus tartományba, akkor $H_0$-t elvetjük (az eredmény *szignifikáns*). Ha nem esik bele, akkor *nem tudjuk elvetni* $H_0$-t.

<br>

> Ha egy hipotézisvizsgálat során a kapott próbastatisztika nem esik bele a kritikus tartományba (így megtartjuk a nullhipotézist), matematikai és logikai szempontból miért óriási szakmai hiba azt mondani, hogy "ezzel bebizonyítottuk, hogy a nullhipotézis igaz"?

---