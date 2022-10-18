[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 05`](../Readme.md) > `Ejercicios`
	
## Ejercicios Sesión 5

<div style="text-align: justify;">

### 1. Objetivos :dart: 

- Aplicar los conceptos adquiridos durante la sesión.

### 2. Requisitos :clipboard:

1. MongoDB Compass instalado.

### 3. Desarrollo :rocket:

Las consultas se realizarán sobre la base `sample_training`.

Todas las consultas que realices deberás mantenerlas dentro del MongoDB Compass. Para hacer esto, da clic en el botón con los puntos `···` y en `Toogle Query History`.
	![image](https://user-images.githubusercontent.com/104279978/196324099-12ae927f-c8bf-4362-935d-ae86933e0509.png)
Busca la última consulta y agrégala a favoritos presionando el ícono con la estrella :star:.
-
-
-
-

## 1. Obtén los datos de contacto de cada compañía.

  en Proyección.
-
-

{email_address:1, phone_number:1}



## 2. Obtén el identificador de la clase de cada calificación.


 en  Proyección. 
-
-
{class_id: 1}



## 3. Obtén el nombre de todas las compañias fundadas en octubre.


en Filtro
-
-

{founded_month: 10}




## 4. Obtén el nombre de todas las compañías fundadas en 2008.


en Filtro. 
-
-
{founded_year: 2008}
-

en Proyección. 
-

-
{name:1}





## 5. Obtén todos los *post* del autor `machine`.




en Filtro. 
-
-
{author:"machine"}




## 6. Obtén todas las calificaciones provenientes de los grupos `357`, `57` y `465`.


en  Filtro. 
-
-
{class_id: {$in: [350, 57, 465]}}



## 7. Obtén todas las compañías fundadas en octubre del 2008.



en Filtro. 
-
-
{founded_year: 2008, founded_month:10}




## 8. Obtén todas las compañias con más de 50 empleados. 


en  Filtro.
-
-
{number_of_employees: {$gt: 50}}



## 9. Obtén las rutas con un número de paradas entre 1 y 5.



en Filtro. 
-
-
{$and: [{stops: {$gte: 1}}, {stops: {$lte: 5}}]}



## 10. Obtén la empresa con el menor número de empleados.



en Filter.
-
-
{number_of_employees: {$ne:null}}
-
-
en  Ordenamiento. 
-

-
{number_of_employees:1}
-

en Limit. 
1



## 11. Obtén la empresa con el mayor número de empleados.



en Ordenamiento. 
-
-
{number_of_employees:-1}
-
-

en Limit. 
-

1


## 12. Obtén el viaje con mayor duración.



en Ordenamiento. 
-

{tripduration: -1}
-
-
en  Limit. 
-
-
1





## 13. Obtén el viaje con menor duración.
o 
13.b Obtén la historia menos comentada.


en Ordenamiento.
-
-
-

{tripduration: -1}
-
-

en  Limit. 
-
-
1




**¡¡¡MUCHA SUERTE!!!**

<br/>

[`Anterior`](../Readme.md) | [`Siguiente`](../Readme.md)

</div>

