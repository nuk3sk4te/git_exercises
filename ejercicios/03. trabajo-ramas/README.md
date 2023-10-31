# 03. Trabajo con ramas

## Configuración

1. Ejecuta `source setup.sh` (or `.\setup.ps1` in PowerShell)

## La tarea

Nuevamente estás en tu propia rama, esta vez haremos un poco de malabarismo con las ramas para mostrar cuán livianas son las ramas en git. 
Pista: git switch te hará cambiar de una rama a otra.

1. Utilice `git branch`para ver las dos ramas que son relevantes para este ejercicio.
2. En qué rama estás?
3. Usa `git branch mybranch` para crear una rama de nombre _mybranch_
4. Usa `git branch` de nuevo para ver la nueva rama creada.
5. Usa `git switch mybranch` para ir a tu nueva rama.
6. Cómo `git status` cambia la salida cuando cambias entre la rama maestra y la nueva que has creado?
7. ¿Cómo cambia el espacio de trabajo cuando cambias entre las dos ramas?
8. Asegúrese de estar en la rama `mybranch` antes de continuar.
9. Crear un fichero de nombre `file1.txt`.
10. `Add` el fichero y crea el `commit` con este cambio.
11. Usa `git log --oneline --graph` para ver la rama apuntando al nuevo commit..
12. Vuelve de nuevo a la rama principal llamada _master_.
13. Usa `git log --oneline --graph` y revisa como el commit que has ehcho sobre `mybranch` no está en la rama `master`.
14. Haz un nuevo fichero de nombre `file2.txt` y haz un nuevo commit con este fichero.
15. Usa `git log --oneline --graph --all` para ver la rama apuntando al nuevo commit y que las 2 ramas ahora tiene diferentes commits.
16. Vuelve de nuevo a la rama  _mybranch_.
17. ¿Qué pasó con su directorio de trabajo? ¿Puedes ver tu `file2.txt`?
18. Usa `git diff mybranch master` para ver las diferencias entre ambas ramas.


## Comandos útiles

- `git switch`
- `git switch -c`
- `git log --oneline --graph`
- `git branch`
- `git diff`
