# 08: Revertir cambios

## Configuración

1. Ejecuta `source setup.sh`

## La tarea

En esta tarea se colaron algunos cambios que nos gustaría sacar a la luz. Nuestra historia es pública, por lo que no podemos simplemente cambiarla. Más bien, necesitamos usar revertir para eliminar los cambios no deseados de forma segura.

1. Usa `git log --oneline` para revisar el log (historia)
2.  Usa `cat` para ver el contenido de `greeting.txt`
3.  Usa `git revert` sobre el más nuevo commit, para borrar los cambios que el último commit añadió
4.  Usa `git log --oneline` para revisar el log
5. ¿El comando de revert agregó o eliminó un commit?
6.  Usa `cat` para ver el contenido del fichero `greeting.txt`
7.  Usa `ls` para ver el contenido de la carpeta (workspace)
8.  Usa `git log --oneline` para encontar el hash del commit añadiendo credenciales al repositorio
9.  Usa `git revert` para revertir el commit que agregó las credenciales
10. Usa `git log --oneline` para revisar el log
11. Usa `ls` para ver el contenido de la carpeta (workspaces)
12. Cuantos commits fuera añadidos o cambiados desde el último `revert`?
13. Usa `git show` con el hash del commit que se revertió para que las credenciales del fichero están aún en la historia
14. Como ahora se ha revertido el fichero de credenciales, se elimina de su directorio de trabajo, es también eliminado de GIT?

## Comandos útiles

- `git revert <ref>`
- `git log --oneline`
- `git show <ref>`
