```C#
using System;

class Program
{
    static void Main()
    {
        const int SCREEN_SIZE = (512 * 256) / 16; // Tamaño del arreglo SCREEN
        ushort[] SCREEN = new ushort[SCREEN_SIZE]; // Simula la memoria de la pantalla
        ushort KBD = 0; // Simula el teclado

        while (true)
        {
            Console.Write("Presiona una tecla o Enter para no haceer  nada: ");
            ConsoleKeyInfo input = Console.ReadKey();
            Console.WriteLine();


            if (input.Key == ConsoleKey.Enter)
            {
                KBD = 0; // esto borra 
            }
            else
            {
                KBD = 1; // esto crea
            }

            if (KBD != 0)
            {
                SCREEN[0] = 0xFFFF; 
            }
            else
            {
                SCREEN[0] = 0x0000; 
            }

            Console.WriteLine($"SCREEN[0] = {SCREEN[0]:X4}");
        }
    }
}
```
