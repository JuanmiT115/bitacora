# Bitácora de aprendizaje
Miguel: ruta Full-Stack y VFX en tiempo real

## 02-nov-2026 . Día 1 . Full-Stack
- Instalé GIT y configuré mi usuario
- Aprendí los 3 estados de GIT

## Prueba de commit y add
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