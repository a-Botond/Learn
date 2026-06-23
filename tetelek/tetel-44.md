<a name="tetel-44"></a>

## 44. Szórásnégyzet (és kiszámítási tétele)
[[ Tartalomjegyzék ]](../README.md#tartalomjegyzek) | [[ Előző ]](./tetel-17.md#tetel-17) | [[ Következő ]](./tetel-49.md#tetel-49)


> A szórásnégyzet azt méri, hogy egy véletlen kísérlet eredményei átlagosan mennyire "szóródnak" (ingadoznak) a várható értéktől – precízen fogalmazva: az átlagtól való eltérések négyzetének az átlaga.


### TÉTEL:
**Definíció:** Legyen $X$ egy valószínűségi változó, melynek létezik a várható értéke ($E(X)$). Az $X$ szórásnégyzete (diszperziója):
$$D^2(X) = E\left((X - E(X))^2\right)$$

**Kiszámítási tétel (Steiner-formula):** A gyakorlatban a szórásnégyzetet majdnem mindig ezzel a sokkal egyszerűbb képlettel számoljuk (és a vizsgán ezt kell levezetni):
$$D^2(X) = E(X^2) - [E(X)]^2$$



### BIZONYÍTÁS:
* **Kiindulópont:** Írjuk fel a szórásnégyzet definícióját a táblára, és a könnyebb írásmód kedvéért jelöljük a várható értéket egy betűvel, mondjuk $m = E(X)$-szel (nagyon fontos hangsúlyozni az oktatónak, hogy az $m$ egy *konstans* szám!):
    $D^2(X) = E\left((X - m)^2\right)$.
* **A "Trükk":** Algebrai kifejtés és linearitás. Bontsuk fel a zárójelet a jól ismert $(a-b)^2$ azonosság alapján: $(X - m)^2 = X^2 - 2mX + m^2$. Ezután erre a háromtagú összegre szabadítsuk rá a várható érték tulajdonságait: az összeg várható értéke a várható értékek összege, a konstans szorzó ($2m$) pedig kiemelhető.
* **Lezárás:** Alkalmazva a linearitást: 
    $E(X^2 - 2mX + m^2) = E(X^2) - 2m \cdot E(X) + E(m^2)$.
    Mivel $m$ konstans, a konstans várható értéke önmaga ($E(m^2) = m^2$), illetve tudjuk, hogy $E(X) = m$. Helyettesítsük be ezeket:
    $E(X^2) - 2m \cdot m + m^2 = E(X^2) - 2m^2 + m^2 = E(X^2) - m^2$.
    Az $m$ helyére visszaírva az eredeti $E(X)$ jelölést, megkapjuk a bizonyítandó tételt: $E(X^2) - [E(X)]^2$.

<br>

> Ha a szórásnégyzet célja az átlagtól való eltérés mérése, miért emeljük matematikailag négyzetre ezeket az eltéréseket ahelyett, hogy simán csak összeadnánk őket, vagy esetleg az abszolút értékük ($|X - E(X)|$) várható értékét vennénk?

---