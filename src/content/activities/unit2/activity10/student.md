```asm
// esto da el SCREEN
@16384
D=A
@16
M=D

(inicio)
    // Leer el teclado
    @KBD
    D=M
    @inicio
    D;JEQ  

 
    @17
    M=D  

    @pantalla
    0;JMP

(retorno_pantalla)
    @inicio
    0;JMP  // esto es el return

(pantalla)
    @17
    D=M  

    // esto es p 
    @112
    D=D-A
    @PINTAR
    D;JEQ  

    // y esta wea b
    @17
    D=M
    @98
    D=D-A
    @BORRAR
    D;JEQ  

    @retorno_pantalla
    0;JMP

(PINTAR)
    @16
    D=M  
    @16395
    D=A  

(PINTAR_LOOP)
    @16
    A=M
    M=-1  
    @16
    M=M+1 //le aumenta 

    @retorno_pantalla

    0;JMP 

(BORRAR)
    @16
    D=M  
    @16395
    D=A 

(BORRAR_LOOP)
    @16
    A=M
    M=0  // Borra pixel 
    @16
    AM=M-1  //le disminuye

    M=0

    @retorno_pantalla
    0;JMP 
```
