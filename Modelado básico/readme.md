___
Una startup tecnológica va a desarrollar un portal de ELearning y nos ha pedido que realizemos el modelo de datos de dicho sistema.
A tener en cuenta:

Va a ser un portal orientado al mundo de la programación.
El portal va a estar compuesto por cursos, cada curso está compuesto a su vez por un número de videos y artículos que lo acompañan.
La página de cursos debe mostrar la lista de autores que lo hicieron.
La página de un video debe mostrar el autor que lo realizó.
Los videos y el contenido de cada artículo se almacenan en un storage S3 y en un headless CMS, en la base de datos sólo almacenaremos los Id's a esos recursos.
Los videos se pueden clasificar por temáticas (Devops / Front End / Back End / ...), para simplificar, un video va a pertenecer a una sóla temática.
Los videos tienen autores (ponemos la restricción de que un video tiene un autor), un curso puede tener varios autores.
En principio los vídeos no se van a compartir entre diferentes cursos (aunque sería una amplicacíon interesante del ejercicio).
Hay una opción para ver la página con la biografía del autor.


 info en la web
 ___
# CURSOS
___
nombre
imagen del curso
descripción
link a leccion(leccion, video) 
Autores
### *RELACIONES*


# LECCION - solo almacenamos ID
___
### *CAMPOS*
muestra titulo
muestra ancestros
muestra 1 video
muestra descripcion
### *RELACIONES*


# AUTOR
___
### *CAMPOS*
Nombre
FOTO
BIO
rrss
cursos en los que ha participado(id, nombre, descripcion)

### *RELACIONES*

# CURSOS
___
### *CAMPOS*
- Nombre curso
- Los datos del artículo (titulo, video/s) se encuentran en remoto, por lo tanto sólo se almacena el ID
- Los autores se obtendrán desde la relación con la entidad lecciones que a su vez tepara no generar redundancia


### *RELACIONES*

Necesitamos traer los datos de las lecciones y el autor del curso
- El campo Lecciones está conectado a la entidad leccion
- El campo autor esta conectado a la tabla autor


# LECCIÓN
___
### *CAMPOS*
Hace de nexo entre los datos de un curso y sus videos en remoto
- Cuenta con su propio Id
- Almacena el ID del contenido relacionado(videos y descripcion)
- Recibe las temáticas desde los datos de sus videos

Relaciones
Una lección puede pertenecer a un curso o ser compartida entre varios, las lecciones tendrán una 
- Relacionada con la entidad cursos
- 
### *RELACIONES*



# AUTOR
___
### *CAMPOS*
- Contará con:
	- Campo Id
	- Cacmpo nombre
	- Campo biografía
	- RRSS
### *RELACIONES*

	
# VIDEO
___
### *CAMPOS*
- La relación entre cursos y los IDs
### *RELACIONES*



# TEMÁTICA
___
### *CAMPOS*
### *RELACIONES*

