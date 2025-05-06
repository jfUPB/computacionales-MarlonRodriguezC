```asm
@SCREEN
M=-1
D=A
@7
M=D

(INFINITE_LOOP)
@KBD
D=M
@132
D=D-A
@mover_derecha
D;JEQ
//Verificar si me debo mover a la izquierda
@KBD
D=M
@130
D=D-A
@mover_izquierda
D;JEQ
@INFINITE_LOOP 
0;JMP 

(mover_derecha)
@7
A=M
M=0    
A=A+1
M=-1         // Dibuja el nuevo píxel
D=A
@7
M=D
@INFINITE_LOOP
0;JMP

(mover_izquierda)
@7
A=M
M=0    
A=A-1
M=-1         // Dibuja el nuevo píxel
D=A
@7
M=D
@INFINITE_LOOP
0;JMP
```

[Link al video](https://youtu.be/mCLeXBBD_pY)
