# Proyecto-Final---GitHub-Algorithms-Portfolio
Este portfolio contiene ejemplos de programación orientada a objetos, búsqueda lineal, búsqueda binaria, bubble sort, y quick sort.


**OOP (Object Oriented Programming)**

Este programa crea dos tipos de variables complejas, siendo rectángulo y círculo. Un tipo de variable simple, como el int, solo contiene un valor. Los rectángulos y círculos contienen más valores, como su perímetro/circunferencia, area, radio/base y altura.


**Linear y Binary Search**

Son métodos de búsqueda, le indicas el dato en un arreglo que deseas buscar, y te devuelven el índice de ese dato. Linear Search busca de manera simple, ya que revisa cada índice de inicio a fin. Al ser tan simple, se tarda mucho en arreglos grandes, o si el dato se encuentra al final. Binary Search solo se puede utilizar si el arreglo está ordenado. Elimina la mitad del arreglo an cada paso, por lo que es más eficiente que Linear Search.

**Linear Search (Búsqueda Lineal)**

Recorre el arreglo elemento por elemento.
Empieza desde el inicio hasta encontrar el valor.
No necesita que el arreglo esté ordenado.

Ejemplo de cómo funciona:

Si buscas 7 en [3, 9, 4, 1, 7]
→ compara 3, luego 9, luego 4, luego 1… hasta encontrar 7.

**Binary Search (Búsqueda Binaria)**

Divide el arreglo en mitades cada vez.
Solo funciona si el arreglo está ordenado.
Compara con el elemento del medio para decidir si ir a la izquierda o derecha.

Ejemplo:

Buscar 7 en [1, 3, 4, 7, 9]
→ mira el medio (4)
→ como 7 es mayor, va a la derecha
→ encuentra 7 rápidamente.




**Bubble Sort, Insertion Sort, Merge Sort & Quick Sort**

Son métodos que ordenan arreglos, ponen los términos en orden de menor a mayor. 

1. Bubble sort: Es el más simple, compara dos valores adyacentes, si el izquierdo es mayor al derecho, intercambia sus índices; si no, no hace nada y se mueve al siguente valor. Continua hasta ordenar el arreglo.  

3. Insertion Sort: Elige un "key", empezando desde el segundo índice. Si el término a la izquerda del key es mayor, lo mueve hacia la izquierda, sino, deja el key en su sitio. De esta manera, el key tendrá un término menor a su izquierda y un término mayor a su derecha. Cuando ocurre esto, elige un nuevo key. El nuevo key que elige es el que estaba a la derecha del key anterior antes de que ocurrieran intercambios.

4. Merge sort: Divide el arreglo en mitades hasta que los arreglos sean de un solo término. Luego los une, creando arreglos temporeros en donde pone dos mitades en orden. Repite esto hasta reconstruir el arreglo original en forma ordenada.

5. Quick sort: Es un algoritmo de ordenamiento basado en divide y vencerás que elige un elemento llamado pivote y reorganiza los elementos del arreglo de modo que todos los menores al pivote queden a su izquierda y los mayores a su derecha; luego repite el proceso en las dos partes resultantes. 


| Algoritmo     | Simplicidad | Rapidez             | Necesita memoria extra? |
|---------------|-------------|---------------------|-------------------------|
| Bubble Sort   | 10/10       | 2/10                | No                      |
| Insertion Sort| 9/10        | 4/10                | No                      |
| Merge Sort    | 6/10        | 8/10                | Sí                      |
| Quick Sort    | 5/10        | 8/10                | Usualmente no           | 


Ejemplos pasos y resultados de algoritmos. 

## Bubble Sort
Compara elementos adyacentes e intercambia si están desordenados.

| Paso | Arreglo | Explicación |
|------|---------|-------------|
| **Inicial** | 64, 34, 25, 12, 22, 11, 90 | Arreglo original desordenado |
| **Pasada 1** | 34, 25, 12, 22, 11, **64, 90** | Compara todos los pares, 90 y 64 "burbujean" al final |
| **Pasada 2** | 25, 12, 22, 11, **34, 64, 90** | 34 burbujea hasta su posición, últimos 2 ya ordenados |
| **Pasada 3** | 12, 22, 11, **25, 34, 64, 90** | 25 se posiciona correctamente, últimos 3 ordenados |
| **Pasada 4** | 12, 11, **22, 25, 34, 64, 90** | 22 se posiciona, últimos 4 ordenados |
| **Pasada 5** | **11, 12, 22, 25, 34, 64, 90** | 11 se posiciona, arreglo completamente ordenado |
| **Final** | **11, 12, 22, 25, 34, 64, 90** | ✅ Ordenado ascendente |

## Insertion Sort
Construye la lista ordenada insertando elementos uno por uno.

| Paso | Arreglo | Explicación |
|------|---------|-------------|
| **Inicial** | **64**, 34, 25, 12, 22, 11, 90 | 64 es la primera parte ordenada |
| **+34** | **34, 64**, 25, 12, 22, 11, 90 | 34 se inserta antes de 64 |
| **+25** | **25, 34, 64**, 12, 22, 11, 90 | 25 se inserta en posición correcta |
| **+12** | **12, 25, 34, 64**, 22, 11, 90 | 12 se inserta al inicio |
| **+22** | **12, 22, 25, 34, 64**, 11, 90 | 22 se inserta entre 12 y 25 |
| **+11** | **11, 12, 22, 25, 34, 64**, 90 | 11 se inserta al inicio |
| **Final** | **11, 12, 22, 25, 34, 64, 90** | ✅ Toda la lista ordenada |

## Merge Sort
Divide y conquista: parte en mitades y fusiona ordenadamente.

| Paso | División/Fusión | Explicación |
|------|-----------------|-------------|
| **Inicial** | [1][2] | Arreglo original |
| **Divide 1** | [1] │ [2] | Divide en mitades ≈ iguales |
| **Divide 2** |  │ [1] │ [2] │  | Continúa dividiendo recursivamente |
| **Orden base** |  │ **[1]** │ **[2]** │ **** | Subarreglos de 2 elementos ordenados |
| **Fusiona 1** | **[1]** │ **[2]** | Fusiona pares ordenados |
| **Final** | **11, 12, 22, 25, 34, 64, 90** | ✅ Fusión final completa |

## Quick Sort
Elige pivote, particiona y recursiona en subarreglos.

| Paso | Subarreglo | Pivote | Explicación |
|------|------------|--------|-------------|
| **Inicial** | [64, 34, 25, 12, 22, 11, **90**] | 90 | Pivote final, todos <90 van a izquierda |
| **Partición** | **[2][1]** │ **90** | Elementos reorganizados por pivote |
| **Izquierda** | [11,12,22,25,34, **64**] | 64 | Nuevo pivote 64 en subarreglo izquierdo |
| **Partición** | **[2][1]** │ **64** | Todos <64 a izquierda |
| **Izquierda** | [11,12,22,25, **34**] | 34 | Pivote 34, subarreglo ya casi ordenado |
| **Final** | **11, 12, 22, 25, 34, 64, 90** | - | ✅ Completamente ordenado |



