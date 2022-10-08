[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 03`](../Readme.md) > `Ejercicios`
	
## Ejercicios Sesión 3

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Aplicar los conceptos adquiridos durante la sesión.

### 2. Requisitos :clipboard:

1. MySQL Workbench instalado.

### 3. Desarrollo :rocket:

Todos los ejercicios debes hacerlos usando la base `classicmodels`.

Todas las consultas que realices deberás mantenerlas dentro del editor de textos de MySQL Workbench. Al finalizar, guarda este archivo, llendo al menú `File` > `Save script`.  **Recuerda añadir a todos los nombres te tus vistas el sufijo con tu identificador**.
-
	-
	-
	-
	-
	-
	
## Para estas consultas usa INNER JOIN*

1. Obtén la cantidad de productos de cada orden.


SELECT o.orderNumber, sum(quantityOrdered)
FROM orders o
JOIN orderdetails od
  ON o.orderNumber = od.orderNumber
GROUP BY o.orderNumber;




2. Obtén el número de orden, estado y costo total de cada orden.



SELECT o.orderNumber, o.status, sum(quantityOrdered * priceEach) total
FROM orders o
JOIN orderdetails od
  ON o.orderNumber = od.orderNumber
GROUP BY o.orderNumber, o.status;




3. Obtén el número de orden, fecha de orden, línea de orden, nombre del producto, cantidad ordenada y precio de cada pieza.


SELECT o.orderNumber, requiredDate, orderLineNumber, p.productName, quantityOrdered, priceEach
FROM orders o
JOIN orderdetails od
  ON o.orderNumber = od.orderNumber
JOIN products p
  ON od.productCode = p.productCode;




4. Obtén el número de orden, nombre del producto, el precio sugerido de fábrica (msrp) y precio de cada pieza.



SELECT o.orderNumber, p.productName, MSRP, priceEach
FROM orders o
JOIN orderdetails od
  ON o.orderNumber = od.orderNumber
JOIN products p
  ON od.productCode = p.productCode;



## Para estas consultas usa LEFT JOIN*

5. Obtén el número de cliente, nombre de cliente, número de orden y estado de cada orden hecha por cada cliente. ¿De qué nos sirve hacer `LEFT JOIN` en lugar de `JOIN`?



SELECT c.customerNumber, customerName, orderNumber, status
FROM customers c
LEFT JOIN orders o
  ON c.customerNumber = o.customerNumber;


6. Obtén los clientes que no tienen una orden asociada.


SELECT c.customerNumber, customerName
FROM customers c
LEFT JOIN orders o
  ON c.customerNumber = o.customerNumber
WHERE orderNumber IS NULL;





7. Obtén el apellido de empleado, nombre de empleado, nombre de cliente, número de cheque y total, es decir, los clientes asociados a cada empleado.



SELECT lastName, firstName, customerName, checkNumber, amount
FROM employees e
LEFT JOIN customers c 
ON e.employeeNumber = c.salesRepEmployeeNumber
LEFT JOIN payments ON 
    payments.customerNumber = c.customerNumber
ORDER BY customerName, checkNumber;




## Para estas consultas usa RIGHT JOIN*


8. Repite los ejercicios 5 a 7 usando *RIGHT JOIN*. ¿Representan lo mismo? Explica las diferencias en un comentario. Para poner comentarios usa `--`.



SELECT c.customerNumber, customerName, orderNumber, status
FROM customers c
RIGHT JOIN orders o
  ON c.customerNumber = o.customerNumber;
  
  
  
  SELECT c.customerNumber, customerName
FROM customers c
RIGHT JOIN orders o
  ON c.customerNumber = o.customerNumber
WHERE orderNumber IS NULL;


SELECT lastName, firstName, customerName, checkNumber, amount
FROM employees e
RIGHT JOIN customers c 
ON e.employeeNumber = c.salesRepEmployeeNumber
LEFT JOIN payments ON 
    payments.customerNumber = c.customerNumber
ORDER BY customerName, checkNumber;



9. Escoge 3 consultas de los ejercicios anteriores, crea una vista y escribe una consulta para cada una.






**¡¡¡MUCHA SUERTE!!!**


[`Anterior`](../Readme.md) | [`Siguiente`](../Readme.md)

</div>
