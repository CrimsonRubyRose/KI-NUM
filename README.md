# KI-NUM
Repozitář vytvořený pro zvládnutí KI/NUM



# Řešení Nelineárních Rovnic (Body 2. a 3.) ####
### puleniIntervalu (Bisekce)       (Zaručená) 
Výhody : Vždy konverguje. Ideální, když potřebujete zaručený výsledek, i když pomalý.
Složitost:  O(log2​(1/ε))        Požadovaná chyba = ε	


Princip: Metoda opakovaně půlí interval, ve kterém se nachází kořen. Kořen je vždy v té polovině, kde má funkce stále opačná znaménka na koncích.

### NewtonHorner
Výhody: Nejrychlejší (kvadratická konvergence O(h**2)). Použijte, pokud je počáteční odhad dobrý.
Složitost: O(n)      stupeň polynomu = n 

Princip:

# Řešení Soustav Lineárních Rovnic (Body 4. a 5.) ###

### GaussEliminationPivoting

Výhody: Nejuniverzálnější a stabilní řešič. Přesné řešení.
Složitost: O(N3)    N = Počet neznámých

Princip: Aproximace tečnou. Začnete v bodě x. Zde se vypočítá tečna k funkci f(x) a jejím průsečíkem s osou x se dostanete k novému, přesnějšímu odhadu kořene. Pro polynomy je to efektivní díky Hornerovu schématu, které počítá f(x) i f′(x) najednou.


### Jacobi (vektorizovaná)

Výhody: Rychlá pro velké, řídké matice. Použijte, když je A diagonálně dominantní.
Složitost: O(N2)   N = Počet neznámých

Princip:

# Interpolace (Body 6. a 7.) ### 
### Newtonův interpolační polynom (Dělené diference)
Výhody:
Složitost: O(N2)  kde N = počet bodů

### Aproximace (LSA) (Body 8. a 9.) ### 
# Metoda nejmenších čtverců (MNC)
O(N2⋅M), kde N je počet koeficientů a M je počet bodů.

# Integrace (Bod 10) ###

### TrapezoidalRule

Výhody: Jednoduchá a rychlá na implementaci, i když jen O(h**2).
Složitost: 

Princip:


### SimpsonsRule

Výhody: Nejvyšší přesnost (O(h**4)). Ideální, když potřebujete malé N.
Složitost:

Princip:


# Numerické Derivování (Bod 11) ###

### DerivativeOneSide

Výhody: Nejjednodušší (O(h)). Použijte, když x je na hranici intervalu.
Složitost:

Princip:


### DerivativeBothSide

Výhody: Nejpřesnější (O(h2)). Použijte vždy, když to x dovolí.
Složitost:

Princip:


# Řešení ODR (Body 12. a 13.) ###


### EulerMethod
Výhody: Nejjednodušší na implementaci. (Ale nepřesný)
Složitost:

Princip:


### RK4
Výhody: Nejpřesnější a standardní (O(h**4)). Vyžaduje nejméně kroků h.
Složitost:

Princip:
