
# Proyecto-Final---GitHub-Algorithms-Portfolio
Este portfolio contiene ejemplos de programación orientada a objetos, búsqueda lineal, búsqueda binaria, bubble sort, y quick sort.

Diego Roldán  
James Lynn  
John Coto  
Yeidegelis Lopez  
Diego Perez  
Universidad Sagrado Corazón  
CCO 140/001  
7 de mayo de 2026


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


 **Ejemplos pasos y resultados de algoritmos.**

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
| **Final** | **11, 12, 22, 25, 34, 64, 90** |  Ordenado ascendente |

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
| **Final** | **11, 12, 22, 25, 34, 64, 90** |  Toda la lista ordenada |

## Merge Sort
Divide y conquista: parte en mitades y fusiona ordenadamente.

| Paso | División/Fusión | Explicación |
|------|-----------------|-------------|
| **Inicial** | [12, 64, 22, 18, 34, 11, 90, 25] | Arreglo original |
| **Divide** | [12, 64, 22, 18]  [34, 11, 90, 25] | Divide en mitades ≈ iguales |
| **Sigue Dividiendo** |  [12] [64] [22] [18] [34] [11] [90] [25]  | Continúa dividiendo hasta tener un elemento en cada arreglo |
| **Fusiona** | [12, 64] [18, 22] [11, 34] [25, 90] | Subarreglos de 2 elementos ordenados |
| **Sigue Fusionando** | **[12, 18, 22, 64]** │ **[11, 25, 34, 90]** | Fusiona pares ordenados |
| **Final** | **11, 12, 18, 22, 25, 34, 64, 90** |  Fusión final completa |

## Quick Sort
##  Tabla de pasos
 
Arreglo de ejemplo: `[8, 3, 1, 7, 5, 2, 9, 4]`
 
### Partición principal — Pivote = 4, rango [0, 7]
 
| Paso | Tipo     | j  | arr[j] | ¿arr[j] ≤ pivote? | Acción               | Estado del arreglo            |
|:----:|:--------:|:--:|:------:|:-----------------:|----------------------|-------------------------------|
| 1    |  Pivote | —  | 4      | —                 | Pivote = arr[7] = 4  | `[8, 3, 1, 7, 5, 2, 9, 4]`  |
| 2    | Comparar | 0 | 8    |  No cambia (8 > 4)     | Sin swap, continuar  | `[8, 3, 1, 7, 5, 2, 9, 4]`  |
| 3    |  Comparar | 1 | 3    |  Sí cambia  (3 ≤ 4)     | i=0, swap(0,1)       | `[3, 8, 1, 7, 5, 2, 9, 4]`  |
| 4    |  Swap   | 2  | 1      |  Sí cambia (1 ≤ 4)     | i=1, swap(1,2)       | `[3, 1, 8, 7, 5, 2, 9, 4]`  |
| 5    |  Comparar | 3 | 7    |  No cambia  (7 > 4)     | Sin swap, continuar  | `[3, 1, 8, 7, 5, 2, 9, 4]`  |
| 6    |  Comparar | 4 | 5    |  No cambia (5 > 4)     | Sin swap, continuar  | `[3, 1, 8, 7, 5, 2, 9, 4]`  |
| 7    |  Swap   | 5  | 2      |  Sí cambia  (2 ≤ 4)     | i=2, swap(2,5)       | `[3, 1, 2, 7, 5, 8, 9, 4]`  |
| 8    | Comparar | 6 | 9    |  No cambia (9 > 4)     | Sin swap, continuar  | `[3, 1, 2, 7, 5, 8, 9, 4]`  |
| 9    |  Colocado | — | 4   | —                 | Pivote → índice 3    | `[3, 1, 2, `**`4`**`, 5, 8, 9, 7]` |
 
>  El **4** quedó en su posición definitiva (índice 3). Nunca más se moverá.
 
---
 
### Recursión izquierda — Pivote = 2, rango [0, 2]
 
| Paso | Tipo       | j  | arr[j] | ¿arr[j] ≤ pivote? | Acción            | Estado            |
|:----:|:----------:|:--:|:------:|:-----------------:|-------------------|-------------------|
| 10   |  Pivote  | —  | 2      | —                 | Pivote = arr[2]=2 | `[3, 1, 2, ...]`  |
| 11   |  Comparar | 0 | 3     |  No cambia  (3 > 2)  | Sin swap          | `[3, 1, 2, ...]`  |
| 12   |  Swap    | 1  | 1      |  Sí cambia  (1 ≤ 2)  | i=0, swap(0,1)    | `[1, 3, 2, ...]`  |
| 13   |  Colocado | — | 2     | —                 | Pivote → índice 1 | `[1, 2, 3, ...]`  |
| 14   |  Fin     | —  | 1      | —                 | 1 sólo elemento   | `[1, ...]` ✓      |
| 15   |  Fin     | —  | 3      | —                 | 1 sólo elemento   | `[..., 3, ...]` ✓ |
 
---
 
### Recursión derecha — Pivote = 7, rango [4, 7]
 
| Paso | Tipo       | j  | arr[j] | ¿arr[j] ≤ pivote? | Acción            | Estado                        |
|:----:|:----------:|:--:|:------:|:-----------------:|-------------------|-------------------------------|
| 16   |  Pivote  | —  | 7      | —                 | Pivote = arr[7]=7 | `[..., 5, 8, 9, 7]`           |
| 17   |  Comparar | 4 | 5     |  Sí cambia  (5 ≤ 7) | i=4, sin swap     | `[..., 5, 8, 9, 7]`           |
| 18   |  Comparar | 5 | 8     |  No cambia (8 > 7)  | Sin swap          | `[..., 5, 8, 9, 7]`           |
| 19   |  Comparar | 6 | 9     |  No cambia  (9 > 7) | Sin swap          | `[..., 5, 8, 9, 7]`           |
| 20   |  Colocado | — | 7     | —                 | Pivote → índice 5 | `[..., 5, 7, 9, 8]`           |
| 21   |  Fin     | —  | 5      | —                 | 1 sólo elemento   | `[..., 5, ...]` ✓             |
 
---
 
### Recursión final — Pivote = 8, rango [6, 7]
 
| Paso | Tipo       | j  | arr[j] | ¿arr[j] ≤ pivote? | Acción            | Estado                  |
|:----:|:----------:|:--:|:------:|:-----------------:|-------------------|-------------------------|
| 22   | Pivote  | —  | 8      | —                 | Pivote = arr[7]=8 | `[..., 9, 8]`           |
| 23   |  Comparar | 6 | 9     |  No cambia  (9 > 8)  | Sin swap          | `[..., 9, 8]`           |
| 24   |  Colocado | — | 8     | —                 | Pivote → índice 6 | `[..., 8, 9]`           |
| 25   | Fin     | —  | 9      | —                 | 1 sólo elemento   | `[..., 9]` ✓            |
 
---
 
### Resultado final
 
```
[8, 3, 1, 7, 5, 2, 9, 4]
         ↓  25 pasos para sacar el resultado correctamente. 
[1, 2, 3, 4, 5, 7, 8, 9] ✓
```
 
| Elemento | 1 | 2 | 3 | 4 | 5 | 7 | 8 | 9 |
|:--------:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Índice   | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
 
---


