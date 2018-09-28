
---

## Github no es Git

![imagen_github](https://i.imgur.com/3B1kzDL.png)

---

## Comandos de Github

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

**Ver branches remotos:**<br>
`git branch -r`

**Ver todos los branches:**<br>
`git branch -a`

**Clonar un repositorio remoto:**<br>
`git clone url`

---

## Dar seguimiento a branches remotos

* LOCAL → REMOTO
> * 1º - Cambios en el repositorio local.
> * 2º - Commit de los cambios.
> * 3º - Añadir cambios a repositorio remoto:<br>
> `git push`

<br>

* REMOTO → LOCAL
> * Sincronización y unión:<br>
> `git fetch origin`<br>
> `git merge origin/master`
> * En un solo paso:<br>
> `git pull`

## Operaciones con branches remotos
* Creación:
> * 1º - Crear branch local.
> * 2º - Hacer cambios en dicho branch.
> * 3º - Hacer commit.
> * 4º - Copiar el branch al repositorio remoto:<br>
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

---

### Instalación

* Utilizaremos eclipse para C++.<br>
[Eclipse para C++<br>](https://www.eclipse.org/downloads/packages/release/photon/r/eclipse-ide-cc-developers)
* Para eclipse existen plugins integrados con git.<br>
https://www.eclipse.org/egit

### Recursos
