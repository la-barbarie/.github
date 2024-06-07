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
