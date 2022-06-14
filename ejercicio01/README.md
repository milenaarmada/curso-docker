# Ejercicio 1

1. Clonar el repo
2. Construir la imagen:

```
docker build -t nginx-image .
```

3. Levantar el contenedor:

```
docker run --name nginx-container -d -p 8080:80 nginx-image
```

4. Ingresar desde el navegador a la dirección http://localhost:8080/
