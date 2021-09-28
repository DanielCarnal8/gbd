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
