# Arquitectura hexagonal con Optimus.

## Requisitos de sistema.

* JDK 17 o superior​
* Gradle 8.1.1 o superior
* Docker 
* Optimus

## Cata

Una gran compañía de video juegos quiere construir un sistema (microservicio), diseñado específicamente para almacenar las caractiristicas de los pokemones que sus usuario agregen como pokemones favoritos.

### Usuarios
– Todos los posibles usuarios de la empresa.

### Requerimientos
* Cada usuario tiene una identificación única en el sistema, en formato UUID.
* Además, cada usuario tiene un nombre y apellido (Deben ser almanacenados en el sistema)
* No es posible registrar dos usuarios con la misma identificación.
* Cada pokemon tiene su propia identificación que en esta caso sera el nombre el pokemon.
* Dos nombres son iguales si hacen referencia al mismo pokemon (el formato es indiferente, por ejemplo: bulbasaur es igual a Bulbasaur o BURBASAUR).
* El sistema debe almacenar los datos de los pokemones (nombre, altura, peso, experiencia y una lista de habilidades).
* Los datos de los pokemones deben ser consultados en una API externa al momento de que el usuario agregue un pokemon como favorito y luego almacenado en base de datos.
* Para recibir la información es necesario exponer dos servicios rest, el primero para registrar los usuario y otro para relacionar el usuario con el pokemon.

### Requerimientos tecnicos
* Usar Spring Boot con WebFlux.
* Usar Optimus.
* Debe usar una base de datos relacional (Postgress o MySQL).