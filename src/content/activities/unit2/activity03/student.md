
**Solucion**: 
```asm
@sum
M=0         
@i
M=1         
(LOOP)
@i
D=M
@100       
D=D-A
@END
D;JGE      
@i
D=M
@sum
M=D+M
@i
M=M+1       
@LOOP
0;JMP      
(END)
@END
0;JMP      

 ```
El ciclo for tanto en ensamblador como en C++ toman la misma cantidad en el ciclo sum  
