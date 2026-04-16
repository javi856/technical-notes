# Comandos básicos de Git

Este documento recoge comandos básicos de **Git** usados para trabajar con proyectos locales y subirlos a **GitHub**.

## Configuración inicial

### Configurar nombre de usuario

`git config user.name "Tu Nombre"`

Sirve para indicar el nombre asociado a los commits.

### Configurar correo electrónico

`git config user.email "tu_correo@example.com"`

Sirve para indicar el correo asociado a los commits.

### Activar el gestor de credenciales en Windows

`git config --global credential.helper manager`

Sirve para facilitar el inicio de sesión con GitHub desde el navegador.

---

## Navegación básica

### Mostrar la ruta actual

`pwd`

Sirve para ver en qué carpeta estás trabajando.

### Ver archivos y carpetas

`ls`

Sirve para listar el contenido de la carpeta actual.

### Entrar en una carpeta

`cd nombre-del-repo`

Sirve para situarse dentro del proyecto local.

### Volver a la carpeta anterior

`cd ..`

Sirve para retroceder un nivel en la estructura de carpetas.

---

## Trabajo con repositorios

### Clonar un repositorio

`git clone URL_DEL_REPOSITORIO`

Ejemplo:

`git clone https://github.com/javi856/nombre-del-repo.git`

Sirve para descargar una copia local de un repositorio que ya existe en GitHub.

### Ver el repositorio remoto configurado

`git remote -v`

Sirve para comprobar a qué repositorio remoto está conectado el proyecto.

### Eliminar el remoto actual

`git remote remove origin`

Sirve para quitar la conexión con el repositorio remoto actual.

### Añadir un nuevo remoto

`git remote add origin https://github.com/javi856/nombre-del-repo.git`

Sirve para conectar el repositorio local con otro repositorio de GitHub.

---

## Estado y seguimiento de cambios

### Ver el estado del repositorio

`git status`

Sirve para comprobar:

- qué archivos han cambiado
- qué archivos son nuevos
- qué archivos están preparados para commit

### Añadir todos los cambios

`git add .`

Sirve para preparar todos los cambios antes de crear un commit.

### Añadir un archivo concreto

`git add nombre-del-archivo`

Sirve para preparar un archivo concreto en lugar de todos.

---

## Guardar cambios

### Crear un commit

`git commit -m "Mensaje del commit"`

Ejemplo:

`git commit -m "Subo proyecto inicial"`

Sirve para guardar un punto de control local con una descripción de los cambios.

---

## Subir cambios a GitHub

### Subir cambios por primera vez

`git push -u origin main`

Sirve para enviar los cambios del repositorio local a GitHub.

La opción `-u` establece la rama remota como referencia para futuros `push`.

### Subir cambios habituales

`git push`

Sirve para subir nuevos commits al repositorio remoto una vez ya está configurado.

### Subir a la rama `master`

`git push -u origin master`

Sirve para subir cambios cuando el repositorio usa `master` en lugar de `main`.

---

## Descargar cambios

### Descargar cambios del repositorio remoto

`git pull`

Sirve para traer al repositorio local los cambios más recientes de GitHub.

---

## Flujo básico de trabajo

1. `git clone URL_DEL_REPOSITORIO`
2. `cd nombre-del-repo`
3. `git status`
4. `git add .`
5. `git commit -m "Mensaje del commit"`
6. `git push -u origin main`

---

## Flujo habitual después de la primera subida

1. `git status`
2. `git add .`
3. `git commit -m "Descripción del cambio"`
4. `git push`

---

## Flujo para subir un proyecto local a un repo ya creado en GitHub

1. `git clone URL_DEL_REPOSITORIO`
2. `cd nombre-del-repo`
3. Copiar dentro los archivos del proyecto
4. `git status`
5. `git add .`
6. `git commit -m "Subo proyecto inicial"`
7. `git push -u origin main`

---

## Flujo para cambiar el repositorio remoto

1. `git remote -v`
2. `git remote remove origin`
3. `git remote add origin https://github.com/javi856/nombre-del-repo.git`
4. `git push -u origin main`

---

## Resumen rápido

- `pwd` → muestra la ruta actual
- `ls` → lista archivos y carpetas
- `cd` → entra en una carpeta
- `cd ..` → vuelve atrás
- `git clone` → descarga un repositorio de GitHub
- `git remote -v` → muestra el remoto configurado
- `git remote remove origin` → elimina el remoto actual
- `git remote add origin` → añade un nuevo remoto
- `git status` → muestra el estado de los archivos
- `git add .` → prepara los archivos para commit
- `git commit -m` → guarda los cambios localmente
- `git push` → sube los cambios a GitHub
- `git pull` → descarga cambios desde GitHub

---

## Observación

No conviene subir archivos de configuración local o temporales como:

- `.idea`
- `.gradle`
- `.kotlin`
- `local.properties`

Conviene usar `.gitignore` para excluir ese tipo de archivos.
