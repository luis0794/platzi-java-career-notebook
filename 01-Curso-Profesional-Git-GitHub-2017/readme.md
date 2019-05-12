# Curso profesional de Git y Github (Handbook)

## Configuraciones Generales

### Configurando nombre y correo
```
git config --global user.name "[USERNAME]"
```
```
git config --global user.email [EMAIL]
```

### Estableciendo editor por defecto
```
git config --global core.editor "nano --wait"
```
```
git config --global core.editor nano
```

### Configurando herramienta de diferencias
```
git config --global merge.tool vimdiff
```

### Listando configuraciones
```
git config --list
```

### Verificando el valor de una configuración
```
git config user.name
``` 


## Limbo  

### Elimina archivos unicamente del stage
```
git rm --cached [FILE]
```

### Muestra el estado de los archivos
```
git status
```

### Agrega archivos del stage al ultimo commit
```
git commit --amend
```


## Etiquetas

### Establece una etiqueta pesada al ultimo commit
```
git tag -a 0.5 -m [MENSAJE]
```

### Muestra el log de commits
```
git log
```

### Establece un tag para un commit
```
git tag 1.0 [SHA 1]
```

### Renombra un tag con el SHA-1 de un commit
```
git tag -f -a 0.1 -m [MENSAJE] [SHA 1]
```

### Lista los tags
```
git tag -l
```

### Elimina un tag
```
git tag -d 1.0
```


## Git Log

### Vista de logs resumida
```
git log --oneline
```

### El grafico de como avanza el proyecto
```
git log --oneline --graph
```

### Para el numero de commit a ver -> dependiendo de la cantidad de logs
```
git log -3
```


## Git Diff

### Que ha cambiando entre el estado actual y el commit seleccionado
```
git diff [SHA 1]
```

### Diferencia entre 2 commits
```
git diff [SHA 1] [SHA 1]
```
```
git diff [version-1] vs [version-2]
```


## Git Reset

### Elimina los cambios hasta el staging area
```
git reset --soft [SHA 1]
```

### Elimina los cambios hasta el working area
```
git reset --mixed [SHA 1]
```

### Regresa hasta el commit del [SHA 1]
```
git reset --hard [SHA 1]
```

### Descarta cambios de un archivo
```
git reset HEAD [FILE]
```

### Regresa al ultimo commit descartando todos los cambios
```
git reset --hard
```

### Regresa a un commit en específico
```
git reset --hard [SHA 1]
```

### En caso de querer volver a un commit futuro luego de hcer un reset hard
```
git reset --hard [SHA 1]
```


## Git Branch

### Crea una rama
```
git branch [BRANCH NAME]
```

### Lista las ramas
```
git branch -l
```

### Borra ramas
```
git branch -d [BRANCH NAME]
```

### Borra ramas forzandolo
```
git branch -D [BRANCH NAME]
```

### Renombra rama 
```
git branch -m [OLD NAME] [NEW NAME]
```


## Git Checkout

### Para cambiar de rama
```
git checkout [BRANCH TO MOVE]
```

### Para cambiar a un commit, solo se retorna al commit
```
git checkout [SHA 1]
```

### Para crear una rama y cambiar a ella de inmediatamente
```
git checkout -b [BRANCH NAME]
```


## Git Merge

### Estrategias de mezcla
* Fast-Forward
* Recursive

### Mezclar rama. Se debe estar en la rama en la que se dese impactar los cambios
```
git merge [BRANCH WITH CHANGES]
```


## Git Rebase

### Impacta cambios en el momento que se creò enla linea de tiempo
```
git rebase [BRANCH TO IMPACT]
```
```
git rebase -i [BRANCH TO IMPACT]
```


## Git Stash
_Es otro de los limbos, como el staging area. Para agregar los cambios estos deben estar en el staging area.

### Para crear un stash
```
git stash
```

### Nos muestra la lista de stash que tengamos.
```
git stash list
```

### Nos permite borrar un stash.
```
git stash drop stash@{[NUMERO]}
```

### Aplicamos el último cambio
```
git stash apply
```


## Cherry Pick

### Para quitar cambios de una modificación
```
git checkout -- [BRANCH NAME]
```

### Para sacar un commit
```
git cherry-pick [SHA 1]
```