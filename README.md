# Balanceador con contenedores Docker

Creando un balanceador para contenedores Docker

## Preparando la máquina

Cuando tengamos la máquina preparada y lista, instalamos docker y docker-compose como hemos hecho en prácticas anteriores.

En esta práctica se va a reutilizar el contenido de la práctica 16 en la que dockerizamos nuestro propio contenedor con apache pero incluyendo el balanceador.

## Trabajando con docker

El archivo .yml que he utilizado en la práctica se encontrará en el repositorio junto con su correspondiente env y dockerfile.

A la hora de levantar nuestra infraestructura lo haremos con el comando docker-compose up -d --scale apache=4 para que se pongan en marcha 4 contenedores y podamos comprobar que el balanceador está funcionando. Podemos editar el html de cada contenedor para diferenciar mejor el balanceo de carga.
