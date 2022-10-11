## Docker no es una tecnologia de virtualización. Es un sistema de contenedores

Cada contenedor debe complir un objetivo, cuando lo cumple debe de morir.

Docker --> objetivo: crear contenedores portables, para moverlo entre entornos de producción y desarrollo. Aplicaciones software.

No se pueden levantar dos contenedores con el mismo nombre

## ¿Qué ventajas tiene?
    - Es flexible
    - Es ligero
    - Es intercambiable
    -  Es portátil
    -  Es escalable
    -  Es apilable

## ¿Qué lo diferencia de las máquinas virtuales?

Docker pesa mucho menos, podemos tener mucho contenedores sin que se note el consumo

## Partes de Docker

Cliente --> por donde nos vamos a comunicar con docker

Imagenes --> como clases en la POO

## Imagenes

Tenemos que distinguir entre distintios tipos de imagenes. Hay públicas y privadas.

Tres tipos: verificadas, oficiales y las de cualquier usuario

## Comandos

- Para crear un contenedor a través de una imagen

`docker run Imagen`

`docker run -p mio:puertoImag -d Imagen`

`docker run --name Nombre -p mio:puertoImag -d Imagen` Ponerle nombre  auna imagen

`docker run -it Imagen` Para entrar dentro del contenedor. Que sea interactvo.

- Para listar los contenedores en marcha

`docker ps`

- Para listar todos los contenedores

`docker ps -a`

`docker container ls`

- PAra saber la versión de docker

`docker version`

- Para conocer que comandos se pueden utilizar

`docker info`

- Para permitir hacer busqedas de imagenes segun su nombre

`docker search`

- Listar imagenes existentes
  
`docker image ls`

- Para descargar una imagen tenemos que hacer lo siguiente:

`docker pull NombreImagen`

- Renombrar un ocntenedor

`docker rename ViejoNombre NuevoNombre`

- Mantener levantado un contenedor

`docker run -dt Imagen`

- Ejecutar un comando sin estar dentro del contenedor

`docker exec ContenedorName Comando`

- Devuelve un array con el ID de los contenedores

`docker ps -a --quiet`

- Como copiar un contenido dentro de un contenedor

`docker cp ArchivoQueQuieroCopiar ContenedorName:/Ubicacion`

- Copiar algo del contenedor en mi ordenador

`docker cp ContenedorName:/Ubicacion ArchivoQueQuieroCopiar`

- Entrar dentro d eun contenedor ya en marcha

`docker exec -ti NombreContenedor bash`

- Parar la ejecución de un contenedor

`docker stop NombreContenedor`

- Para levantar un contenedor parado

`docker start ContenedorID`

- Para matar un contenedor

`docker rm ContenedorID` Para contenedores ya muertos

`docker rm -f Contenedor ID` Para contenedores que estan corriendo