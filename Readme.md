<div align="center">
  <img height="200" src="https://avatars.githubusercontent.com/u/2975064?s=200&v=4"  />
</div>

###

<h1 align="center">Curso Profesional Git y GitHub</h1>

###

## Tabla de Contenido

- [¿Qué es Git?](#qué-es-git)
- [Comandos más comunes](#comandos-más-comunes)
  - [Comandos Básicos](#comandos-básicos)
  - [Ramas y Branching](#ramas-y-branching)
  - [Comparación y Revisión](#comparación-y-revisión)
  - [Historial y Blame](#historial-y-blame)
  - [Comandos Avanzados](#comandos-avanzados)
  - [Comandos para Configuración](#comandos-para-configuración)
  - [Comandos para SSH y Alias](#comandos-para-ssh-y-alias)
  - [Otros Comandos Útiles](#otros-comandos-útiles)
- [Estados del Archivo](#estados-del-archivo)
- [Conclusión](#conclusión)

###

### ¿Qué es Git? <a name="qué-es-git"></a>

Git es un sistema de control de versiones distribuido que permite gestionar el historial de los archivos en un proyecto. Su principal ventaja es la posibilidad de trabajar de manera colaborativa y mantener un registro de todos los cambios realizados en el código fuente.

## Comandos más comunes <a name="comandos-más-comunes"></a>

### Comandos Básicos <a name="comandos-básicos"></a>

- **`git --help`**: Muestra la ayuda de Git.
- **`git init`**: Inicializa un nuevo repositorio en el directorio actual.
- **`git add <archivo>`** o **`git add .`**: Agrega los cambios al área de preparación (staging). El `.` agrega todos los cambios realizados.
- **`git commit -m "mensaje"`**: Realiza un commit de los cambios preparados con un mensaje descriptivo.
- **`git commit -am "mensaje"`**: Realiza un commit de los cambios en archivos ya existentes sin necesidad de usar `git add`.
- **`git commit --amend`**: Modifica el último commit realizado. Puedes cambiar el mensaje o agregar nuevos cambios a ese commit.
- **`git show`**: Muestra el historial de commits.
- **`git log <archivo>`**: Muestra el historial de cambios de un archivo específico.
- **`git log --stat`**: Muestra información sobre los cambios realizados en los archivos desde el último commit.
- **`git status`**: Muestra el estado actual de los archivos, indicando cuáles han sido modificados, cuáles están listos para commit, etc.
- **`git push`**: Envía los cambios al repositorio remoto.
- **`git fetch`**: Obtiene los cambios del repositorio remoto sin fusionarlos con tu rama local.
- **`git pull`**: Obtiene los cambios del repositorio remoto y los fusiona automáticamente con la rama actual.
- **`git remote add <URL>`**: Vincula el repositorio local con un repositorio remoto.
- **`git remote -v`**: Muestra las URLs de los repositorios remotos vinculados.
- **`git pull origin <rama>`**: Obtiene los cambios de una rama específica del repositorio remoto.

### Ramas y Branching <a name="ramas-y-branching"></a>

- **`git branch <nombre>`**: Crea una nueva rama.
- **`git branch`**: Muestra todas las ramas locales del repositorio.
- **`git branch -d <nombre>`**: Elimina una rama local.
- **`git branch -r`**: Muestra las ramas remotas.
- **`git branch -a`**: Muestra todas las ramas locales y remotas.
- **`git checkout <nombre de la rama>`**: Cambia de rama.
- **`git merge <nombre de la rama>`**: Fusiona los cambios de otra rama con la rama actual.

### Comparación y Revisión <a name="comparación-y-revisión"></a>

- **`git diff <commit1> <commit2>`**: Muestra las diferencias entre dos commits.
- **`git show-branch`**: Muestra las ramas y su historial de commits.
- **`git tag -a <nombre del tag> -m "mensaje"`**: Crea un tag con un mensaje descriptivo en el commit especificado.
- **`git push origin --tags`**: Envía los tags creados al repositorio remoto.
- **`git tag -d <nombre del tag>`**: Elimina un tag local.
- **`git push origin :refs/tags/<nombre del tag>`**: Elimina un tag remoto.

### Historial y Blame <a name="historial-y-blame"></a>

- **`git log --all --graph`**: Muestra el historial de commits en forma de gráfico.
- **`git blame <archivo>`**: Muestra qué persona y qué commit modificaron cada línea de un archivo.
- **`git shortlog`**: Muestra los commits realizados por cada colaborador en el proyecto.
- **`git shortlog -sn`**: Muestra la cantidad de commits realizados por cada colaborador.
- **`git shortlog -sn --all --no-merges`**: Muestra los commits realizados por cada colaborador, excluyendo los merges.

### Comandos Avanzados <a name="comandos-avanzados"></a>

- **`git cherry-pick <commit>`**: Aplica un commit específico de otra rama a la rama actual.
- **`git reflog`**: Muestra el historial de todos los cambios, incluso los eliminados.
- **`git reset --hard <commit>`**: Restaura el repositorio al estado de un commit específico.
- **`git grep <palabra>`**: Busca una palabra o expresión en el repositorio.
- **`git grep -n <palabra>`**: Busca una palabra en el repositorio y muestra el número de línea.
- **`git grep -c <palabra>`**: Cuenta cuántas veces se utiliza una palabra en los archivos del repositorio.

### Comandos para Configuración <a name="comandos-para-configuración"></a>

- **`git clone <URL>`**: Clona un repositorio remoto en tu máquina local.
- **`git stash`**: Guarda los cambios no confirmados temporalmente.
- **`git stash pop`**: Recupera los cambios guardados en el stash y los aplica a la rama actual.
- **`git stash drop`**: Elimina un cambio guardado en el stash.
- **`git clean -f`**: Elimina archivos no rastreados en el directorio de trabajo.
- **`git rebase <rama>`**: Reescribe el historial de commits y fusiona ramas de una forma más limpia.

### Comandos para SSH y Alias <a name="comandos-para-ssh-y-alias"></a>

#### Configuración SSH

- **`ssh-keygen -t rsa -b 4096 -C "correo@dominio.com"`**: Genera una nueva clave SSH.
- **`eval $(ssh-agent -s)`**: Inicia el agente SSH.
- **`ssh-add ~/.ssh/id_rsa`**: Añade la clave SSH al agente.

#### Crear un Alias

- **`alias <nombre_del_alias>="git log --all --graph --decorate --oneline"`**: Crea un alias para un comando de Git.
- **`git config --global alias.<nombre_del_alias> "hortlog -sn --all --no-merges"`**: Configura el alias globalmente para que puedas usarlo como un comando corto.

### Otros Comandos Útiles <a name="otros-comandos-útiles"></a>

- **`git remote add upstream <URL del repositorio original>`**: Agrega el repositorio original como una fuente para traer cambios.
- **`git pull upstream master`**: Trae los cambios del repositorio original a tu rama local.

## Estados del Archivo <a name="estados-del-archivo"></a>

Los archivos en Git pueden estar en diferentes estados a lo largo del proceso:

- **Directorio** → **Staging** → **Repositorio**  
  - **Staging**: Es el área temporal donde se guardan los archivos antes de hacer un commit. Es similar a la memoria RAM, donde se almacenan los cambios pendientes.

## Conclusión <a name="conclusión"></a>

Git es una herramienta poderosa que te permite controlar y gestionar el código de manera eficiente. Utilizando los comandos adecuados, puedes gestionar fácilmente tu flujo de trabajo y colaborar con otros en proyectos de desarrollo.
