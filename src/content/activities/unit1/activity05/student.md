documenta cada ciclo Fetch-Decode-Execute. Para cada instrucción:

¿Qué valor tiene el PC al inicio del ciclo?
¿Qué instrucción se busca en la memoria?
¿Cómo se decodifica la instrucción?
¿Qué operación se realiza en la fase Execute? ¿Cómo cambian los valores de los registros A, D y M (memoria)?
Entrega: una tabla que documente el ciclo Fetch-Decode-Execute para cada instrucción del programa elegido.

Para la siguiente actividad se utilizara el siguiente codigo ya visto en clase:

```asm
@1 
D=A 
@2 
D=D+A 
@16 
M=D 
@6 
0;JMP
```
1.Por defecto el PC siempre iniciara en 0, apenas siga el comando @1, PC ya tendra el valor de 1 
2.Siempre buscara la instruccion por el orden establecido en la ROM, iniciara en la linea 0 (donde se ubica @1) y luego de completar esta orden seguira con la linea 1 y 2 y 3 y asi hasta que acabe.

3. la instruccion se decodifica con ayuda de dos instrucciones A-Instruction y C-Instruction, 'A' da la direccion y 'C' la calcula, apenas 'c' termina su tarea, 'A' vuelve a direccionar y el proceso se repite
   
4.Los valores A, D y M suelen cambiar segun la orden recibida pero en este caso se puede ver como se iguala el valor de D con A al usar "D=A"


COMP-un1-ac5.png

