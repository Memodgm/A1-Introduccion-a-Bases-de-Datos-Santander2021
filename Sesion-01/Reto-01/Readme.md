[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 01`](../Readme.md) > `Reto 1`
	
## Reto 1: Estructura de una tabla

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Consultar la estructura de algunas tablas.

### 2. Requisitos :clipboard:

1. MySQL Workbench instalado.

### 3. Desarrollo :rocket:

Usando la base de datos `tienda`, muestra la descripción de las tablas `articulo`, `puesto` y `venta`. Por cada tipo de dato que encuentres llena la siguiente tabla (a mano, puedes dibujarla en un cuaderno o dónde tú prefieras). Usa la [Documentación de MySQL](https://dev.mysql.com/doc/refman/8.0/en/data-types.html) como referencia si no recuerdas cómo se usa un comando, o por supuesto, preguntarle al experto.

	
	
                   Tabla artículo
	
| Tipo   | Descripción |
|---|---|
| int  | id_articulo  |
| varchar(45)  | nombre  |
| double | precio |
| double | iva  |
| int  | cantidad |

	
	
	
	
	
	
                    Tabla puesto
	
| Tipo   | Descripción |
|---|---|
| int  |  id_puesto |
| varchar(45)  | nombre  |
| double | salario |
	
	
	
	
	
	
                    Tabla venta
	
| Tipo   | Descripción |
|---|---|
| int  | id_venta |
| int  | id_articulo |
| int  | id_empleado |
| varchar(45)  | clave |
| timestamp  | fecha |


	
	
	
	
	
<br/>

[`Anterior`](../Ejemplo-02/Readme.md) | [`Siguiente`](../Readme.md)

</div>
