
#### 1. ¿Qué ocurre? ¿Por qué?

Se crea las variables globales de "global_inicializada" y "global_no_inicializada" las cuales dnetro del main se mostrara su valor inicial (42 y
0), luego cambian sus valores a 69 y 666 y el main muestra este cambio el cual se hizo en todo el programa

#### 2. ¿Qué ocurre? ¿Por qué?

Se crea una funcion con el nombre de  " void funcionConStatic() " y esta crea una variable estatica con el valor de 100, y muestra este valor,
pero dentro del main se cambia este valor a 42 y se intenta mostrar pero esto no es posible ya que dentro de main la variable no la declara lo cual esta cree
que la variable no es definida y tiene un mensaje de error 

#### ¿Qué pasa con las variables cada que entras y sales de la función?

Si la funcion hace un cambio dentro de la informacion de las variables y estas son globales, esta informacion se guardara en la memoria, aunque salga y quiera volver a 
repetir el proceso de la funcion igualmente esta hara su respectivo cambio

#### En relación a la pregunta anterior ¿Qué pasa con las variables locales estáticas?
En el caso de las variables locales estaticas, aunque se puede usar las variables estaticas de forma global para restringir la variable dentro de su respectivo archivo
(encapsulandola), si esta es local (como ocurre dentro del experimento) esta no podra modificarse porque su ambito es limitado 
