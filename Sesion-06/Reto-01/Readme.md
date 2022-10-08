[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 06`](../Readme.md) > `Reto 1`
	
## Reto 1: Expresiones regulares

<div style="text-align: justify;">

### 1. Objetivos :dart: 

- Poner en práctica el uso de expresiones regulares.

### 2. Requisitos :clipboard:

1. MongoDB Compass instalado.

### 3. Desarrollo :rocket:

Usando la base de datos `sample_airbnblistingsAndReviews`, realiza los siguientes filtros:
-
-
-
-

- Propiedades que no permitan fiestas.

{house_rules: /No Parties/i}

![image](https://user-images.githubusercontent.com/104279978/194728315-03317c03-312b-4543-8270-75f3d279ab91.png)


- Propiedades que admitan mascotas.

{house_rules: /Pets Allowed/i}

![image](https://user-images.githubusercontent.com/104279978/194728322-4f75e868-a04a-411f-a06e-2d524ad43a5e.png)




- Propiedades que no permitan fumadores.


{house_rules: /No Smoking/i}	

![image](https://user-images.githubusercontent.com/104279978/194728331-8efea56b-84e2-4b7a-beef-a265a8819846.png)



- Propiedades que no permitan fiestas ni fumadores.

{house_rules: /No Smoking|No Parties/i}


![image](https://user-images.githubusercontent.com/104279978/194728336-fb379c3e-f4b9-4d70-a474-cfa0037c9fa4.png)





<br/>

[`Anterior`](../Ejemplo-01/Readme.md) | [`Siguiente`](../Readme.md)

</div>
