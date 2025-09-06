___
# CURSOS
___
name
imagen del curso
description
link a leccion(leccion, video) 
Authors

### *RELACIONES*
Se relacionará con las lecciones pertenecientes al curso en cuestión
Los autores del curso se recibirán desde la tabla Authors


# LECCION
___
### *CAMPOS*
titles
video
description

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

