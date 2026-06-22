<a name="tetel-18"></a>

## 18. Binomiális eloszlás
[[ Tartalomjegyzék ]](/README.md#tartalomjegyzek) | [[ Előző ]](./tetel-49.md#tetel-49) | [[ Következő ]](./tetel-22.md#tetel-22)


> A binomiális eloszlás pontosan megmondja, mekkora az esélye annak, hogy ha egy kísérletet (például egy cinkelt érme feldobását) egy fix számszor megismétlünk, akkor abból pontosan egy adott darabszámú alkalommal kapunk "sikeres" kimenetelt.


### TÉTEL:
Egy $X$ diszkrét valószínűségi változó binomiális eloszlású ($n$ és $p$ paraméterekkel, jelölése $X \sim \text{Bin}(n, p)$), ha egy $p$ ($0 < p < 1$) valószínűségű esemény bekövetkezéseinek számát méri $n$ darab teljesen független kísérletből.

Valószínűség-eloszlása (annak esélye, hogy pontosan $k$ siker történik):
$$P(X = k) = \binom{n}{k} p^k (1-p)^{n-k} \quad \text{ahol } k \in \{0, 1, \dots, n\}$$

*Legfontosabb jellemzői (szóbeli vizsgán gyakran kérik azonnal):*
* Várható értéke: $E(X) = n \cdot p$
* Szórásnégyzete: $D^2(X) = n \cdot p \cdot (1-p)$



### BIZONYÍTÁS:
* **Kiindulópont:** (Az eloszlás képletének levezetése) Képzeljünk el egyetlen konkrét kimenetel-sorozatot, amelyben pontosan $k$ darab "siker" és $n-k$ darab "kudarc" követi egymást egy fix sorrendben (pl. először jön az összes siker, majd a kudarcok). Mivel a kísérletek függetlenek, a szorzástétel alapján ennek a konkrét sorozatnak a valószínűsége: $p^k \cdot (1-p)^{n-k}$.
* **A "Trükk":** Kombinatorikai leszámlálás. Észre kell venni, hogy a mi feltételünk csak a sikerek *darabszámát* rögzíti ($k$), a sorrendjüket nem! Hányféleképpen válasszuk ki az $n$ darab kísérletből azt a $k$ helyet, ahová a sikerek kerülnek? Ez egy ismétlés nélküli kombináció: pontosan $\binom{n}{k}$-féleképpen történhet.
* **Lezárás:** Mivel az eltérő sorrendű kimenetelek egymást kizáró események (vagy ez a sorrend valósul meg, vagy az), az axiómák miatt a valószínűségeiket össze kell adni. Mivel mind a $\binom{n}{k}$ darab verziónak pontosan ugyanaz a valószínűsége, egyszerűen megszorozzuk az egy sorozatra jutó esélyt az összes lehetséges sorrend számával, így megkapjuk a $P(X=k)$ végleges képletét. *(Oktatói bónusz: Ha megkérdik, honnan tudjuk, hogy ezek összege 1-et ad, vágd rá: a Newton-féle binomiális tétel miatt, hiszen $\sum \binom{n}{k} p^k (1-p)^{n-k} = (p + (1-p))^n = 1^n = 1$.)*

<br>

> Ha egy szabályos érmét 100-szor feldobsz, a fejek számának várható értéke pontosan 50. Miért van az, hogy matematikailag mégis nagyon kicsi (kevesebb mint 8%) az esélye annak, hogy *hajszálpontosan* 50 fejet dobj, holott elméletben ez a leginkább "valószínű" egyedi forgatókönyv?

---