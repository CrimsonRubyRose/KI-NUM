# KI-NUM
Repozitář vytvořený pro zvládnutí KI/NUM


# Obsah
* [Řešení Nelineárních Rovnic](#Řešení-Nelineárních-Rovnic)
* [Řešení Soustav Lineárních Rovnic](#Řešení-Soustav-Lineárních-Rovnic)
* [Interpolace](#Interpolace)
* [Aproximace](#Aproximace)
* [Integrace](#Integrace)
* [Numerické Derivování](#Numerické-Derivování)
* [Řešení Obyčejných Diferenciálních Rovnic](#Řešení-Obyčejných-Diferenciálních-Rovnic)
* [Tahák](#Tahák)
* [Rychlé informace](#Rychlá-tabulka)

# Předchozí zápočty a řešení


## [Příklad1 24.12.20](https://gist.github.com/CrimsonRubyRose/9275c0cc2944fc1a1669bb88ca0bc676)
![Alternativní Text Obrázku](/Obrázky/ZápočetNUM24-12-20.png)

## [Příklad2:](https://gist.github.com/CrimsonRubyRose/9275c0cc2944fc1a1669bb88ca0bc676)
![Alternativní Text Obrázku](/Obrázky/ZápočetNUM25-01-24.png)

## [Příklad3:]()
![Alternativní Text Obrázku](/Obrázky/ZápočetNUM-24-02-16.png)

## [Příklad4:]()
![Alternativní Text Obrázku](/Obrázky/ZápočetNUM-24-03-22.png)

## [Příklad5:]()
![Alternativní Text Obrázku](/Obrázky/ZápočetNUM-25-04-16.png)

## [Příklad6:]()
![Alternativní Text Obrázku](/Obrázky/ZápočetNUM-25-07-03.png)


# Tahák

## 1. Numerická integrace
* [Zpět na Obsah](#Obsah)
### Jak zadání poznat
* Znak integrálu (∫), oblast pod křivkou, odhadni a definuj integrál a analyzuj chybu oproti n

### Příklady:
* Spočítej ∫₁² (1/x) dx pomocí Newton-Cotes, a vyzuálně ukažte (plot)

### Doporučené metody:
* SimpsonRule
* MidpointRule
* TrapezoidalRule

## 2. Řešení lineráních systémů (Ax = b)
* [Zpět na Obsah](#Obsah)
### Jak zadání poznat
* Maticové Zadání Ax = b, "vyřeš pro x", přičemž prvky matice jsou definováný pomocí integrálů. 

### Příklady:
* “Vyřeš Ax = b kde A_ij = ∫₀¹ t^{i+j-2} dt.”

### Doporučené metody:
* GaussPivot
* Jacobi
* (Gauss,GaussSeidel)

## 3. Interpolace
* [Zpět na Obsah](#Obsah)
### Jak jí poznat
* "Najděte polynom skrz všechny datové body, "interpolujte", křivka musí projít skrz všechny body.”

### Příklady:
* “Vyrob polyon který přesně projde skrz daná data, vytvoř plot s výsledkem graficky.

### Doporučené metody:
* Lagrange
* NewtonInterpolation
* Vandermonde

## 4. Aproximace/ Regrese/ Nejméně čtverců
* [Zpět na Obsah](#Obsah)
### Jak jí poznat
* "Best fit”, “Aproximuj”, “Regresse”, “trend”, “minimalizuj sumu squared chyb”, noisy (šum) data.

### Příklady:
* “Fit a polynomial of degree 2 to experimental data.”

### Doporučené metody:
* LSA (Least Squares Approximation)
* LSS (Least Squares Solution)



## 5. Nelineární aproximace, odhad parametrů
* [Zpět na Obsah](#Obsah)
### Jak zadání poznat
* “aproximuj nelineární model”, například a(p) = am * bp / (1+bp), “odhadni parametry modelu.

### Příklady:
* “Fit a(p) model to data, estimate am and b.”

### Doporučené metody:
* NonLinearFit ???


## 6. Hledání Kořene
* [Zpět na Obsah](#Obsah)
### Jak zadání poznat
* “Najdi f(x)=0”, kde se přímky střetnou/protnou.“

### Příklady:
* ““Najdi x kdef(x) = 0”, nebo průnik dvou proložených přímek.

### Doporučené metody:
* Bisekce (půlení intervalu)
* NewtonHorner ??

Nové: Diskrétní trapezoidal, solve_ode 

## Rychlá tabulka
* [Zpět na Obsah](#Obsah)

| Numerický Úkol | Typická Fráze v Zadání (CZ) | Anglický Ekvivalent | Doporučené Metody |
| :--- | :--- | :--- | :--- |
| **Numerická Kvadratura** | *Určitý integrál INT, plocha pod křivkou, odhadněte* | *Numerical Integration* | **Simpsonovo pravidlo**, Lichoběžníkové pravidlo |
| **Lineární Soustavy** | *Lineární soustava Ax = b, řešte pro x* | *Linear System, Ax=b solve* | **Gaussova eliminace**, **Gauss-Seidelova metoda**, Jacobiho metoda |
| **Interpolace** | *Proložení všemi body, interpolujte* | *Interpolation* | **Lagrangeův polynom**, **Newtonova interpolační formule** |
| **Aproximace (Regrese)** | *Nejlepší proložení (fit), trend* | *Least Squares (LSS)* | **Metoda nejmenších čtverců (MNČ)** |
| **Nelineární Regrese** | *Model s parametry, a(p), odhad parametrů* | *Nonlinear Fit / Parameter Estimation* | **Nelineární prokládání** (iterativní) |
| **Hledání Kořenů** | *f(x)=0, průsečík funkcí, nulový bod* | *Root finding / Intersection* | **Metoda půlení intervalu (Bisekce)**, **Newtonova metoda** |


## Rychlé rozhodnutí

| Otázka/Cíl v Zadání | Odpověď (Použijte Metodu) | Konkrétní Typy Metod |
| :--- | :--- | :--- |
| **Přesné proložení všemi body?** | **Interpolace** | Lagrangeův polynom, Newtonova interpolace |
| **Nejlepší proložení / Trend (ne přesné)?** | **Regrese / Aproximace** | Metoda nejmenších čtverců (MNČ) |
| **Soustava rovnic ($Ax = b$)?** | **Řešení Lineárních Soustav** | Gaussova eliminace, Gauss-Seidelova metoda |
| **Integrál / Plocha pod křivkou?** | **Numerická Integrace (Kvadratura)** | Simpsonovo pravidlo, Lichoběžníkové pravidlo |
| **Kořen / Průsečík / Nulový bod ($f(x)=0$)?** | **Hledání Kořenů** | Metoda půlení intervalu (Bisekce), Newtonova metoda |
| **Odhad parametrů v nelineární formuli?** | **Nelineární Regrese** | Nelineární prokládání (NonlinearFit) |


# Řešení Nelineárních Rovnic
* [Zpět na Obsah](#Obsah)

![Alternativní Text Obrázku](/Obrázky/ŘešeníNelineárníchRovnic.png)


### [puleniIntervalu (Bisekce) (Hledání kořenů) (Zaručená)](https://gist.github.com/CrimsonRubyRose/9beb2b1fcb5b5862a0b2fbc9bd2155be), ### [PomocnáFunkceProBisekci(Nalezení Intervalu)](https://gist.github.com/CrimsonRubyRose/25e35f91e915159bb49ff3c650bf870c)
Výhody : Vždy konverguje. Ideální, když potřebujete zaručený výsledek, i když pomalý.

Složitost:  O(log2​(1/ε))        Požadovaná chyba = ε	

Podmínky: Funkce musí být spojitá. Hodnoty intervalu musí mít jiné znaménko na začátku.

Princip: Metoda opakovaně půlí interval, ve kterém se nachází kořen. Kořen je vždy v té polovině, kde má funkce stále opačná znaménka na koncích.

### [NewtonHorner] (Hledání Kořenů) (https://gist.github.com/CrimsonRubyRose/3fdb6b3943c0d4548f07a09d185e4adf)

Výhody: Nejrychlejší (kvadratická konvergence O(h**2)). Použijte, pokud je počáteční odhad dobrý.  Zjednodušuje velké polynomy při výpočtu.

Složitost: O(n)      stupeň polynomu = n 

Podmínky: Počáteční odhad se musí blížit hledanému kořenu a derivace nesmí být nikdy nulová! 

Princip: Vkládáme hodnoty. Dokoud není výsledek 0. Což je kořen. Každá následující hodnota je vypočítaná jako : hodnota x - P(x)/Derivace P(x) = Nová hodnota x.  

Epsilon (ε) určuje kdy se algoritmus zastaví. Např u 0.01 (Menší = přesnější, ale pomalejší)

# Řešení Soustav Lineárních Rovnic
* [Zpět na Obsah](#Obsah)
### [GaussEliminationPivotingZobrazit Kód](https://gist.github.com/CrimsonRubyRose/dffc325d9d48a38eed4d3f42c4e1d1d5)

Výhody: Nejuniverzálnější a stabilní řešič. Přesné řešení.

Složitost: O(N3)    N = Počet neznámých

Princip: Aproximace tečnou. Začnete v bodě x. Zde se vypočítá tečna k funkci f(x) a jejím průsečíkem s osou x se dostanete k novému, přesnějšímu odhadu kořene. Pro polynomy je to efektivní díky Hornerovu schématu, které počítá f(x) i f′(x) najednou.


### [Jacobi (vektorizovaná)](https://gist.github.com/CrimsonRubyRose/af176eb6891e9f7fa6cafb7f7be9fd8e)

Výhody: Rychlá pro velké, řídké matice (přes 90% nul). Použijte, když je A diagonálně dominantní.

Složitost: O(N2)   N = Počet neznámých

Podmínky: Matice by měla být přes 90% z nul. Aby tento algoritmus byl rychlejší než gauss. NEBO musí být diagonálně dominantní (Absolutní hodnota členů v diagonále je větší než součet členů v absolutních hodnotách v řádku). Pro diagonálě dominantní členy je často potřeba matici upravit změnou řádků!

Princip: Vytvoříme pro každé x rovnici x=.... . Každou iterací dosadíme hodnoty x které nám vyšli v předchozí iteraci a tak pokračujem dokud se nepřiblížíme k požadovaným hodnotám tak že nastavená Xmin a Xmax odchylka je splněna.

# Interpolace
* [Zpět na Obsah](#Obsah)
### Newtonův interpolační polynom (Dělené diference) [koeficienty](https://gist.github.com/CrimsonRubyRose/8f1501da74fff5fb4fa46e779b7e40a5) ,    [Hodnota](https://gist.github.com/CrimsonRubyRose/900d6f11e692cc04f3194bc4d31afb64) 
Výhody: Lepší než lagrange, rekuriznví. 

Složitost: O(N2)  kde N = počet bodů,  (Řád polynomu je N-1)

Nevýhoda: Interpolace vrátí pouze koeficienty. Pro jejich zpracování je potřeba např.  (hornernewton)

Princip: Metoda která najde koeficienty polynomiálu který projde našimi body. Spočítáme c0-cn.  c0 je zadaný první bod. c1 je směrnice (rozdíl sklonu c0,c1). c2 až cn měří jak moc se sklon změnil mezi nima a předchozím bodem.     Výsledek: Polynom=c0​+c1​⋅(člen 1)+c2​⋅(člen 2)+...

# Aproximace
* [Zpět na Obsah](#Obsah)
### [ Metoda nejmenších čtverců (MNC) ###  ](https://gist.github.com/CrimsonRubyRose/4c5827374d9b4e26cfd68141394654e0)
 

Výhody:
Složitost: O(N2⋅M), kde N je počet koeficientů a M je počet bodů.

Princip: Spočte koeficienty aproximačního polynomu stupně n − 1 pro body zadané vektory x→ , y→ .

# Integrace
* [Zpět na Obsah](#Obsah)
### [TrapezoidalRule](https://gist.github.com/CrimsonRubyRose/01b896c71e61f81f0c6c8e4002a18a1c) , [TrapezoidalDiskrétní](https://gist.github.com/CrimsonRubyRose/b73434be120211574b8cf4990aeea030) Specificky pro diskrétní výstup RK4

Výhody: Jednoduchá a rychlá na implementaci, i když jen O(h**2).

Složitost: 

Princip:






### [SimpsonsRule](https://gist.github.com/CrimsonRubyRose/b73434be120211574b8cf4990aeea030)

Výhody: Nejvyšší přesnost (O(h**4)). Ideální, když potřebujete malé N.

Složitost:

Princip:


# Numerické Derivování
* [Zpět na Obsah](#Obsah)
### DerivativeJednosměrná [Dopředu+](https://gist.github.com/CrimsonRubyRose/363e9afbfd96ca83ce09b1155e1ec93c), [Dozadu-UNTESTED](https://gist.github.com/CrimsonRubyRose/ac1ec6f9fa6da4859d309c399394f070)
Výhody: Nejjednodušší (O(h)). Použijte, když x je na hranici intervalu.

Složitost:

Princip:



### [DerivativeBothSide](https://gist.github.com/CrimsonRubyRose/f36d5167514d63d681bcb3e2bd26b332)

Výhody: Nejpřesnější (O(h2)). Použijte vždy, když to x dovolí.

Složitost:

Princip:


# Řešení Obyčejných Diferenciálních Rovnic
* [Zpět na Obsah](#Obsah)

### EulerMethod [Dopředu](https://gist.github.com/CrimsonRubyRose/7ecdf48a63b37498bceaa531ba569371), [Oběstrany](https://gist.github.com/CrimsonRubyRose/f36d5167514d63d681bcb3e2bd26b332), [Dozadu](https://gist.github.com/CrimsonRubyRose/da470d40dd90ae52bcffcd526386eec6)
Výhody: Nejjednodušší na implementaci. (Ale nepřesný)

Složitost:

Princip:


### [RK4](https://gist.github.com/CrimsonRubyRose/0aaf8f6090fac076239a9c8c307657f5)
Výhody: Nejpřesnější a standardní (O(h**4)). Vyžaduje nejméně kroků h. Ale extrémně pomalá.   Pro interval v zadání potřebuje solve_ode

Složitost:

Princip:


# Pomocné funkce




### [solve_ode](https://gist.github.com/CrimsonRubyRose/a0d45e2840169f0386c1215d28cb1c7e)
Princip: Volá ostatní funkce jako např. RK4 a je využita když je v zadání ODR definován interval.
