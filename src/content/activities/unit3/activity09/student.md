
#### Explica qué ocurre al copiar un objeto en C++ y en C#. ¿Qué diferencias encuentras?
Se puede ver como en C++ al copiar un objeto y hacer modificaciones, estas modificacionesnno afectan a la original, estas llegan a tener cambios cuando se hace uso 
de punteros, pero en C# las modificaciones afectan tanto el objeto original como a la copia

#### ¿Qué es copia en C++ y en C#? ¿Es una copia independiente de original?

La diferencia entre C++ y en C# es en el codigo del experimento de C# no se hace del todo una copia, aunque si recibe al nombre de "copia" las variables mostradas como "name", "x", "y" son apuntadas al mismo sitio que el punto original esta apuntando, esto ocurre porque por defecto las clases de C# se gestionan por referencia
