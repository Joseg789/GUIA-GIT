# Comandos de Git Explicados

## Configuración Inicial

- `git config --global user.name "Tu Nombre"`  
   Configura tu nombre de usuario globalmente.

- `git config --global user.email "tu@email.com"`  
   Configura tu correo electrónico globalmente.

## Repositorios

- `git init`  
   Inicializa un nuevo repositorio Git en el directorio actual.

- `git clone <url>`  
   Clona un repositorio remoto en tu máquina local.

## Cambios y Versiones

- `git status`  
   Muestra el estado de los archivos (modificados, sin seguimiento, etc.).

- `git add <archivo>`  
   Añade archivos al área de preparación (staging area).

- `git add .`  
   Añade todos los archivos modificados al área de preparación.

- `git commit -m "mensaje"`  
   Guarda los cambios preparados con un mensaje descriptivo.

- `git commit -am "mensaje"`  
   Añade y guarda todos los archivos rastreados en un solo paso.

- `git log`  
   Muestra el historial de commits.

- `git diff`  
   Muestra las diferencias entre archivos modificados y el último commit.

## Ramas (Branches)

- `git branch`  
   Lista todas las ramas.

- `git branch <nombre>`  
   Crea una nueva rama.

- `git checkout <nombre>`  
   Cambia a la rama especificada.

- `git checkout -b <nombre>`  
   Crea y cambia a una nueva rama.

- `git merge <rama>`  
   Fusiona la rama especificada en la rama actual.

- `git branch -d <nombre>`  
   Elimina la rama especificada.

## Repositorio Remoto

- `git remote add origin <url>`  
   Añade un repositorio remoto llamado "origin".

- `git remote -v`  
   Muestra los repositorios remotos configurados.

- `git push origin <rama>`  
   Envía los commits de la rama local al repositorio remoto.

- `git push -u origin <rama>`  
   Envía la rama y la configura para hacer futuros push/pull fácilmente.

- `git pull`  
   Descarga y fusiona los cambios del repositorio remoto.

- `git fetch`  
   Descarga los cambios del repositorio remoto sin fusionar.

## Otros Comandos Útiles

- `git reset --hard <commit>`  
   Restaura el repositorio al commit especificado, perdiendo cambios posteriores.

- `git stash`  
   Guarda temporalmente los cambios no confirmados.

- `git stash pop`  
   Recupera los cambios guardados con `stash`.

- `git rm <archivo>`  
   Elimina un archivo del repositorio y del sistema de archivos.

- `git mv <archivo1> <archivo2>`  
   Renombra o mueve un archivo.
- git config core.autocrlf true

---

> Estos son los comandos más usados y sus explicaciones. Puedes profundizar en cada uno con `git help <comando>`.
