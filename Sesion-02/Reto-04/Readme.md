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
	
![image](https://user-images.githubusercontent.com/104279978/194204635-1ce938ba-b429-422d-a2d3-1ed5e5fcc393.png)

	
- ¿Cuál es la cantidad mínima y máxima de ventas de cada empleado?
	
	
	
SELECT id_empleado, min(total_ventas), max(total_ventas)
FROM
 (SELECT clave, id_empleado, count(*) total_ventas
      FROM venta
      GROUP BY clave, id_empleado) AS sq
GROUP BY id_empleado;	
	

	
- ¿Cuál es el nombre del puesto de cada empleado?
	
SELECT nombre, apellido_paterno, (SELECT nombre FROM puesto WHERE id_puesto = e.id_puesto)
FROM empleado AS e;	
	

<br/>

[`Anterior`](../Ejemplo-04/Readme.md) | [`Siguiente`](../Readme.md)            

</div>
