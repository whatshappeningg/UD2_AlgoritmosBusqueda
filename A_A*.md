# Algoritmos A y A*
Prioridades:
1. Menor evaluación
2. FIFO
## Nomenclatura
$^{g}$ N f $^{h}$

N = nodo

g = coste (↑↓ +1, ←→ +2)

h = heurística (casillas hasta e)

f = evaluación (g + h)

## Ejercicio

F = { **$^{0}$ i 4 $^{4}$** }  →  Test( $^{0}$ i 4 $^{4}$ )  → C = { $^{0}$ i 4 $^{4}$ }

F = { **$^{1}$ A 4 $^{3}$**, $^{1}$ B 6 $^{5}$ }  →  Test( $^{1}$ A 4 $^{3}$ )  → C = { $^{0}$ i 4 $^{4}$, $^{1}$ A 4 $^{3}$ }

F = { $^{1}$ B 6 $^{5}$, **$^{3}$ C 5 $^{2}$**, $^{3}$ D $^{4}$ }  →  Test( $^{3}$ C 5 $^{2}$ )  → C = { $^{0}$ i 4 $^{4}$, $^{1}$ A 4 $^{3}$, $^{3}$ C 5 $^{2}$ }

F = { **$^{1}$ B 6 $^{5}$**, $^{3}$ D 7 $^{4}$ }  →  Test( $^{1}$ B 6 $^{5}$ )  → C = { $^{0}$ i 4 $^{4}$, $^{1}$ A 4 $^{3}$, $^{3}$ C 5 $^{2}$, $^{1}$ B 6 $^{5}$ }

F = { **$^{3}$ D 7 $^{4}$**, $^{3}$ E 7 $^{4}$, $^{3}$ F 9 $^{6}$ }  →  Test( $^{3}$ D 7 $^{4}$ )  → C = { $^{0}$ i 4 $^{4}$, $^{1}$ A 4 $^{3}$, $^{3}$ C 5 $^{2}$, $^{1}$ B 6 $^{5}$, $^{3}$ D 7 $^{4}$ }

F = { **$^{3}$ E 7 $^{4}$**, $^{3}$ F 9 $^{6}$, $^{4}$ G 7 $^{3}$ }  →  Test( $^{3}$ E 7 $^{4}$ )  → C = { $^{0}$ i 4 $^{4}$, $^{1}$ A 4 $^{3}$, $^{3}$ C 5 $^{2}$, $^{1}$ B 6 $^{5}$, $^{3}$ D 7 $^{4}$, $^{3}$ E 7 $^{4}$ }

F = { $^{3}$ F 9 $^{6}$, **$^{4}$ G 7 $^{3}$**, $^{5}$ H 10 $^{5}$ }  →  Test( $^{4}$ G 7 $^{3}$ )  → C = { $^{0}$ i 4 $^{4}$, $^{1}$ A 4 $^{3}$, $^{3}$ C 5 $^{2}$, $^{1}$ B 6 $^{5}$, $^{3}$ D 7 $^{4}$, $^{3}$ E 7 $^{4}$, $^{4}$ G 7 $^{3}$ }

F = { $^{3}$ F 9 $^{6}$, $^{5}$ H 10 $^{5}$, **$^{5}$ I 7 $^{2}$** }  →  Test( $^{5}$ I 7 $^{2}$ )  → C = { $^{0}$ i 4 $^{4}$, $^{1}$ A 4 $^{3}$, $^{3}$ C 5 $^{2}$, $^{1}$ B 6 $^{5}$, $^{3}$ D 7 $^{4}$, $^{3}$ E 7 $^{4}$, $^{4}$ G 7 $^{3}$, $^{5}$ I 7 $^{2}$ }

