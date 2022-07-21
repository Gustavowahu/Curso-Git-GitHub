# Empezando con Git.
1. [¿Qué es un sistema de control de versiones?](#¿Qué-es-un-sistema-de-control-de-versiones?)
2. [¿Qué es Git?](#¿Qué-es-Git?)
3. [Herramientas de Trabajo](#Herramientas-de-trabajo)
4. [Configurando Git por primera vez](#Configurando-git-por-primera-vez)
5. [Crear repositorio de Git](#Crear-repositorio-de-Git)
6. [Guardar cambios](#Guardar-cambios)
7. [Historial de confirmaciones](#Historial-de-confirmaciones) 
8. [Volver a una versión anterior](#Volver-a-una-versión-anterior) 

---
## ¿Qué es un sistema de control de versiones?
El sistema de control de versiones guarda lo que es modificado, donde se hizo el cambio, cuando ocurrió y quién lo hizo ya sea un cambio grande o un cambio pequeño.

--- 
## ¿Qué es Git?
Git es un sistema de control de versiones distribuido que modela sus datos más como un conjunto de instantáneas de un mini sistema de archivos. Git es el encargado de guardar los cambios.

---
## Herramientas de Trabajo
- Git.

  [git-scm.com](https://git-scm.com/)
- Visual Studio Code.

  [code.visualstudio.com](https://code.visualstudio.com/)
---
## Configurando Git por primera vez
- Configuarando Git.

  Para ver todas la configuraciones de git y cómo funciona cada configuración use el comando git config
  ~~~
  Capiuly@DESKTOP-NEHRF83 MINGW64 /c/proyecto1 (master)
  $ git config
  ~~~

  Para ver la configuración por defecto de git use el comando git config --list.
  ~~~
  Capiuly@DESKTOP-NEHRF83 MINGW64 /c/proyecto1 (master)
  $ git config --list
  ~~~

  Para ver donde están guardadas las configuraciones usa el comando git config --list--show-origin.
  ~~~
  Capiuly@DESKTOP-NEHRF83 MINGW64 /c/proyecto1 (master)
  $ git config --list--show-origin
  ~~~

  Lo primero que deberás hacer cuando instales Git es establecer tu nombre de usuario y dirección de correo electrónico. Esto es importante porque los "commits" de Git usan esta información, y es introducida de manera inmutable en los commits que envías.
  ~~~
  Capiuly@DESKTOP-NEHRF83 MINGW64 /c/proyecto1 (master)
  $ git config --global user.name "Alexander"

  Capiuly@DESKTOP-NEHRF83 MINGW64 /c/proyecto1 (master)
  $ git config --global user.email "roel.alexander@gmail.com" 
  ~~~
  
- Comprovando la configuración.

  Para mostrar todas las propiedades que Git ha configurado usa el comando git config --list.
  ~~~
  Capiuly@DESKTOP-NEHRF83 MINGW64 /c/proyecto1 (master)
  $ git config --list
  ~~~

- Como obterner ayuda.

  Existen tres formas de ver la página del manual.
  ~~~
  $ git help <verb>
  $ git <verb> --help
  $ man git-<verb>
  ~~~
- Resumen.

  En este momento debes tener una comprensión básica de lo que es Git, y en qué se diferencia de cualquier otro sistema de control de versiones centralizado que pudieras haber utilizado previamente. De igual manera, Git debe estar funcionando en tu sistema y configurado con tu identidad personal. Es hora de aprender los fundamentos de Git.
---

## Crear repositorio de Git
Para inicializar un repositorio con Git se usa el comando git init.
~~~
Capiuly@DESKTOP-NEHRF83 MINGW64 /c/proyecto1 (master)
$ git init
Initialized empty Git repository in C:/proyecto1/.git/
~~~

Para obtener la información necesaria sobre la rama actual usa el comando git status.
~~~
Capiuly@DESKTOP-NEHRF83 MINGW64 /c/proyecto1 (master)
$ git status
~~~

Para incluir los cambios del o de los archivos en tu siguiente commit usa el comando git add.
~~~
Capiuly@DESKTOP-NEHRF83 MINGW64 /c/proyecto1 (master)
$ git add Biografia.txt
~~~

Para guardar los cambios usa el comando git commit.
~~~
Capiuly@DESKTOP-NEHRF83 MINGW64 /c/proyecto1 (master)
$ git commit -m "Este es el primer commit de este archivo"
~~~
Recuerda siempre usar git add para cualquier cambio.

Para eliminar archivos usa el comando rm.
~~~
Capiuly@DESKTOP-NEHRF83 MINGW64 /c/proyecto1 (master)
$ rm Biografia.txt
~~~
--- 
## Guardar cambios
Para obtener información de los cambios sobre la rama actual usa el comando git status.
~~~
Capiuly@DESKTOP-NEHRF83 MINGW64 /c/proyecto1 (master)
$ git status
~~~

Para incluir los cambios del o de los archivos en tu siguiente commit usa el comando git add.
~~~
Capiuly@DESKTOP-NEHRF83 MINGW64 /c/proyecto1 (master)
$ git add Biografia.txt
~~~
Para guardar los cambios que seha realizado usa el comando git commit.
~~~
Capiuly@DESKTOP-NEHRF83 MINGW64 /c/proyecto1 (master)
$ git commit -m "Este es el primer commit de este archivo"
~~~

Para ver el último cambio que se hizo usa el comando git show.
~~~ 
Capiuly@DESKTOP-NEHRF83 MINGW64 /c/proyecto1 (master)
$ git show
~~~
Para ver todos los commits que ser realizaron usa el comando git log Biografia.txt
~~~
Capiuly@DESKTOP-NEHRF83 MINGW64 /c/proyecto1 (master)
$ git log Biografia.txt
~~~
Importante.

Que pasa si no le agregamos un mensaje al ejecutar el commit.
~~~
Capiuly@DESKTOP-NEHRF83 MINGW64 /c/proyecto1 (master)
$ git commit
~~~

![Editor VIM](../img/commit.png)

Para salir del editor VIM  
- Esc + shift + zz 
- Esc :q para salir sin matener los cambios.
- Esc :wq para salir guardando.

Para que no nos envié al editor VIM, recuerda siempre agregar un mensajes al commit.
## Historial de confirmaciones
Para mostrar todos los commits en el historial del repositorio usa el comando git log.
~~~
C:\proyecto1(master)
λ git log Biografia.txt
~~~
Para mostrar todos los cambios específicos en el historial del repositorio, usa el comando git log --stat
~~~
C:\proyecto1(master)
λ git log --stat
~~~
Para ver detalles ampliados en objetos de Git, como blobs, árboles, etiquetas y confirmaciones usa el comando git show.
~~~
C:\proyecto1(master)             
λ git show Biografia.txt 
~~~
Para ver las diferencias con los archivos anteriores
usa el comando git diff.
~~~
C:\proyecto1(master)
λ git diff 0698cddd344bd99c374a72b0ba89da3bd9af6d31
 02733e70ade0519ea2fe0868d1d09c652780a2b4
~~~
## Volver a una versión anterior 
Para regresar a una versión anterior usa el comando git checkout.
~~~
C:\proyecto1(master)
λ git checkout 6b9da92efb48624065d33b9b9aeba16e2fa3c5fa 
~~~
Para borrar y regresar a una versión  anterior usa el comando git reset.
~~~
C:\proyecto1(master)
λ git reset 6b9da92efb48624065d33b9b9aeba16e2fa3c5fa --hard
~~~
