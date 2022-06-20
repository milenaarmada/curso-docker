# Ejercicio 7

### �Cu�ntos contenedores se est�n ejecutando? (pueden verlo en el archivo docker-compose-jobvacancy.yml y tambi�n ejecutando docker ps)

Se est�n ejecutando dos contenedores.

### �Cuales son las im�genes en las que est�n basados los mencionados contenedores?

El primer contenedor est� basado en la imagen nicopaez/jobvacancy-ruby:1.3.0 y el segundo en la imagen postgres.

### �Puedes leer el docker-compose-jobvacancy.yml y describir lo que hace cada una de sus lineas?

El archivo define dos servicios.

**version: '2'**: Versi�n de docker compose
**services:** Lista de servicios definidos. Docker compose llama **servicios** a los contenedores porque puede haber m�s de un contenedor con la misma imagen.
&nbsp;&nbsp;**web:** Nombre de un servicio
&nbsp;&nbsp;&nbsp;&nbsp;**image: nicopaez/jobvacancy-ruby:1.3.0** Imagen del contenedor
&nbsp;&nbsp;&nbsp;&nbsp;**links:** **Servicios con los que interactua**
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**- db** **Nombre del servicio con que interactua**
&nbsp;&nbsp;&nbsp;&nbsp;**ports:** Lista de los mapeos de puertos
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**- "3000:3000"** Mapeo de puertos
&nbsp;&nbsp;&nbsp;&nbsp;**environment:** Variables de entorno
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;PORT: "3000"
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;RACK_ENV: "production"
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;DATABASE_URL: "postgres://postgres:Passw0rd!@db:5432/postgres"
&nbsp;&nbsp;&nbsp;&nbsp;**depends_on:** Lista de servicios de los que depende este servicio
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**- db** Nombre del servicio del que depende
&nbsp;&nbsp;**db:** Nombre del servicio
&nbsp;&nbsp;&nbsp;&nbsp;**image: postgres** Imagen del contenedor
&nbsp;&nbsp;&nbsp;&nbsp;**environment:** Variables de entorno
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;POSTGRES_PASSWORD: Passw0rd!

### Dado que cada contenedor corre en forma aislada �C�mo es posible que esos contenedores se vean entre s�?

Docker compose crea una red para los contenedores definidos. En la red los nombres se resuelven con el nombre del contenedor (por ejemplo, si el contenedor se llama **db**, se podr� referenciar con el nombre **db**).