F = { $^{3}$ F 9 $^{6}$, $^{5}$ H 10 $^{5}$, $^{6}$ J 9 $^{3}$, **$^{7}$ K 8 $^{1}$** }  →  Test( $^{7}$ K 8 $^{1}$ )  → C = { $^{0}$ i 4 $^{4}$, $^{1}$ A 4 $^{3}$, $^{3}$ C 5 $^{2}$, $^{1}$ B 6 $^{5}$, $^{3}$ D 7 $^{4}$, $^{3}$ E 7 $^{4}$, $^{4}$ G 7 $^{3}$, $^{5}$ I 7 $^{2}$, $^{7}$ K 8 $^{1}$ }

F = { **$^{3}$ F 9 $^{6}$**, $^{5}$ H 10 $^{5}$, $^{6}$ J 9 $^{3}$, $^{8}$ L 10 $^{2}$, $^{9}$ e 9 $^{0}$ }  →  Test( $^{3}$ F 9 $^{6}$ )  → C = { $^{0}$ i 4 $^{4}$, $^{1}$ A 4 $^{3}$, $^{3}$ C 5 $^{2}$, $^{1}$ B 6 $^{5}$, $^{3}$ D 7 $^{4}$, $^{3}$ E 7 $^{4}$, $^{4}$ G 7 $^{3}$, $^{5}$ I 7 $^{2}$, $^{7}$ K 8 $^{1}$, $^{3}$ F 9 $^{6}$ }

F = { $^{5}$ H 10 $^{5}$, **$^{6}$ J 9 $^{3}$**, $^{8}$ L 10 $^{2}$, $^{9}$ e 9 $^{0}$ }  →  Test( $^{6}$ J 9 $^{3}$ )  → C = { $^{0}$ i 4 $^{4}$, $^{1}$ A 4 $^{3}$, $^{3}$ C 5 $^{2}$, $^{1}$ B 6 $^{5}$, $^{3}$ D 7 $^{4}$, $^{3}$ E 7 $^{4}$, $^{4}$ G 7 $^{3}$, $^{5}$ I 7 $^{2}$, $^{7}$ K 8 $^{1}$, $^{3}$ F 9 $^{6}$, $^{6}$ J 9 $^{3}$ }

F = { $^{5}$ H 10 $^{5}$, $^{8}$ L 10 $^{2}$, **$^{9}$ e 9 $^{0}$** }  →  Test($^{9}$ e 9 $^{0}$ )  → C = { $^{0}$ i 4 $^{4}$, $^{1}$ A 4 $^{3}$, $^{3}$ C 5 $^{2}$, $^{1}$ B 6 $^{5}$, $^{3}$ D 7 $^{4}$, $^{3}$ E 7 $^{4}$, $^{4}$ G 7 $^{3}$, $^{5}$ I 7 $^{2}$, $^{7}$ K 8 $^{1}$, $^{3}$ F 9 $^{6}$, $^{6}$ J 9 $^{3}$, $^{9}$ e 9 $^{0}$ }

## Resultado
C = { $^{0}$ i 4 $^{4}$, $^{1}$ A 4 $^{3}$, $^{3}$ C 5 $^{2}$, $^{1}$ B 6 $^{5}$, $^{3}$ D 7 $^{4}$, $^{3}$ E 7 $^{4}$, $^{4}$ G 7 $^{3}$, $^{5}$ I 7 $^{2}$, $^{7}$ K 8 $^{1}$, $^{3}$ F 9 $^{6}$, $^{6}$ J 9 $^{3}$, $^{9}$ e 9 $^{0}$ }

F = { $^{5}$ H 10 $^{5}$, $^{8}$ L 10 $^{2}$ }

Solución = { $^{0}$ i 4 $^{4}$, $^{1}$ A 4 $^{3}$, $^{3}$ D 7 $^{4}$, $^{4}$ G 7 $^{3}$, $^{5}$ I 7 $^{2}$, $^{7}$ K 8 $^{1}$, $^{9}$ e 9 $^{0}$ }

Coste total = 9

![Diagrama 3](/img/Diagrama1.4.png)

## Cuestiones

**La heurística utilizada en el algoritmo A, ¿es admisible? ¿Por qué?**  
Sí es admisible porque la heurística nunca sobreestima el coste.

***¿Podemos decir que el algoritmo es A*?***  
Sí, sería un algoritmo A*.
