
---

## Github no es Git

![imagen_ramas](https://i.imgur.com/3B1kzDL.png)

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
> * Cambios en el repositorio local.
> * Commit de los cambios.
> * Añadir cambios a repositorio remoto:<br>
> `git push`

<br>

* REMOTO → LOCAL
> * Sincronización y unión:<br>
> `git fetch origin`<br>
> `git merge origin/master`
> * En un solo paso:<br>
> `git pull`
