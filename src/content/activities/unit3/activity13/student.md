#### Código fuente de tu programa.
``` cpp
#include <iostream>
using namespace std;

class Identificacion {
public:
    string nombre;
    int ID;
    static int contador;
    
    // Constructor
    Identificacion(string _nombre, int _ID) : nombre(_nombre), ID(_ID) {
        cout << "Constructor: ID(" << nombre << ", " << ID << ") creado." << endl;
        ID = ++contador;
    }

    // Destructor
    ~Identificacion() {
        cout << "Destructor: ID(" << nombre << ", " << ID << ") destruido." << endl;
    }

    // Método para imprimir valores
    void imprimir() {
        cout << "ID(" << nombre << ", " << ID << ")" << endl;
    }
    static void mostrarTotal() {
        cout << "Total de personas creadas hoy: " << contador << endl;
    }
    

};

void ContadorTrabajadores(int& NumeroTrabajadores)
{
    NumeroTrabajadores = NumeroTrabajadores + Identificacion::contador;
}

int Identificacion::contador = 0;

int main() {
    int NumeroTrabajadores = 10;

    {
        cout << "Bienvenido a la inscripcion de nombre, presione la tecla (enter)  para continuar en cada mensaje" << endl;
        cin.get();
    }
    {

        

        cout << "Esta empresa empezo con (" <<NumeroTrabajadores <<") de trabajadores" << endl;


      
        ContadorTrabajadores(NumeroTrabajadores);


        cout << "Actualmente somos (" << NumeroTrabajadores << ") trabajadores" << endl;
        cin.get();

    }

    {
        cout << "Inicio de la lista" << endl;

        string nombre1;
        int id1;
        cout << "Ingrese el nombre del primer trabajador: ";
        cin >> nombre1;
        cout << "Ingrese el ID del primer trabajador: ";
        cin >> id1;

        Identificacion Lista1(nombre1, id1);

        Identificacion::mostrarTotal();
        Lista1.imprimir();
    }

    Identificacion* Lista2 = nullptr;
    {
        cout << "Inicio de la segunda lista" << endl;

        string nombre2;
        int id2;
        cout << "Ingrese el nombre del segundo trabajador: ";
        cin >> nombre2;
        cout << "Ingrese el ID del segundo trabajador: ";
        cin >> id2;

        Lista2 = new Identificacion(nombre2, id2);

        Lista2->imprimir();
        Identificacion::mostrarTotal();
    }

    ContadorTrabajadores(NumeroTrabajadores);


    cout << "Actualmente somos (" << NumeroTrabajadores << ") trabajadores" << endl;
    cin.get();

    delete Lista2;

    return 0;
}
```
#### Explica cómo aplicaste cada concepto en tu ejemplo.
Para empezar pense en un proyecto simple que tuviese objetos sin tantos atributos (en ) para poder hacer el tema de clases y objetos, un contador para poder hacer una variable estatica y pense en utilizar tambien este para parametro por referencia el cual podria sumarse con este contador,  y obviamente utilizaria un puntero para crear un objeto (los cuales solo crearia dos uno con puntero y otro sin) demostrando como en el ejercicio pasado el objeto puede estar en la memoria heap con el constructor new y el desctructor delete pero el puntero seguiria siendo parte de la memoria stack

Entonces decidi hacer un creador de ID en una empresa que contase los ID que se van creando apartir del uso de memoria stack o de la memory heap

#### Análisis detallado de la memoria. Indica en qué segmento de memoria se está almacenando cada variable y objeto.
Todos estan guardados en el stack (a exceptcion del contador el cual es estatico) y el que no esta guardado en el stack es el objeto Identificacion Lista2 creado apartir del puntero y que termina en delete, a diferencia de este Lista1 (creado en el stack) termina apenas acaba el bloque
