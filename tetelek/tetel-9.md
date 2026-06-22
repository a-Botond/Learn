<a name="tetel-9"></a>

## 9. Kolmogorov-féle axiómák 
[[ Tartalomjegyzék ]](#tartalomjegyzek) | [[ Előző ]](./tetelek/tetel-9b.md) | [[ Következő ]](./tetelek/tetel-9b.md)


> A valószínűség lényegében egy olyan matematikai "mérleg", ami sosem mutat negatívat, a biztos dolgokra mindig pontosan 100%-ot (1-et) mér, és ha események egyszerre nem következhetnek be (kizárják egymást), akkor a közös esélyüket egyszerűen a külön-külön vett esélyeik összeadásával kapjuk meg.


### TÉTEL:
Legyen $\Omega$ az eseménytér (a lehetséges kimenetelek halmaza) és $\mathcal{A}$ az események $\sigma$-algebrája. A $P: \mathcal{A} \to \mathbb{R}$ halmazfüggvényt valószínűségnek (vagy valószínűségi mértéknek) nevezzük, ha teljesíti az alábbi három axiómát:

1. **Nemnegativitás:** Minden $A \in \mathcal{A}$ eseményre:
$$P(A) \ge 0$$
2. **Normáltság:** A biztos esemény valószínűsége 1:
$$P(\Omega) = 1$$
3. **$\sigma$-additivitás (megszámlálható additivitás):** Ha $A_1, A_2, \dots \in \mathcal{A}$ páronként egymást kizáró (diszjunkt) események (azaz $A_i \cap A_j = \emptyset$ minden $i \neq j$ esetén), akkor:
$$P\left(\bigcup_{i=1}^{\infty} A_i\right) = \sum_{i=1}^{\infty} P(A_i)$$



### BIZONYÍTÁS:
* **Kiindulópont:** Oktatóként itt azt akarom hallani, hogy tudod: *az axiómákat definíció szerint nem bizonyítjuk* (ezek a matematika játékszabályai). A szóbeli vizsgán ilyenkor egy alaptulajdonságot, például a **komplementer esemény tételét** ($P(\overline{A}) = 1 - P(A)$) kell levezetni, hogy megmutasd, tudod használni az axiómarendszert.
* **A "Trükk":** Írjuk fel a biztos eseményt ($\Omega$) egy tetszőleges $A$ esemény és annak komplementere ($\overline{A}$) diszjunkt uniójaként: $\Omega = A \cup \overline{A}$. Mivel a két halmaz metszete üres, rászabadíthatjuk az unióra a 3. axiómát (véges esetre alkalmazva).
* **Lezárás:** A 2. axióma miatt a bal oldalon $P(\Omega) = 1$. A jobb oldalon a 3. axióma alapján $P(A \cup \overline{A}) = P(A) + P(\overline{A})$. Ebből azonnal adódik az $1 = P(A) + P(\overline{A})$ egyenlet, amit $P(\overline{A})$-ra rendezve megkapjuk a bizonyítandó állítást.

<br>

> Ha a valószínűséget felfoghatjuk úgy, mint területek mérését, miért van elvi szükség a végtelen sok elemre vonatkozó $\sigma$-additivitásra (3. axióma) a "sima" véges additivitás helyett, és miért omlana össze enélkül a folytonos valószínűségi változók (pl. egyetlen pontszerű érték eltalálása a normális eloszlásnál) elmélete?

---