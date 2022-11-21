# Documentación

Esto es una aplicación web utilizando el framework realizada con flask y bootstrap. Su propósito es ejemplificar un CRUD utilizando el recurso mensaje.

Los datos se guardan en la base de datos postgres utilizando migraciones.

Las dependencias del proyecto se gestionan con pipenv.

## Dependencias
Para correr este proyecto usted necesita previamente tener instalado python 3 y su herramienta pip.

Para revisar que quede instalado debe ejecutar los siguientes comandos:

```
python -V
pip -V
```

El resultado deberia indicar a un numero superior o igual a 3.
Luego de clonar el repositorio y para instalar las dependencias 
debe ejecutar el comando `pipenv install`

## Migraciones
Para ejecutar las migraciones el comando es el siguiente:
```
flask db upgrade
```

En caso de modificar un modelo agregando o modificando un atribitu, debemos generar una nueva migración con el comando
`flask db migrate -m "elmensaje"`

**nota** Los espacios anteriores deben ejecutarse dentro de `pipenv shell`

## Levantando la aplicación 

Para ejecutar el servidor de desarrollo el comando es el siguiente

```
flask --app app --debug run
```