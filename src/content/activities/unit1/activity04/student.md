##### A-Instructions C-Instrucions
1. La A-Instructions conlleva una sintaix de tipo "@valor", el cual dentro de su registro se tendra un numero
positivo el cual luego C-Instructions manipulara y hara las operaciones y le dira al computador donde se debe almacenar el valor computado,

2. A-instructions se representa como: 0 vvv vvvv vvvv vvvv, y la 'v' es la  que representa los bits dentro del valor por ejemplo para establecer cifras como el numero 5 se tomaria de la sigueinte forma: 0000000000000101
Si aumentamos este numero, la cifra binaria cambiaria aumentando los ceros y unos:  0000000000110010

Si fuese un numero mas elevado como 100 la cifra cambiaria a 0000000001100100



Y las C-instructions se representa como: 111a cccc ccdd djjj , en esta la  'a' y la 'c' son las cuales especifican la operacion ALU,'d' es el destino del resultado y 'j' la condicion de salto.

Por ejemplo si se hace la operacion D=M+1, en binario seria: 1111110111010000 (si fuese M-1 la 'c' cambiarai a   1 1 0 0 1 0).
Si es un salto como JMP seria: 1110101010000111
O un salto solo si el resultado es mayor a cero comoJGT seria; 1110001100000001


 

