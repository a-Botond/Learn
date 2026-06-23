<a name="tetel-34"></a>

## 34. Összeg (Műveletek valószínűségi változókkal)
[[ Tartalomjegyzék ]](../README.md#tartalomjegyzek) | [[ Előző ]](./tetel-26.md#tetel-26) | [[ Következő ]](./tetel-38.md#tetel-38)


> Ha két bizonytalan dolgot összeadunk (például két befektetés hozamát), akkor a várható átlaguk mindig egyszerűen összeadódik, de a teljes bizonytalanságuk (a szórásnégyzetük) csak akkor adódik össze tisztán, ha a két dolog teljesen független egymástól – ha viszont van köztük kapcsolat, akkor ez az együttmozgás növelheti vagy épp csökkentheti a végső kockázatot.


### TÉTEL:
Legyen $X$ és $Y$ két tetszőleges valószínűségi változó, amelyeknek létezik várható értéke és szórásnégyzete. Az összegükre vonatkozó alaptételek a következők:

**1. A várható érték additivitása (mindig igaz):**
$$E(X + Y) = E(X) + E(Y)$$

**2. A szórásnégyzet additivitása (általános alak):**
$$D^2(X + Y) = D^2(X) + D^2(Y) + 2 \cdot cov(X,Y)$$

**3. Szórásnégyzet független (vagy korrelálatlan) esetben:**
Ha $X$ és $Y$ függetlenek, akkor a kovarianciájuk nulla ($cov(X,Y) = 0$), így a képlet leegyszerűsödik:
$$D^2(X + Y) = D^2(X) + D^2(Y)$$



### BIZONYÍTÁS:
* **Kiindulópont:** A szóbeli vizsgán ezen a ponton a szórásnégyzet összegképletének levezetése a klasszikus elvárás. Írjuk fel az összeg szórásnégyzetének definícióját a táblára. Vezessük be az $m_x = E(X)$ és $m_y = E(Y)$ jelöléseket a könnyebb írásmód kedvéért: 
  $D^2(X + Y) = E[((X + Y) - E(X + Y))^2]$.
* **A "Trükk":** Az algebrai átcsoportosítás! A linearitás miatt tudjuk, hogy $E(X+Y) = m_x + m_y$. Helyettesítsük ezt be, és a belső zárójelet rendezzük át okosan úgy, hogy a változókat kizárólag a saját átlagukkal párosítjuk össze: $((X - m_x) + (Y - m_y))^2$. Ezután egyszerűen bontsuk fel ezt a kifejezést a jól ismert $(a+b)^2 = a^2 + b^2 + 2ab$ binomiális azonosság alapján!
* **Lezárás:** A négyzetre emelés után ezt kapjuk: $E[(X - m_x)^2 + (Y - m_y)^2 + 2(X - m_x)(Y - m_y)]$. Szabadítsuk rá az egészre a várható érték linearitását (az összeg várható értéke a várható értékek összege, a konstans kiemelhető). Az első tag $E[(X - m_x)^2]$ definíció szerint pontosan $D^2(X)$. A második tag adja a $D^2(Y)$-t. A harmadik, vegyes szorzat várható értéke pedig hajszálpontosan a kovariancia definíciója, azaz $2 \cdot cov(X,Y)$. Ezzel a tételt azonnal és elegánsan beláttuk.

<br>

> Ha két teljesen egyforma, szabályos dobókockával dobunk, az eredmények összegének várható értéke 7. Miért lesz az összeg bizonytalansága (szórása) mégis kisebb, mintha csak egyetlen kockával dobnánk, de a kapott eredményt a szabályok szerint mindig megszoroznánk kettővel?

---