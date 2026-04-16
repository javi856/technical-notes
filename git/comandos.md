# Comandos básicos de Git

Resumen práctico de comandos básicos de **Git** para trabajar con proyectos locales y subirlos a **GitHub**.

## Configuración inicial

`git config user.name "Tu Nombre"`  
Configura el nombre asociado a los commits.

`git config user.email "tu_correo@example.com"`  
Configura el correo asociado a los commits.

`git config --global credential.helper manager`  
Facilita la autenticación con GitHub desde Windows.

## Navegación básica

`pwd`  
Muestra la ruta actual.

`ls`  
Lista archivos y carpetas.

`cd nombre-del-repo`  
Entra en una carpeta.

`cd ..`  
Vuelve a la carpeta anterior.

## Comandos principales

`git clone URL_DEL_REPOSITORIO`  
Descarga una copia local de un repositorio de GitHub.

`git status`  
Muestra el estado de los archivos del repositorio.

`git add .`  
Prepara todos los cambios para el commit.

`git commit -m "Mensaje del commit"`  
Guarda los cambios localmente con una descripción.

`git push -u origin main`  
Sube los cambios a GitHub por primera vez.

`git push`  
Sube cambios habituales después de la primera subida.

`git pull`  
Descarga cambios del repositorio remoto.

## Repositorio remoto

`git remote -v`  
Muestra el repositorio remoto configurado.

`git remote remove origin`  
Elimina el remoto actual.

`git remote add origin https://github.com/javi856/nombre-del-repo.git`  
Añade un nuevo repositorio remoto.

## Flujo básico

1. `git clone URL_DEL_REPOSITORIO`
2. `cd nombre-del-repo`
3. `git status`
4. `git add .`
5. `git commit -m "Mensaje del commit"`
6. `git push -u origin main`

## Flujo habitual

1. `git status`
2. `git add .`
3. `git commit -m "Descripción del cambio"`
4. `git push`

## Observación

No conviene subir archivos temporales o de configuración local como `.idea`, `.gradle`, `.kotlin` o `local.properties`.
