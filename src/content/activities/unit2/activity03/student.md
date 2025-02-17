
**Solucion**: 
``` c
 @sum // sum refers to some memory location.
 M=0 // sum=0
 (LOOP)
 int i=1;
 int sum=0;
 @i
 D=M // D=i
 @100
 D=D-A // D=i-100
 @i
 M=M+1 // i=i+1
 @END
 D;JGT // If(i-100)>0 gotoEND
 @i
 D=M // D=i
 @sum
 M=D+M // sum=sum+i
 @LOOP
 0;JMP // GotoLOOP
 (END)
 @END
 ```
El ciclo for tanto en ensamblador como en 
