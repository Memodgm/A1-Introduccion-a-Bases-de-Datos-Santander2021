[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 02`](../Readme.md) > `Reto 4`
	
## Reto 4: Subconsultas

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Escribir consultas que permitan responder a algunas preguntas.

### 2. Requisitos :clipboard:

1. MySQL Workbench instalado.

### 3. Desarrollo :rocket:

Usando la base de datos `tienda`, escribe consultas que permitan responder las siguientes preguntas.
	
	


- ¿Cuál es el nombre de los empleados cuyo sueldo es menor a $10,000?
	
Nota: sale NULL porque todos  los suledos son mayores a 10000.


1.- Las tablas puesto y empleado tienen en comùn id_puesto.
	
2.- Se filtrò primero en puesto por los salarios.   
	
3.- Luego, empleado por el nombre y apellido del empleado.
	
se unen con:
WHERE id_puesto IN(
SELECT id_puesto

![image](https://user-images.githubusercontent.com/104279978/194204635-1ce938ba-b429-422d-a2d3-1ed5e5fcc393.png)



	
- ¿Cuál es la cantidad mínima y máxima de ventas de cada empleado?
	
las tablas ventas y empleado tienen en comun id_empleado.
	
1.- se obtiene de la tabla ventas la cantidad de ventas que hizo cada empleado por clave , id_empleado.
	
2.- se hace el agrupamiento para obtener la cantidad mìnima y màxima que vendiò cada empleado  
	
![image](https://user-images.githubusercontent.com/104279978/194204937-44654e73-d22e-4e81-9c38-d89950cc1f6c.png)


	
- ¿Cuál es el nombre del puesto de cada empleado?
	
![image](https://user-images.githubusercontent.com/104279978/194204999-49f6c5d1-2280-4113-ab3b-4af06ad499cf.png)	
	

<br/>

[`Anterior`](../Ejemplo-04/Readme.md) | [`Siguiente`](../Readme.md)            

</div>
