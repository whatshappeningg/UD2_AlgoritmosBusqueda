# UD2: Algoritmos de búsqueda
## Conceptos básicos

**Problema:**
- Mundo: Espacio operable.
- Estado: Configuración cocnreta del mundo.
- Estado inicial: Denominado como ``i``, desde aquí se empieza a operar.
- Estado objetivo: Denominado como ``e``, aquí es a donde se quiere llegar.
- Función sucesora: Acciones posibles, varían según el problema. (Ej.: ↑↓ ←→)
- Coste: Facultativo, implica un valor añadido al cambiar de estado. (Ej.: ↑↓ +1, ←→ +2)
- Heurística: Facultativo, característico de los algoritmos de [búsqueda informada](#tipos-de-búsquedas).

**Algoritmo:**
- Frontera: Conjunto de nodos no expandidos. (Ej.: ``F = {A, F, G}``)
- Explorados: Conjunto de nodos expandidos. (Ej.: ``C = {i, B, D, C, E}``)
- Solución: Conjunto de estados a seguir para llegar del inicial al objetivo. (Ej.: ``Sol. = {i, A, B, D, e}``)
- Test objetivo: Se usa para saber si el estado actual es el objetivo. (Ej.: ``Test(D)``)
- Métodos: Ayudan a definir qué nodo del conjunto frontera expandir a continuación.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;FIFO: 'First In First Out', el elemento que más tiempo lleva en el conjunto. (Ej.: ``F = {A, F, G}`` => ``A``)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;LIFO: 'Last In Fist Out', el elemento que menos tiempo lleva en el conjunto. (Ej.: ``F = {A, F, G}`` => ``G``)
- Nodo: Estado con características añadidas.

**Solución:**

**Árbol de deciciones:**
- Utiliza el método GRAFO.
- Estado inicial + Función sucesora = Espacio de estados
- Nodo padre / raíz: Nodo inicial (``i``)
- Nodo hoja: Nodo no expansible.
- Backtraking: Escalar por las ramas del árbol hasta el anterior nodo sin expandir.
- Profundidad: Número de nodos a expandir antes de hacer backtraking. Variable.


### Tipos de búsquedas
**No informada:** No se tiene información complementaria de los nodos, no dejan nodos sin explorar y no repiten ninguno.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Algoritmos:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Búsqueda en anchura  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Búsqueda de coste uniforme ([Ejercicio](/CosteUniforme.md))  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Búsqueda en profundidad ([Ejercicio](/BúsquedaProfundidad.md))  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Búsqueda bidireccional

**Informada:** Se iene información complementaria de los nodos: la heurística. Viene dada por una función ``h(n)`` que indica cuán prometedor es cierto nodo y qué decisión tomar a continuación. (Ej.: Cercanía del potencial nodo a ``e``)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Algoritmos:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Método de ascensión de colinas  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Búsqueda por el mejor nodo  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Algoritmo A y A* ([Ejercicio](/A_A*.md))








