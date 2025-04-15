#### GIT BASIS

### Create GIT repository
GIT --> all kind of language and repos

create directory

```
mkdir 11_GitRepo
cd 11_GitRepo
New-Item - Path "my_file.py"
code my_file.py  // abre en visual studio code
```

initialize new repository inside the repo. Creates git directory, it is hidden, si hacemos 'ls' no se ve
```
git init 
``` 

Para ver elementos ocultos:
```
ls -Force
```
Status of repository
```
git status
```

Antes de hacer commit se añaden todos los achivos o solo archivos que queremos añadir en el commit
```
git add .  //add all files
git add my_file.py // solo sube el archivo
```

Para hacer commit:

```
git commit -m "Initial commit"
```

### Push a Local Git Repository to GitHub

* Crear repositorio en github
* empujar el repositorio a remoto: 
``` 
git remote add origin git@github.com:arrese-a/git-module.git
```
* o con hhtps
```
git remote add origin https://github.com/arrese-a/git-module.git
```
Se pega eso en terminal (la primera opcion)
Probatzeko 

```
git remote -v

output: 
origin  https://github.com/arrese-a/git-module.git (fetch)
origin  https://github.com/arrese-a/git-module.git (push)
```

fetch --> si alguien cambia el repositorio remoto, para traerlo a local

```
git push -u origin master
```

Lleva todo lo que hemos hecho comit a la rama "master" del repositorio remoto

### Review of the Git Workflow

Si ya estamos en una rama, despues de hacer `git add` y `git commit -m`, se puede hacer solo `git push`

### Examining the Dot Git Directory

El diretorio puede ser de ayuda si se nos olvida algun comando o algo. Entraremos en detalle más adelante. 

hooks --> herramienta y proceso que se puede ejecutar en un tiempo especifico. scripts que se ejecutan automaticamente cuando ocurren ciertos eventos

info.exclude --> archivos que son excluidos del repositorio git

logs --> mensajes de commit que hemos hecho
logs.HEAD --> el logc

object --> objetos en memoria, normalmente no se toca
refs --> parecido a logs, referencias de verdad. refs.tagsno se suele tocar pero se puede usar para editar commits


### How to Hide Files and Directories from Git with gitignore

.gitignore --> todos los archivos que pongamos aqui no se subiran a github, no aparecen en git status, por lo que no se añaden ni se hace commit. es importante que se escriba el nombre de los archivos correctamente

con directorios tambien se puede



