
#### 1. ¿Qué ocurre? ¿Por qué?
Se muestra dentro de un ciclo for las interacciones que hace la variable estatica y no estatica, mientras que la estatica incrementa su numero la
no estatica sigue siendo 100 aun asi que el programa acabe 

#### Ves alguna diferencia entre las variables locales estáticas y no estáticas?

las estaticas aunque no se editaran globalmente ( como en el ejercicio pasado) estas igual al estar estaticamente dentro de la funcion, hacen su 
debido proceso y guardan este progreso, encambio las no estaticas simplemente se reinicia, es utilizada una vez en la funcion para cumplir su trabajo
pero no lo guarda 

#### ¿Qué pasa con las variables cada que entras y sales de la función?
Las estaticas guardan su procedimiento las no estaticas aunque cumplen su funcion, estas no salvaran los datos modificados 


#### 2.¿Qué ocurre? ¿Por qué?
El programa  nos muestra como dentro de un ciclo for con limite de tam (osea 5) este con ayuda de un puntero comienza a mostrarnos una operacion 
matematica de 10 en 10 (sumandole 1 a 'i' y multiplicando 10), donde luego nos muestra la direccion de cada una, despues de esto se hace un delete[] la
cual  hace que los datos dentro de este array ya no se puedan usar (aunque siguen existiendo dentro de la memoria igualmente cosas como las direcciones
ya no son seguras dentro del programa) y despues de esto meustra el arrayHeap[0], que hace que se genere un error ya que el delete hizo que la 
informacion dentro de este array ya no se pueda mostrar


#### ¿Qué diferencias notas entre el comportamiento y la gestión del Heap en comparación con el Stack?

Stack es una forma automatica dentro de las funciones encambio Heap tienes que administrarla como se mostro dentro del ejemplo usando delete o new 

#### ¿Qué consecuencias tendría no liberar la memoria reservada con new?

Puede seguir consumiendo recursos dentro de la memoria y puede hacer que no sea tan eficiente al tener que tener encuenta cosas que ya no necesita

#### ¿Por qué es importante usar delete[] al liberar memoria asignada para un arreglo?

Porque si no la  memoria utilizada en la ram no seria liberada y puede generar fallos dentro del programa
