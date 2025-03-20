#### Respuestas
¿Qué es el direccionamiento directo? ¿Cómo se usa en el lenguaje ensamblador Hack?

El direccionamiento directo es el proceso donde se le especifica que el lugar de la memoria que se quiere  acceder, en el computador Hack se usa por orden cronológico cambiando de linea cada que se cumple el 
codigo planteado con @


¿Qué significa M=D en lenguaje ensamblador Hack? ¿Y D=M?

M=D guarda una cifra dentro de la ram, su valor va a depender segun lo que se tenga en D y se guardara en una lista de valores, en esta lista de valores se tomara el valor actual de A y este sera el numero donde se guarde
la cifra de D ya antes hablada. En el caso de D=M, D tomara el numero guardado en la cifra actual de A 

Explica con tus palabras el concepto de "puntero" en el contexto de la memoria y proporciona un ejemplo sencillo en lenguaje ensamblador Hack. (Puedes usar el ejemplo de la página 61 del documento como inspiración, pero adáptalo a un caso más simple).

El termino puntero hace referencia a cuando se almacena una variable en la direccion de otra variable, el puntero puede manipular el sistema de almacenaje para lograr hacer el proceso mas eficiente y facil.

Un ejemplo puede ser el uso del comando @foo el cual si guardamos que es igual a una variable M,

``` asm
@foo
M=10 
```
y se toma el puntero 'ptr'
``` asm
@ptr
M=foo 
```
y ahora foo podra tomar direccionar A o D en la cifra guardada de M
``` asm
@ptr
A=M 
D=M
```
