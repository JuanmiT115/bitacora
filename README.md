
# Bitacora de Miguel de programación

Miguel: Programador FullStack

## 02-nov-2026 . Día 1 . Full-Stack
- Instalé GIT y configuré mi usuario
- Aprendí los 3 estados de GIT

### Prueba de commit y add
- Este es un primer cambio para aplicar el add y luego el commit.
- Esta es un segundo cambio para lo mismo.
- Esta última línea es para probar el push.

## 03-nov-2026 . Día 2 . FullStack
### Los 3 estados de GIT:
- Confirmación: Es lo que se sube después de ser modificado y esta en la parte de preparación.
- Modifiación: Cualquier cambio o diferencia en un archivo.
- Preparación: Lugar en donde se "suben" las modificaciones para poder ser confirmadas, sin este proceso una modificación no queda atualizada y confirmada.
### Ciclo add --> commit --> push
- Add: es mandar a la zona de preparación cualquier modificación que se le hace a un archivo.
- Commit: confirmar la modificación del archivo, para realizar esta primero se tuvo que aplicar el add y dejar listo para el push.
- Push: la subida de las actualizaciones al repositorio en GITHUB. 

### .gitignore
Se debe crear un .gitignore y dentro de este poner los archivos que se van a ignorar.

## 09-nov-2026 . Día 3 . FullStack
### git diff y git diff --staged
- git diff, muestra exactamente todos los cambios que no has preparado, es decir los que no estan con git add, si tus cambios ya estan preparados, el comando no devuelve nada.
- git diff --staged, muestra exatamente los cambios ya preparados pero que son diferentes con el último commit realizado.
### git restore y git restore --staged
- git restore, descarta los cambios realizados y el archivo vuelve a omo estaba en el último commit, este borra los cambios sin preguntar.
- git restore --staged, saca los archivos que estan preaparados pero no altera los cambios que ya les realisaste.
### git.ignore
- Este comando funciona para ignorar archivos que no queremos que sean rastreados, para no estar viendo en todo momento que no son rastreados.

### Comandos que ya sé
- git status, add, commit, push, diff, restore

### Ramas
- ¿Qué es una rama? --> Una sesión de trabajo, en donde puedes modificar tranquilamente el código sin afectar alguna versión anterior directamente hasta que no hagas un commit y un merge.
- ¿Qué hacen switch -c, merge, branch -d?:
    - switch -c, crea una nueva rama y nos mueve directamente a esta nueva rama.
    - merge, fusiona una rama cualquiera a la rama en la cual ya estoy.
    - branch -d, borra una rama.

### Línea de prueba conflicto.

- Practiqué subir una rama a GitHub.

### Diferencia entre Fast-Forward de un merge a tres bandas
- El fast-forward es cuando haces cambio en una nueva rama y no modificas nada desde la rama principal.
- El merge a tres bandas es cuando haces cambios en la nueva rama y al mismo tiempo haces cambio en la rama principal.

## 10-nov-2026 . Día 4 . FullStack
### Repaso día anterior
- Diferencia entre FAST-FORWARD y un COMMIT MERGE
    - El fast-forward se da cuando realizas alguna modificación en una rama a parte y no haces naada en la rama principal, el commit merge (merge a tres bandas) se da cuando haces un cambio en la nueva rama y al mismo tiempo realizas un cambio en la rama main.
- El git push -u origin nombre_rama, lo que hace es subir la rama al repositorio en GITHUB.

### Qué es un conflicto?
- Es cuando desde dos ramas diferentes se modifica la misma línea de un mismo archivo.
    - Como solucionarlo, se debe primero corregir el cambio y decidir cual se va a dejar fijo, luego de esto se ejecuta un add para confirmarle a git que se resolvio el conflicto y luego se ejecuta un commit con el cual se sube el archivo con el conflicto solucionado.

### git pull
- Este comando trae la versión más reciente del repositorio desde github.
    - Como hábito siempre ejecutar un git pull antes de empezar a trabajar para tener la versión más reciente siempre.
    
## 11-nov-2026 . Día 5 . FullStack
### git diff --check
- Se ejecuta antes de un git add después de resuelto un conflicto con el fin de confirmar de que no haya quedado nada mal.
    - Como hábito, ejecutar este comando siempre antes de un add después de resolver un conflicto.

### Pull Request
- Es un proceso en el cual compara la rama en la que estoy trabajando con el main y permite revisión y comentar antes de fusionar, todo esto desde git hub.
    - Pasos:
        - Se debe crear una nueva rama de trabajo.
            - En esta se debe hacer la modificació, el add y luego el commit, no se hace el merge desde main.
        - Se debe hacer un git push -u origin rama, para subir lo trabajado en la rama a git hub.
        - Luego en github se hace un compare & pull request, donde nos muestra los cambios realizados, que diferencias hay con el main.
            - En este se debe poner un título claro y una descripción detallada de lo que se hizo y porqué para que lo revisen. Luego se revisa y estos dejaran comentarios de si esta bien o toca hacer algún otro cambio. (Los comentarios se hacen en las línea de código con el + azul.)
        - Luego de realizada la revisión de hace el Merge pull request y luego confirm merge, con lo cual se fusiona la rama con el main con los cambios realizados.
        - Después de todo esto como el merge se hizo desde github, el trabajo desde mi computador estara desactualizado por lo cual debo hacer un git pull para traer los cambios realizados desde github.
            - Si se desea después de haber realizado los cambios en la otra rama y terminar de trabajar con ella se puede borrar desde github y tambien en el equipo después de realizado el git pull. (Para realizar el git pull a mi equipo primero se debe cambiar a la rama main.)

