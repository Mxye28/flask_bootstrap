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

Para ejecutar hacia adelante
```
flask db upgrade
```
Para ejecutar hacia atras

```
flask db downgrade

Cuando hacemos algun cambio en un modelo y necesitamos considerar esos datos también en la base de datos, hay que generar una nueva migración

```
`flask db migrate -m "elmensaje"
```

En caso de modificar un modelo agregando o modificando un atribitu, debemos generar una nueva migración con el comando
`flask db migrate -m "elmensaje"`

**nota** Los espacios anteriores deben ejecutarse dentro de `pipenv shell`

## Levantando la aplicación 

Para ejecutar el servidor de desarrollo el comando es el siguiente

```
flask --app app --debug run
```

## Blueprint

Los blueprint permiten componer aplicaciones desde componentes pequeños, cada componente es como una mini aplicación. Permiten crear aplicaciones grandes manteniendo el código y la estructura simples.

## Módulos

Para que los blueprint esten bien organizados, es mejor trabajarlos como módulos, es decir que estén dentro de una carpeta. Los módulos se pueden anidar, de hecho nosotros hicimos el `módulo app`  con su respectivo `__init__.py y dentro tenemos otros modulos como el modulo `messages` que es además un blueprint.

## Tarea

Crear un nuevo recurso sencillo, sin base de datos, como blueprint bajo el url      `/memes` y debe renderiar un html lleno de memes
