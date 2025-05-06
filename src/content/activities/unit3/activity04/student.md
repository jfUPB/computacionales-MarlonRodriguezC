1. Se intenta utilizar un puntero de tipo void tomando la direccion del main y se guarda en ptr, se muestra la
 direccion del actual puntero ,osea la direccion del main y luego se cambiar el ptr a un int (una variable de tipo entero) el cual
 quiere escribir  0  dentro de la direccion de main pero el programa no lo permitira ya que el main es una funcion creada para que
 pueda ser codificada de forma de solo lectura entonces el usuario aunque pueda verla y usarla no pueda editarla

2. Este  experimento llega a ser mas importante ya que en creacion del mensaje_ro se escribe dos "const" este con el proposito de que la
  primera "const"  hace que el contenido no se pueda modificar y la segunda nos dice que no se le puede cambiar direccion al puntero
  y se le aplica otro puntero "char* ptr ", se muestra la direccion del puntero y luego se intenta cambiar el valor de la direccion del puntero
  a 0 lo cual da un error " segmentation fault."


