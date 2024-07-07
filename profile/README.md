# ¡Bienvenidos a La barbarie!

## Índice

1. [Repositorios en La barbarie](#repositorios-en-la-barbarie)
   - [Repositorios de código](#repositorios-de-código)
   - [Repositorios de archivos](#repositorios-de-archivos)
   - [Repositorios de prueba](#repositorios-de-prueba)
2. [Introducción a Git y GitHub](#introducción-a-git-y-github)
   - [Conceptos básicos de Git](#conceptos-básicos-de-git)
     - [Pull](#pull)
     - [Commit](#commit)
     - [Push](#push)
     - [Merge](#merge)
   - [Consejos para trabajar con Git/GitHub en equipo](#consejos-para-trabajar-con-gitgithub-en-equipo)
3. [Conceptos y comandos para utilizar docker](#conceptos-y-comandos-para-utilizar-docker)
   - [Ejecutar un contenedor](ejecutar-un-contenedor)
   - [Ejecutar un comando en un contenedor en ejecución](ejecutar-un-comando-en-un-contenedor-en-ejecución)
   - [Detener un contenedor](detener-un-contenedor)
   - [Iniciar un contenedor](iniciar-un-contenedor)
   - [Ver logs de un contenedor](ver-logs-de-un-contenedor)
   - [Crear una red](crear-una-red)
   - [Iniciar servicios con Docker Compose](iniciar-servicios-con-docker-compose)
   - [Crear un volumen](crear-un-volumen)
   - [Listar volúmenes](listar-volúmenes)
   - [Eliminar un volumen](eliminar-un-volumen)
   - [Inspeccionar un contenedo, imágen o volúmen](inspeccionar-un-contenedo-imágen-o-volúmen)

## Repositorios en La barbarie

En nuestra organización, podrás encontrar los siguientes tipos de repositorios:

### Repositorios de código

Estos repositorios estarán dedicados a las materias o proyectos en los que estemos trabajando en grupo. Cada repositorio llevará el nombre de la materia o del proyecto correspondiente.

### Repositorios de archivos

Aquí almacenaremos archivos importantes en formatos como PDF, imágenes (JPG, PNG, JPEG, etc.), entre otros. Estos repositorios serán útiles para compartir recursos gráficos, documentos y otros tipos de archivos necesarios para nuestros proyectos.

### Repositorios de prueba

Si necesitas realizar alguna prueba, tienes total libertad para crear tu propio repositorio de prueba. Solo te pedimos que sigas una regla simple: el nombre del repositorio debe comenzar o terminar con `{test}-{nombre_creador}`. Esto nos ayudará a mantener el orden y a identificar fácilmente los repositorios de prueba.

## Introducción a Git y GitHub

Git es un sistema de control de versiones que nos permite llevar un registro de los cambios en el código fuente a lo largo del tiempo. GitHub es una plataforma basada en la web que utiliza Git y nos facilita la colaboración en proyectos de software. Aquí te dejamos un breve tutorial para que te familiarices con su uso.

### Conceptos básicos de Git

#### Pull

`git pull` se utiliza para actualizar tu repositorio local con los cambios más recientes del repositorio remoto. Es una combinación de `git fetch` y `git merge`.

#### Commit

`git commit` se usa para guardar los cambios realizados en el repositorio local. Debes añadir un mensaje descriptivo que explique lo que has hecho. 

Ejemplo:
```bash
git commit -m "Añadida nueva funcionalidad a la interfaz"
```

#### Push

`git push` se utiliza para enviar los cambios que has realizado en tu repositorio local al repositorio remoto.

Ejemplo:
```bash
git push origin master
```

#### Merge

`git merge` se utiliza para combinar las ramas de desarrollo. Si has trabajado en una rama secundaria y deseas incorporar esos cambios en la rama principal, usarás `git merge`.

Ejemplo:
```bash
git merge <nombre_de_la_rama>
```

### Consejos para trabajar con Git/GitHub en equipo

#### Clonar un repositorio

Para obtener una copia de un repositorio remoto en tu máquina local.

```bash
git clone <url_del_repositorio>
```

#### Crear una rama

Trabaja en una nueva característica o corrección sin afectar la rama principal.

Ejemplo:
```bash
git checkout -b <nombre_de_la_rama>
```

#### Agregar cambios

Añade los archivos modificados al área de preparación antes de hacer un commit.

```bash
git add <archivo_modificado>
```

#### Resolver conflictos

Si dos ramas tienen cambios en la misma línea del mismo archivo, Git generará un conflicto que deberás resolver manualmente.

#### Pull requests

En GitHub, puedes solicitar que tus cambios sean revisados y fusionados en la rama principal mediante una Pull Request.

## Conceptos y comandos para utilizar docker

Los siguientes puntos hacen referencia a una herramienta de contenedores llamada Docker. Se utiliza principalmente para el despliegue independiente de apliaciones a través de una máquina virtual que utiliza Linux. Si no saben utilizar docker, acá se detallan algunos de los comandos esenciales que hay que saber al momento de utilizarlo.

### Ejecutar un contenedor

```bash
docker run -d -p 80:80 nginx
```

```
-d: Ejecuta el contenedor en segundo plano (detached mode).
-p 80:80: Publica el puerto 80 del contenedor en el puerto 80 del host.
```

### Construir una imagen

```bash
docker build -t my_image .
```

```
-t my_image: Asigna una etiqueta (nombre) a la imágen creada.
```

### Descargar una imágen

Descarga la imagen especificada desde Docker Hub.

```bash
docker pull ubuntu
```

### Listar contenedores en ejecución

Muestra los contenedores en ejecución.

```bash
docker ps
```

### Listar todos los contenedores

```bash
docker ps -a
```

```
-a: Muestra todos los contenedores, tanto en ejecución como detenidos
```

### Listar imágenes

Lista todas las imágenes almacenadas localmente.

```bash
docker images
```

### Eliminar una imagen

Elimina la imágen especificada

```bash
docker rmi my_image
```

### Eliminar un contenedor

Elimina el contenedor especificado

```bash
docker rm my_container
```

### Ejecutar un comando en un contenedor en ejecución

```bash
docker exec -it my_container bash
```

```
-i: Modo interactivo.
-t: Asigna una terminal (tty).
```

### Detener un contenedor

Detiene el contenedor en ejecución.

```bash
docker stop my_container
```

### Iniciar un contenedor detenido

Inicia el contenedor detenido

```bash
docker start my_container
```

### Ver logs de un contenedor

Muestra los logs del contenedor especificado.

```bash
docker stop my_container
```

### Crear una red

Crea una nueva red para contenedores

```bash
docker network create my_network
```

### Iniciar servicios con Docker Compose

Inicia los servicios definidos en el archivo `docker-compose.yml`.

```bash
docker-compose up
```

### Detener y eliminar servicios con Docker Compose

Detiene y elimina los contenedores, redes, volúmenes e imágenes creados por `docker-compose up`.

```bash
docker-compose down
```

### Crear un volumen

Crea un nuevo volmen

```bash
docker volume create my_volume
```

### Listar volúmenes

Lista todos los volúmenes

```bash
docker volume ls
```

### Eliminar un volumen

Elimina el volumen especificado

```bash
docker volume rm my_volume
```

### Inspeccionar un contenedo, imágen o volúmen

Muestra información detallada sobre el contenedor, imagen, red o volumen especificado.

```bash
docker inspect my_container
```
