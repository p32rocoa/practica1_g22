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

## Github no es Git

![imagen_github](https://i.imgur.com/3B1kzDL.png)

---

### Comandos de Github

**Añadir repositorio remoto:**<br>
`git remote add origin url`

**Ver repositorios remotos:**<br>
`git remote -v`

**Eliminar repositorio remoto:**<br>
`git remote rm origin`

**Añadir cambios del repositorio local al remoto:**<br>
`git push -u origin master`

**Añadir cambios del repositorio remoto al local:**<br>
`git pull`

**Ver *branches* remotos:**<br>
`git branch -r`

**Ver todos los *branches*:**<br>
`git branch -a`

**Clonar un repositorio remoto:**<br>
`git clone url`

---

### Dar seguimiento a *branches* remotos

* LOCAL → REMOTO
> * 1º - Cambios en el repositorio local.
> * 2º - *Commit* de los cambios.
> * 3º - Añadir cambios a repositorio remoto:<br>
> `git push`

<br>

* REMOTO → LOCAL
> * Sincronización y unión:<br>
> `git fetch origin`<br>
> `git merge origin/master`
> * En un solo paso:<br>
> `git pull`

### Operaciones con branches remotos
* Creación:
> * 1º - Crear *branch* local.
> * 2º - Hacer cambios en dicho *branch*.
> * 3º - Hacer *commit*.
> * 4º - Copiar el *branch* al repositorio remoto:<br>
> `git push -u origin branch_remoto`
<br>
* Copia: <br>
`git checkout -b local remoto`

* Eliminación: <br>
`git push origin -- delete branch_remoto`

---

## Lenguaje Markdown
* Markdown es un lenguaje de etiquetado ligero que simplifica
la elaboración de documentos.

* Se ideó pensando en una herramienta para escribir páginas
web en un texto simple fácil de leer.

* Actualmente, se utiliza para documentar software ya que al
ser texto plano puede entrar dentro de cualquier sistema de
control de versiones e incluye muchas extensiones para
colorear código fuente en distintos lenguajes.

### Sintaxis

![imagen_sint1](https://i.imgur.com/hT1M11d.png)

![imagen_sint2](https://i.imgur.com/lhVNdXs.png)

---
## Eclipse

Eclipse es un entorno integrado de desarrollo (IDE).
 * Se diseñó inicialmente como IDE para Java, sin embargo ahora soporta otros lenguajes como C++.

 * Ayuda a escribir código más rápido y libre de algunos errores sintácticos, y ayuda a mantener un estilo de programación homogéneo.

* Facilita la depuración de código.

* Hay una gran documentación.

### Instalación

* Utilizaremos eclipse para C++.<br>
[Eclipse para C++<br>](https://www.eclipse.org/downloads/packages/release/photon/r/eclipse-ide-cc-developers)
* Para eclipse existen plugins integrados con git.<br>
https://www.eclipse.org/egit

---

## Recursos
Recursos Git:

* [Guía sencilla de Git.](http://rogerdudler.github.io/git-guide/index.es.html)
* [Pro Git book.](https://git-scm.com/book/en/v2)<br>

Recursos Markdown:
* [Markdown Cheatsheet.](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
* [Guía en castellano extendida.](https://joedicastro.com/pages/markdown.html)<br>

Recursos Eclipse:
* En las aulas se puede cargar con la orden eclipse3.3
* [Eclipse para C++](https://www.eclipse.org/downloads/packages/release/photon/r/eclipse-ide-cc-developers)
