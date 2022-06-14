# Ejercicio 1

1. Clonar el repo

```
git clone git@github.com:milenaarmada/curso-docker.git
```
2. Posicionarse en el directorio del ejercicio 01:

```
cd curso-docker/ejercicio01
```

3. Construir la imagen:

```
docker build -t nginx-image .
```

4. Levantar el contenedor:

```
docker run --name nginx-container -d -p 8080:80 nginx-image
```

5. Ingresar desde el navegador a la dirección http://localhost:8080/

## Notas para el docente

Hice la versión más básica de colocar el nombre en index.html, que es el archivo que por defecto sirven los servidores web. Pensé que la entrega era el miércoles en clase, hoy me di cuenta que era ayer, así que estoy ya fuera de término y haciendo lo más rápido posible.

## Notas de estudio

 * Para la consigna era necesario construir una imagen con la imagen base de nginx.
 * En el Dockerfile:
    * Se especifica esa imagen base con FROM
    * Copio la carpeta que quiero servir con COPY (el destino es la carpeta de nginx dentro del contenedor)

 * Construyo la imagen con docker build:
    * El parámetro -t xxx le asigna un nombre/tag a la imagen (para poder referenciarla después).

 * Levanto el contenedor con docker run:
    * El parámetro --name le asigna un nombre al contenedor
    * -p 8080:80 hace el mapeo de puertos para que sea accesible desde afuera
    * -d (o --detach) hace que se ejecute y libere la consola. Esto es útil cuando el contenedor queda corriendo, para seguir trabajando en esa ventana.
    * Luego del run se coloca el nombre de la imagen a utilizar.

 * Mientras hacía el ejercicio construí la imagen y el contenedor varias veces.
 * Para volver a levantar el contenedor, hay que hacer stop y luego rm.
 * La construcción de la imagen no requiere borrarla.
