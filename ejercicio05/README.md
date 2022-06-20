# Ejercicio 5

## HEALTHCHECK

Es una mecanismo para verificar que un contenedor se está ejecutando correctamente.
Un contenedor puede estar levantado pero las aplicaciones que ejecuta pueden estar en un estado no válido. Por ejemplo, puedo ver con docker ps que un contenedor está activo pero internamente su aplicación está caída. Healthcheck se utiliza para poder verificar que las aplicaciones estén corriendo correctamente.

El healtcheck puede definirse en el Dockerfile, vía docker compose o en el comando run. Quien define el contenedor define cómo se realiza esta verificación (pueden ser aplicaciones conocidas como curl o scripts específicos).

La verificación de salud se utiliza para monitorear el contenedor "a mano" y la utilizan los orquestarores para decidir sobre la infraestructura.



## ONBUILD

ONBUILD es un comando para definir en una imagen, qué acciones ejecutar en la construcción de otra imagen que la tome como base.

Este mecanismo permite evitar duplicación de instrucciones cuando se generan muchas imágenes con lógica similar.

El ejemplo más mencionado es el caso en que hay que construir imágenes que realizan compilación de código de proyectos. En la imagen base, además de la configuración de la misma,
se define el mecanismo de compilación del proyecto, que se ejecutará en las imágenes "hijas" al inicio de la construcción.

## VOLUME

Este comando (dentro del Dockerfile) crea un volumen. A diferencia de crear volúmenes con comandos fuera del Dockerfile, esta opción crea volúmenes sin nombre y sin poder especificar el directorio físico en el host.
