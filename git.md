# Curso Git Platzi

##Git
Este comentario está basado en el video, comentarios de éste mismo video y wikipedia.
Personalmente recomiendo leer y guardar el comentario. No se asusten, es sólo un resumen para que no tengan que hacerlo luego.

­

Git es un sistema de control de versiones, pensado para la eficiencia y la confiabilidad del mantenimiento de versiones en un proyecto. Su propósito es llevar un registro de los cambios en archivos de computadora y coordinar el trabajo que varias personas realizan sobre archivos compartidos.
Git permite guardar únicamente los cambios realizados en algún archivo o proyecto y nos permite saber dónde, quién o cuándo se han realizado los cambios.

­

##Los comandos básicos en Git son los siguientes:

`git init:` Permite iniciar el repositorio (lugar donde se almacenarán los cambios).

`git add <nombre_archivo>:` Git comienza a “trackear”, comienza a hacerle un seguimiento archivo en cuestión.

`git commit:` Envía los últimos cambios del archivo a la base de datos del sistema de control de versiones. Una buena práctica al usar este comando es añadir -m; al hacer esto, podemos escribir un mensaje que nos permita recordar los cambios que hicimos en ese momento.

`git add .:` Es un comando que nos permite agregar al repositorio todos los archivos a los cuales se le haya hecho algún cambio.

`git status:` Permite ver el estado de la base de datos. Por ejemplo, podemos ver si hay algunos cambios que no se han guardado en el repositorio, y si no hay nada nos dirá que todo esta bien.

`git show`: Mostrara todos los cambios que hemos hecho, esto incluye las líneas que hemos cambiado, cuando y quien hizo dicho cambios.

`git log <nombre_archivo>`: Muestra todo el historial del archivo.

`git push`: Permite enviar los cambios realizados a un servidor remoto.

`git push origin <nombre_rama>`: Sube la rama “nombre_rama” al servidor remoto.

`git fetch`: Descarga los cambios realizados en el repositorio remoto.

`git merge <nombre_rama>`: Impacta en la rama en la que te encuentras parado, los cambios realizados en la rama “nombre_rama”.

`git pull`: Unifica los comandos fetch y merge en un único comando.

`git checkout -b <nombre_rama_nueva>`: Crea una rama a partir de la que te encuentres parado con el nombre “nombre_rama_nueva”, y luego salta sobre la rama nueva, por lo que quedas parado en esta última.

`git checkout -t origin/<nombre_rama>`: Si existe una rama remota de nombre “nombre_rama”, al ejecutar este comando se crea una rama local con el nombre “nombre_rama” para hacer un seguimiento de la rama remota con el mismo nombre.

`git branch`: Lista todas las ramas locales.

`git branch -a`:Lista todas las ramas locales y remotas.

`git branch -d <nombre_rama>`: Elimina la rama local con el nombre “nombre_rama”.

`git push origin <nombre_rama>`: Commitea los cambios desde el branch local origin al branch “nombre_rama”.

`git remote prune origin`: Actualiza tu repositorio remoto en caso que algún otro desarrollador haya eliminado alguna rama remota.

`git reset --hard HEAD`: Elimina los cambios realizados que aún no se hayan hecho commit.

`git revert <hash_commit>`: Revierte el commit realizado, identificado por el “hash_commit”.

Cuando se habla de “quedar parado”, se refiere a donde estás posicionado, dónde o en qué ruta estás realizando los comandos en la terminal.

### Crear usuario

Es importante registrar usuario y e-mail en git.

`git config`: muestra configuraciones de git también podemos usar –list para mostrar la configuración por defecto de nuestro git y si añadimos `--show-origin inhales` nos muestra las configuraciones guardadas y su ubicación.

`git config --global user.name`: cambia de manera global el nombre del usuario, seguidamente ponemos entre comillas nuestro nombre.

`git config --global user.email`: cambia de manera global el email del usuario, seguidamente ponemos entre comillas nuestro nombre.

## Cambiar a main

`git config --global init.defaultBranch main`:cambia el nombre de la rama principal

`git branch -M main`: cambia el nombre de master a main



## Terminal

###Comandos Principales

`pwd` nos muestra el path o ruta de la carpeta en donde nos encontramos ubicados


`cd` me permite acceder (entrar) a una carpeta en un nivel o varios niveles

`cd ..` me permite salir de una carpeta en un nivel o varios niveles OJO los dos puntos deben ser separados por un espacio del comando cd

`ls` me muestra los archivos que contiene una carpeta, puede ser la ubicación actual o una ruta especifica, no muestra los archivos ocultos

`ls -a` me muestra los archivos que contiene una carpeta, puede ser la ubicación actual o una ruta especifica, incluyendo los archivos ocultos

`ls -l` me lista los archivos que contiene una carpeta con sus atributos, puede ser la ubicación actual o una ruta especifica, no muestra los archivos ocultos

`ls -la` me lista los archivos que contiene una carpeta con sus atributos, puede ser la ubicación actual o una ruta especifica, incluyendo los archivos ocultos

`clear` limpiar la consola o terminal, o un shorcut `crtl + L`

`mkdir <nombre carpeta>` nos permite crear una carpeta

`touch <nombre del archivo>` nos permite crear un archivo

`cat <nombre del archivo>` me permite visualizar el contenido del un archivo y lo muestra en el terminal
history nos muestra un historial de los comandos que hemos utilizado

`rm <nombre del archivo>` me permite borrar un archivo
OJO en Windows el terminal no es case sensitive (Sensible las mayusculas), con Linux,y UNIX si son case sensitive

## Configurar llaves
Generar una nueva llave SSH: (Cualquier sistema operativo)

```
ssh-keygen -t rsa -b 4096 -C "youremail@example.com"
```

Comprobar proceso y agregarlo (Windows)

```
eval $(ssh-agent - s)
ssh-add ~/.ssh/id_rsa

```
En Github agregar la llave y luego cambiar url git con el siguiente comando:
```
git remote set-url origin git@github.com:AlvaroRubilar/curso_git
```
