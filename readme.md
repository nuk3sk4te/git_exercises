# GIT Ejercicios (Katas)

## Propósito de estos ejercicios

Este repositorio es una colección de ejercicios de Git

Los ejercicios son diseñados para aprendizaje de Git, y para practicar el uso de Git en un ambiente de equipo.


## Sugerido camino de aprendizaje

La siguiente lista indica el orden en el que se deberían seguir los ejercicios para su aprendizaje.

- [01. Commits primeros pasos](./ejercicios/01.Commit-primeros-pasos/README.md)
- [02. Trabajo area staging](./ejercicios/02.Trabajo-area-staging/README.md)
- [03. Trabajo con ramas](./ejercicios/03.Trabajo-con-ramas/README.md)
- [04. Mergear ramas tipo Fast-Forward](./ejercicios/04.Mergear-ramas/README.md)
- [05. Mergear ramas tipo 3-way](./ejercicios/05.Anexar-ramas-otras-formas/README.md)
- [06. Resolver conflictos](./ejercicios/06.Anexar-conflicto/README.md)
- [07. Revertir cambios](./ejercicios/07.Rebase-rama/README.md)
- [08. Rebase interactivo](./ejercicios/08.Revertir-cambios/README.md)
- [09. Resetear cambios](./ejercicios/09.Reset/README.md)


## Chuleta de comandos

Una colección de comandos útiles para usar en todos los ejercicios y en el día a día:

```shell
# Inicializar un vacio repositorio.
git init            # Inicializa una vacio repositorio en el actual directorio.

# Clonar repositorio
git clone https://github.com/praqma-training/git-katas.git      # Clone el repositorio url y crea un directorio con el repo del repositorio

# Git (usuario and repositorio nivel) configuraciones
git config --local user.name "Repo-level Username"          # For setting a local git repo level user name.
git config --local user.email "Repo-level.Email@Example.com" # For setting a local git repo level user email.
                                                            # --global -> User level git config stored in <user-home>/.gitconfig for e.g. ~/.gitconfig
                                                            # --local -> repo level config stored in repo's main dir under .git/config


# Ver cambios en local
git status                  # Muestra el estado del directorio-trabajo
git diff                    # Muestra cambios en el actual directorio-trabajo (aún no staged)
git diff --cached           # Muestra cambios actualmente staged para commit

# Agregar ficheros al staging (anges de hacer commit)
git add myfile.txt          # Agregar myfile.txt al stage
git add .                   # Agregar el directorio de trabajo completo al stage

# Hacer commits
git commit                              # Hace un nuevo commit con los cambios en el area de staging. Abrirá el editor para agregar un mensaje.
git commit -m "I love documentation"    # Hace un nuevo commit con los cambios en el area de staging. Usa el mensaje dado.
git commit -a                           # Hace un nuevo commit y automaticamente agregar los cmabios para todos los ficheros conocidos por git
git commit -am "I still do!"            # Una combinación de las 2 opciones anteriores
git commit --amend                      # Rehace el commit message del previos commit (sino está subido al remoto)
                                        #  Nunca cambiar la historia pública
git reset <file>                        # Unstage un fichero agregado al area de staging para dejarlo en el directorio-trabajo sin perder ningún cambio.
git reset --soft [commit_hash]          # Resetea la actual rama. No toca el staging area o el arbol de directorios en nada.
                                        # --hard modo debería descartar todos los cambios.

# Configurando un diferente editor
- `git config --global core.editor nano`

## Para Windows:
- Use Notepad:
`git config --global core.editor notepad`

- or for instance Notepad++:
`git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"`


# Revisar historial
git log             # Muestra el historial de commits
git log --oneline   # Formatear commits a una single linea (atajo para --pretty=oneline  --abbrev-commit)
git log --graph     # Mostrar un grafico de los commits y ramas
git log --pretty=fuller     # Ver la historia de los comits de forma detallada con autor y detalles del commit.
git log --follow <file>     # Lista la historia de un fichero más alla de los renombradosrenames
git log branch2..branch1    # Muestra commits alcanzables desde rama1 pero no en la rama2

# Defiriendo
git stash                               # Stash (store temporarily) changes in working branch and enable checkingout a new branch
git stash list                          # List stored stashes.
git stash apply <stash>                 # Apply given <stash>, or if none given the latest from stash list.


# Working with Branches
git branch my-branch       # Create a new branch called my-branch
git switch my-branch     # Switch to a different branch to work on it
git switch -c my-branch  # Create a new branch called my-branch AND switch to it
git branch -d my-branch    # Delete branch my-branch that has been merged with master
git branch -D my-branch    # Forcefully delete a branch my-branch that hasn't been merged to master

# Merging
git merge master         # Merge the master branch into your currently checked out branch.
git rebase master        # Rebase current branch on top of master branch

# Working with Remotes
git remote              # Show your current remotes
git remote -v           # Show your current remotes and their URLs
git push                # Publish your commits to the upstream master of your currently checked out branch
git push -u origin my-branch  # Push newly created branch to remote repo setting up to track remote branch from origin.
                              # No need to specify remote branch name, for e.g., when doing a 'git pull' on that branch.
git pull                # Pull changes from the remote to your currently checked out branch

# Re/moving files under version control
git rm <path/to/the/file>                 # remove file and stage the change to be committed.
git mv <source/file> <destination/file>   # move/rename file and stage the change to be committed.

# Aliases - it's possible to make aliases of frequently used commands
#   This is often done to make a command shorter, or to add default flags

# Adding a shorthand "sw" for "switch"
git config --global alias.sw "switch"
# Usage:
git sw master     # Does a "git switch master"

## Logging
git log --graph --oneline --all # Show a nice graph of the previous commits
## Adding an alias called "lol" (log oneline..) that shows the above
git config --global alias.lol "log --graph --oneline --all"
## Using the alias
git lol     # Does a "git log --graph --oneline --all"
```

## Testing

There is a very small test that you can run in powershell or bash.
It is contained in the scripts `test.sh` and `test.ps1`.

### Cleanup

You can remove testing artifacts, `exercise` directories, with the git clean command:
