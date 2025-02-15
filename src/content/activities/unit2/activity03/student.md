#### Convierte un ciclo while en un ciclo for

**Enunciado**: considera el siguiente programa: 

``` c
//Adds 1+...+100.
 int i=1;
 int sum=0;
 
 while(i <=100){
    sum+= i;
    i++;
 }
 ```

 Vamos a transformar este programa a su equivalente usando un ciclo for:

 ``` c
//Adds 1+...+100.
int sum=0;
for(int i = 1; i <=100; i++){
    sum+= i;
}
 ```

Ambos son equivlaentes porque ambos toman la variable 'i' y esta va ir subiendo su valor dede 1 hasta 100 con ayuda del int 'sum' el cual hara
que se sume automaticamente con sigo mismo, cuando llegue a su valor 100 el codigo parara

- Convierte la versión del for a ensamblador.
- No olvides comprobar el funcionamiento de los programas en ensamblador en el simulador.
- Compara las versiones en ensamblador del while y del for. ¿Qué puedes concluir?

**Entrega**: la solución a las cuestiones planteadas en el enunciado.
