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

## FUNCIÓN QUE INDICA EL NÚMERO MÁS GRANDE ENTRE TRES DE ESTOS

```sql
drop function if exists CalcularMayor
go

create function dbo.CalcularMayor
(
@numero1 dec(6,3),
@numero2 dec(6,3),
@numero3 dec(6,3)
)
returns varchar (50)
as
	begin
		declare
			@mayor dec(6,3)
		if(@numero1=@numero2) and (@numero1=@numero3)
			return 'Los tres numero son iguales'
		else
			if(@numero1>@numero2) and (@numero1>@numero3)
				begin
					set @mayor=@numero1
					return 'El mayor numero de los 3 es: '+cast(@mayor as varchar(30))
				end
				else
					if(@numero2>@numero1) and (@numero2>@numero3)
						begin
							set @mayor=@numero2
							return 'El mayor numero de los 3 es: '+cast(@mayor as varchar(30))
						end
				else
					set @mayor=@numero3
					return 'El mayor numero de los 3 es: '+cast(@mayor as varchar(30))
	end

select dbo.CalcularMayor(10,108,100) as Mensaje
```
