<a name="tetel-10"></a>

## 10. Feltételes valószínűség (és Szorzástétel)
[[ Tartalomjegyzék ]](/README.md#tartalomjegyzek) | [[ Előző ]](./tetel-9.md#tetel-9) | [[ Következő ]](./tetel-11.md#tetel-11)


> A feltételes valószínűség azt mutatja meg, hogyan változik egy esemény esélye, ha megtudjuk, hogy egy másik esemény már biztosan bekövetkezett – ilyenkor a teljes "lehetséges világ" (az eseménytér) leszűkül kizárólag azokra az esetekre, ahol ez az új információ igaz.


### TÉTEL:
**Definíció:** Ha $B$ egy esemény, amelyre $P(B) > 0$, akkor az $A$ esemény $B$-re vonatkozó feltételes valószínűsége:
$$P(A|B) = \frac{P(A \cap B)}{P(B)}$$

**Szorzástétel (Láncszabály):** Ebből a definícióból következik tetszőleges $A_1, A_2, \dots, A_n$ események együttes bekövetkezésére (metszetére) az alábbi tétel:
$$P(A_1 \cap A_2 \cap \dots \cap A_n) = P(A_1) \cdot P(A_2|A_1) \cdot P(A_3|A_1 \cap A_2) \cdots P(A_n|A_1 \cap \dots \cap A_{n-1})$$



### BIZONYÍTÁS:
* **Kiindulópont:** Magát a feltételes valószínűséget axiómaszerű definícióként kezeljük, azt nem bizonyítjuk. A szóbeli vizsgán a belőle származó **Szorzástételt** kell levezetni, amihez írjuk fel a definíciót, és mutassuk be a logikát $n=3$ esetre felírva a jobb oldalt: $P(A_1) \cdot P(A_2|A_1) \cdot P(A_3|A_1 \cap A_2)$.
* **A "Trükk":** A "teleszkopikus szorzat". A felírt láncolatban minden egyes feltételes valószínűséget bontsunk ki a táblán az alapdefiníció szerint: 
  $P(A_1) \cdot \frac{P(A_1 \cap A_2)}{P(A_1)} \cdot \frac{P(A_1 \cap A_2 \cap A_3)}{P(A_1 \cap A_2)}$.
* **Lezárás:** Egyszerűsítsünk "keresztbe"! Látjuk, hogy minden tört nevezője (a feltétel) pontosan megegyezik az előző szorzótényező számlálójával (vagy magával az előző taggal), így ezek mind kiesnek. A dominóeffektus végén csak a legutolsó tört számlálója marad meg: $P(A_1 \cap A_2 \cap A_3)$, ami pontosan a bizonyítandó állítás bal oldala.

<br>

> Ha kiszámolod, hogy $P(A|B) = P(A)$, vagyis a $B$ esemény bekövetkezése (az új információ) egyáltalán nem változtatta meg az $A$ eredeti esélyét, mit jelent ez a két esemény kapcsolatára nézve a való világban, és hogyan egyszerűsödik le ilyenkor az $A \cap B$ metszet valószínűségének képlete?

---