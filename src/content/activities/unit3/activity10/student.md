Entrega:

#### ¿Qué ocurre después de llamar a la función cambiarNombre?
Se crea una copia del punto original  y se cambia su nombre a "cambiado" y este se destruye al final delcodigo
#### ¿Por qué aparece el mensaje Destructor: Punto cambiado(70, 80) destruido.?
Porque "cambiado" es el nombre con el cual se le otorgo a la copia y porque dentro de estaa funcion ~Punto su principal
funcion es mostrar este mensaje 
#### ¿Por qué original sigue existiendo luego de llamar cambiarNombre?
Esto se debe ya que el original 
#### ¿En qué parte del mapa de memoria se encuentra original y en qué parte se encuentra p? ¿Son el mismo objeto? (recuerda usar siempre el depurador para responder estas preguntas).




"Modifica la función cambiarNombre:"
``` cpp
void cambiarNombre(Punto& p, string nuevoNombre) {
	p.name = nuevoNombre;
}
```
####  ¿Qué ocurre ahora? ¿Por qué?

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
#### En este caso ¿Cuál es la diferencia entre pasar un objeto por valor, por referencia y por puntero?
