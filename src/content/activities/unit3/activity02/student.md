#include <iostream>

using namespace std;


void swapPorValor(int m, int a) {

    m += 5;
    a += 5;
}


void swapPorReferencia(int &m, int &a) {
    m += 5;
    a += 5;
}

void swapPorPuntero(int *m, int *a) {
    *m += 5;
    *a += 5;
}

int main() {
    int x = 20;
    int y = 25;
    
    cout << "Valores iniciales: x = " << x << ", y = " << y << endl;
    
    cout << "\nLlamando a modificarPorValor(x,y)..." << endl;
    swapPorValor(x, y);
    cout << "Después de swapPorValor: x = " << x << ", y = " << y << endl;
    
    
    x = 20; 
    y = 25;
 
    
    cout << "\nLlamando a modificarPorReferencia(x,y)..." << endl;
    swapPorReferencia(x, y);
    cout << "Después de swapPorReferencia: x = " << x << ", y = " << y << endl;

    x = 20; 
    y = 25;

    
    cout << "\nLlamando a modificarPorPuntero(&x ,&y)..." << endl;
    swapPorPuntero(&x, &y);
    cout << "Después de swapPorPuntero: x = " << x << ", y = " << y << endl;
    
    return 0;
}


Por qué la versión de swapPorValor no logra intercambiar los valores de x e y en el main()?

porque esta crea unas copias de lo que serian las variables dentro de la funcion, y su modificacion acaba cuando la funcion termina su ultima linea 
acabando tambien con las copias, es como clonar a un ser humano y que el clon  pase toda su vida y se haga cirugias y  muera , aunque era igual a la 
persona original, igual su ciclo de vida no afecto a la principal y asi mismo termino con la suya 

¿Cómo y por qué logran las otras dos funciones (por referencia y por puntero) modificar las variables originales?
Como lo decia la lectura anterior, la letra que se toma en las funciones por referencias esta usaba 'n' como un alias de la variable usada en el main 
, un ejemplo divertido podria ser un vaquero que es bandido el cual usa un alias, al tener acciones encontra de la ley, estas actuan encontra de su 
alias, pero las consecuencias las pagara tanto el alias como el vaquero que usa este alias

¿Cuáles son las ventajas y consideraciones de usar referencias versus punteros en este caso?
Aunque los punteros  pueden cambiar su direccion a la cual apunta, pero  creeria que en este caso  las ventajas que pueden traer las referencias es que
no es necesario confirmar el puntero con * antes de cada variable 

