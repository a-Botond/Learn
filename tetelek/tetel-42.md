<a name="tetel-42"></a>

## 42. Torzítatlanság (Becsléselmélet)
[[ Tartalomjegyzék ]](../README.md#tartalomjegyzek) | [[ Előző ]](./tetel-52.md#tetel-52) | [[ Következő ]](./tetel-75.md#tetel-75)


> A torzítatlanság azt jelenti, hogy a becslési módszerünk nem "húz" szisztematikusan se lefelé, se felfelé: ha a kísérletet végtelen sokszor megismételnénk és újabb mintákat vennénk, az ezekből számolt becsléseink átlaga hajszálpontosan a keresett, valódi elméleti értékre állna be.


### TÉTEL:
**Definíció:** Egy $\hat{\theta}$ statisztika (a mintából számított véletlen mennyiség) a $\theta$ elméleti paraméter **torzítatlan becslése**, ha a becslőfüggvény várható értéke pontosan a keresett paraméter:
$$E(\hat{\theta}) = \theta$$

**Alaptétel (A mintaátlag torzítatlansága):** Legyen $X_1, X_2, \dots, X_n$ egy minta (azonos eloszlású változók), melynek elméleti várható értéke $E(X_i) = m$. Ekkor a mintaátlag ($\overline{X} = \frac{1}{n} \sum_{i=1}^n X_i$) az $m$ paraméter torzítatlan becslése, azaz:
$$E(\overline{X}) = m$$



### BIZONYÍTÁS:
* **Kiindulópont:** A szóbeli vizsgán a fogalom definiálása után a fenti alaptételt, a mintaátlag torzítatlanságát kell levezetned (ez az oktatók kedvence, mert rövid és elegáns). Írd fel a táblára a mintaátlag várható értékét a definíció alapján: $E(\overline{X}) = E\left( \frac{1}{n} \sum_{i=1}^{n} X_i \right)$.
* **A "Trükk":** A várható érték linearitása! Ez a tulajdonság garantálja, hogy a konstans szorzó kiemelhető az $E()$ operátor elé, az összeg várható értéke pedig a várható értékek összege lesz (és ehhez még csak a mintaelemek függetlenségére sincs szükség). Emeljük ki az $\frac{1}{n}$-et, és bontsuk fel az operátort a szummán belülre: $\frac{1}{n} \sum_{i=1}^{n} E(X_i)$.
* **Lezárás:** Mivel a minta minden eleme ugyanabból az eloszlásból származik, mindegyiknek a várható értéke egzaktan $m$. Így az összegzésben valójában az $m$ konstanst adjuk össze önmagával $n$-szer, aminek az eredménye $n \cdot m$. Ezt visszahelyettesítve a kifejezésbe kapjuk: $\frac{1}{n} \cdot (n \cdot m)$. Az $n$-ek egyszerűsítésével tisztán az $m$ marad, amivel bebizonyítottuk a tételt.

<br>

> Ha egy becslési módszerről matematikailag tökéletesen be van bizonyítva, hogy torzítatlan (vagyis az elméleti várható értéke a valódi paraméter), miért lehet az, hogy amikor te a laborban csinálsz *egy darab* 10 elemű méréssorozatot, a kapott konkrét eredményed mégis borzalmasan messze lesz a valóságtól?

---