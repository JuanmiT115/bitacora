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
|6°|git diff|Muestra las modificaciones realizadas a un archivo (*modificacciones que no hayan sido preparadas*)| |
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
|19°|git reset| ~~Trae todo lo que habia antes de realizado un merge~~| |
|20°|git remote **add origin *url_repositorio***|**Víncula un repositorio de GitHub al cual estoy trabajando en local (*el add origin le da el alias al repositorio de origin para no tener que poner el url cada vez que se hace un push*)**|**Definición puesta después de revisado mis apuntes**|
|21°|**pwd**|En la terminal me muestra donde estoy| |
