<a name="tetel-49"></a>

## 49. Kovariancia (és kiszámítási tétele)
[[ Tartalomjegyzék ]](../README.md#tartalomjegyzek) | [[ Előző ]](./tetel-44.md#tetel-44) | [[ Következő ]](./tetel-18.md#tetel-18)


> A kovariancia azt méri, hogy két dolog mennyire "mozog együtt" a valóságban: ha az egyik a saját átlaga felett van, akkor jellemzően a másik is ott van-e (pozitív együttmozgás), vagy épp ellenkezőleg, a másik olyankor inkább az átlaga alatt húzódik meg (negatív együttmozgás).


### TÉTEL:
**Definíció:** Két valószínűségi változó, $X$ és $Y$ kovarianciája az átlagtól való eltéréseik szorzatának várható értéke:
$$cov(X,Y) = E[(X - E(X))(Y - E(Y))]$$

**Kiszámítási tétel:** A gyakorlatban – akárcsak a szórásnégyzetnél – ezt is egy sokkal barátibb, egyszerűsített képlettel számoljuk (a vizsgán ezt a tételt vezetjük le):
$$cov(X,Y) = E(XY) - E(X) \cdot E(Y)$$



### BIZONYÍTÁS:
* **Kiindulópont:** Írjuk fel a definíciót a táblára, és hogy ne fulladjunk bele a jelölésekbe, vezessük be az $m_x = E(X)$ és $m_y = E(Y)$ jelöléseket. Kulcsfontosságú, hogy az oktatónak jelezd: az $m_x$ és $m_y$ *konstans* számok!
    $cov(X,Y) = E[(X - m_x)(Y - m_y)]$.
* **A "Trükk":** Az algebrai kifejtés és a várható érték linearitása. Először szorozzuk össze a zárójeleket (tagonként): $(X - m_x)(Y - m_y) = XY - X \cdot m_y - Y \cdot m_x + m_x \cdot m_y$. Ezután bontsuk fel a várható értéket erre a négy tagra, kihasználva, hogy az összeg várható értéke a várható értékek összege, a konstansok pedig kiemelhetők.
* **Lezárás:** Alkalmazva a linearitást, ezt kapjuk:
    $E(XY) - m_y \cdot E(X) - m_x \cdot E(Y) + E(m_x \cdot m_y)$.
    Mivel $E(X) = m_x$ és $E(Y) = m_y$, valamint a konstans várható értéke önmaga, visszahelyettesítünk:
    $E(XY) - m_y \cdot m_x - m_x \cdot m_y + m_x \cdot m_y$.
    Az utolsó három tag összevonható: $-2 m_x m_y + m_x m_y = -m_x m_y$. Így marad az $E(XY) - m_x m_y$, amibe a konstansokat visszaírva megkapjuk a bizonyítandó tételt: $E(XY) - E(X)E(Y)$.

<br>

> Ha egy számítás során azt kapod, hogy a kovariancia $cov(X, Y) = 0$, miért óriási hiba azonnal rávágni, hogy ez a két dolog teljesen független egymástól a való világban?

---