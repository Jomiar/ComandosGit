# CURSO PROFESIONAL DE GIT Y GITHUB - PLATZI

## COMANDOS DE COMO SUBIR ARCHIVO DESDE GIT Y EXCLUSIVOS DE GIT
- echo "# ComandosUnix" >> README.md
- **git init**
- **git add [NombreDelArchivo.extension]** : Es para guardar una modicacion y luego subirlo al repositorio local. 
- **git add .** : Agrega todos archivos contenidas en el proyecto.
- **git commit -m "first commit"** : Es para subir un archivo al repositorio local.
- **git branch -M main**
- **git remote add origin [LinkDelRepositorio]**
- **git push -u origin main**

## COMANDOS PARA CAMINAR POR EL S.O.
- **cd [NombreDelaCarpeta]**: Sirve para ingresar a una carpeta
- **cd ..**: Sirve para retrocer a la carpetar anterior o contenedora de la actual.
- **ls** : Sirve para ver la lista de carpetas que que contiene la carpeta en la que uno se encuentra.
- **cat [NombreDelArchivo]:** Sirve para visulizar el texto plano en consola.

## COMANDOS PARA ANALIZAR CAMBIOS EN LOS ARCHIVOS DEL PROYECTO
- **git show [NombreDelArchivo]**: Muestra en consolo los cambios que han habido en el documento.
- **git log [NombreDelArchivo]**: Permite ver una lista de todos los commits realizados mas sus comentarios y los id de tus commits
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

## USO DEL COMANDO GIT RESET Y GIT RM
### git rm
Este comando nos ayuda a eliminar archivos de Git sin eliminar su historial del sistema de versiones. Esto quiere decir que si necesitamos recuperar el archivo solo debemos “viajar en el tiempo” y recuperar el último commit antes de borrar el archivo en cuestión.

Recuerda que git rm no puede usarse así nomás. Debemos usar uno de los flags para indicarle a Git cómo eliminar los archivos que ya no necesitamos en la última versión del proyecto:

- **git rm --cached** : git rm --cached: Elimina los archivos de nuestro repositorio local y del área de staging, pero los mantiene en nuestro disco duro. Básicamente le dice a Git que deje de trackear el historial de cambios de estos archivos, por lo que pasaran a un estado untracked.

- **git rm force** : git rm --force: Elimina los archivos de Git y del disco duro. Git siempre guarda todo, por lo que podemos acceder al registro de la existencia de los archivos, de modo que podremos recuperarlos si es necesario (pero debemos usar comandos más avanzados).

