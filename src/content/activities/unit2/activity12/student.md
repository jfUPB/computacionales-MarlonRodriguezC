Enunciado: vas a inventar un ejemplo, diferente a los de la unidad, en lenguaje de alto nivel con su equivalente en lenguaje ensamblador para cada uno de los siguientes conceptos:

#### Condicionales:
Un ejemplo facil podria ser, si el numero ingresado es mayor a 0 el codigo nos dara como respuesta un 1 
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

#### Ciclos while
Un ciclo while podria ser si un int que empieza en 1 llega hasta 10 con ayuda de un sum la cual ira sumando la cifra consigo misma

#### Ciclos for
Un ciclo for puede ser parecido al ejemplo del ciclo while, donde se tiene como limite el numero 10.

#### Escritura de variables por medio de punteros

#### Lectura de variables por medio de punteros

#### Manipulación de un arreglo por medio de punteros.

#### Llamado a funciones con parámetros.

#### Llamado a funciones con retorno de parámetros (no lo trabajamos en la unidad pero tienes las herramientas para proponer un ejemplo)
NO OLVIDES SIMULAR CADA EJEMPLO en lenguaje ensamblador para asegurar que está correcto


Entrega: el programa en alto nivel y su equivalente en ensamblador.
