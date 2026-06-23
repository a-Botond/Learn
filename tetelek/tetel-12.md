<a name="tetel-12"></a>

## 12. Bayes tétele
[[ Tartalomjegyzék ]](../README.md#tartalomjegyzek) | [[ Előző ]](./tetel-11.md#tetel-11) | [[ Következő ]](./tetel-15.md#tetel-15)


> A Bayes-tétel azt mutatja meg, hogyan kell racionálisan frissíteni egy esemény bekövetkezésének esélyét (a korábbi tudásunkat), amint egy új, ahhoz kapcsolódó információ vagy bizonyíték napvilágot lát.


### TÉTEL:
Ha $A$ és $B$ tetszőleges események, és $P(B) > 0$, akkor az $A$ esemény $B$ feltétel melletti valószínűsége:
$$P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}$$

**Általános (teljes) alak:** Ha $A_1, A_2, \dots, A_n$ teljes eseményrendszert alkotnak (és $P(A_i) > 0$), akkor a nevezőt a teljes valószínűség tételével kifejtve kapjuk a gyakorlatban leginkább használt formát:
$$P(A_i|B) = \frac{P(B|A_i) \cdot P(A_i)}{\sum_{j=1}^{n} P(B|A_j) \cdot P(A_j)}$$



### BIZONYÍTÁS:
* **Kiindulópont:** Írjuk fel a feltételes valószínűség definícióját (vagy a szorzástételt) az $A$ és $B$ események metszetére mindkét irányból:
    $P(A \cap B) = P(A|B) \cdot P(B)$
    $P(B \cap A) = P(B|A) \cdot P(A)$
* **A "Trükk":** Mivel a halmazok metszete szimmetrikus ($A \cap B = B \cap A$), a két egyenlet bal oldala ugyanaz. Ezt kihasználva tegyük egyenlővé a két jobb oldalt:
    $P(A|B) \cdot P(B) = P(B|A) \cdot P(A)$.
* **Lezárás:** Egyszerűen osszuk le mindkét oldalt a feltételünk valószínűségével, azaz $P(B)$-vel (mivel $P(B) > 0$, ezt megtehetjük). Ezzel azonnal adódik a tétel alapképlete. A kiterjesztett alakhoz az utolsó lépésben a nevezőbeli $P(B)$-re alkalmazzuk a teljes valószínűség tételét.

<br>

> Ha egy nagyon ritka (például 10 000-ből mindössze 1 embert érintő) betegség szűrőtesztje 99%-os pontosságú, és a te teszted pozitív lett, matematikailag (az "alapgyakoriság" miatt) miért teljesen logikus az, hogy a valódi megbetegedési esélyed még mindig csak 1% körül mozog?

---