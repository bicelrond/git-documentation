# GIT [Revisar documentacion](https://git-scm.com/book/es/v2) 





## Comandos Basicos git
| Comando | Utilidad | 
| -- | -- | 
| ls | Ver el contenido del directorio en el que se encuentra el prompt. | 
| cd directorio | Acceder al directorio. | 
| cd .. | Un paso atras del promp. | 
| pwd | Revisar donde estamos ubicados. | 
| mkdir nomrbecarpeta | Crear carpeta.|
| touch nombrefichero.py, js, html, css, etc  | Crear archivos vacíos y cambiar marcas de tiempo de archivos o carpetas|

>Tambien se puede utilizar `ls` con el nombre de un directorio para ver el contenido.

***
### Indentificadores de colores
**Indentificador de colores, segun tipo de archivo/elemento:**
| Color | Referencia | 
| -- | -- | 
| Color azul | Carpetas | 
| Color verde | Archivos ejecutables | 
| Color azul celeste | Carpetas especiales de Windows | 
| Color blanco | Archivos (pdf, jpg, doc, md, js, etc.) | 

***
## Repositorio:
### Configuracion:

~~~
git config --global user.name "name"
git config --global user.email name@example.com
~~~
Combiar nombre de la rama (master a main):
~~~
git branch -m nombredelarama
~~~
### Comandos basicos repositorio :
>Normalmente mas usados:

Iniciar un repositorio local:
~~~
git init 
~~~
Agrega el repositorio a ***"STAYING AREA"***. "Por Confirmar" para luego transformarlo en un **COMMIT** (versión):
~~~
git add <archivo> 
~~~
O (si queremos agregar todos los cambios de todos los archivos del **Directorio** actual a ***"STAYING AREA"***):
~~~
git add . 
~~~
Agregar la versión al repositorio. (**-m = mensaje**):
~~~
git commit -m "mensajedeconfirmación" <archivo>
o 
git commit -a -m "amensajedeconfirmación"
~~~
Al agregar `-a` no es necesario hacer un `add .` antes. Se salta el area de preparacion.

### Revisar el Estado de tus Archivos

Revision **ESTADO** general del repositorio:
~~~
git status 
o
git status -s  
~~~
`-s` es para no mostrar tanta informacion.
>El comando te indica en cuál rama estás y te informa que no ha variado con respecto a la misma rama en el servidor.
1. Revisaremos si se hicieron los cambios con `git status`.
#### Historial se Confirmaciones
2. Luego revisaremos la version de commit con su identificador unico o **HASH** con su respectiva informacion:
~~~
git log 
o
git log --oneline
~~~
>El mecanismo que usa Git para generar esta suma de comprobación se conoce como hash SHA-1. Se trata de una cadena de 40 caracteres hexadecimales (0-9 y a-f), y se calcula con base en los contenidos del archivo o estructura del directorio en Git. Por ejemplo:
~~~
24b9da6552252987aa493b52f8696cd6d3b00373
~~~
>Git guarda todo no por nombre de archivo, sino por el valor hash de sus contenidos.

Tambien se puede hacer variantes de `git log` como :

| Comando log | Funcion | 
| -- | -- | 
| -p | Muestra las diferencias introducidas en cada confirmación. | 
| -2 | Se muestren únicamente las dos últimas entradas del historial. | 
| -p -2 | Diferencias y ultimas entradas del hitorial. | 
| --stat: | Estadísticas de cada confirmación. | 

### Alias
Para no escribir el comando completo. Se puede guardar un comando corto en un alias para luego escribirlo:
>Esto se guardara en `.gitconfig`. Esto se encuentra la mayoria de veces en `user`, en nuestro dispositivo. 
~~~
git config --global alias.tree "log --graph --decorate --all --oneline"
~~~
Ahora se puede usar `git tree` y ejecutara el comando completo.

### Ignore

### Deshacer un Archivo Preparado
Si queremos deshacer los cambios que hemos hecho, volveremos al commit original.
~~~
git checkout <numero de commit al que queremos ir>
~~~

### Para eliminar un commit:
Escribir el commit anterior a los cambios que queremos hacer:
~~~
git reset <numer de indentificador>
~~~
### GitHub
Para subir los archivos al servidor Remoto debemos pasar por los estados de  **ADD** y luego el **COMMIT**.

Para subir los cambios a **GITHUB** :
~~~
git push origin main
~~~
Nos pedira Clave o Key.
***
### Clonar un repositorio:
Clonar un repositorio de ***GITHUB*** :
~~~
git clone <copiamos y pegamos el ssh del repositorio que queremos clonar>
~~~
No pedira la Clave o Key.

***
### Mover
Para mover un archivo a un nuevo directorio:
1. Mover los archivos a la carpeta deseada arrastrandolo.
2. Agregar los comandos:
    - git add .
    - git status 
    - git commit -m "Move file to new directory"
    - git push origin main
***
### Eliminacion de **archivos**
~~~
rm <archivo>
~~~
Si estamos en un archivo de un repositorio deberemos agregar los cambios a la ***"STAYING AREA"***

~~~
git add <archivo eliminado>
~~~
Luego el commit:
~~~
git commit -m "Eliminacion de archivo"
~~~
***Si antes del commit no queremos eliminar el archivo, aun cuando el archivo este en Staying Area:***
~~~
git restore --staged <archivo>
git restore <archivo> 
~~~
***

### TAG
Esta funcionalidad se usa típicamente para marcar versiones
de lanzamiento (v1.0, por ejemplo).

#### TAG Ligero:
Una etiqueta
ligera no es más que el checksum de un commit guardado en un archivo - no incluye
más información:
~~~
git tag <nombre del tag>
~~~
Listar las etiquetas disponibles `git tag`
### TAG anotada
La forma más fácil de hacerlo es especificar la opción `-a` cuando ejecutas el comando `git tag`
~~~
git tag -a <nombreversion> -m '<mensaje de la etiqueta>'
~~~
Para ver la información de la etiqueta junto con el commit que está etiquetado al usar el comando `git show`

### TAG tardio 
También se puede etiquetar commits mucho tiempo después de haberlos hecho.
Para etiquetar un **commit**, debes especificar el **checksum** del commit (o parte de él) ***al final del comando***: 
~~~ 
git tag -a v1.2 -m '<mensaje de la etiqueta>' <id de commit>
~~~

Para transferir el tag o tags a un servidor remoto como **GITHUB**:
~~~
git push origin [etiqueta] 
o
git push origin --tags
~~~
Por lo tanto, cuando alguien clone o traiga información de tu repositorio, también obtendrá todas las etiquetas.

***
### END
Git log muestra el historial de todos los commits que hay, si hay muchos commits saldrá un signo de dos puntos `:` y la línea de donde se encuentra el cursor parpadeando, si presionamos `espacio` mostrará mas commits hasta llegar al último, y cuando termine, dira: `(END)`, para **SALIR**, presionamos `q`

***
### BRANCH O RAMAS
Las ramas o branch las ocuparemos normalmente cuando trabajemos en equipo o cuando queramos hacer una nueva funcion que no queremos agregar a la rama `main`.
>Por ejemplo queremos hacer un Login para una nueva pagina web.
>Entonces para no usar la rama principal. Hacemos una nueva rama

