# Explicar cada comando

La idea es que yo tengo un repositorio local y voy enviando los cambios que quiera al remoto. Allí deben ser aceptados si no hay problemas.

---
## git es control de versiones
## github es el sitiopara trabajar en equipo con git, son repositorios remotos
``` Configuraciones
git config user.name
git config --global user.name""
git config --global user.email""
```

---
# `git init` : inicializa un repositorio local en la PC.
# `git remote add oriin www...`: conecta el repositorio local al de la nube.
---
## `git clone <URL-del-repositorio>`

Clona el repositorio remoto que creamos en GitHub.

---

### `git branch`

Muestra en qué rama estamos trabajando actualmente.

---
### `git branch -M`

Crea una nueva rama

---
### `git switch <nombre-rama>`

Cambia a la rama en la que deseamos trabajar.

---

### `git add <nombre-archivo>`

Agrega el archivo al *staging area* (área de preparación) para que esté listo para el commit. Lo agrega para enviar a la nube.

---

### `git add .`

Agrega **todos los archivos modificados o nuevos** al staging area.

---

### `git commit -m "mensaje"`

Toma los archivos que marcaste con `git add` (los *staged files*) y los guarda como un nuevo *snapshot* del proyecto, con un mensaje descriptivo de lo que hiciste. Envia la info a la nube.

---

### `git push`

Sube tus cambios locales al repositorio remoto. Toma los commits que hiciste localmente con `git commit` y los envía al servidor remoto (por ejemplo, GitHub).

---

### `git remote -v`

Muestra a qué repositorio remoto está conectado tu repositorio local (y con qué URL).

---

### `git fetch`

Trae los cambios del repositorio remoto **pero no los aplica** a tu rama actual. Sirve para ver si hay cambios nuevos en el remoto antes de hacer un `merge` o un `pull`.

---

### `git pull`: me trae informacion
---
### `.gitignore`: archivos ignorados al utilizar git add .
--- 
### `pull request`: compara si hay conflictos con los cambios que se producen en una rama con la rama principal. 
