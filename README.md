# Proyecto-Final---GitHub-Algorithms-Portfolio
Este portfolio contiene ejemplos de programación orientada a objetos, búsqueda lineal, búsqueda binaria, bubble sort, y quick sort.


**OOP (Object Oriented Programming)**

Este programa crea dos tipos de variables complejas, siendo rectángulo y círculo. Un tipo de variable simple, como el int, solo contiene un valor. Los rectángulos y círculos contienen más valores, como su perímetro/circunferencia, area, radio/base y altura.


**Linear y Binary Search**

Son métodos de búsqueda, le indicas el dato en un arreglo que deseas buscar, y te devuelven el índice de ese dato. Linear Search busca de manera simple, ya que revisa cada índice de inicio a fin. Al ser tan simple, se tarda mucho en arreglos grandes, o si el dato se encuentra al final. Binary Search solo se puede utilizar si el arreglo está ordenado. Elimina la mitad del arreglo an cada paso, por lo que es más eficiente que Linear Search.


**Bubble Sort, Insertion Sort, Merge Sort & Quick Sort**

Son métodos que ordenan arreglos, ponen los términos en orden de menor a mayor. 

1. Bubble sort: Es el más simple, compara dos valores adyacentes, si el izquierdo es mayor al derecho, intercambia sus índices; si no, no hace nada y se mueve al siguente valor. Continua hasta ordenar el arreglo. 

2. Insertion Sort: Elige un "key", empezando desde el segundo índice. Si el término a la izquerda del key es mayor, lo mueve hacia la izquierda, sino, deja el key en su sitio. De esta manera, el key tendrá un término menor a su izquierda y un término mayor a su derecha. Cuando ocurre esto, elige un nuevo key. El nuevo key que elige es el que estaba a la derecha del key anterior antes de que ocurrieran intercambios.

3. Merge sort: Divide el arreglo en mitades hasta que los arreglos sean de un solo término. Luego los une, creando arreglos temporeros en donde pone dos mitades en orden. Repite esto hasta reconstruir el arreglo original en forma ordenada.

4. Quick sort: 

| Algoritmo     | Simplicidad | Rapidez             | Necesita memoria extra? |
|---------------|-------------|---------------------|-------------------------|
| Bubble Sort   | 10/10       | 2/10                | No                      |
| Insertion Sort| 9/10        | 4/10                | No                      |
| Merge Sort    | 6/10        | 8/10                | Sí                      |
| Quick Sort    | 5/10        | 8/10                | Usualmente no           | 
