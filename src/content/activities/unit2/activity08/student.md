#### Analisis y funcionamiento del programa
El codigo crea una linea que negra que pinta la pantalla a medida que el usuario tiene alguna tecla presionada, si este deja de presionarla, la linea comenzara a desaparecer y
retroceder hasta llegar a su inicio

Para empezar el codigo inicia con el codigo 16384 el cual es el codigo usado como @SCREEN para usar la pantalla y este numero es guardado en la poscion 16 de la ram, despues de esto
desde la direccion 4 hasta la direccion 13 de la rom entra en un modo donde el comando @24576 dectecta si  ninguna tecla se esta tocando y se mantiene en bucle hasta que
alguna tecla sea tocada (ojo, que si es presionada alguna tecla y despues no se interactua el codigo ahora se ejecutara de la linea 4 a las 18 y empezara a borrar  el tramo la linea ya creada con anterioridad y volvera  ejecutando el comando AM=M-1 donde tanto como A para M se le restara 1) 
 
Si se presiona alguna telca este saltara de la direccion 7 hasta la 19 y desde la 19 hasta la 32 se encargara de verificar si la tecla esta siendo presionada y se pintara la linea con el codigo M=-1
