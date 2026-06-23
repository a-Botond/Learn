<a name="tetel-30"></a>

## 30. Normális eloszlás (és a Gauss-integrál)
[[ Tartalomjegyzék ]](../README.md#tartalomjegyzek) | [[ Előző ]](./tetel-28.md#tetel-28) | [[ Következő ]](./tetel-46.md#tetel-46)


> A normális eloszlás azt a természetben (például testmagasság, mérési hibák, IQ) lépten-nyomon előforduló "haranggörbe" jelenséget írja le, ahol az értékek leginkább az átlag körül sűrűsödnek, és attól mindkét irányba távolodva, szimmetrikusan egyre ritkábban fordulnak elő.


### TÉTEL:
Egy $X$ folytonos valószínűségi változó normális (Gauss-) eloszlású $m$ várható értékkel és $\sigma > 0$ szórással (jelölése: $X \sim \mathcal{N}(m, \sigma^2)$), ha a sűrűségfüggvénye:
$$f(x) = \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x-m)^2}{2\sigma^2}} \quad (x \in \mathbb{R})$$

**Standard normális eloszlás:** Ha $m=0$ és $\sigma=1$, a sűrűségfüggvénye (jelölése $\varphi(x)$):
$$\varphi(x) = \frac{1}{\sqrt{2\pi}} e^{-\frac{x^2}{2}}$$

**Standardizálás tétele:** Ha $X \sim \mathcal{N}(m, \sigma^2)$, akkor a levont átlaggal és leosztott szórással kapott új változó standard normális eloszlású lesz: $Z = \frac{X-m}{\sigma} \sim \mathcal{N}(0, 1)$.



### BIZONYÍTÁS:
* **Kiindulópont:** A szóbeli vizsgán a normális eloszláshoz kapcsolódó legszebb és leginkább várt levezetés a normáló tényező, vagyis a **Gauss-integrál** bizonyítása (hogy a sűrűségfüggvény alatti terület tényleg 1). Ehhez azt kell belátnunk, hogy a görbe "magjának" integrálja: $I = \int_{-\infty}^{\infty} e^{-x^2/2} dx = \sqrt{2\pi}$.
* **A "Trükk":** Az egydimenziós integrálnak nincs zárt alakú primitív függvénye, ezért "kilépünk a síkba"! Emeljük négyzetre az integrált ($I^2$), és írjuk fel egy kétdimenziós kettős integrálként az $x-y$ síkon: $\iint_{\mathbb{R}^2} e^{-(x^2+y^2)/2} dx dy$. Ezt követően térjünk át **polárkoordinátákra**, ahol $x^2+y^2 = r^2$, a terület metrikája ($dx dy$) pedig $r \cdot dr d\varphi$-re változik!
* **Lezárás:** A polárkoordinátás alak csodát tesz. A szögre vett integrál ($0$-tól $2\pi$-ig) egyszerűen ad egy $2\pi$ szorzót. A sugárra vett integrál pedig $\int_0^\infty r e^{-r^2/2} dr$ lesz, amit már triviális integrálni, hiszen az $r$ szorzó pont a kitevő belső függvényének deriváltja (az eredménye $1$). Így kapjuk, hogy $I^2 = 2\pi \cdot 1$, amiből gyököt vonva azonnal adódik a keresett $\sqrt{2\pi}$ érték.

<br>

> Mivel a normális eloszlás haranggörbéje alatti területet (vagyis az eloszlásfüggvényt) analitikusan lehetetlen zárt alakban integrálni, hogyan tudjuk mégis egyetlen, fix (a standard normális eloszláshoz tartozó $\Phi(x)$) táblázat segítségével a világ összes létező normális eloszlású (bármilyen átlagú és szórású) problémáját megoldani?

---