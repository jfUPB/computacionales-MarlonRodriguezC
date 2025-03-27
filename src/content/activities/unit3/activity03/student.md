``` bash
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
``` 

``` bash
+----------------------------------------------------------------------+
| main, suma, funcionConStatic()                                       |
|      crearArrayHeap()                                                |
+----------------------------------------------------------------------+
|'global_inicializada': 00007FF75BFDF000                               |
|'global_no_inicializada':00007FF75BFDF4C0                             |
|mensaje_ro	00007FF75BFDBBC0 "Hola, memoria de solo lectura"           |
|var_estatica (static): 00007FF75BFDF004                               |
+----------------------------------------------------------------------+
| arrayHeap[0] = 0 en 000001EA74BE3790                                 |
| arrayHeap[9] = 9 en 000001EA74BE37B4                                 |
+----------------------------------------------------------------------+
|variable local 'a': 000000A68A0FF7A4                                  | <--- Variables locales
|variable local 'b': 000000A68A0FF7C4                                  |
|variable local 'c' (resultado): 000000A68A0FF7E4                      |
+----------------------------------------------------------------------+
``` 
![Resultado del programa](../../../../assets/unidad3.4.jpeg)
