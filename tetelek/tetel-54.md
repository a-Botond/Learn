<a name="tetel-54"></a>

## 54. u-próba (Egymintás u-próba)
[[ Tartalomjegyzék ]](/README.md#tartalomjegyzek) | [[ Előző ]](./tetel-75.md#tetel-75) | [[ Következő ]](./tetel-55.md#tetel-55)


> Az u-próba egyszerűen azt méri meg, hogy a mintánkból kiszámolt átlag hány "szabványlépésre" (szabványos hibára) van az elméletileg elvárt céltól; ha ez a távolság gyanúsan nagy (tipikusan 2-nél több), akkor az eredeti feltevésünket elvetjük.


### TÉTEL:
**Feltételek:** Legyen $X_1, X_2, \dots, X_n$ egy normális eloszlású populációból vett minta, amelynek a várható értéke ($m$) ismeretlen, de a szórása ($\sigma$) **ismert**.
*(Nagy mintaelemszám, $n > 30$ esetén a centrális határeloszlás-tétel miatt az eredeti eloszlásnak nem is kell normálisnak lennie).*

**Nullhipotézis ($H_0$):** A populáció várható értéke pontosan megegyezik egy előre megadott $m_0$ konstanssal ($m = m_0$).

**A próbastatisztika:**
$$u = \frac{\overline{X} - m_0}{\frac{\sigma}{\sqrt{n}}}$$

**Eloszlás:** Ha a nullhipotézis igaz, akkor az $u$ próbastatisztika standard normális eloszlást követ: $u \sim \mathcal{N}(0, 1)$.



### BIZONYÍTÁS:
* **Kiindulópont:** Írjuk fel a táblára magának a mintaátlagnak ($\overline{X}$) az eloszlását! Tudjuk, hogy független normális változók összege (és így az átlaguk is) normális eloszlású marad. Ha $H_0$ igaz, az átlag várható értéke $m_0$ lesz, a szórásnégyzete pedig az eredeti szórásnégyzet $n$-ed részére csökken. Képletben: $\overline{X} \sim \mathcal{N}\left(m_0, \frac{\sigma^2}{n}\right)$.
* **A "Trükk":** A **standardizálás**! Hogy egy univerzális, a táblázatból könnyen kikereshető értéket kapjunk, a változóból le kell vonni a saját várható értékét, és el kell osztani a saját szórásával. Itt jön a hallgatók leggyakoribb hibája: a mintaátlag szórása nem $\sigma$, hanem a szórásnégyzet gyöke miatt $\frac{\sigma}{\sqrt{n}}$ (ezt hívjuk standard hibának). Ezt kell a nevezőbe írni.
* **Lezárás:** Mivel a normális eloszlás lineáris transzformációja (egy konstans levonása és egy konstanssal való osztás) garantáltan normális eloszlású marad, az $m_0$ levonása miatt a görbe közepe behúzódik $0$-ra, a szórásával való leosztás miatt pedig a szélessége (szórása) pontosan $1$ lesz. Ezzel be is láttuk, hogy a kiszámolt képlet egzaktan az $\mathcal{N}(0, 1)$ standard normális eloszlást adja.

<br>

> Ha az alapsokaság eredeti ingadozása (a $\sigma$ szórás) hatalmas, a józan ész azt diktálná, hogy lehetetlen egy kis eltérést észrevenni. Miért garantálja a képlet nevezőjében megbújó $\sqrt{n}$ tényező mégis azt, hogy ha elegendően sok adatot gyűjtünk (növeljük a mintát), a legapróbb hamisság is "tűélesen" lelepleződik az u-próba során?

---