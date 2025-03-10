# Algoritmo de búsqueda en profundidad
Prioridad de movimientos: ↑ ↓  ← →  
Método: LIFO
## Sin límite de profundidad
F = {**i**}  →  Test(i)  → C = {i}

F = {A, **B**}  →  Test(B)  → C = {i, B}

F = {A, C, **D**}  →  Test(D)  → C = {i, B, D}

F = {A, **C**}  →  Test(C)  → C = {i, B, D, C}

F = {A, **E**}  →  Test(E)  → C = {i, B, D, C, E}

F = {A, F, **G**}  →  Test(G)  → C = {i, B, D, C, G, E}

F = {A, F, **H**}  →  Test(H)  → C = {i, B, D, C, G, H}

F = {A, F, **I**}  →  Test(I)  → C = {i, B, D, C, G, H, I}

F = {A, F, **J**}  →  Test(J)  → C = {i, B, D, C, G, H, I, J}

F = {A, F, K, **L**}  →  Test(L)  → C = {i, B, D, C, G, H, I, J, L}

F = {A, F, K, **M**}  →  Test(M)  → C = {i, B, D, C, G, H, I, J, L, M}

F = {A, F, K, N, **e**}  →  Test(e)  → C = {i, B, D, C, G, H, I, J, L, M, e}

### Resultado
C = {i, B, D, C, G, H, I, J, L, M, e}

F = {A, F, K, N}

Solución = {i, B, C, E, G, H, I, J, L, M, e}

![Diagrama 1](/img/Diagrama1.1.png)

## Con límite de profundidad 5
F = {**i**}  →  Test(i)  → C = {i}

F = {A, **B**}  →  Test(B)  → C = {i, B}

F = {A, C, **D**}  →  Test(D)  → C = {i, B, D}

F = {A, **C**}  →  Test(C)  → C = {i, B, D, C}

F = {A, **E**}  →  Test(E)  → C = {i, B, D, C, E}

F = {A, F, **G**}  →  Test(G)  → C = {i, B, D, C, E, G}

F = {A, F, **H**}  →  Test(H)  → C = {i, B, D, C, E, G, H}

F = {A, **F**}  →  Test(F)  → C = {i, B, D, C, E, G, H, F}

F = {**A**}  →  Test(A)  → C = {i, B, D, C, E, G, H, F, A}

F = {I, **J**}  →  Test(J)  → C = {i, B, D, C, E, G, H, F, A, J}

F = {I, **K**}  →  Test(K)  → C = {i, B, D, C, E, G, H, F, A, J, K}

F = {I, **L**}  →  Test(L)  → C = {i, B, D, C, E, G, H, F, A, J, K, L}

F = {I, M, **N**}  →  Test(N)  → C = {i, B, D, C, E, G, H, F, A, J, K, L, N}

F = {I, M, Ñ, **e**}  →  Test(e)  → C = {i, B, D, C, E, G, H, F, A, J, K, L, N, e}

### Resultado
C = {i, B, D, C, E, G, H, F, A, J, K, L, N, e}

F = {I, M, Ñ}

Solución = {i, A, J, K, L, N, e}

![Diagrama 2](/img/Diagrama1.2.png)
