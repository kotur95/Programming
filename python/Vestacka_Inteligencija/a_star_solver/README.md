## Pokretanje
1) `./a_star_solver.py`
2) Putem jupyter notebook-a (`a_star_solver.ipynb`)

## Primeri (izlaz resavaca):
```
Primer 3.5 (Iz knjige)
|-------|-----------------------------------------|------------|
|Tekuci |Stanje otvorenje liste                   |U zatvorenu |
|cvor   |cvor(roditelj, g+h)                      |L se dodaje |
|-------|-----------------------------------------|------------|
|       |A(-, 0+6)                                |            |
|-------|-----------------------------------------|------------|
| A(6)  |D(A,6+5), G(A,5+6)                       |    A(-)    |
|-------|-----------------------------------------|------------|
| D(11) |G(A,5+6), H(D,9+3), F(D,9+3), C(D,10+6)  |    D(A)    |
|-------|-----------------------------------------|------------|
| G(11) |H(D,9+3), F(D,9+3), C(D,10+6)            |    G(A)    |
|-------|-----------------------------------------|------------|
| H(12) |B(H,11+1), F(D,9+3), C(D,10+6)           |    H(D)    |
|-------|-----------------------------------------|------------|
| B(12) |F(D,9+3), E(B,13+0), C(D,10+6)           |    B(H)    |
|-------|-----------------------------------------|------------|
| F(12) |E(B,13+0), C(D,10+6)                     |    F(D)    |
|-------|-----------------------------------------|------------|
| E(13) |C(D,10+6)                                |            |
|-------|-----------------------------------------|------------|
Pronadjen put: A -> D -> H -> B -> E
```
## Resavanje Lavirinta:
```
Zadatak 4.8
---- MAZE ----
# F . . . 
. X # X . 
. . S . . 
--------------
A B C D E 
F G H I J 
K L M N O 
--------------
RESENJE:
|-------|------------------------------|------------|
|Tekuci |Stanje otvorenje liste        |U zatvorenu |
|cvor   |cvor(roditelj, g+h)           |L se dodaje |
|-------|------------------------------|------------|
|       |M(-, 0+3)                     |            |
|-------|------------------------------|------------|
| M(3)  |L(M,1+2), N(M,1+4), H(M,6+2)  |    M(-)    |
|-------|------------------------------|------------|
| L(3)  |K(L,2+3), N(M,1+4), H(M,6+2)  |    L(M)    |
|-------|------------------------------|------------|
| K(5)  |F(K,3+2), N(M,1+4), H(M,6+2)  |    K(L)    |
|-------|------------------------------|------------|
| F(5)  |N(M,1+4), H(M,6+2), A(F,9+1)  |    F(K)    |
|-------|------------------------------|------------|
| N(5)  |O(N,2+5), H(M,6+2), A(F,9+1)  |    N(M)    |
|-------|------------------------------|------------|
| O(7)  |J(O,3+4), H(M,6+2), A(F,9+1)  |    O(N)    |
|-------|------------------------------|------------|
| J(7)  |E(J,4+3), H(M,6+2), A(F,9+1)  |    J(O)    |
|-------|------------------------------|------------|
| E(7)  |D(E,5+2), H(M,6+2), A(F,9+1)  |    E(J)    |
|-------|------------------------------|------------|
| D(7)  |C(D,6+1), H(M,6+2), A(F,9+1)  |    D(E)    |
|-------|------------------------------|------------|
| C(7)  |B(C,7+0), H(M,6+2), A(F,9+1)  |    C(D)    |
|-------|------------------------------|------------|
| B(7)  |H(M,6+2), A(F,9+1)            |            |
|-------|------------------------------|------------|
Pronadjen put: M -> N -> O -> J -> E -> D -> C -> B
---- MAZE SOLUTION ----
# F * * * 
. X # X * 
. . S * * 
-----------------------
```
