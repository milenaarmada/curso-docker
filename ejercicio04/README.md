# Ejercicio 4

1. Construir la imagen

```
docker build -t password-api-image .
```

2. Ejecutar la imagen

```
docker run --name password-api-container -d -p 8080:80 password-api-image
```
