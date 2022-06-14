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
