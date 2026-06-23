<a name="tetel-35-37"></a>

## 35-37. Összegek eloszlásai (és a reproduktivitás)
[[ Tartalomjegyzék ]](/README.md#tartalomjegyzek) | [[ Előző ]](./tetel-41.md#tetel-41) | [[ Következő ]](./tetel-50.md#tetel-50)


> Ha azonos típusú, egymástól független véletlen dolgokat adunk össze (például két normális eloszlású hibát vagy két Poisson-folyamat eseményeit), bizonyos "kiválasztott" eloszlások csodálatos módon megtartják az eredeti alakjukat, és csupán a paramétereik (az átlaguk és a szórásuk) adódnak össze.


### TÉTEL:
**Általános eset (Konvolúció):** Ha $X$ és $Y$ független folytonos valószínűségi változók, összegük sűrűségfüggvénye a két sűrűségfüggvény konvolúciója:
$$f_{X+Y}(z) = \int_{-\infty}^{\infty} f_X(x) \cdot f_Y(z-x) dx$$

**A reproduktivitás tétele (Normális eloszlásra):**
Ha $X \sim \mathcal{N}(m_1, \sigma_1^2)$ és $Y \sim \mathcal{N}(m_2, \sigma_2^2)$ független valószínűségi változók, akkor az összegük is pontosan normális eloszlású marad:
$$X + Y \sim \mathcal{N}(m_1 + m_2, \sigma_1^2 + \sigma_2^2)$$
*(Ugyanez az alaktartó tulajdonság igaz független Poisson, Binomiális (azonos $p$-vel) és Gamma eloszlások összegére is).*



### BIZONYÍTÁS:
* **Kiindulópont:** A konvolúciós integrál kiszámítása normális eloszlásokra egy algebrai rémálom, ezért egy egyetemi vizsgán a legfőbb fegyvert, a **karakterisztikus függvényt** (vagy momentumgeneráló függvényt) vetjük be! Írjuk fel a táblára az alaptételt: független változók összegének karakterisztikus függvénye a változók karakterisztikus függvényeinek szorzata, azaz $\varphi_{X+Y}(t) = \varphi_X(t) \cdot \varphi_Y(t)$.
* **A "Trükk":** Mivel a normális eloszlás karakterisztikus függvénye exeponenciális alakú ($\varphi_X(t) = e^{i m_1 t - \frac{1}{2}\sigma_1^2 t^2}$), a szorzás puszta összeadássá szelídül! Az azonos alapú hatványok szorzásának szabálya miatt a kitevőket egyszerűen csak össze kell adni, a bázis ($e$) érintetlen marad.
* **Lezárás:** A kitevők összevonása után ezt kapjuk: $\exp\left[i(m_1+m_2)t - \frac{1}{2}(\sigma_1^2+\sigma_2^2)t^2\right]$. Ezt ránézésre azonosítjuk: ez hajszálpontosan egy $m_1+m_2$ várható értékű és $\sigma_1^2+\sigma_2^2$ szórásnégyzetű normális eloszlás karakterisztikus függvénye. Mivel az eloszlások és a karakterisztikus függvények között egy-egy értelmű a kapcsolat (kölcsönösen egyértelműségi tétel), bebizonyítottuk, hogy az összeg tényleg normális eloszlású.

<br>

> Ha két független normális eloszlás összege ismét egy gyönyörű haranggörbe lesz, miért van az, hogy két független egyenletes eloszlás összege (mint például két szabályos dobókocka eredménye) már elveszíti a lapos "tégla" alakját, és egy csúcsos, háromszög alakú eloszlássá torzul?

---