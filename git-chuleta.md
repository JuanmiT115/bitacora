# Chuleta de repaso general fase 0

> [!NOTE]
> Esta chuleta funciona como repaso propio de lo aprendido en la primera semana de la fase 0 de mi estudio independiente para ser desarrollador FullStack.


## Tabla de comandos con definición
Esta tabla muestra las definiciones de los comandos desde la memoria, no es la definición oficial.<br/>
Las corecciones son la definción o complementación de lo que escriba de memoria.<br/>
En negrilla estaran las correcciones realizadas y aquellos comandos que no escribi a memoria.


|N°|Comando|Qué hace|Corección|
|---|---|---|---|
|1°|git init|Inicializa un repositorio desde la terminal| |
|2°|git status|Este muestra el estado de un archivo modificado, lo muestra en rojo cuando la modificación no ha pasado a la fase stage y en verde cuando ya esta en esta etapa.| |
|3°|git add *nombre_archivo*|Agrega las modificaciones realizadas a un archivo a la fase de preparación para que puedan salir al siguiente commit| |
|4°|git commit -m "*mensaje commit*"|Es la fase de confirmación de las modificaciones que estan preparadas| |
|5°|git log|Muestra los commits realizados en el repositorio| |
|6°|git diff|Muestra las modificaciones realizadas a un archivo (*modificaciones que no hayan sido preparadas*)| |
|7°|git diff --staged|Muestra las modificaciones que ya estan preparadas de un archivo| |
|8°|git restore ***nombre_archivo***|**Se descarta el cambio y el archivo vuelve a como estaba en el último commit. Este borra los cambios sin preguntar.**|
|9°|**git restore --staged *nombre_archivo***|**Se saca el archivo que ya esta preparado, pero los cambios realizados siguen en el archivo**|**Definición puesta después de revisado mis apuntes** |
|10°|git branch|Muestra las ramas que tiene actualmente el repositorio, muestra con un * la rama en cual se esta trabajando| |
|11°|git branch -d *nombre_rama*|Elimina una rama en la cual ya no estemos trabajando, preferiblemente después de realizado el merge con la principal| |
|12°|git switch *nombre_rama*|Cambia a la rama en la cual quiero trabajar| |
|13°|git switch -c *nombre_rama*|Crea una nueva rama y me cambia a esta después de crearla| |
|14°|git merge *nombre_rama*|Fusiona la rama que nombre a la rama en la cual estoy actualmente| |
|15°|git pull|Me trae la última versión del repositorio puesta o alojada en GitHub **(Trae los commits nuevos de GitHub y los fusiona con mi rama)**|**Aclaración corregida** |
|16°|git push -u origin *nombre_rama*|~~Esta se hace desde la rama en la cual estoy trabajando, la cual si es diferente al main, esto genera un pull request en GitHub **(*el -u se usa solo la primera vez que se realiza el push de una rama en local, después el comando es solo git push origin nombre_rama [esto último aplica para cuando se haga el push desde el main]*)**~~|**El push no crea el pull request. Solo sube la rama; GitHub te ofrece un botón (“Compare & pull request”) para crearlo, pero el PR lo abres tú. Después del -u, el siguiente push es solo git push, sin origin nombre_rama, y vale para cualquier rama, incluida main. El -u deja la rama enlazada; por eso no hay que repetir el nombre.**|
|17°|git push origin|Sube todo los commits realizados desde local al repositorio en GitHub| |
|18°|git clone *url_repositorio*|Clona un repositorio desde GitHub a mi local| |
|19°|git reset| ~~Trae todo lo que habia antes de realizado un merge~~|**mueve la rama actual a otro commit**|
|20°|git remote **add origin *url_repositorio***|**Víncula un repositorio de GitHub al cual estoy trabajando en local (*el add origin le da el alias al repositorio de origin para no tener que poner el url cada vez que se hace un push*)**|**Definición puesta después de revisado mis apuntes**|
|21°|**pwd**|En la terminal me muestra donde estoy| |
|22°|cd *directorio*|Me cambia al directorio en la terminal| |
|23°|cd ..|Me devuelve al directorio anterior al cual estoy trabajando| |
|24°|touch *nombre_archivo.tipo*|Desde la terminal crea un archivo| |
|25°|code .|Desde la terminal abre el VS (Visual Studio Code) para trabajar los archivos| |
|26°|**mkdir** *nombre_directorio*|Crea un directorio desde la terminal| | 
|27°|**ls**|Me muestra desde la terminal lo que hay dentro de un directorio||
|28°|**git branch -M main**|**Nombra a la fuerza la rama como main**|**Definición puesta después de revisado mis apuntes**|
|29°|**touch .gitignore**|**Crea un archivo en el cual dentro van a ir todas las especificaciones de los archivos que no queremos que sean rastreados dentro del repositorio**|**Definición puesta después de revisado mis apuntes**|
|30°|**git diff --check**|**Este se usa después de resuelto un conflicto de algún merge, si no muestra nada es por que esta limpio el archivo después de solucionado dicho conflicto**|**Definición puesta después de revisado mis apuntes**|
|31°|**git rm *nombre_archivo***|**Elimina el archivo del directorio de trabajo y prepara la eliminación para la próxima confirmación**|**Definición puesta después de revisado mis apuntes**|
|32°|**git reset HEAD *nombre_archivo***|**Prácticamente hace lo mismo que el comando git restore --staged**|**Definición puesta después de revisado mis apuntes**|
|33°|**git reset --hard HEAD**|**Elimina todas las modificaciones preparadas y no preparadas de todo el repositorio hasta el último commit**|**Definición puesta después de revisado mis apuntes**|
|34°|**git merge --abort**|**Cancela un merge con conflicto y vuelve a como estaba antes**|**Definición puesta después de revisado mis apuntes**|
|35°|**git log --oneline --graph --all**|**Muesta el historial como árbol, con todas las ramas**|**Definición puesta después de revisado mis apuntes**|
|36°|**git push origin --delete *nombre_rama***|**Borra una rama en GitHub**|**Definición puesta después de revisado mis apuntes**|

