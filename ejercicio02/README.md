# Ejercicio 1

1. Descargar la imagen

```
docker pull nicopaez/pingapp:3.0.0
```
2. Crear un repositorio en https://hub.docker.com/. Para eso que registrarse y crear un repositorio desde la interfaz web.

3. Crear otra imagen tagueando la imagen descargada

```
docker tag  nicopaez/pingapp milenaarmada/pingapp:1.0.0
```

4. Subir la imagen al repositorio creado. Para eso primero hay que loguearse a dockerhub desde la consola

```
docker login -u milenaarmada -p [password]
docker push milenaarmada/pingapp:1.0.0
```


5. Para descargar la imagen creada, ejecutar la siguiente instrucción

```
docker pull milenaarmada/pingapp:1.0.0
```
