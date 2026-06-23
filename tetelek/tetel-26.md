<a name="tetel-26"></a>

## 26. Egyenletes eloszlás
[[ Tartalomjegyzék ]](../README.md#tartalomjegyzek) | [[ Előző ]](./tetel-24.md#tetel-24) | [[ Következő ]](./tetel-36.md#tetel-36)


> A folytonos egyenletes eloszlás a "tökéletes igazságosság" modellje: egy adott tartományon belül bárhová is bökünk, a valószínűség pusztán attól függ, hogy mekkora a "célkeresztünk" (az intervallum hossza), és egyáltalán nem függ attól, hogy ez a sáv hol helyezkedik el.


### TÉTEL:
Egy $X$ folytonos valószínűségi változó egyenletes eloszlású az $[a, b]$ intervallumon (jelölése: $X \sim U(a,b)$), ha a sűrűségfüggvénye egy konstans ezen a tartományon, azon kívül pedig nulla:
$$f(x) = \begin{cases} \frac{1}{b-a}, & \text{ha } a \le x \le b \\ 0, & \text{egyébként} \end{cases}$$

Eloszlásfüggvénye (az esélyek felhalmozódása) az $[a,b]$ intervallumon belül egyenesen arányosan nő:
$$F(x) = \frac{x-a}{b-a} \quad (\text{ha } a \le x \le b)$$

*Legfontosabb jellemzői (szóbeli vizsgán a levezetésük a tétel része):*
* Várható értéke: $E(X) = \frac{a+b}{2}$
* Szórásnégyzete: $D^2(X) = \frac{(b-a)^2}{12}$



### BIZONYÍTÁS:
* **Kiindulópont:** A vizsgán a **várható érték** levezetését várják el leginkább. Írjuk fel a folytonos várható érték definícióját: $E(X) = \int_{-\infty}^{\infty} x \cdot f(x) dx$. Mivel a sűrűségfüggvényünk csak az $[a, b]$ szakaszon nem nulla, az integrálási határok $a$ és $b$ lesznek, az $f(x)$ helyére pedig egyszerűen beírjuk a $\frac{1}{b-a}$ konstanst.
* **A "Trükk":** Mivel a $\frac{1}{b-a}$ egy sima szám, emeljük ki az integráljel elé! Ami bent marad, az csupán az $\int_{a}^{b} x dx$. Az $x$ primitív függvénye $\frac{x^2}{2}$, így a Newton-Leibniz formula alapján behelyettesítve a felső és alsó határokat a $\frac{b^2 - a^2}{2}$ kifejezést kapjuk.
* **Lezárás:** Alkalmazzuk a jól ismert algebrai azonosságot a számlálóra: $b^2 - a^2 = (b-a)(b+a)$. Ezt összeszorozva a kiemelt konstanssal: $\frac{1}{b-a} \cdot \frac{(b-a)(b+a)}{2}$. A $(b-a)$ tényezők elegánsan kiejtik egymást, és pontosan a $\frac{a+b}{2}$ eredmény marad, ami – a józan ésszel is teljesen összhangban – pont az intervallum geometriai felezőpontja.

<br>

> Ha a folytonos egyenletes eloszlásnál matematikai értelemben bármelyik *konkrét egyetlen pont* (pl. hajszálpontosan a 2,5000...) eltalálásának a valószínűsége nulla, hogyan lehetséges az, hogy ha végtelen sok "nulla esélyű" pontot összerakunk egy intervallummá, annak mégis lesz egy jól mérhető, pozitív valószínűsége?

---