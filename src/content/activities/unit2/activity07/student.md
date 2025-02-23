```asm
@sum
M=0          

@i
M=1         

@0     // Dirección inicial 
D=A
@inicio
M=D

(LOOP)
@i
D=M
@11    // Comparador jasdfjajfa
D=D-A
@END
D;JGE    // Si es mayor esto sale del bucle

@i
D=M        
@sum
M=D+M   // sum es el que tendra que dar si o si 55

@inicio
A=M        //guarda los valores
M=D       

@i
M=M+1   //le sube un numero al dato a guardar

@inicio
M=M+1      //le sube un numero a la direccion a guardar

 

@LOOP
0;JMP      

(END)
@END
0;JMP   
```
