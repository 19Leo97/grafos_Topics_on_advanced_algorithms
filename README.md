# Algoritmos Avanzados de Grafos - TAA

Este repositorio contiene un entorno interactivo y visual para el estudio de algoritmos complejos sobre grafos, desarrollado como parte del taller de la asignatura **Topics on Advanced Algorithms**. El proyecto integra implementaciones algorítmicas con visualizaciones dinámicas de estados y estructuras de datos.

## 🚀 Algoritmos Implementados

El núcleo del proyecto se encuentra en el cuaderno `graphs.ipynb`, que incluye las siguientes implementaciones:

* **Búsqueda en Anchura (BFS):** Recorre el grafo por niveles desde un nodo fuente, gestionando el estado de los nodos mediante colores (blanco, gris, negro) y calculando la distancia mínima desde el origen.
* **Búsqueda en Profundidad (DFS):** Implementación que registra tiempos de descubrimiento ($d$) y finalización ($f$) para cada nodo.
    * **Clasificación de Aristas:** Identificación automática de aristas de árbol, avance, retroceso y cruzadas.
* **Componentes Fuertemente Conectados (SCC):** Basado en la ejecución de DFS sobre el grafo original y su traspuesto ($G^T$) para identificar conjuntos de vértices mutuamente alcanzables.
* **Algoritmo de Kruskal:** Encuentra el Árbol de Expansión Mínima (MST) seleccionando aristas en orden de peso y utilizando estructuras de conjuntos disjuntos (*Union-Find*) para evitar ciclos.
* **Algoritmo de Prim:** Construye el MST seleccionando de forma voraz el nodo más cercano al árbol en crecimiento mediante una cola de prioridad.
* **Algoritmo de Dijkstra:** Calcula las rutas más cortas desde un único origen en grafos con pesos no negativos.
* **Algoritmo de Johnson:** Diseñado para hallar los caminos más cortos entre todos los pares de nodos, incluso en presencia de pesos negativos, mediante una técnica de re-pesado que utiliza el algoritmo de Bellman-Ford.

## 📊 Herramientas de Visualización

El proyecto utiliza `NetworkX` y `Matplotlib` para generar una salida visual detallada en cada paso del algoritmo:

* **Representación Gráfica:** Dibujo dinámico del grafo donde los colores de los nodos y el estilo de las aristas reflejan el estado actual (nodos visitados, aristas del árbol, etc.).
* **Tablas de Estado:** Generación de tablas que muestran en tiempo real los valores de distancia, predecesores y tiempos de ejecución.
* **Matrices de Resultados:** Visualización clara de las matrices de distancias mínimas y predecesores al finalizar algoritmos de todos los pares como el de Johnson.

## 🛠️ Requisitos

Para ejecutar el código, es necesario tener instalado Python y las siguientes librerías:

```bash
pip install networkx matplotlib
