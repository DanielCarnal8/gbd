## SUMAS

```sql
drop procedure if exists suma
go

create procedure suma
@dato_1 int,
@dato_2 int
as
begin
	declare
		@suma int
	set @suma=@dato_1+@dato_2
	print 'La suma es: '+cast(@suma as varchar(6))  -- "cast" convierte una variable numerica a varchar o caracter --
end

exec suma 12,9  -- una vez ejecutada la suma la podremos ejecutar las veces que queramos porque estamos borrando el procedimeinto --

```
## AREAS, EN ESTE CASO DE UN TRAPECIO
```sql 
drop procedure if exists Trapecio
go

create procedure Trapecio
@base_Ma int,
@base_me int,
@altura int
as
	begin
		declare
			@area int
		set @area=((@base_MA+@base_me)*@altura)/2
		print 'EL valor del area es: '+cast(@area as varchar(5))
end

exec Trapecio 10,8,5
```
## CALCULADORA
```sql
drop procedure if exists calculadora
go

create procedure calculadora
@num_1 int,
@num_2 int,
@opera char(1)

as
	begin
		declare
			@resultado int
-- procedie¡miento para la suma --
		if @opera= '+'
			begin
				set @resultado=(@num_1+@num_2)
				print 'El resultado de la suma es: '+cast (@resultado as varchar(10))
			end
		if @opera= '-'
			begin
				set @resultado=(@num_1-@num_2)
				print 'El resultado de la resta es: '+cast (@resultado as varchar(10))
			end
		if @opera= '*'
			begin
				set @resultado=(@num_1*@num_2)
				print 'El resultado de la multiplicacion es: '+cast (@resultado as varchar(10))
			end
		if @opera= '/'
			begin
				set @resultado=(@num_1/@num_2)
				print 'El resultado de la division es: '+cast (@resultado as varchar(10))
			end
	end

exec calculadora 15,8,'-'
```
