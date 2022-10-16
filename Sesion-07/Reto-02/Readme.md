[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 07`](../Readme.md) > `Reto 2`
	
## Reto 2: Asociación de colecciones

<div style="text-align: justify;">

### 1. Objetivos :dart: 

- Proyectar columnas sobre distintos documentos para repasar algunos conceptos.

### 2. Requisitos :clipboard:

1. MongoDB Compass instalado.

### 3. Desarrollo :rocket:

Usando las colecciones `comments` y `users`, se requiere conocer el correo y contraseña de cada persona que realizó un comentario. Construye un pipeline que genere como resultado estos datos.

---

:warning: **NO CIERRES ESTE *PIPELINE* PUES LO USAREMOS MÁS ADELANTE**

---



Primero, obtenemos la relación con $lookup.

{
  from: 'users',
  localField: 'name',
  foreignField: 'name',
  as: 'usuario'
}

![image](https://user-images.githubusercontent.com/104279978/196056756-dda6bda3-664a-4a21-98eb-8568ba184637.png)




-
-
Posteriormente, obtenemos el objeto del arreglo, su campo password y finalmente proyectamos los datos necesarios.

$addFields
{
  usuario_objeto: {$arrayElemAt: ["$usuario", 0]}
}
$addFields
{
  usuario_password: "$usuario_objeto.password"
}
$project
{
  _id:0,
  name:1,
  email:1,
  usuario_password:1
}



![image](https://user-images.githubusercontent.com/104279978/196056774-7666f5e3-d211-49ad-830a-b2c307a7f0d4.png)












<br/>

[`Anterior`](../Ejemplo-02/Readme.md) | [`Siguiente`](../Readme.md)   

</div>
