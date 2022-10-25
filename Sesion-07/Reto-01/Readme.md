[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 07`](../Readme.md) > `Reto 1`
	
## Reto 1: Agrupamientos

<div style="text-align: justify;">

### 1. Objetivos :dart: 

- Poner en práctica el uso de agrupamientos.

### 2. Requisitos :clipboard:

1. MongoDB Compass instalado.

### 3. Desarrollo :rocket:

Con base en el ejemplo 1, modifica el agrupamiento para que muestre el costo promedio por habitación por país de las propiedades de tipo casa.

Cada que agreguemos un filtro usar boton

![image](https://user-images.githubusercontent.com/104279978/197655164-84a0cf14-4ef5-4160-9d19-a8a7ced293b6.png)

-
-
Filtramos las propeidades con 
	$match

{
   property_type: 'House',
   bedrooms: {$gte: 1}
}


![image](https://user-images.githubusercontent.com/104279978/196056577-0e38f4ef-2a90-4573-92c0-b3d697d8a080.png)

-
-

Agregamos el costo por recámara con
	
 $addFields

{
   costo_recamara: {$divide: ["$price", "$bedrooms"]}
}


![image](https://user-images.githubusercontent.com/104279978/196056589-18f970dc-9c16-448c-91f4-67abfad68958.png)



-
-
Agrupamos la suma de recamaras y del total agrupando en este caso por país. Para ello usamos
	
 $group.

{
  _id: "$address.country",
  recamaras: {
    $sum: 1
  },
  total: {
    $sum: "$costo_recamara"
  }
}



![image](https://user-images.githubusercontent.com/104279978/196056602-69cb8b4c-d047-4c87-8f21-2fc946ed3698.png)



-
-
Agregamos el campo costo promedio para cada pas con
	
 $addFields
	
, creamos un alias al _id para hacer más claro el valor que guarda.

{
  pais: "$_id",
  costo_promedio: {$divide: ["$total", "$recamaras"]}
}


![image](https://user-images.githubusercontent.com/104279978/196056621-4e999440-39fe-476c-8045-54dd84e152e9.png)



-
-
Agregamos una proyección para quitar campos irrelevantes con project.

{
  _id:0,
  pais:1,
  costo_promedio:1
}


![image](https://user-images.githubusercontent.com/104279978/196056641-2e222943-5864-47ec-a893-de994bbc0217.png)












<br/>

[`Anterior`](../Ejemplo-01/Readme.md) | [`Siguiente`](../Readme.md)   
