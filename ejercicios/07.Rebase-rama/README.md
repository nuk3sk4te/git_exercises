# 07. Rebase una rama

## Configuración

1. Ejecuta `source setup.sh`

## La tarea

Nuevamente estas en tu propia rama, esta vez haremos un poco de malabarismo con las ramas para mostrar cuán livianas son las ramas en git.

1. Qué ramas existen?
2. Revisa el log para la rama master
3. Cambia a la rama `uppercase`
4. ¿Cómo se compara el registro con el registro de la rama `master`?
5. Haz un rebase de la rama `uppercase` con la rama master (`git rebase master`)
6. Qué ha ocurrido. Dibujalo!
7. Ahora cambia a la rama master
8. Anexa la rama `uppercase` en la rama `master`
9. ¿Cómo se ve el log ahora?


## Comandos útiles

- `git switch <branch-name>`
- `git rebase <branch-name>`
- `git log --oneline --graph --all`
- `git merge <branch-name>`
