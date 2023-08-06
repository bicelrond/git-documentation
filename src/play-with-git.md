## Create folders from console:

Para **ver el contenido de la carpeta en la que se encuentra el prompt**: Listara el contenido de la carpeta:
~~~
ls  
~~~
Tambien se puede utilizar ls con una directorio para ver el contenido de una carpeta sin tener que estar dentro de un prompt.

**Indentificador de colores, segun tipo de archivo/elemento:**

| Color | Referencia | 
| -- | -- | 
| Color azul | Carpetas | 
| Color verde | Archivos ejecutables | 
| Color azul celeste | Carpetas especiales de Windows | 
| Color blanco | Archivos (pdf, jpg, doc, md, js, etc.) | 



**Para acceder a la carpeta:**
~~~
cd <carpeta o directorio>
~~~

**Crear carpeta:**
~~~
mkdir <nombre de carpeta>
~~~
***
## Repositorios:

Iniciar un repositorio local:
~~~
git init 
~~~
Revision **ESTADO** general del repositorio:
~~~
git status 
~~~
Agrega el repositorio a ***"STAYING AREA"***. "Por Confirmar" para luego transformarlo en un **COMMIT** (versión):
~~~
git add <archivo> 
~~~
O (si queremos agregar todos los cambios de todos los archivos del **Directorio** actual a ***"STAYING AREA"***):
~~~
git add . 
~~~
Agregar la versión al repositorio. (*-m = mensaje*):
~~~
git commit -m "**Nombre del commit**" <archivo>
~~~
1. Revisaremos si se hicieron los cambios con **GIT STATUS**.
2. Luego revisaremos la version de commit con su identificador unico o **HASH** con su respectiva informacion:
~~~
git log o git log --oneline
~~~
Para ver una version del commit anterior al que estamos:
(Pero pasaremos a un estado "detached HEAD")
~~~
git checkout <numero de commit al que queremos ir>
~~~
Para no estar en "detached HEAD" y volver a la rama master del ultimo COMMIT:
~~~
git checkout master
~~~
***
### Para eliminar un commit:
Escribir el commit anterior a los cambios que queremos hacer:
~~~
git reset <numer de indentificador>
~~~
Luego hacemos el proceso de **ADD** y luego el **COMMIT**

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









