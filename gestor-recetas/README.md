##Documentacion##

#Ramas creadas y respuestas#
- feature/recetas-colombianas
- feature/recetas-mexicanas
- feature/recetas-italianas
- rama-conflicto
- main

#Comandos ejecutados#
git init

# Clonar repositorio
git clone https://github.com/Ferfelipe30/gestor_recetas.git

# Ver estado del repositorio
git status

# Ver historial de commits
git log
git log --oneline
git log --graph --oneline --all

# Agregar archivos al staging area
git add <archivo>
git add .                    # Agregar todos los archivos
git add *.js                 # Agregar archivos específicos

# Hacer commit
git commit -m "Mensaje descriptivo del commit"
git commit -am "Mensaje"     # Agregar y commitear archivos modificados

# Ver diferencias
git diff                     # Ver cambios no agregados
git diff --staged           # Ver cambios en staging area
git diff HEAD~1             # Ver cambios del último commit


### Ramas (Branches)
# Ver ramas
git branch
git branch -a               # Ver todas las ramas (locales y remotas)

# Crear y cambiar a nueva rama
git checkout -b <nombre-rama>
git switch -c <nombre-rama> # Comando más moderno

# Cambiar entre ramas
git checkout <nombre-rama>
git switch <nombre-rama>    # Comando más moderno

# Eliminar rama
git branch -d <nombre-rama>
git branch -D <nombre-rama> # Forzar eliminación

# Agregar repositorio remoto
git remote add origin <url>

# Ver repositorios remotos
git remote -v

# Subir cambios
git push origin <rama>
git push -u origin <rama>   # Establecer upstream

# Bajar cambios
git pull origin <rama>
git fetch origin            # Solo descargar sin fusionar

# Clonar rama específica
git clone -b <rama> <url>

# Merge (fusionar rama actual con la especificada)
git merge <rama>

# Rebase (reorganizar commits)
git rebase <rama>

# Descartar cambios en archivo
git checkout -- <archivo>
git restore <archivo>       # Comando más moderno

# Descartar cambios en todos los archivos
git checkout -- .
git restore .               # Comando más moderno

# Deshacer último commit (mantener cambios)
git reset --soft HEAD~1

# Deshacer último commit (descartar cambios)
git reset --hard HEAD~1

# Revertir commit (crear nuevo commit)
git revert <hash-commit>

# Guardar cambios temporalmente
git stash
git stash push -m "Mensaje descriptivo"

# Ver stashes guardados
git stash list

# Aplicar stash
git stash pop              # Aplicar y eliminar
git stash apply stash@{0}  # Aplicar sin eliminar

# Eliminar stash
git stash drop stash@{0}
git stash clear            # Eliminar todos

# Crear tag
git tag <nombre-tag>
git tag -a <nombre-tag> -m "Mensaje"  # Tag anotado

# Ver tags
git tag

# Subir tags
git push origin --tags

# Ver qué rama contiene un commit
git branch --contains <hash>

# Ver quién modificó una línea
git blame <archivo>

# Buscar en el historial
git log -S "texto-buscado"
git log --grep "patrón"

# Ver archivos de un commit
git show --name-only <hash>

# Crear rama para nueva funcionalidad
git checkout -b feature/nueva-funcionalidad

# Trabajar en recetas específicas
git checkout -b feature/recetas-colombianas
git checkout -b feature/recetas-mexicanas
git checkout -b feature/recetas-italianas

# Subir cambios de una rama
git push origin feature/recetas-colombianas

# Fusionar rama de feature a main
git checkout main
git merge feature/recetas-colombianas
git push origin main

#Capturas de pantalla de PRs, merges y resolucion de conflictos.


