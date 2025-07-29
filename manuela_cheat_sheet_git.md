# Curso de Git y Github: 

Tabla de contenidos

- [Git y Github](#git-y-github)
  - [Configuracion de Git](#configuracion-de-git)
  - [Repositorio remoto](#repositorio-remoto)
  - [Ramas](#ramas)
  - [Agregar archivos](#agregar-archivos)
- [Comandos más usados](#comandos-mas-usados)
    
# Git y Github

* **git** es control de versiones.

* **github** es el sitio para trabajar en equipo con git, son repositorios remotos.

###### La idea es que yo tengo un repositorio local y voy enviando los cambios que quiera al remoto. Allí deben ser aceptados si no hay problemas.

### Configuracion de Git

``` Configuraciones
git config user.name
git config --global user.name""
git config --global user.email""
```
+ `mkdir`: creamos la carpeta donde queremos guardar el repositorio local en nuestra pc. Opcional(si estamos desde temrinal crear un archivo README.md con el comando echo "#Github..." >> README.md
+ `git init` : inicializa un repositorio local en la PC o reinicia uno existente (verificar que estemos en la carpeta correcta).

+ `git remote add oriin www...`: conecta el repositorio local al de la nube.

### Repositorio remoto

+ `git clone <URL-del-repositorio>`: clona el repositorio remoto que creamos en GitHub.

+ `git remote -v` : muestra a qué repositorio remoto está conectado tu repositorio local (y con qué URL). Si estas conectado a un repositorio remoto, te va a indicar que esa URL se usa para fetch: traer cambios desde GitHub a tu compu (git pull) y
push: enviar tus commits desde tu compu a GitHub (git push).

### Ramas

+ `git branch` : Muestra las ramas existentes en tu repositorio actual.
Te indica en qué rama estás trabajando con un *.

+ `git branch -M main` : enombra la rama actual a main, forzando el cambio incluso si main ya existe.
La -M es como -m (rename), pero con mayúscula, que fuerza el cambio. Si en vez de main, utilizo nombre_rama, se renombra la rama actual a nombre_rama.
👉 Útil si estás en una rama llamada master y querés seguir la convención moderna de usar main.

+ `git branch <nombre_rama>`: crea la nueva rama nombre_rama, pero no cambia a esa rama. En versiones viejas, antes de cambiar de rama tenes que salir de la que trabajas con `git checkout <nombre_rama>`. Pero en versiones actuales, se usa `git switch`.

+ `git switch <nombre-rama>` :cambia a la rama en la que deseamos trabajar.

### Agregar archivos

+ `git add <nombre-archivo>`: agrega el archivo al *staging area* (área de preparación) para que esté listo para el commit. Lo agrega para enviar a la nube.

+ `git add .`: agrega **todos los archivos modificados o nuevos** al staging area.

# Comandos más usados

+ `git commit -m "titulo"-m "descripcion"`: toma los archivos que marcaste con `git add` (los *staged files*) y los guarda como un nuevo *snapshot* del proyecto, con un mensaje descriptivo de lo que hiciste. Envia la info a la nube.

+ `git push`: sube tus cambios de la rama actual al repositorio remoto (si ya está configurado).
Toma los commits que hiciste localmente con `git commit` y los envía al servidor remoto (por ejemplo, GitHub).
Pero **si es la primera vez que hacés push** de esa rama, `git push -u origin <nombre_rama>`. Lo que significa que sube tu rama <nombre_Rama>(puede ser main) al remoto origin, es decir, asocia esa rama local con la remota (hace "tracking").
Después de eso, sí podés usar simplemente `git push` y Git ya sabe que debe empujar main a origin/main.

+ `git fetch`: trae los cambios del repositorio remoto **pero no los aplica** a tu rama actual. Sirve para ver si hay cambios nuevos en el remoto antes de hacer un `merge` o un `pull`.

+ `git merge <feature-branch>`: fusiona los cambios de la rama feature-branch en tu rama actual.

+ `git stash`: guarda tus cambios no comprometidos para que puedas cambiar de rama o trabajar en otra tarea sin perderlos. Para recuperar los cambios: `git stash apply`.

+ `git log`: muestra el historial de commits con detalles como el hash del commit, autor, fecha y mensaje del commit. Para una versión más corta: `git log --oneline`

+ ` git reset --hard HEAD~1`: deshace el último commit y restaura el estado del repositorio al commit anterior. La opción `--hard` también elimina los cambios en los archivos de trabajo.

+ **git pull**: actualiza tu rama local con los cambios que hay en el repositorio remoto.

+ **git pull origin main**: descarga los cambios de la rama main del repositorio remoto origin y los fusiona en tu rama local actual.

+ **.gitignore**: archivos ignorados al utilizar git add ., no se subiran al repositorio remoto. Todo archivo que delante tenga un "." son ocultos, y todo lo que no quiero que se suba lo incluyo por nombre en este archivo.

+ **pull request**: es una solicitud para fusionar cambios de una rama hacia otra (usualmente la rama principal). La plataforma GitHub compara los cambios y avisa si hay conflictos que deben resolverse antes de hacer el merge.
