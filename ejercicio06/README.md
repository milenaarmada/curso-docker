# Ejercicio 6


0. Acceso a la imagen sin registrarme en REDHAT

https://catalog.redhat.com/software/containers/redhat-openjdk-18/openjdk18-openshift/58ada5701fbe981673cd6b10?container-tabs=gti&gti-tabs=unauthenticated

```
docker pull registry.access.redhat.com/redhat-openjdk-18/openjdk18-openshift:1.12-1.1655301789
```

1. Construir la imagen

```
docker build -t password-api-image-redhat .
```

2. Ejecutar la imagen

```
docker run -d -p 8089:8080 password-api-image-redhat
```

3. Descarga de la imagen

```
docker pull milenaarmada/password-api-image:latest
```

**No me funcion�**
