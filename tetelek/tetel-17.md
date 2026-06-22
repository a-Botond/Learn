<a name="tetel-17"></a>

## 17. Várható érték (és linearitása)
[[ Tartalomjegyzék ]](/README.md#tartalomjegyzek) | [[ Előző ]](./tetel-15.md#tetel-15) | [[ Következő ]](./tetel-44.md#tetel-44)


> A várható érték lényegében a valószínűségekkel súlyozott átlag: megmutatja, hogy ha egy kísérletet (például egy szerencsejátékot) végtelen sokszor megismételnénk, egy-egy alkalomra vetítve átlagosan milyen eredményt kapnánk (ez egyben a valószínűségi eloszlás "tömegközéppontja" is).


### TÉTEL:
**Definíció (Diszkrét eset):** Ha $X$ diszkrét valószínűségi változó, ami az $x_i$ értékeket $p_i = P(X = x_i)$ valószínűségekkel veszi fel, akkor a várható értéke:
$$E(X) = \sum_{i} x_i \cdot p_i$$
*(Feltéve, hogy a sor abszolút konvergens: $\sum |x_i| p_i < \infty$.)*

**Definíció (Folytonos eset):** Ha $X$ folytonos, $f(x)$ sűrűségfüggvénnyel, akkor:
$$E(X) = \int_{-\infty}^{\infty} x \cdot f(x) dx$$
*(Feltéve, hogy az integrál abszolút konvergens.)*

**Linearitás tétele:** Tetszőleges $a, b \in \mathbb{R}$ konstansok és $X$ valószínűségi változó esetén:
$$E(aX + b) = aE(X) + b$$



### BIZONYÍTÁS:
* **Kiindulópont:** Magát a várható értéket definícióként fogadjuk el, ezt nem bizonyítjuk. Egy egyetemi vizsgán ilyenkor a legfontosabb tulajdonságát, a **linearitást** kell levezetni (mutassuk be folytonos esetre, mert az elegánsabb). Írjuk fel a definíciót az $aX + b$ transzformált változóra: 
    $E(aX + b) = \int_{-\infty}^{\infty} (ax + b) \cdot f(x) dx$.
* **A "Trükk":** Használjuk ki az integrálképzés lineáris tulajdonságait! Bontsuk fel a zárójelet, szedjük szét két külön integrál összegére, és a konstans szorzókat ($a$ és $b$) emeljük ki az integráljelek elé:
    $a \int_{-\infty}^{\infty} x \cdot f(x) dx + b \int_{-\infty}^{\infty} f(x) dx$.
* **Lezárás:** Ismerjük fel a kapott tagokat! Az első integrál pontosan az $E(X)$ definíciója. A második integrál a sűrűségfüggvény teljes görbe alatti területe, ami a 2. Kolmogorov-axióma (normáltság) értelmében kötelezően $1$. Így az eredmény: $a \cdot E(X) + b \cdot 1$, amivel a tételt beláttuk.

<br>

> Egy szabályos dobókockával dobva az eredmény várható értéke 3,5. Hogyan nevezhetjük ezt a számot "várható" értéknek, ha a valóságban fizikailag lehetetlen ezt az eredményt egy dobásból megkapni, és mégis mit jelent ez a szám egy kaszinó tulajdonosának egy hosszú este végén?

---