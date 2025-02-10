# UD2: Algoritmos de búsqueda
## Conceptos básicos

**Problema:**
- Estado: Configuración cocnreta del mundo.
- Estado inicial: Denominado como ``i``, desde aquí se empieza a operar.
- Estado objetivo: Denominado como ``e``, aquí es a donde se quiere llegar.
- Función sucesora: Acciones posibles, varían según el problema. (Ej.: ↑↓ ←→)
- Coste: Facultativo. Implica un valor añadido al cambiar de estado. (Ej.: ↑↓ +1, ←→ +2)
- Heurística: Facultativo. Característico de los algoritmos de [búsqueda informada](#tipos-de-búsquedas).

**Algoritmo:**
- Frontera: Conjunto de nodos no expandidos. (Ej.: ``F = {A, F, G}``)
- Explorados: Conjunto de nodos expandidos. (Ej.: ``C = {i, B, D, C, E}``)
- Solución: Conjunto de estados a seguir para llegar del inicial al objetivo. (Ej.: ``Sol. = {i, A, B, D, e}``)
- Test objetivo: Se usa para saber si el estado actual es el objetivo. (Ej.: ``Test(D)``)

**Solución:**

**Árbol de deciciones:**
- Utiliza el método GRAFO.
- Estado inicial + Función sucesora = Espacio de estados
- 


### Tipos de búsquedas
**No informada:** No se tiene información complementaria de los nodos, no dejan nodos sin explorar y no repiten ninguno.

Algoritmos:
- Búsqueda en anchura
- Búsqueda de coste uniforme
- Búsqueda en profundidad
- Búsqueda bidireccional

**Informada:** Se iene información complementaria de los nodos: la heurística. Viene dada por una función ``h(n)`` que indica cuán prometedor es cierto nodo y qué decisión tomar a continuación.

Algoritmos:
- Método de ascensión de colinas
- Búsqueda por el mejor nodo
- Algoritmo A y A*








