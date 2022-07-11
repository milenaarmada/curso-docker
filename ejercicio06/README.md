# Ejercicio 6


1. Acceso a la imagen sin registrarme en REDHAT

https://catalog.redhat.com/software/containers/redhat-openjdk-18/openjdk18-openshift/58ada5701fbe981673cd6b10?container-tabs=gti&gti-tabs=unauthenticated

```
docker pull registry.access.redhat.com/redhat-openjdk-18/openjdk18-openshift:1.12-1.1655301789
```

2. Construir la imagen

```
docker build -t password-api-image-redhat .
```

3. Ejecutar la imagen (para probar)

```
docker run -d -p 8089:8080 password-api-image-redhat
```

4. Crear otra imagen tagueando la imagen creada

```
docker tag  password-api-image-redhat milenaarmada/password-api-image-redhat:1.0.0
```

5. Subir la imagen al repositorio

```
docker login -u milenaarmada -p [password]
docker push milenaarmada/password-api-image-redhat:1.0.0
```

3. Descarga de la imagen

```
docker pull milenaarmada/password-api-image-redhat:1.0.0
```


