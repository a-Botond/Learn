<a name="tetel-11"></a>

## 11. Teljes valószínűség tétele 
[[ Tartalomjegyzék ]](/README.md#tartalomjegyzek) | [[ Előző ]](./tetel-10.md#tetel-10) | [[ Következő ]](./tetel-12.md#tetel-12)


> Ha egy esemény többféle, egymást kizáró „forgatókönyv” (rész-eset) szerint is megvalósulhat, akkor a teljes esélyét úgy kapjuk meg, hogy minden egyes forgatókönyv bekövetkezési esélyét megszorozzuk az esemény adott forgatókönyv melletti feltételes esélyével, majd ezeket az eredményeket egyszerűen összeadjuk (súlyozott átlagot vonunk).


### TÉTEL:
Legyen $A_1, A_2, \dots, A_n$ egy teljes eseményrendszer (azaz páronként kizárják egymást: $A_i \cap A_j = \emptyset$, ha $i \neq j$, és lefedik a teljes eseményteret: $\bigcup_{i=1}^n A_i = \Omega$), továbbá $P(A_i) > 0$ minden $i$-re. Ekkor egy tetszőleges $B$ esemény valószínűsége felírható az alábbi módon:
$$P(B) = \sum_{i=1}^{n} P(B|A_i) \cdot P(A_i)$$



### BIZONYÍTÁS:
* **Kiindulópont:** Induljunk ki abból a triviális tényből, hogy a $B$ esemény ugyanaz, mintha elmetszenénk a biztos eseménnyel ($\Omega$). A biztos eseményt pedig írjuk át a teljes eseményrendszer uniójára:
    $B = B \cap \Omega = B \cap \left( \bigcup_{i=1}^n A_i \right)$.
* **A "Trükk":** "Szeleteljük fel" a $B$-t! A disztributív szabályt alkalmazva bontsuk fel a zárójelet, így a $B$-t diszjunkt darabok uniójára vágjuk: $B = \bigcup_{i=1}^n (B \cap A_i)$. Mivel az $A_i$ események (így a metszetek is) páronként diszjunktak, a harmadik Kolmogorov-axióma (additivitás) értelmében a valószínűségük simán összeadható: 
    $P(B) = \sum_{i=1}^n P(B \cap A_i)$.
* **Lezárás:** Csak helyettesítsük be az összegzés minden egyes tagjába a feltételes valószínűségből származó szorzástételt: $P(B \cap A_i) = P(B|A_i) \cdot P(A_i)$. Ezzel a lépéssel azonnal meg is kapjuk a tétel állítását.

<br>

> Ha meg akarjuk becsülni, hogy mekkora eséllyel fog esni holnap egy adott országban, amely sivatagos, hegyvidéki és tengerparti régiókból áll, miért vezetne teljesen fals eredményre, ha egyszerűen vennénk a három régió eső-valószínűségének a sima számtani átlagát, és hogyan korrigálja ezt a hibát a teljes valószínűség tétele?

---