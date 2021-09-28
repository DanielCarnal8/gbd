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
## FUNCIÓN QUE DA LA MEDIA ENTRE DOS NÚMEROS

```sql
Drop function if exists F_promedio
go

create function dbo.F_promedio
(
@valor1 dec (6,3),
@valor2 dec (6,3)
)
returns dec (6,3)
as
	begin
		declare
			@resultado dec (6,3)
			set @resultado=(@valor1+@valor2)/2
			return @resultado
	end

select dbo.F_promedio(15,20) as 'El numero promedio es: '
```
