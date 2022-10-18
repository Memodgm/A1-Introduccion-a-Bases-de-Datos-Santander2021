[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 05`](../Readme.md) > `Reto 2`
	
## Reto 2: Filtros básicos

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Proyectar columnas sobre distintos documentos para repasar algunos conceptos.

### 2. Requisitos :clipboard:

1. MongoDB Compass instalado.

### 3. Desarrollo :rocket:

Usando la base de datos `sample_mflix`, agrega proyeccciones, filtros, ordenamientos y límites que permitan contestar las siguientes preguntas:
-
-
-
-
	-
	

	
### Ahora no se pusieron solo en filter , checarlo 	

	
	
- ¿Qué comentarios ha hecho Greg Powell?


{name: "Greg Powell"}

	
![image](https://user-images.githubusercontent.com/104279978/194728062-64f0bda8-9372-4254-bc6e-92243ad8a46e.png)






- ¿Qué comentarios han hecho Greg Powell o Mercedes Tyler?

poner en filter
	-
	-
	

{$or: [{name: "Greg Powell"}, {name: "Mercedes Tyler"}]}


![image](https://user-images.githubusercontent.com/104279978/194728071-4d6649d9-f155-4aed-8262-12e0fa5f9ee0.png)


	


- ¿Cuál es el máximo número de comentarios en una película?



Para responder esta pregunta, necesitamos tres cosas.

i.- Proyectar el número de comentarios en project 
	-
	-
	
{num_mflix_comments: 1}	

ii.-Ordenar el número de comentarios de forma descendente en sort.
	-
	-
	-
	
{num_mflix_comments:-1}

iii.-Limitar los resultados a 1.




![image](https://user-images.githubusercontent.com/104279978/194728098-5be7abc0-a364-458e-ad52-55327302e01f.png)
	
	
	
	


- ¿Cuál es título de las cinco películas más comentadas?

Para responder esta pregunta, necesitamos tres cosas.

i.-Proyectar el título de las películas en project.
	-
	-
	
{title: 1}	

ii.-Ordenar el número de comentarios de forma descendente en sort.
-
-
	
{num_mflix_comments: -1}

iii.-Limitar los resultados a 5.

![image](https://user-images.githubusercontent.com/104279978/194728118-8055eec9-f67e-425b-80fe-d55286ed5124.png)





<br/>

[`Anterior`](../Ejemplo-02/Readme.md) | [`Siguiente`](../Readme.md)

</div>
