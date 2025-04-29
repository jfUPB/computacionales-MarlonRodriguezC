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
