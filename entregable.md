# Ingeniería del Software
# 2º Curso. Grado en Ingeniería Informática
# Escuela Politécnica Superior (Universidad de córdoba)
# Práctica 1. Introducción a Git, Markdown y Eclipse
## Grupo 22

---
---

## Contenidos

1. Git
    1. Introducción
    2. Instalación y configuración
    3. Uso básico
    4. Ramas
    5. GitHub
2. Markdown
    1. Introducción
    2. Código
3. Eclipse
    1. Introducción
    2. Instalación
4. Recursos

---

## Git y GitHub

>![logo_git](https://git-scm.com/images/logo@2x.png)
>
>Sistema para el control distribuido de versiones
>de código. Fundamentalmente permite:
>
>* Dar seguimiento a los cambios realizados sobre un archivo.
>* Almacenar una copia de los cambios.

<br>

>![logo_github](http://www.myiconfinder.com/uploads/iconsets/256-256-2412e9e2aeec1b5f9dee8ac0ec7bde93.png)
>
> Sitio web dónde podemos subir una copia de
nuestro repositorio Git.

---

### Ventajas

> **Git**
> * Habilidad de deshacer cambios.
> * Historial y documentación de cambios.
> * Múltiples versiones de código.
> * Habilidad de resolver conflictos entre versiones de distintos
>programadores.
> * Copias independientes.

<br>

> **GitHub**
> * Documentación de requerimientos.
> * Ver el avance del desarrollo.

---

### Instalación

* Para instalar Git: https://git-scm.com
* En el curso se utilizará Git a través de líneas de comandos.
* Para eclipse existen plugins integrados: https://www.eclipse.org/egit

### Configuración básica

**Nombre del administrador:**<br>
`git config --global user.name "ejemplo de nombre"`

**Correo electrónico:**<br>
`git config --global user.email <usuario>@uco.es`

**Editor de texto:**<br>
`git config --global core.editor "gedit"`

**Color de la interfaz:**<br>
`git config --global color.ui true`

**Listado de la configuración:**<br>
`git config --list`

---

### Comandos básicos

**Iniciar repositorio en un directorio:**<br>
`git init`

**Agregar cambios al área de *staging*:**<br>
`git add`

**Validar cambios en el repositorio:**<br>
`git commit -m "Mensaje"`

**Hacer los dos pasos anteriores en uno:**<br>
`git commit -am "Mensaje"`

**Historial de *commits*:**<br>
`git log`

**Ayuda del listado anterior:**<br>
`git help log`

**Listar los 5 *commits* más recientes:**<br>
`git log -n 5`

**Listar los *commits* desde una fecha:**<br>
`git log --since=2018-09-18`

**Listar los *commits* por autor:**<br>
`git log --author="Antonio"`

**Ver cambios en el directorio:**<br>
`git status`

**Ver diferencia entre ficheros en el directorio y el repositorio de git:**<br>
`git diff`

**Ver diferencia entre ficheros en el *staging* y el repositorio:**<br>
`git diff --staged`

**Eliminar archivos:**
~~~
git rm <archivo>
git commit -m "Mensaje"
~~~

**Mover o renombrar archivos:**
~~~
git mv <antiguo> <nuevo>
git commit -m "Mensaje"
~~~

**Deshacer cambios con git:**<br>
`git checkout -- nombre_fichero`

**Retirar archivos del *staging*:**<br>
`git reset HEAD nombre_fichero`

**Complementar último *commit*:**<br>
`git commit --amend -m "Mensaje"`

**Recuperar versión de un fichero de *commit* antiguo:**<br>
`git checkout <id_commit> -- nombre_archivo`

**Revertir un *commit*:**<br>
`git revert <id_commit>`

**Deshacer múltiples cambios en el repositorio:**
~~~
git reset --soft <id_commit>
git reset --mixed <id_commit>
git reset --hard <id_commit>
~~~

**Listar archivos que git no controla:**<br>
`git clean -n`

**Eliminar archivos que git no controla:**<br>
`git clean -f`

>Ignorar archivos en el repositorio: .gitignore

**Listar el contenido del repositorio de git:**
~~~
git ls-tree master
git ls-tree master^^^
git ls-tree master~3
~~~

**Log en una línea:**<br>
`git log --oneline`

**Log con los tres últimos *commits* en una línea:**<br>
`git log --oneline -3`

>Para más opciones consultar documentación de git.

**Examinar el contenido de un *commit*:**<br>
`git show <id>`

**Comparar un *commit* con el actual:**<br>
`git diff <id> nombre_archivo`

**Comparar dos *commits*:**<br>
`git diff id..id nombre_archivo`

---

### Ramas o *Branches*
<br>
![imagen_ramas](https://sdlambert.github.io/img/git-nodes.png)

<br>
Es la forma para separar la línea actual de desarrollo con respecto
a la principal. Normalmente representan versiones del software que
posteriormente son integradas a la línea principal.

### Comandos de Ramas

**Ver listado de ramas:**<br>
`git branch`

**Crear una rama:**<br>
`git branch <nombre_rama>`

**Cambiarnos a una rama:**<br>
`git checkout <nombre_rama>`

**Crear una rama y moverse en un paso:**<br>
`git checkout -b <nombre_rama>`

**Comparar ramas:**<br>
`git diff <nombre_rama1>..<nombre_rama2>`

**Ver ramas idénticas a la actual:**<br>
`git branch --merged`

**Renombrar ramas:**<br>
`git branch -m <nombre_antiguo> <nombre_nuevo>`

**Eliminar ramas:**
~~~
git branch -d <nombre_rama>
git branch -D <nombre_rama>
~~~

**Integrar ramas a la actual:**<br>
`git merge <nombre_rama>`

**Resolver conflictos** *(se suele hacer manualmente)* **:**<br>
`git merge --abort`

**Almacenar cambios temporales:**<br>
`git stash save "Mensaje"`

**Listar cambios:**<br>
`git stash list`

**Ver contenido de un cambio temporal:**<br>
`git stash show -p <nombre_stash>`

**Eliminar un cambio temporal:**<br>
`git stash drop <nombre_stash>`

**Aplicar cambio del *stash*:**
~~~
git stash apply <nombre_stash>
git stash pop <nombre_stash>
~~~

---

### GitHub
