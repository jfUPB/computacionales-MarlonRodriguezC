+-------------------------------+
|       Segmento de código      |
|   (instrucciones, funciones)  |
+-------------------------------+
| Variables globales y estáticas|
+-------------------------------+
|           Heap                | <--- Asignación dinámica (new/malloc)
|                               |
|                               |
+-------------------------------+
|           Stack               | <--- Variables locales
+-------------------------------+


+-------------------------------+
| main, suma, funcionConStatic()|
|      crearArrayHeap()         |
+-------------------------------+
| 'global_inicializada': 00007FF77989F000, 
|'global_no_inicializada': 00007FF77989F4C0
+-------------------------------+
|           Heap                | <--- Asignación dinámica (new/malloc)
|                               |
|                               |
+-------------------------------+
|variable local 'a': 000000B2AA3EF934| <--- Variables locales
|variable local 'b': 000000B2AA3EF954|
|variable local 'c' (resultado): 000000B2AA3EF974| 
+-------------------------------+
