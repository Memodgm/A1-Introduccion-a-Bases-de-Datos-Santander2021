[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 04`](../Readme.md) > Reto 2

## Reto 2: Importando datos a una tabla en formato CSV

### 1. Objetivos :dart:
- Aplicar el procedimiento para importación de datos a una tabla
- Validar que la correcta importación de los datos

### 2. Requisitos :clipboard:
- Servidor __MySQL__ instalado

### 3. Desarrollo :rocket:

1. Usando como base el archivo `movies.dat`, limpiarlo e importar los datos en la tabla `movies` creada en el Reto 1.   

   > **Importante:** Este archivo presenta un problema muy común de *encoding*, es decir, la codificación con la que fue definido, no es reconocida por __MySQL__. Para solucionar este problema, elige una codificación diferente al momento de cargar los datos.


-
-


Agregamos el encabezado correspondiente a movies.dat y reemplazamos el símbolo :: por ,. Guardamos el archivo como movies.csv.

id,title,generos
1,Toy Story (1995),Animation|Children's|Comedy
2,Jumanji (1995),Adventure|Children's|Fantasy
3,Grumpier Old Men (1995),Comedy|Romance
4,Waiting to Exhale (1995),Comedy|Drama
5,Father of the Bride Part II (1995),Comedy
6,Heat (1995),Action|Crime|Thriller
7,Sabrina (1995),Comedy|Romance
8,Tom and Huck (1995),Adventure|Children's
9,Sudden Death (1995),Action
10,GoldenEye (1995),Action|Adventure|Thriller
...






2. Usando como base el archivo `ratings.dat`, limpiarlo e importar los datos en la tabla `ratings` creada en el Reto 2.   

   > **Importante:** Como podrás notar, este archivo tiene demasiados registros, de manera que es normal que la carga sea muy lenta. Esto es algo muy común cuando nos enfrentamos a la carga de archivos. Si ya lleva mucho tiempo y no finaliza, no te preocupes, puedes cancelar la carga.



-
-
Agregamos el encabezado correspondiente a ratings.dat y reemplazamos el símbolo :: por ,. Guardamos el archivo como ratings.csv.

userid,movieid,rating,time_stamp
1,1193,5,978300760
1,661,3,978302109
1,914,3,978301968
1,3408,4,978300275
1,2355,5,978824291
1,1197,3,978302268
1,1287,5,978302039
1,2804,5,978300719
1,594,4,978302268
...






3. Finalmente, añade un registro en cada tabla usando `INSERT INTO`.



Cargamos movies.csv y ratings.csv usando MySQL Workbench. Comprobamos los resultados con las siguientes consultas.

SELECT *
FROM movies
LIMIT 10;

SELECT *
FROM ratings
LIMIT 10;



Finalmente insertamos los registros correspondientes:

INSERT INTO movies(id,title,generos) VALUES (5000,'Avengers', 'Adventures');

-- Si añadiste llaves foráneas, recuerda que debes añadir primero los registros en las tablas users y movies.
INSERT INTO ratings(userid,movieid,rating,time_stamp) VALUES (1,1193,2,978300760);


-
-
-





## Opcional

Otra forma de cargar grandes archivos de datos, debido a la lentitud de Workbench es usar comandos específicos. Listamos el proceso a continuación. Esto puede cambiar ligeramente de equipo en equipo. En caso de no funcionar recuerda: Google es tu amigo. Más detalles puedes consultarlos aquí.

1.-Revisa la configuración de la variable local_infile, si muestra un valor ON, ve al paso 3, en caso contrario, ve al paso 2.

SHOW VARIABLES LIKE "local_infile";

-
-


2.-Ejecuta el siguiente comando:

SET GLOBAL local infile = 'ON';

-
-
3.-Revisa la configuración de la variable secure_file_priv, esto nos dará la ruta en nuestro equipo que tiene configurada MySQL Server para cargar archivos:

SHOW VARIABLES LIKE "secure_file_priv";
Por ejemplo:

C:\ProgramData\MySQL\MySQL Server 8.0\Uploads\

4.-Copia el archivo que deseas cargar en la ruta dada.

5.-Ejecuta el siguiente comando:

LOAD DATA INFILE 'C:\ProgramData\MySQL\MySQL Server 8.0\Uploads\ratings.csv' 
INTO TABLE ratings 
FIELDS TERMINATED BY ',' 
ENCLOSED BY '"' 
LINES TERMINATED BY '\n'
IGNORE 1 ROWS; 
Algunos sistemas operativos (Windows), requieren cambiar la posición de las diagonales:

LOAD DATA INFILE 'C:/ProgramData/MySQL/MySQL Server 8.0/Uploads/ratings.csv' 
INTO TABLE ratings 
FIELDS TERMINATED BY ',' 
ENCLOSED BY '"' 
LINES TERMINATED BY '\n'
IGNORE 1 ROWS; 

-
-

Observa cómo la carga lleva simplemente segundos.








<br/>

[`Anterior`](../Ejemplo-03/Readme.md) | [`Siguiente`](../Readme.md)
