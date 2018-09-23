# Ingeniería Software
# 2º Curso. Grado en Ingeniería Informática
# Escuela Politécnica Superior (Universidad de córdoba)
# Práctica 1. Introducción a Git, Markdown y Eclipse
## Grupo 22

---
---

## Contenidos

1. Git
    1. Introducción.
    2. Instalación y configuración.
    3. Uso básico.
    4. Ramas
    5. GitHub
2. Markdown
    1. Introducción.
    2. Código.
3. Eclipse
    1. Introducción.
    2. Instalación.
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

## Ventajas

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

## Instalación

* Para instalar Git: https://git-scm.com
* En el curso se utilizará Git a través de líneas de comandos.
* Para eclipse existen plugins integrados: https://www.eclipse.org/egit

## Configuración básica

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

## Comandos básicos

**Iniciar repositorio en un directorio:**<br>
`git init`

**Agregar cambios al área de staging:**<br>
`git add`

**Validar cambios en el repositorio:**<br>
`git commit -m "Mensaje"`

**Hacer los dos pasos anteriores en uno:**<br>
`git commit -am "Mensaje"`

**Historial de commits:**<br>
`git log`
