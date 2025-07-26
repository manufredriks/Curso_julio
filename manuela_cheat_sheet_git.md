# Git y Github: comandos

####La idea es que yo tengo un repositorio local y voy enviando los cambios que quiera al remoto. Allí deben ser aceptados si no hay problemas.

**git** es control de versiones
**github** es el sitiopara trabajar en equipo con git, son repositorios remotos

``` Configuraciones
git config user.name
git config --global user.name""
git config --global user.email""
```
`git init` : inicializa un repositorio local en la PC.

`git remote add oriin www...`: conecta el repositorio local al de la nube.

`git clone <URL-del-repositorio>`: clona el repositorio remoto que creamos en GitHub.

`git branch` :muestra en qué rama estamos trabajando actualmente.

`git branch -M` : crea una nueva rama

`git switch <nombre-rama>` :cambia a la rama en la que deseamos trabajar.

`git add <nombre-archivo>`: agrega el archivo al *staging area* (área de preparación) para que esté listo para el commit. Lo agrega para enviar a la nube.

`git add .`: agrega **todos los archivos modificados o nuevos** al staging area.

`git commit -m "mensaje"`: toma los archivos que marcaste con `git add` (los *staged files*) y los guarda como un nuevo *snapshot* del proyecto, con un mensaje descriptivo de lo que hiciste. Envia la info a la nube.

`git push`: sube tus cambios locales al repositorio remoto. Toma los commits que hiciste localmente con `git commit` y los envía al servidor remoto (por ejemplo, GitHub).

`git remote -v` : muestra a qué repositorio remoto está conectado tu repositorio local (y con qué URL).

`git fetch`: trae los cambios del repositorio remoto **pero no los aplica** a tu rama actual. Sirve para ver si hay cambios nuevos en el remoto antes de hacer un `merge` o un `pull`.

**git pull**: me trae informacion

**.gitignore**: archivos ignorados al utilizar git add .

**pull request**: compara si hay conflictos con los cambios que se producen en una rama con la rama principal. 
