<a name="tetel-29"></a>

## 29. Béta-eloszlás
[[ Tartalomjegyzék ]](/README.md#tartalomjegyzek) | [[ Előző ]](./tetel-27.md#tetel-27) | [[ Következő ]](./tetel-31.md#tetel-31)


> A Béta-eloszlás a "valószínűségek valószínűsége": egy 0 és 1 közötti skálán modellezi, hogy mennyire lehetünk biztosak egy esemény (például egy dobókocka cinkeltsége vagy egy weboldal konverziós rátája) valódi esélyében, miután már megfigyeltünk bizonyos számú $\alpha-1$ sikert és $\beta-1$ kudarcot.


### TÉTEL:
Egy folytonos $X$ valószínűségi változó Béta-eloszlású $\alpha > 0$ és $\beta > 0$ alakparaméterekkel (jelölése: $X \sim \text{Beta}(\alpha, \beta)$), ha a sűrűségfüggvénye a $(0, 1)$ nyílt intervallumon:
$$f(x) = \frac{1}{B(\alpha, \beta)} x^{\alpha-1} (1-x)^{\beta-1}$$
és $0$ egyébként. 

*(Ahol a nevezőben lévő norma, a Béta-függvény így számítható a Gamma-függvények segítségével: $B(\alpha, \beta) = \int_0^1 t^{\alpha-1} (1-t)^{\beta-1} dt = \frac{\Gamma(\alpha)\Gamma(\beta)}{\Gamma(\alpha+\beta)}$).*

Legfontosabb mutatói (vizsgán kérik):
* Várható érték: $E(X) = \frac{\alpha}{\alpha + \beta}$
* Szórásnégyzet: $D^2(X) = \frac{\alpha \beta}{(\alpha+\beta)^2(\alpha+\beta+1)}$



### BIZONYÍTÁS:
* **Kiindulópont:** A szóbeli vizsgán tipikusan a *várható érték* levezetését kérik, mert az teszteli a Béta- és Gamma-függvények kapcsolatának ismeretét. Írjuk fel a definíciót: $E(X) = \int_0^1 x \cdot \frac{1}{B(\alpha, \beta)} x^{\alpha-1} (1-x)^{\beta-1} dx$.
* **A "Trükk":** Az integranduson belüli "elnyelés" és az új eloszlás felismerése! Vonjuk össze a szorzó $x$-et a hatvánnyal, így $x^{\alpha}$ lesz belőle, amit rögtön írjunk át $x^{(\alpha+1)-1}$ alakra. Ezt észrevéve az integrálon belül hirtelen egy *új*, $\alpha+1$ és $\beta$ paraméterű Béta-eloszlás magfüggvényét látjuk. Szorozzuk be és osszuk is el az integrált a hiányzó $B(\alpha+1, \beta)$ konstanssal, hogy a belső rész egy teljes (és így $1$-re integrálódó) sűrűségfüggvénnyé váljon!
* **Lezárás:** Az 1-re integrálódás miatt a borzalmas integrál eltűnik, és csak a konstansok szorzata marad: $\frac{B(\alpha+1, \beta)}{B(\alpha, \beta)}$. A befejezéshez írjuk át ezeket Gamma-függvényekké! Használjuk a $\Gamma(z+1) = z\Gamma(z)$ faktoriális-szerű azonosságot: a számláló $\frac{\alpha\Gamma(\alpha)\Gamma(\beta)}{(\alpha+\beta)\Gamma(\alpha+\beta)}$ lesz. A korábbi $\Gamma$ tagok tökéletesen, egy az egyben kiejtik a nevezőt, és elegánsan, pusztán algebrai egyszerűsítéssel a táblán marad az $\frac{\alpha}{\alpha+\beta}$ végeredmény.

<br>

> Ha a Béta-eloszlás képletébe az $\alpha = 1$ és $\beta = 1$ paramétereket helyettesítjük, a bonyolult függvény meglepő módon azonnal összeomlik az $\sim U(0,1)$ egyenletes eloszlás lapos, "tégla" alakjává – ha a Béta-eloszlás a sikereink és kudarcaink mérlegét mutatja, logikailag mit jelent ez az egyenletes, "lapos" állapot egy kísérletsorozat megkezdése előtt?

---