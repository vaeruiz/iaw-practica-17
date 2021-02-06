# Balanceador con contenedores Docker

Creando un balanceador para contenedores Docker con HAProxy

## Preparando la máquina

Tenemos que tener una máquina de AWS con los puertos 80, 8080, y 1936 abiertos, se han utilizado 4GB de memoria para esta práctica. Cuando tengamos la máquina preparada y lista, instalamos docker y docker-compose como hemos hecho en prácticas anteriores.

En esta práctica se va a reutilizar el contenido de la práctica 16 en la que dockerizamos nuestro propio contenedor con apache pero incluyendo el balanceador y con las correspondientes adaptaciones en los archivos, recordemos que es necesario tener las carpetas correspondientes en la máquina, para cualquier duda ver el repositorio de la [practica-16](https://github.com/vaeruiz/iaw-practica-16).

## Trabajando con docker

El archivo .yml que he utilizado en la práctica se encontrará en el repositorio junto con su correspondiente env y dockerfile.

A la hora de levantar nuestra infraestructura lo haremos con el comando docker-compose up -d --scale apache=4 para que se pongan en marcha 4 contenedores y podamos comprobar que el balanceador está funcionando. Podemos editar el html de cada contenedor para diferenciar mejor el balanceo de carga.


- **Dirección IP de la máquina de Amazon funciomal.** Ya no puedo editar la entrega en el aula virtual, así que dejo la IP de la máquina corregida [34.236.191.15](http://34.236.191.15) | [ec2-34-236-191-15.compute-1.amazonaws.com](http://ec2-34-236-191-15.compute-1.amazonaws.com)
