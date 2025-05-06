Dentro del ciclo de vida en stack después que termina su respectivo bloque este termina su tiempo de vida automáticamente, encambio en el caso de un objeto echo con Heap se mantendrá dentro de la memoria hasta que el programador la libere con delete

No compila ya que tiene un erro en la en la linea 47, 'pBloque2': identificador no declarado
, esto se debe ya que cuando se crea el new punto con ayuda del puntero, este se inicializa dentro del bloque por tanto este no se puede acceder, ni borrar.

Para poder hacer esto se podría dejar el puntero antes del bloque primero me guie de la  este ejemplo que encontré en Google 
``` cpp
 MiClase* puntero_objeto = nullptr;

    // 2. Asignar memoria para el objeto usando 'new'
    puntero_objeto = new MiClase(10);

    // 3. Acceder al objeto y utilizarlo a través del puntero
    if (puntero_objeto != nullptr) {
        std::cout << "Valor del objeto: " << puntero_objeto->getValor() << std::endl;  // Usando el operador ->
        std::cout << "Valor del objeto: " << (*puntero_objeto).getValor() << std::endl; // Usando el operador * y .

        // 4. Liberar la memoria asignada con 'delete'
        delete puntero_objeto;
        puntero_objeto = nullptr; // Se recomienda asignar a nullptr para evitar errores futuros
    }
``` 
Y cree dos líneas de código fuera del bloque 
Punto* pBloque2 = nullptr;
pBloque2 =  new Punto(500, 600);

Pero aun asi esta tenia que inicializarse dentro del bloque asi que meti  el código pBloque2 =  new Punto(500, 600); dentro del código 


#### ¿Por qué el objeto pBloque se destruye al salir del bloque y pBloque2 no? Recuerda de nuevo, pBloque2 es un objeto o es una referencia a un objeto? ¿En qué parte de la memoria se almacena pBloque2? ¿En qué parte de la memoria se almacena el objeto al que apunta pBloque2?

Porque el pBloque2 es una referencia a un  objeto dinamico ( el cual solo se puede borrar de manera manual) y aunque el pBloque2 esta apuntando (con ayuda del puntero jaja) a un objeto dinamico, este igual pertenece a la memoria stack como pBloque 


