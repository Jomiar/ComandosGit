# CURSO PROFESIONAL DE GIT Y GITHUB - PLATZI

## **1.Por qué usar el sistema de control de versiones Git?**

Un sistema de control de versiones como Git nos ayuda a guardar el historial de cambios y crecimiento de los archivos de nuestro proyecto.

En realidad, los cambios y diferencias entre las versiones de nuestros proyectos pueden tener similitudes, algunas veces los cambios pueden ser solo una palabra o una parte específica de un archivo específico. Git está optimizado para guardar todos estos cambios de forma atómica e incremental, o sea, aplicando cambios sobre los últimos cambios, estos sobre los cambios anteriores y así hasta el inicio de nuestro proyecto.
![](https://static.platzi.com/media/user_upload/GIT%20GITHUB-21de2769-fd6c-4835-b078-04128276f16f.jpg)

![](https://static.platzi.com/media/user_upload/Git-8d9b1bbd-6ab1-4532-8f5b-83f8c514e2c9.jpg)
- El comando para iniciar nuestro repositorio, o sea, indicarle a Git que queremos usar su sistema de control de versiones en nuestro proyecto, es ``git init``.
- El comando para que nuestro repositorio sepa de la existencia de un archivo o sus últimos cambios es ``git add``. Este comando no almacena las actualizaciones de forma definitiva, únicamente las guarda en algo que conocemos como “Staging Area” (área de montaje o ensayo).
- El comando para almacenar definitivamente todos los cambios que por ahora viven en el staging area es ``git commit``. También podemos guardar un mensaje para recordar muy bien qué cambios hicimos en este commit con el argumento ``-m "Mensaje del commit"``.
- Por último, si queremos mandar nuestros commits a un servidor remoto, un lugar donde todos podamos conectar nuestros proyectos, usamos el comando ``git push``.
## **1.1 Comandos básicos de git**
- echo "# ComandosUnix" >> README.md
- **``git init``**: Inicializa un repositorio GIT en la carpeta donde se ejecuta el comando.
- **``git add [NombreDelArchivo.extension]``** : Añade los archivos especificados al área de preparación (stating).
- **git add .** : Agrega todos archivos contenidas en el proyecto.
- **``git commit -m "first commit"``** : Añade al staging area y hace un commit mediante un solo comando. (No funciona con archivos nuevos)
- **``git status``**: Ofrece una descripción del estados de los archivos (untracked, ready to commit, nothing to commit)
- **``git rm (. -r, filename) (–cached)``**: remueve los archivos del index.
- **``git config --global user.email tu@email.com``**: configura un email.
- **``git config --global user.name <Nombre como se verá en los commits>``**: configura un nombre.
- **``git config --list``**: lista las configuraciones.
- **git branch -M main**
- **git remote add origin [LinkDelRepositorio]**
- **git push -u origin main**

## **1.2 Analizar cambios en los archivos de un proyecto Git**
- **``git log``**: lista de manera descendente los commits realizados.
- **``git log --stat``**: además de listar los commits, muestra la cantidad de bytes añadidos y eliminados en cada uno de los archivos modificados.
- **``git log --all --graph --decorate --oneline``**: muestra de manera comprimida toda la historia del repositorio de manera gráfica y embellecida.
- **``git show filename``**: permite ver la historia de los cambios en un archivo.
- **``git diff <commit1> <commit2>``**: compara diferencias entre en cambios confirmados.
## **COMANDOS PARA CAMINAR POR EL S.O.**
- **cd [NombreDelaCarpeta]**: Sirve para ingresar a una carpeta
- **cd ..**: Sirve para retrocer a la carpetar anterior o contenedora de la actual.
- **ls** : Sirve para ver la lista de carpetas que que contiene la carpeta en la que uno se encuentra.
- **ls -al** : Sirve para ver la lista de carpetas que que contiene la carpeta en la que uno se encuentra.
- **cat [NombreDelArchivo]:** Sirve para visulizar el texto plano en consola.

## COMANDOS PARA ANALIZAR CAMBIOS EN LOS ARCHIVOS DEL PROYECTO
- **``git log``**: lista de manera descendente los commits realizados.
- **``git log --stat``**: Ademas de listar los commits, muestra la cantidad de bytes añadidos y eliminados en cada uno de los archivos modificados.
- **``git log --all --graph --decorate --oneline``**: muestra de manera comprimida toda la historia del repositorio de manera gráfica y embellecida.
- **``git show [FileName]``**: muestra de manera comprimida toda la historia del repositorio de manera gráfica y embellecida.
- **``git show filename``**: permite ver la historia de los cambios en un archivo.
- **git pull**: Traer repositorio remoto
- **git diff [CodigoDelCommit1] [CodigoDelCommit2]**: Automaticamente la base de datos de git compara ambas versiones y los cambios que han sufrido el codigo.

## COMANDO PARA VOLVER A UNA VERSION ANTERIOR
- **git log**
- **git reset [Id de la version a la que queremos volver] --hard** : Todo vuelve a la version que indica el id.
- **git reset [Id de la version a la que queremos volver] --soft** : Volvemos a la version anterior pero lo que esta en el stading sigue en el stading.
- **git checkout [id de la version]** : Sirve para visualizar una version del archivo
- **git add .**
- **git commit -m** : "Reemplazo de una version por otra de la historia"
- **git log**: ver las versiones
- **git log --stat**: ver las versiones y cambio de peso en bytes
## 1.3 Analizar cambios en los archivos de un proyecto Git
## USO DEL COMANDO GIT RESET Y GIT RM
### git rm
Este comando nos ayuda a eliminar archivos de Git sin eliminar su historial del sistema de versiones. Esto quiere decir que si necesitamos recuperar el archivo solo debemos “viajar en el tiempo” y recuperar el último commit antes de borrar el archivo en cuestión.

Recuerda que git rm no puede usarse así nomás. Debemos usar uno de los flags para indicarle a Git cómo eliminar los archivos que ya no necesitamos en la última versión del proyecto:

- **git rm --cached** : git rm --cached: Elimina los archivos de nuestro repositorio local y del área de staging, pero los mantiene en nuestro disco duro. Básicamente le dice a Git que deje de trackear el historial de cambios de estos archivos, por lo que pasaran a un estado untracked.

- **git rm force** : git rm --force: Elimina los archivos de Git y del disco duro. Git siempre guarda todo, por lo que podemos acceder al registro de la existencia de los archivos, de modo que podremos recuperarlos si es necesario (pero debemos usar comandos más avanzados).



