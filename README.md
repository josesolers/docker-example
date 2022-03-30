# Docker example

Este proyecto consta de un servidor REST sencillo para la gestión de items.

## Construir la aplicación (en local)

Para construir la imagen Docke del proyecto (y lanzar los test):

```
    mvn spring-boot:build-image
```

## Lanzar la aplicación (en local)

Para lanzar la aplicación el local:

```
    docker run -p 8080:8080 items:0.0.1-SNAPSHOT
```

## Construimos y subimos la imagen a DockerHub

```
    docker login
    docker tag items:0.0.1-SNAPSHOT <hub-user>/items:0.0.1-SNAPSHOT
    docker push <my_user>/items:0.0.1-SNAPSHOT
```

## Lanzamos la imagen

```
    docker run -p 8080:8080 <my_user>/items:0.0.1-SNAPSHOT
```


EDICION DEL YML PARA EJERCICIO 1: 
    1. Genero los tags antes de generar la imagen
    2. Genero la imagen con el nombre en el formato pedido
    3. Modifico el push de la imagen que acabo de crear con el nombre en el formato pedido
    4. Commit de los cambios y ejecuto el job
