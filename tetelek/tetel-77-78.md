<a name="tetel-77-78"></a>

## 77-78. Neyman-Pearson-lemma
[[ Tartalomjegyzék ]](/README.md#tartalomjegyzek) | [[ Előző ]](./tetel-74.md#tetel-74) | [[ Következő ]](./tetel-27.md#tetel-27)


> A Neyman-Pearson-lemma azt mondja ki, hogy ha két konkrét feltételezés (például két gyanúsított) közül kell a legkevesebb hibával választanunk, akkor a legjobb döntés az, ha a bizonyítékok (az adatok) valószerűségének hányadosát nézzük, és ott húzzuk meg a határt, ahol ez a mérleg a leginkább kibillen az egyik irányba.


### TÉTEL:
Legyen $\mathbf{X} = (X_1, \dots, X_n)$ egy minta. Két egyszerű hipotézist vizsgálunk az ismeretlen $\theta$ paraméterre: 
A nullhipotézis $H_0: \theta = \theta_0$, az ellenhipotézis pedig $H_1: \theta = \theta_1$.
A minta együttes sűrűségfüggvénye (likelihood-függvénye) a két esetben legyen $L_0(\mathbf{x}) = L(\theta_0; \mathbf{x})$ és $L_1(\mathbf{x}) = L(\theta_1; \mathbf{x})$.

A lemma kimondja, hogy az $\alpha$ terjedelmű (elsófajú hiba) próbák közül a **legerősebb** (amely a legkisebb másodfajú hibát adja) kritikus tartománya ($K$) a következő alakú:
$$K = \left\{ \mathbf{x} : \frac{L_1(\mathbf{x})}{L_0(\mathbf{x})} \ge c \right\}$$
ahol a $c$ konstans úgy van megválasztva, hogy teljesüljön a méretfeltétel: $P(\mathbf{X} \in K \mid H_0) = \alpha$.



### BIZONYÍTÁS:
* **Kiindulópont:** A bizonyításhoz vegyünk egy tetszőleges *másik*, a miénkkel versengő $K^*$ kritikus tartományt, aminek a terjedelme legfeljebb $\alpha$ (tehát $\int_{K^*} L_0 d\mathbf{x} \le \alpha$). A célunk megmutatni, hogy a mi likelihood-hányadoson alapuló $K$ tartományunk "ereje" jobb vagy egyenlő, mint a versenytársé: $\int_K L_1 d\mathbf{x} \ge \int_{K^*} L_1 d\mathbf{x}$.
* **A "Trükk":** Bontsuk fel a két kritikus tartományt közös metszetre és csak az egyikhez tartozó (diszjunkt) részekre! A zseniális észrevétel a hányados definíciójából adódik: a $K \setminus K^*$ tartományon (ami a mi próbánk része) az $L_1 \ge c \cdot L_0$ egyenlőtlenség igaz, míg a $K^* \setminus K$ tartományon (amit mi kihagytunk) az $L_1 < c \cdot L_0$ érvényes.
* **Lezárás:** Vizsgáljuk meg a két próba erejének különbségét, és integráljuk az $L_1$-et a szétbontott tartományokon. Mivel mindkét próba $\alpha$ terjedelmű, a $L_0$ feletti integrálok különbségeinél a $c$-vel szorzott tagok matematikailag egymásba alakíthatók és egyenlőtlenséggé formálhatók. Az integrálok algebrai rendezése után (kihasználva a fenti $\ge c$ és $< c$ szabályokat) egzaktan adódik, hogy a különbségük nem lehet negatív. Ezzel beláttuk, hogy a mi $K$ próbánk ereje felülmúlhatatlan.

<br>

> Ha a Neyman-Pearson-lemma matematikailag tökéletesen bebizonyítja, hogy az egyszerű hipotézisek esetén a likelihood-hányados adja a létező legerősebb próbát, miért omlik össze ez a gyönyörű, egzakt bizonyítás a való életben leggyakrabban használt összetett hipotézisek (például ha azt vizsgáljuk, hogy a várható érték "kisebb-e, mint 50") esetében?

---