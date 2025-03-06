Enunciado: vas a inventar un ejemplo, diferente a los de la unidad, en lenguaje de alto nivel con su equivalente en lenguaje ensamblador para cada uno de los siguientes conceptos:

#### Condicionales:
Un ejemplo facil podria ser, si el numero ingresado es mayor a 0 el codigo nos dara como respuesta un 1 
Ejemplo en C#
```C#
using System;
class Program
{
    static void Main()
    {
        // Solicitar al usuario que ingrese un número
        Console.Write("Ingresa un número: ");
        int numero = int.Parse(Console.ReadLine());

        // Condicional para verificar si el número es mayor a 0
        if (numero > 0)
        {
            Console.WriteLine("1");
        }
    }
}
```
Ahora en ensamblador 
```asm
@5 
D=A 
@16 
M=D 
@8 
D;JGT 
@14 
0;JMP 
@1 
D=A
```

#### Ciclos while
Un ciclo while podria ser si un int que empieza en 1 llega hasta 15 con ayuda de un sum la cual ira sumando la cifra consigo misma
Ejemplo en C#

```C#
using System;

class Program
{
    static void Main()
    {
        int i = 1;
        int sum = 0;

        while (i <= 15)
        {
            sum += i;  
            i++;       
        }


    }
}

```
Ahora en ensamblador 
```asm
// Adds1+...+100.
 @i 
 M=1 
 @sum 
 M=0 
 (LOOP)
 @i
 D=M 
 @15
 D=D-A 
 @END
 D;JGT 
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
#### Ciclos for
Un ciclo for puede ser parecido al ejemplo del ciclo while, donde se tiene como limite el numero 15.
Ejemplo en C#
```C#
using System;

class Program
{
    static void Main()
    {
        int sum = 0;

        // Ciclo for que se ejecuta desde i = 1 hasta i = 15
        for (int i = 1; i <= 15; i++)
        {
            sum += i;  // Sumar el valor de i a sum
        }
    }
}
```
Ahora en ensamblador 
```asm
@sum
M=0
@i
M=1
(LOOP)
@i
D=M
@15
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
#### Escritura de variables por medio de punteros
Para esto se cambiara una variable con un valor de 15 por una de valor 25

Ejemplo en C#
```C#
using System;
class Program
{
    static unsafe void Main()
    {

        int number = 15;
    
        int* pointer = &number;


        *pointer = 25;

    }
}
```
Ahora en ensamblador 
```asm
@a
@25
D=A
@16
M=D

@b
@15
D=A
@17
M=D

@a
D=M
@p
M=D

@b
M=D
```

#### Lectura de variables por medio de punteros
En este caso se cambiara el valor de 'b' que es 20 a 30 por medio de 'a'
Ejemplo en C#
```C#
using System;

class Program
{
    static unsafe void Main()
    {
       
        int a = 30;
        int b = 20;

        int* p;

        p = &a;

  
        b = *p; 

    }
}
```
Ahora en ensamblador 
```asm
@a
@20
D=A
@16
M=D
@b
@30
D=A
@17
M=D
A=D
@p
M=D
@a
M=D
```
#### Manipulación de un arreglo por medio de punteros.
En este caso se creara un arreglo de 1 a 10 , donde un puntero cambiara el numero 2 dentro del arreglo por un 3 
Ejemplo en C#
```C#
using System;

class Program
{
    static unsafe void Main()
    {
        // Inicialización del arreglo
        int[] arr = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};

        // Mostrar el arreglo original
        Console.WriteLine("Arreglo original:");
        foreach (var item in arr)
        {
            Console.Write(item + " ");
        }
        Console.WriteLine();

        // Bloquear el arreglo en memoria y usar un puntero
        fixed (int* p = arr)
        {
            // Cambiar el valor de arr[1] (que es 2) a 3
            p[1] = 3;
        }

        // Mostrar el arreglo después de la modificación
        Console.WriteLine("Arreglo después de cambiar el valor de arr[1] a 3:");
        foreach (var item in arr)
        {
            Console.Write(item + " ");
        }
    }
}

```
Ahora en ensamblador 
```asm

```
#### Llamado a funciones con parámetros.

#### Llamado a funciones con retorno de parámetros (no lo trabajamos en la unidad pero tienes las herramientas para proponer un ejemplo)
NO OLVIDES SIMULAR CADA EJEMPLO en lenguaje ensamblador para asegurar que está correcto


Entrega: el programa en alto nivel y su equivalente en ensamblador.
