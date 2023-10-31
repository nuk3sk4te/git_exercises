# 09. Resetear commits

Podemos manipular mucho la Historia. Sólo deberíamos retocar nuestra historia local.
Una vez los cambios han sido compartidos con otros, no deberíamos cambiar la historia.

Usamos reset para deshacer cambios, pero también podemos hacer muchas más cosas diferentes.

## Configuración

1. Ejecuta `source setup.sh`

## La tarea

1. ¿Cómo se ve el directorio de trabajo?
2. Cómo se muesta el log? y el stage?
3. Intenta ejecutar el comando `git reset --soft HEAD~1`
4. Qué ha ourrido al directorio de trabajo, y al stage?
5. Ejecuta `git reset --mixed HEAD~1`
6. Qué ha ourrido al directorio de trabajo, y al stage?
7. Ejecuta `git reset --hard HEAD~1`
8. Qué ha ourrido al directorio de trabajo, y al stage?
9. Ahora intenta ejecutar `git revert HEAD~1`
10. Qué ha ourrido al directorio de trabajo, y al stage?


## Comandos útiles

- `git log --oneline`
- `git commit --amend`
- `git status`
- `git reset --soft`
- `git reset --mixed`
- `git reset --hard`
- `git revert`
