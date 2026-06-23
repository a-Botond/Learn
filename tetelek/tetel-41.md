<a name="tetel-41"></a>

## 41. Az összeg várható értéke
[[ Tartalomjegyzék ]](../README.md#tartalomjegyzek) | [[ Előző ]](./tetel-38.md#tetel-38) | [[ Következő ]](./tetel-35-37.md#tetel-35-37)


> Két véletlen esemény (vagy befektetés) együttes átlageredménye pontosan megegyezik a külön-külön vett átlagaik összegével, teljesen függetlenül attól, hogy a két dolog hat-e egymásra.


### TÉTEL:
Legyen $X$ és $Y$ két tetszőleges valószínűségi változó, amelyeknek létezik véges várható értékük. Ekkor az összegük várható értékére fennáll:
$$E(X + Y) = E(X) + E(Y)$$

Általánosítva (akár végtelen sok, vagy nem független változóra):
$$E\left(\sum_{i=1}^n X_i\right) = \sum_{i=1}^n E(X_i)$$



### BIZONYÍTÁS:
* **Kiindulópont:** Írjuk fel a kétdimenziós (együttes) eloszlás alapján az összeg várható értékének definícióját folytonos esetben (diszkrétnél szumma szerepelne):
    $E(X + Y) = \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} (x + y) \cdot f_{X,Y}(x,y) \,dx\,dy$.
* **A "Trükk":** Lineáris szétbontás! Bontsuk fel az integrálon belüli összeget két külön integrálra: az egyik az $x$-et szorozza az együttes sűrűséggel, a másik az $y$-t. Ezzel az integrálok összegét kapjuk:
    $\iint x f_{X,Y}(x,y) \,dx\,dy + \iint y f_{X,Y}(x,y) \,dx\,dy$.
* **Lezárás:** Alkalmazzuk a peremeloszlásra való áttérést (integráljuk ki a "zavaró" változókat). Az első tagban az $y$ szerinti integrálás eltünteti $y$-t, és tisztán az $X$ peremsűrűségfüggvénye marad: $\int x f_X(x) \,dx = E(X)$. A második tagban az $x$ szerinti integrálás marad $E(Y)$, így megkapjuk a kívánt összeget: $E(X) + E(Y)$.

<br>

> Ha az összeg várható értékének additivitása miatt két kocka dobásának összege $3,5 + 3,5 = 7$ (ami teljesen igaz), vajon ugyanez a linearitás megmarad-e akkor is, ha nem az *összegük*, hanem a *szorzatuk* várható értékét akarjuk kiszámolni két dobókocka esetén?

---