[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 06`](../Readme.md) > `Reto 3`
	
## Reto 3: Introducción a las agregaciones

<div style="text-align: justify;">

### 1. Objetivos :dart: 

- Proyectar columnas sobre distintos documentos para repasar algunos conceptos.

### 2. Requisitos :clipboard:

1. MongoDB Compass instalado.

### 3. Desarrollo :rocket:

Usando la colección `sample_airbnb.listingsAndReviews`, mediante el uso de agregaciones, 
![image](https://user-images.githubusercontent.com/104279978/196840837-af25414f-2e2d-40b8-94a5-ec7df086ca26.png)

encontrar el número de publicaciones que tienen conexión a Internet, sea desde Wifi o desde cable (Ethernet).

-
-
-

## Debe mostrar automaticamente la previsualización al agregar la consulta , si no aparece es porque se agregaron corchetes de más.

1.- Primero filtramos los documentos con Internet desde Wifi o desde cable. Para ello usamos
	
	$match 
	
que permite realizar filtros dentro de agregaciones.


   amenities: {$in: ["Wifi", "Ethernet"]}



![image](https://user-images.githubusercontent.com/104279978/194728391-a8aa1d17-95b4-44a1-a374-6bb7ed1b70ee.png)

2.- Ahora contamos el número de registros resultantes con
	
	$group
	
 Los agrupamientos al igual que en SQL necesitan un campo por el cual agrupar y una función de agrupamiento.

Dado que contaremos los registros no necesitamos campo, así que ponemos      _id: null.

Para agrupar usaremos la función $sum con el parámetro 1. Es decir, por cada documento sumará un 1, trayendo al final el total de documentos.


   _id: null,
   total: {
      $sum: 1
   }



![image](https://user-images.githubusercontent.com/104279978/194728402-4166e950-211d-427e-8905-d1e391d9c36d.png)












<br/>

[`Anterior`](../Ejemplo-03/Readme.md) | [`Siguiente`](../Readme.md)

</div>