## Preguntas rápidas

1. ¿Qué diferencia hay entre git add y git commit?<br/>
  Git add envia las modificaciones que realice a algún archivo a la zona de preparación y git commit confirma dichas modificaciones que estan ya en la área de preparación.
2.  ¿Por qué falla un git push y cómo se arregla?<br/>
   GitHub tiene commits que tú no tienes en tu computador, por ejemplo porque alguien (o tú desde la web) subió cambios. Git rechaza el push para no sobrescribir ese trabajo. El mensaje dice algo como rejected y te sugiere hacer fetch o pull primero. git pull para traer esos commits y fusionarlos con los tuyos.
Si aparece un conflicto, lo resuelves (y verificas con git diff --check), luego add y commit.
git push otra vez.
3. ¿Qué haces si un merge te genera conflicto?<br/>
   Si es fácil de solucionar reviso el conflicto que me genera y decido que modificación mantener o los complemento entre sí, si wa muy dificil y no lo entiendo lo mejor es aplicar un git merge --abort para cancelar el merge y que vuelva todo a como estaba antes.
4. ¿Qué es un pull request y para qué sirve?<br/>
   Es una solicitud para fusionar una rama con la principal o con otra en la cual notifico a mi equipo de que quiero realizar dicha modificación para que puedan revisar las modificaciones y me comenten que cambios hacerles o que cambiarle y poder tener el vistaso bueno para fusionar la rama.
5. ¿Qué archivos pondrías en .gitignore y por qué?<br/>
    Aquellos archivos que no quiero que sean reastreados para que no me aparezcan en rojo siempre que ejecute un git status. Tambien para no subir archivos a GitHub que no deberian estar ahi.
6. ¿Qué hace git reset --hard y cuándo es peligroso?<br/>
   Elimina todas las modificaciones esten o no preparadas de todo el repositorio y deja el repositorio a como estaba con el último commit, y este cambio es irreversible. Es peligroso cuando quiero resetear un solo archivo por x o y razon y termino reseteando todo lo demás trabajado en el repositorio obligandome a realizar nuevamente todo lo que ya habia hecho.
