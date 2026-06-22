<a name="tetel-15"></a>

## 15. Sűrűségfüggvény, eloszlásfüggvény
[[ Tartalomjegyzék ]](/README.md#tartalomjegyzek) | [[ Előző ]](./tetel-12.md#tetel-12) | [[ Következő ]](./tetel-17.md#tetel-17)


> Az eloszlásfüggvény megmutatja, mennyi eséllyel "gyűlt össze" a valószínűség egy adott pontig (mint egy futólagos egyenleg), a sűrűségfüggvény pedig a valószínűség helyi "intenzitását" adja meg, amelynek a görbe alatti területe jelenti a tényleges (egy adott sávba esési) esélyt.


### TÉTEL:
**Eloszlásfüggvény ($F(x)$):** Tetszőleges $X$ valószínűségi változóra:
$$F(x) = P(X < x)$$
*(Megjegyzés: A magyar statisztikai oktatásban általában a szigorú egyenlőtlenséget ($<$) használják, míg a nemzetköziben gyakran a megengedőt ($\le$). Folytonos esetben a kettő ekvivalens.)*

**Sűrűségfüggvény ($f(x)$):** Folytonos $X$ esetén az a nemnegatív függvény, amelyre igaz, hogy az eloszlásfüggvény előáll az integráljaként:
$$F(x) = \int_{-\infty}^{x} f(t) dt$$

Ebből a két definícióból következik az intervallumba esés alaptétele (amit a vizsgán kérdeznek):
$$P(a \le X < b) = F(b) - F(a) = \int_{a}^{b} f(x) dx$$



### BIZONYÍTÁS:
* **Kiindulópont:** A fogalmakat definícióként fogadjuk el, ezeket nem kell bizonyítani. A vizsgán az ezekből származó alapállítást, az intervallumba esés valószínűségét ($P(a \le X < b) = F(b) - F(a)$) kell levezetni az axiómákból. Írjuk fel a táblára a $\{X < b\}$ eseményt!
* **A "Trükk":** Vágjuk ketté az eseményt egy $a < b$ pont mentén két egymást kizáró (diszjunkt) rész uniójára: $\{X < b\} = \{X < a\} \cup \{a \le X < b\}$. Mivel a két esemény diszjunkt, a 3. Kolmogorov-axióma (additivitás) értelmében a valószínűségük egyszerűen összeadható:
    $P(X < b) = P(X < a) + P(a \le X < b)$.
* **Lezárás:** Csak helyettesítsük be a $P(X < x)$ valószínűségek helyére az eloszlásfüggvény definícióját: $F(b) = F(a) + P(a \le X < b)$. Ezt az egyenletet a keresett intervallum valószínűségére átrendezve azonnal adódik a tétel. (Az integrálos rész egyenlősége pedig sima analízis, a Newton-Leibniz formula egyenes következménye).

<br>

> Tudjuk, hogy egy esemény valószínűsége sosem lehet 1-nél (100%-nál) nagyobb. Mégis miért lehetséges az, hogy a sűrűségfüggvény ($f(x)$) értéke egy adott pontban (pl. egy nagyon keskeny, hegyes haranggörbe csúcsán) akár 50 vagy 1000 is legyen, anélkül, hogy ez megsértené a valószínűségszámítás szabályait?

---