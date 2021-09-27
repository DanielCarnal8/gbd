# FUNCIONES CON BBDD

## PARA EL USO DE FUNCIONES HACE FALTA ESTAR DENTRO DE UNA BASE DE DATOS O CREAR UNA. EN MI CASO CREO UNA BASE DE DATOS QUE SE LLAMA FUNCIONES

```sql
create database Funciones
go

use Funciones
go
```
###### UNA VEZ HECHO EN PASO ANTERIOR YA PODEMOS REALIZAR FUNCIONES


## FUNCIÓN QUE TE DA UN MENSAJE EN PANTALLA 


```sql
drop function if exists holamundo
go

create function dbo.holamundo()
returns varchar(20)
as
	Begin
		return 'Hola mundo'
	end
go

select dbo.holamundo() as Mensaje
```
