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

5. Ingresar desde el navegador a la direcci�n http://localhost:8080/

## Notas para el docente

Hice la versi�n m�s b�sica de colocar el nombre en index.html, que es el archivo que por defecto sirven los servidores web. Pens� que la entrega era el mi�rcoles en clase, hoy me di cuenta que era ayer, as� que estoy ya fuera de t�rmino y haciendo lo m�s r�pido posible.

## Notas de estudio

 * Para la consigna era necesario construir una imagen con la imagen base de nginx.
 * En el Dockerfile:
    * Se especifica esa imagen base con FROM
    * Copio la carpeta que quiero servir con COPY (el destino es la carpeta de nginx dentro del contenedor)

 * Construyo la imagen con docker build:
    * El par�metro -t xxx le asigna un nombre/tag a la imagen (para poder referenciarla despu�s).

 * Levanto el contenedor con docker run:
    * El par�metro --name le asigna un nombre al contenedor
    * -p 8080:80 hace el mapeo de puertos para que sea accesible desde afuera
    * -d (o --detach) hace que se ejecute y libere la consola. Esto es �til cuando el contenedor queda corriendo, para seguir trabajando en esa ventana.
    * Luego del run se coloca el nombre de la imagen a utilizar.

 * Mientras hac�a el ejercicio constru� la imagen y el contenedor varias veces.
 * Para volver a levantar el contenedor, hay que hacer stop y luego rm.
 * La construcci�n de la imagen no requiere borrarla.
