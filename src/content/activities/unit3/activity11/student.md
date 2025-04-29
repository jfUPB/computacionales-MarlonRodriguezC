#### ¿Qué puedes concluir de los miembros estáticos y de instancia de una clase en C++? ¿Cómo se gestionan en memoria? ¿Qué ventajas y desventajas tienen? ¿Cuándo es útil utilizarlos?
Una instancia aunque se puede crear como un objeto
y que este tenga datos propios, los datos estaticos pueden 
llevar informacion en comun de diversos objetos de forma global, 
como por ejemplo en este caso seria el contador, este usandolo con
las instancia de valor dentro de c1 c2 y c3

Depende de como se crea, se alamacena en el stack si es de forma
automatica o en el heap si es de forma dinamica como en el caso del contador y cada
nuevo objeto crea una nueva direccion dentro de la memoria     

#### En el programa, en qué segmento de memoria se están almacenando c1, c2, c3 y Contador::total? Ten especial cuidado con la respuesta que das para el caso de c3, piensa de nuevo, qué es c3 y qué está almacenando. Ahora, responde de nuevo, en qué segmento de la memoria se está almacenando c3 y en qué segmento de la memoria se está almacenando el objeto al que apunta c3.
Usando el "Add Watch" mirando el codigo y procedimiento de cada "c"
creado, me di cuenta que esta daba una direccion "c3	0x000002b4437aa820 {valor=16 }	Contador *"
lo cual al verificar el codigo de nuevo esto tendria logica puesto que esta usando un puntero a la 
hora de crear "c3" y  contador(15) es el que esta usando la memoria dinamica (heap)
