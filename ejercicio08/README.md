# Ejercicio 08

1. Build

```
docker-compose build
```

2 . Run

```
docker-compose up --scale password-api=2
```

## Dudas

1. No pude generar las dos instancias dentro de compose. La documentación menciona la opción build/replicas pero no estaba soportada en mi versión de docker-compose.

2. No me funcionó montar ngix.conf dentro del docker-compose. Tuve que armar una imagen separada que lo copie.

3. No me queda claro el tema de hardcodear los nombres de los containers dentro del nginx.conf siendo que estos nombres son aleatorios generados por docker.