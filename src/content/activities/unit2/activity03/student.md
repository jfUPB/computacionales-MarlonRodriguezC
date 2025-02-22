
**Solucion**: 
``` c
 @sum
 M=0 
 (LOOP)
 int i=1;
 int sum=0;
 @i
 D=M 
 @100
 D=D-A 
 @i
 M=M+1 
 @END
 D;JGT 
 @i
 D=M 
 @sum
 M=D+M 
 @LOOP
 0;JMP 
 (END)
 @END
 ```
El ciclo for tanto en ensamblador como en C++ toman la misma cantidad en el ciclo sum  
