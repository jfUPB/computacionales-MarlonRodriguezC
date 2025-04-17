Entrega:

#### ¿Qué ocurre después de llamar a la función cambiarNombre?
Se crea una copia del punto original  y se cambia su nombre a "cambiado" y este se destruye al final delcodigo
#### ¿Por qué aparece el mensaje Destructor: Punto cambiado(70, 80) destruido.?
Porque "cambiado" es el nombre con el cual se le otorgo a la copia y porque dentro de estaa funcion ~Punto su principal
funcion es mostrar este mensaje 
#### ¿Por qué original sigue existiendo luego de llamar cambiarNombre?

Esto se debe ya que los cambios creados en "cambiarNombre" no afectan al original, original si o si tendra los mismos datos

#### ¿En qué parte del mapa de memoria se encuentra original y en qué parte se encuentra p? ¿Son el mismo objeto? (recuerda usar siempre el depurador para responder estas preguntas).

El original esta dentro de la dentro de Stack en main  junto a p pero aun asi  es un objeto distinto y ocupán  diferentes lugares en la memoria



"Modifica la función cambiarNombre:"
``` cpp
void cambiarNombre(Punto& p, string nuevoNombre) {
	p.name = nuevoNombre;
}
```
####  ¿Qué ocurre ahora? ¿Por qué?

Ahora esta referenciando a el original, entonces el cambio de nombre lo puede afectar

"Modifica ahora a cambiarNombre y a main de la siguiente manera:"
``` cpp
void cambiarNombre(Punto* p, string nuevoNombre) {
	p->name = nuevoNombre;
}

int main() {
    // Objeto original
    Punto original("original",70, 80);
    original.imprimir();

	cambiarNombre(&original, "cambiado");
	original.imprimir();
    return 0;
}
``` 
#### ¿Qué ocurre ahora? ¿Por qué?
el uso de '&'  con el original hace que el puntero pueda obtener la direccion de memoria del origina y con  esto se comienza a acceder al original
#### En este caso ¿Cuál es la diferencia entre pasar un objeto por valor, por referencia y por puntero?
al hacerlo por valor se crea una copia encambio con la referencia y el puntero se puede modificar
el original 


