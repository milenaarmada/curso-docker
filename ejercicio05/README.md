# Ejercicio 5

## HEALTHCHECK

Es una mecanismo para verificar que un contenedor se est� ejecutando correctamente.
Un contenedor puede estar levantado pero las aplicaciones que ejecuta pueden estar en un estado no v�lido. Por ejemplo, puedo ver con docker ps que un contenedor est� activo pero internamente su aplicaci�n est� ca�da. Healthcheck se utiliza para poder verificar que las aplicaciones est�n corriendo correctamente.

El healtcheck puede definirse en el Dockerfile, v�a docker compose o en el comando run. Quien define el contenedor define c�mo se realiza esta verificaci�n (pueden ser aplicaciones conocidas como curl o scripts espec�ficos).

La verificaci�n de salud se utiliza para monitorear el contenedor "a mano" y la utilizan los orquestarores para decidir sobre la infraestructura.



## ONBUILD

ONBUILD es un comando para definir en una imagen, qu� acciones ejecutar en la construcci�n de otra imagen que la tome como base.

Este mecanismo permite evitar duplicaci�n de instrucciones cuando se generan muchas im�genes con l�gica similar.

El ejemplo m�s mencionado es el caso en que hay que construir im�genes que realizan compilaci�n de c�digo de proyectos. En la imagen base, adem�s de la configuraci�n de la misma,
se define el mecanismo de compilaci�n del proyecto, que se ejecutar� en las im�genes "hijas" al inicio de la construcci�n.

## VOLUME

Este comando (dentro del Dockerfile) crea un volumen. A diferencia de crear vol�menes con comandos fuera del Dockerfile, esta opci�n crea vol�menes sin nombre y sin poder especificar el directorio f�sico en el host.
