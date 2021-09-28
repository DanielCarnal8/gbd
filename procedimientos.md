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
