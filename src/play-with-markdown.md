

## Título
### Subtítulo
Este es un ejemplo de texto que da entrada a una lista genérica de elementos:
- Elemento 1
- Elemento 2
- Elemento 3
Este es un ejemplo de texto que da entrada a una lista numerada:
1. Elemento 1
2. Elemento 2
3. Elemento 3
Al texto en Markdown puedes añadirle formato como **negrita** o *cursiva* de una manera muy sencilla.

Bloque de codigo:
~~~
Creando códigos de bloque.
Puedes añadir tantas líneas y párrafos como quieras.  
~~~

Encabezados:
# Encabezado 1
## Encabezado 2
### Encabezado 3
#### Encabezado 4
##### Encabezado 5
###### Encabezado 6


Esto es una cita:
> Un país, una civilización se puede juzgar por la forma en que trata a sus animales.  — Mahatma Gandhi

Si el parrafo tiene mas lineas 

> Parrafo 1 
> Parrafo 2 

Listas
- Elemento de lista 1
- Elemento de lista 2
* Elemento de lista 3
* Elemento de lista 4
+ Elemento de lista 5
+ Elemento de lista 6

Lineas Horizontales:
***
---
___

Negritas y cursivas:

- *cursiva*
- _cursiva_
- **negrita**	
- __negrita__	

Si se quire agregar los dos:

***cursiva negrita***

Enlaces:

[enlace en línea](https://www.youtube.com/)

Enlaces de referencia:

En el texto se ***enlazaran*** **palabras o codigos** (letras y/o numeros) En otro lugar mas apartado del documento tendras definidos como **URLS**
~~~
[nombre que quieres darle a tu enlace][nombre de tu referencia]
[nombre de tu referencia]: https://www.youtube.com/
~~~
Ejemplo:
~~~
[blog]: https://www.youtube.com/
Soy Ron y tengo una pagina web donde se pueden subir [videos][blog].
En dicha [web][blog] la gente podra subir videos y se mantendra en el tiempo.
~~~
Codigo:
`Esto es una línea de código`
Es util para insertar "codigo" dentro de la misma linea o parrafo.

Imagenes:

`![Texto alternativo](/imagen.jpg)`

- El texto alternativo es lo que se mostraría si la carga de la imagen fallase.
- También podrás añadir un título alternativo entrecomillándolo al final de la ruta. 
Esto sería el título mostrado al dejar el cursor del ratón sobre la imagen.

`![Texto alternativo](/ruta/a/la/imagen.jpg "Título alternativo")`

Al añadir imagenes, se esta tratando con URLs. Entonces se puede hacer algo parecido al metodo anterior.
~~~
[img1]: /ruta/a/la/imagen.jpg "Título alternativo"
[img2]: /ruta/a/la/imagen2.jpg "Título alternativo"
De esta forma podrías insertar una imagen
![nombre de la imagen][img1]
O dos, sin ensuciar tu espacio de escritura.
![nombre de la imagen2][img2]
~~~
Mostrar URL completa
`<http://www.limni.net>`

Nuevas funciones de Markdown:

Abreviaciones:
- Definir abreviaciones en Multimarkdown utilizando la siguiente sintaxis.

Referencias cruzadas:
Las referencias cruzadas sirven para añadir links a partes específicas del documento.

Para especificar qué un link de referencia, deberás incluir entre llaves el nombre que quieres que tenga dicho enlace de la siguiente manera `{#EnlaceReferencia}`.
~~~
## Encabezado que quieres referenciar {#EncabezadoReferencia}
Así se generan referencias a partes concretas de un documento con Multimarkdown.
~~~

Una vez definido, se puede enlazar desde cualquier palabra o texto fácilmente como en la sintaxis de links, pero en 
lugar de una URL, se debe escribir el #NombreDeTuReferencia.
~~~
Quiero que [este enlace](#referencia) vaya al encabezado de referencias cruzadas.
~~~

