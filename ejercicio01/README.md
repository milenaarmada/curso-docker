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


# Versión 2 (sin crear una nueva imagen)

```
docker run --name nginx-container -v $PWD/html:/usr/share/nginx/html:ro -p 8080:80 -d nginx
```
