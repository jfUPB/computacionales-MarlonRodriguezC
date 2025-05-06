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
@sum
M=0

@i
M=1

@0     // Dirección inicial
D=A
@inicio
M=D

@ptr    // Puntero a la dirección donde se cambiará el 2 por 3
M=0

(LOOP)
@i
D=M
@11    // Comparador hsdfajfa
D=D-A
@END
D;JGE    // Si es mayor esto sale del bucle

@i
D=M
@sum
M=D+M   // sum es el que tendrá que dar 55

@inicio
A=M        // Guarda los valores
M=D

// Verifica si el número almacenado es 2 y lo cambia a 3
@2
D=A
@inicio
A=M
D=M-D
@SKIP
D;JNE  // Si no es 2, salta

@3
D=A
@inicio
A=M
M=D   // Cambia el 2 por 3

(SKIP)
@i
M=M+1   // Incrementa el índice

@inicio
M=M+1   // Incrementa la dirección

@LOOP
0;JMP

(END)
@END
0;JMP

```
#### Llamado a funciones con parámetros.
```C#
using System;

class Program
{
    static void Main()
    {
        Console.Write("Ingrese un número: ");
        int numero = int.Parse(Console.ReadLine());
        
        VerificarEstado(numero);
    }

    static void VerificarEstado(int num)
    {
        if (num > 0)
        {
            CambiarEstado();
        }
        else
        {
            Console.WriteLine("El número no es mayor a 0.");
        }
    }

    static void CambiarEstado()
    {
        Console.WriteLine(2); // Señal de que el número es mayor a 0
    }
}

```

```asm
@INPUT
M=1  // El numero que se debe cambiar para que sea mayor o menor que y nos de el writeline 2

@PROMPT
0;JMP  // Saltamos a la sección donde pedimos el número

(PROMPT)
@INPUT
D=M
@CHECK
D;JMP  // Verificamos la condición

(CHECK)
@INPUT
D=M
@0
D=D-A  // Restamos 0 para verificar si es mayor
@SHOW_TWO
D;JGT  // Si es mayor que 0, saltamos a SHOW_TWO

@END
0;JMP  // Si no es mayor a 0, terminamos el programa

(SHOW_TWO)
@2
D=A
@16
M=D  // Guardamos el número 2 en la dirección 16 de la RAM

(END)
@END
0;JMP  // Loop infinito al final
```


#### Llamado a funciones con retorno de parámetros (no lo trabajamos en la unidad pero tienes las herramientas para proponer un ejemplo)
NO OLVIDES SIMULAR CADA EJEMPLO en lenguaje ensamblador para asegurar que está correcto
En este proyecto se dbee hacer un return sumandole un numero al numero escrito (en este caso en asm es un 5 y tiene que dar 6)
```C#
using System;

class Program
{
    static void Main()
    {
        Console.Write("Ingrese un número: ");
        int numero = int.Parse(Console.ReadLine());

        int resultado = Siguiente(numero);

        Console.WriteLine("El numero que le sigue a ese numero es: " + resultado);
    }

    static int Siguiente(int numero)
    {
        return numero + 1; // Retorna el doble del número
    }
}

```

```asm

@5  
D=A
@10 
M=D

@10  Cargar el numero desde RAM
D=M  
@SUMA
0;JMP 
 // Saltar a la función Suma
@END
0;JMP 

(SUMA)
D=D+1  // D = D + 1
@17  
M=D   // Guardar el resultado en 17

//return
@8
0;JMP

// Fin del programa
(END)



```
Entrega: el programa en alto nivel y su equivalente en ensamblador.
