#### SOLUCION - caso en el  D que es menor que 
```asm
@5 
D=M 
@10 
D=D-A 
@10 
D;JLT 
@7 
M=0 
@13 
0;JMP 
@1 
@7 
M=1 
@0 
0;JMP 
```
#### SOLUCION - caso en el D que es mayor que 

```asm
@12
M=A
D=M 
@10 
D=D-A 
@10 
D;JLT 
@7 
M=0 
@13 
0;JMP 
@1 
@7 
M=1 
@0 
0;JMP 
```

