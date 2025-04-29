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

        Identificacion Lista1("luis", 200);

        Identificacion::mostrarTotal();

        Lista1.imprimir();
        
        // Coloca un breakpoint aquí para ver 'pBloque' en el stack.
    }

    Identificacion* Lista2 = nullptr;
    {
        cout << "Inicio de la segunda lista" << endl;

        Lista2 = new Identificacion("alejandra", 600);


        Lista2->imprimir(); 

        Identificacion::mostrarTotal();
    }

    ContadorTrabajadores(NumeroTrabajadores);


    cout << "Actualmente somos (" << NumeroTrabajadores << ") trabajadores" << endl;
    cin.get();

    Lista2->imprimir();
    delete Lista2;

    return 0;
}


Código fuente de tu programa.
Explica cómo aplicaste cada concepto en tu ejemplo.
Análisis detallado de la memoria. Indica en qué segmento de memoria se está almacenando cada variable y objeto.

