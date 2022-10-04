[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 01`](../Readme.md) > `Ejercicios`
	
## Ejercicios Sesión 1

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Aplicar los conceptos adquiridos durante la sesión.

### 2. Requisitos :clipboard:

1. MySQL Workbench instalado y conectado al servidor del curso.

### 3. Desarrollo :rocket:

**En esta serie de ejercicios aplicarás los conceptos adquiridos durante la sesión:**

- Descripción de tablas  
- Consulta de los campos de una tabla  
- Cláusula WHERE  
- Operadores relacionales  
- Operadores lógicos  
- Cláusula ORDER BY  
- Cláusula LIMIT  

Todas las consultas que realices deberás mantenerlas dentro del editor de textos de MySQL Workbench. Al finalizar, guarda este archivo, llendo al menú `File` > `Save script`. Recuerda que para hacer consultas a una tabla debes conocer primero su estructura.

**Deberás entregar el archivo `.sql` correspondiente**

1. Dentro del mismo servidor de bases de datos, conéctate al esquema `classicmodels`.
	
![image](https://user-images.githubusercontent.com/104279978/193730750-8f1b637f-6d71-48c1-8bf6-1a6fa50e76f9.png)


2. Dentro de la tabla `employees`, obtén el apellido de todos los empleados.
	
![image](https://user-images.githubusercontent.com/104279978/193722361-f311cb7c-f81b-4eef-8348-5382e493e32c.png)
	

3. Dentro de la tabla `employees`, obtén el apellido, nombre y puesto de todos los empleados.
	
![image](https://user-images.githubusercontent.com/104279978/193722572-dffd5ec1-8d87-46c4-8d6f-33e180ccae51.png)


4. Dentro de la tabla `employees`, obtén todos los datos de cada empleado.
	
![image](https://user-images.githubusercontent.com/104279978/193722633-478432b1-583a-4498-afb3-9c60e7cfbe07.png)
	

5. Dentro de la tabla `employees`, obtén el apellido, nombre y puesto de todos los empleados que tengan el puesto `Sales Rep`.
	
![image](https://user-images.githubusercontent.com/104279978/193722848-a73aad2c-a7ce-480f-ab1a-087099020d0d.png)

	

6. Dentro de la tabla `employees`, obtén el apellido, nombre, puesto y código de oficina de todos los empleados que tengan el puesto `Sales Rep` y código de oficina `1`.

	
![image](https://user-images.githubusercontent.com/104279978/193723994-268c64c1-6d87-4e50-a05f-3fcd525a0434.png)
	
	

7. Dentro de la tabla `employees`, obtén el apellido, nombre, puesto y código de oficina de todos los empleados que tengan el puesto `Sales Rep` o código de oficina `1`.

	
![image](https://user-images.githubusercontent.com/104279978/193724714-d6743dfc-896c-44a8-a842-b17c4b398799.png)
	
	
8. Dentro de la tabla `employees`, obtén el apellido, nombre y código de oficina de todos los empleados que tenga código de oficina `1`, `2` o `3`.
	
![image](https://user-images.githubusercontent.com/104279978/193724965-238046e5-8240-4d1b-bd23-3b4d2d594865.png)
	

9. Dentro de la tabla `employees`, obten el apellido, nombre y puesto de todos los empleados que tengan un puesto distinto a `Sales Rep`.

![image](https://user-images.githubusercontent.com/104279978/193725244-6568e24b-dc19-4470-a190-9b726f3ebb14.png)
	


10. Dentro de la tabla `employees`, obtén el apellido, nombre y código de oficina de todos los empleados cuyo código de oficina sea mayor a `5`.

![image](https://user-images.githubusercontent.com/104279978/193725347-10339465-3c65-4473-83ec-2f60e623c60a.png)

	
	
11. Dentro de la tabla `employees`, obtén el apellido, nombre y código de oficina de todos los empleados cuyo cdigo de oficina sea menor o igual `4`.

	
![image](https://user-images.githubusercontent.com/104279978/193727266-13401f0d-54a3-4dc1-bb71-a8a2799cdfa8.png)
	
	
12. Dentro de la tabla `customers`, obtén el nombre, país y estado de todos los clientes cuyo país sea `USA` y cuyo estado sea `CA`.


![image](https://user-images.githubusercontent.com/104279978/193727800-833ef32d-1e32-407c-b767-3a7b8907def5.png)

	
	
13. Dentro de la tabla `customers`, obtén el nombre, país, estado y límite de crédito de todos los clientes cuyo país sea, `USA`, cuyo estado sea `CA` y cuyo límite de crédito sea mayor a `100000`.

	

![image](https://user-images.githubusercontent.com/104279978/193728047-fc474a98-b3f3-45be-a7d5-dd9c9fc16ec9.png)
	
	
14. Dentro de la tabla `customers`, obtén el nombre y país de todos los clientes cuyo país sea `USA` o `France`.
	

![image](https://user-images.githubusercontent.com/104279978/193728341-831f07af-3def-43cc-9fb4-893709a6ef7c.png)
	
	

15. Dentro de la tabla `customers`, obtén el nombre, país y límite de crédito de todos los clientes cuyo país sea `USA` o `France` y cuyo límite de crédito sea mayor a `100000`. Para este ejercicio ten cuidado con los paréntesis.
	

![image](https://user-images.githubusercontent.com/104279978/193728763-52944510-f468-4f16-be96-31e440c28711.png)

	
	
	
	
16. Dentro de la tabla `offices`, obtén el código de la oficina, ciudad, teléfono y país de aquellas oficinas que se encuentren en `USA` o `France`.

	

![image](https://user-images.githubusercontent.com/104279978/193731427-8c787cf7-9d48-4e5b-88bf-729db71e99b7.png)

	
	
	
17. Dentro de la tabla `offices`, obtén el código de la oficina, ciudad, teléfono y país de aquellas oficinas que *no* se encuentren en `USA` o `France`.
	

![image](https://user-images.githubusercontent.com/104279978/193731635-bdfada3e-dbc7-413b-9bd5-bb198f088733.png)
	
	

18. Dentro de la tabla `orders`, obtén el número de orden, número de cliente, estado y fecha de envío de todas las órdenes con el número `10165`, `10287` o `10310`.
	

	
![image](https://user-images.githubusercontent.com/104279978/193732508-06873ac4-1c1f-449d-92a9-871980d8acd4.png)


	
	
19. Dentro de la tabla `customers`, obtén el apellido de contacto y nombre de cada cliente y ordena los resultados por apellido de forma ascendente.
	
	

![image](https://user-images.githubusercontent.com/104279978/193729131-6a4b8f07-9628-44dc-b254-2c916feb717f.png)


	
	
20. Dentro de la tabla `customers`, obtén el apellido de contacto y nombre de cada cliente y ordena los resultados por apellido de forma descendente.

	
![image](https://user-images.githubusercontent.com/104279978/193729436-fc744bc1-cc01-418b-bb83-18aeb4c8731d.png)
	
	

21. Dentro de la tabla `customers`, obtén el apellido y nombre de cada cliente y ordena los resultados por apellido de forma descendente y luego por nombre de forma ascendente.
	

![image](https://user-images.githubusercontent.com/104279978/193730138-36794409-9806-4275-972c-774f22f0ea67.png)
	


22. Dentro de la tabla `customers`, obtén el número de cliente, nombre de cliente y el límite de crédito de los cinco clientes con el límite de crédito más alto (top 5).
	

	
![image](https://user-images.githubusercontent.com/104279978/193730407-43d929af-0635-4348-b8bd-a27c7169ae7e.png)
	
	


23. Dentro de la tabla `customers`, obtén el número de cliente, nombre de cliente y el límite de crédito de los cinco clientes con el límite de crédito más bajo diferente de 0.

![image](https://user-images.githubusercontent.com/104279978/193730639-fe534fd9-f8ab-43fa-ab62-3446a919a442.png)
	
	


**¡¡¡MUCHA SUERTE!!!**

<br/>

[`Anterior`](../Readme.md) | [`Siguiente`](../Readme.md)

</div>
