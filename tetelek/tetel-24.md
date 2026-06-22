<a name="tetel-24"></a>

## 24. Hipergeometriai eloszlás
[[ Tartalomjegyzék ]](/README.md#tartalomjegyzek) | [[ Előző ]](./tetel-20.md#tetel-20) | [[ Következő ]](./tetel-26.md#tetel-26)


> A hipergeometriai eloszlás azt mutatja meg, mekkora eséllyel húzunk ki pontosan egy adott számú "nyertes" (vagy épp selejtes) elemet egy véges sokaságból, ha a kihúzott elemeket – az ötöslottóhoz vagy a kártyaosztáshoz hasonlóan – *nem tesszük vissza*.


### TÉTEL:
Egy $X$ diszkrét valószínűségi változó hipergeometriai eloszlású, ha egy $N$ elemű sokaságból – melyből $M$ darab rendelkezik a vizsgált tulajdonsággal ("nyertes") és $N-M$ darab nem – visszatevés nélkül húzunk $n$ elemet, és $X$ a kihúzott "nyertes" elemek számát jelöli.

Valószínűség-eloszlása:
$$P(X = k) = \frac{\binom{M}{k} \cdot \binom{N-M}{n-k}}{\binom{N}{n}}$$
*(Ahol $k$ természetes szám, a logikus $0 \le k \le n$, valamint $k \le M$ és $n-k \le N-M$ feltételek mellett).*

*Legfontosabb jellemzői (szóbeli vizsgán gyakran kérik a binomiálissal való rokonság miatt):*
* Várható értéke: $E(X) = n \cdot \frac{M}{N}$
* Szórásnégyzete: $D^2(X) = n \cdot \frac{M}{N} \left(1 - \frac{M}{N}\right) \frac{N-n}{N-1}$



### BIZONYÍTÁS:
* **Kiindulópont:** A klasszikus valószínűségi modellt (kedvező esetek száma osztva az összes eset számával) írjuk fel. Az összes lehetséges kimenetel száma annak a kombinatorikai problémának felel meg, hogy $N$ elemből hányféleképpen húzhatunk ki $n$ darabot a sorrend figyelembevétele nélkül: ez ismétlés nélküli kombináció, azaz $\binom{N}{n}$.
* **A "Trükk":** A kedvező esetek összeszámolásához gondolatban "két kupacra" osztjuk a sokaságot. Ahhoz, hogy pontosan $k$ nyertest húzzunk a mintába, az $M$ darab nyertes közül kell kiválasztanunk $k$ darabot (ez $\binom{M}{k}$-féleképpen tehető meg), ÉS a maradék $N-M$ darab "vesztesből" kell kihúznunk a hiányzó $n-k$ elemet (ez $\binom{N-M}{n-k}$-féleképpen lehetséges). Mivel ez a két választás egymástól független, a kombinatorika szorzásszabálya alapján a két binomiális együtthatót összeszorozzuk.
* **Lezárás:** A kedvező esetek így kapott szorzatát, azaz a $\binom{M}{k} \cdot \binom{N-M}{n-k}$ értéket a táblán egyszerűen elosztjuk az összes eset $\binom{N}{n}$ számával. Ezzel algebrai bűvészkedés nélkül, tisztán kombinatorikai és logikai úton le is vezettük a tétel alapképletét.

<br>

> Ha egy 10 millió alkatrészt tartalmazó óriási raktárból húzunk ki mindössze 5 darabot ellenőrzésre, miért ad a "visszatevés nélküli" hipergeometriai eloszlás szinte hajszálpontosan megegyező eredményt a "visszatevéses" binomiális eloszlással, és a szórásnégyzet fenti képletében melyik az a konkrét szorzótényező, ami ezt a matematikai "békülést" okozza?

---