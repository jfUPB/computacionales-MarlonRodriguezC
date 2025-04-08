Copia de objetos y su ubicación en memoria
Enunciado: implementa un experimento para observar lo que ocurre al copiar un objeto. Ejecuta el programa y observa el comportamiento en el depurador para que puedas concluir.

Modifica la clase Punto:

#include <iostream>
#include <string>
using namespace std;

class Punto {
public:
	string name;
    int x;
    int y;

    // Constructor
    Punto(string _name, int _x, int _y) : name(_name),x(_x), y(_y) {
        cout << "Constructor: Punto "<< name <<" (" << x << ", " << y << ") creado." << endl;
    }

    // Destructor
    ~Punto() {
        cout << "Destructor: Punto " << name << "(" << x << ", " << y << ") destruido." << endl;
    }

    // Método para imprimir valores
    void imprimir() {
        cout << "Punto "<< name << "(" << x << ", " << y << ")" << endl;
    }
};


int main() {
    // Objeto original
    Punto original("original",70, 80);
    original.imprimir();
	Punto* p = &original;

    // Copia del objeto
    Punto copia = original;
	copia.name = "copia";
	copia.x = 100;
	copia.y = 200;
    copia.imprimir();
    original.imprimir();
    
	p->name = "p";
	p->x = 300;
	p->y = 400;
	p->imprimir();
	original.imprimir();
    return 0;
}
Compara con C# (puedes crear un nuevo proyecto de consola C# en una nueva ventana de Visual Studio):

using System;

public class Punto
{
    public int x;
    public int y;
    public string name;

    // Constructor
    public Punto(string _name, int _x, int _y)
    {
        name = _name;
        x = _x;
        y = _y;
        Console.WriteLine($"Constructor: Punto {name}({x}, {y}) creado.");
    }

    // Método para imprimir valores
    public void Imprimir()
    {
        Console.WriteLine($"Punto {name}({x}, {y})");
    }
}

class Program
{
    static void Main(string[] args)
    {
        // Objeto original
        Punto original = new Punto("original",70, 80);
        original.Imprimir();

        Punto copia = original;
        copia.name = "copia";
        copia.x = 100;
        copia.y = 200;
        copia.Imprimir();
        original.Imprimir();

        // Coloca breakpoints en la creación de 'original' y en la línea de la copia.
        // Observa que 'copia' es una copia independiente de 'original'.
    }
}
Ejecuta los programas en modo depuración y detente en los breakpoints para comparar. Experimenta libremente.

Entrega:

Explica qué ocurre al copiar un objeto en C++ y en C#. ¿Qué diferencias encuentras?
Se puede ver como en C++ al copiar un objeto y hacer modificaciones, estas modificacionesnno afectan a la original, estas llegan a tener cambios cuando se hace uso 
de punteros, pero en C# las modificaciones afectan tanto el objeto original como a la copia

¿Qué es copia en C++ y en C#? ¿Es una copia independiente de original?

La diferencia entre C++ y en C# es en el codigo del experimento de C# no se hace del todo una copia, aunque si recibe al nombre de "copia" las variables mostradas como "name", "x", "y" son apuntadas al mismo sitio que el punto original esta apuntando, esto ocurre porque por defecto las clases de C# se gestionan por referencia 

