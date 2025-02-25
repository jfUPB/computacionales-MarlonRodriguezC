// crea pantalla
@16384 
D=A 
@15 
M=D 
//no hace nada

@LOOP 
@24576 
D=M 
@CHECK_B 
D;JEQ 

// salta si se toca la tecla    

@16 
D=M 
@16384 
D=D-A 
@4 
D;JLE 
@16 
AM=M-1 
M=0 
@4 
0;JMP

// empieza a pintar 

(CHECK_B) 
@98 // Valor ASCII de 'b'
D=D-A 
@PAINT 
D;JEQ 
@LOOP 
0;JMP

(PAINT) 
@16 
D=M 
@16384 
D=D-A 
@4 
D;JGE 
@16 
A=M 
M=-1 
@16 
M=M+1 
@LOOP 
0;JMP 
