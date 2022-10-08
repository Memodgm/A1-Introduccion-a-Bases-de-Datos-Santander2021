[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 03`](../Readme.md) > `Reto 2`
	
## Reto 2: Definición de vistas

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Definir vistas sobre algunas consultas.

### 2. Requisitos :clipboard:

1. MySQL Workbench instalado.

### 3. Desarrollo :rocket:

---

<img src="../../imagenes/tabla.gif" align="right" height="170" width="200"> 

:warning: <ins>**IMPORTANTE**</ins>

_Para este reto necesitarás un identificador único. Tu identificador serán los últimos tres dígitos de tu número de celular. Por ejemplo, si tu número es: 5512345678 tu identificador debe ser 678. <ins>¡No lo olvides!</ins>_   

_**Te pedimos esto para que todos puedan realizar los ejemplos y retos.**_


_Si no sigues las instruciones..._   

---

Usando la base de datos `tienda`, define las siguientes vistas que permitan obtener la siguiente información.

**AÑADE A TODOS LOS NOMBRES DE TUS VISTAS EL SUFIJO `_<tu identificador>`.** Por ejemplo `mi_vista_hermosa_123`.

- Obtener el puesto de un empleado.

CREATE VIEW puestos_123 AS
SELECT concat(e.nombre, ' ', e.apellido_paterno), p.nombre
FROM empleado e
JOIN puesto p
  ON e.id_puesto = p.id_puesto;
  
  SELECT *
FROM puestos_123;



- Saber qué artículos ha vendido cada empleado.


CREATE VIEW empleado_articulo_123 AS
SELECT v.clave, concat(e.nombre, ' ', e.apellido_paterno) nombre, a.nombre articulo
FROM venta v
JOIN empleado e
  ON v.id_empleado = e.id_empleado
JOIN articulo a
  ON v.id_articulo = a.id_articulo
ORDER BY v.clave;





SELECT *
FROM  empleado_articulo_123;

- Saber qué puesto ha tenido más ventas.


CREATE VIEW puesto_ventas_123 AS
SELECT p.nombre, count(v.clave) total
FROM venta v
JOIN empleado e
  ON v.id_empleado = e.id_empleado
JOIN puesto p
  ON e.id_puesto = p.id_puesto
GROUP BY p.nombre;


SELECT *
FROM puesto_ventas_123
ORDER BY total DESC
LIMIT 1;



<br/>

[`Anterior`](../Ejemplo-02/Readme.md) | [`Siguiente`](../Readme.md)

</div>
