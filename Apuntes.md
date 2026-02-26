<!-- Dia 1 -->
# LENGUAJE MARKDOWN E INICIACIÓN A GIT

Antes de empezar, el markdown es un
lenguaje de marcaje ligero
que utiliza caracteres de puntuación simples
(asteriscos, almohadillas, guiones) para dar
formato al texto plano, siendo fácil de leer
y convirtiéndose fácilmente a HTML, PDF o DOCX.
Es ampliamente utilizado para documentación técnica, repositorios Git, notas y blogs.

## Lista de los elementos basicos del md

### Headings

# Heading level 1

## Heading level 2

### Heading level 3

#### Heading level 4

##### Heading level 5

###### Heading level 6

---

### Texto bold (negritas)

I just love **bold text**.
Love**is**bold

---

### Texto italico

Italicized text is the *cat's meow*.
A *cat* meow.

---

### Texto en negrita y cursiva

This text is ***really important***.
This is really***very***important text.

---

### Citas en bloque

> Dorothy followed her through many of the beautiful rooms in her castle.
>
>> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

---

### Listas desordenadas

- First item
- Second item
- Third item
- Fourth item

---

### Texto como codigo

At the command prompt, type `nano`.

---

### Bloques de codigo

```java
System.out.println("Hola Mundo");
```

---

### URLs

<https://www.markdownguide.org>
<fake@example.com>

---

### Formato de enlaces

I love supporting the **[EFF](https://eff.org)**.
This is the *[Markdown Guide](https://www.markdownguide.org)*.
See the section on [`code`](#code).

---

### Imagenes

![Gatito fiesta](./fotos/Zafrafiesta.webp)

---
---

## Inicio a Git

### Pasos para iniciar

El primer paso que vamos a necestiar para
empezar a usar Git. Es un usuario y un email,
para ello el comando fundamental para configurar cualquier
cosa de git es:

- `git config --global user.name "tuUsuario"`

este comando abre la configuracion de git de forma global,
es decir, para todos los usuarios del equipo en uso y crea un usuario "tuUsuario".

- `git config --global user.email "tuUsuario@email"`

Este comando es para agregar el email de tu usuario.

Ya con esto, para inicializar un repositorio git en un directorio que nosotros queramos, nos ubicamos dentro del directorio y ahí podemos usar el comando:

- `git init`

Con esto iniciamos git en ese directorio en un branch llamado "master".

---

### Commits

Por el momento empezaremos a trabajar en una rama llamada master, que es la
copia definitiva de el proyecto.

Para poder empezar a subir cambios de nuestros archivos, tenemos que entender
primero que todo lo que modifiquemos o que creamos, está trabajándose localmente,
es decir, no afectará al repositorio, en cambio si queremos guardar cambios de los
archivos, tenemos que poner estos archivos en algo llamado  "staging area".

Este básicamente es un área intermedia entre tu directorio de trabajo y el
repositorio donde preparas los cambios para que se hagan efectivos con un commit.
Para poner archivos en esta area, se usa el comando:

- `git add tuarchivo.ext`

Con esto, ahora el archivo está en el staging area.

Para manejar mejor estas adiciones, se usa el comando:

- `git status`

Que lo que hace es mostrar el estado actual de tu repositorio, detallando qué archivos han sido modificados, cuáles están preparados para el siguiente commit (staging area) y cuáles no están siendo rastreados.

Si ya estamos listos para que estos cambios sean efectuados, podemos hacer un commit
y con esto actualizar la "versión" o "copia" de nuestro proyecto en nuestra
rama master, esto con el siguiente comando:

- `git commit -m "Un mensaje obligatorio para tu commit"`

Y con esto ya tenemos nuestra primer versión de nuestro proyecto en nuestro
repositorio, cabe recalcar que cada versión que subamos tendrá un identificador
único.

Para ver el historial de los commits junto con la información de los mismos
podemos usar el comando:

- `git log`

Este comando fundamental de Git utilizado para visualizar el historial de confirmaciones (commits) de un repositorio, mostrando cronológicamente (del más reciente al más antiguo) el identificador (hash SHA), autor, fecha y mensaje de cada cambio.

Si tenemos modificado un archivo pero queremos devolerlo a como estaba en
el último commit realizado, podemos usar el comando:

- `git restore tuarchivo`

El cual descarta cambios que no se pusieron en el área de staging.

En cambio si lo que buscamos es deshacer todos los cambios locales
del repositorio, usamos el comando

- `git reset`

El cual mueve el puntero de la rama (HEAD) a una confirmación (commit) anterior y ajustando el área de preparación (staging area) y el directorio de trabajo según el modo utilizado (--soft, --mixed, --hard). Actúa como una máquina del tiempo para reescribir la historia localmente, siendo la opción --hard la más drástica al eliminar cambios no confirmados.

Principales modos de git reset:

- soft: Mueve el HEAD al commit especificado, pero mantiene tus cambios actuales en el área de preparación (listos para un nuevo commit).
- mixed (predeterminado): Mueve el HEAD y restablece el área de preparación al commit indicado, pero mantiene los cambios en el directorio de trabajo como archivos no modificados (unstaged).
- hard: Mueve el HEAD, restablece el área de preparación y el directorio de trabajo al commit especificado. Borra todos los cambios no confirmados, por lo que es una operación destructiva.

asdf

---

### Branches

Las ramas (branches) en Git son punteros ligeros y móviles hacia los commits,permitiendo crear entornos de trabajo aislados, paralelos y seguros, sin afectar la rama principal (main/master). Facilitan el desarrollo de nuevas funcionalidades, pruebas o correcciones, permitiendo fusionar cambios posteriormente.
