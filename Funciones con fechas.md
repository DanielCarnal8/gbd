# FUNCIONES CON FECHAS

## DIFERENCIAS ENTRE DÍAS, MESES, AÑOS Y HORAS.

```sql
-- Diferencias de años --
select DATEDIFF(YEAR, '2011/08/25','2017/08/25') as AñosDiferencia

-- Diferencia de meses --
select DATEDIFF(MONTH, '2011/08/25','2017/08/25') as MesesDiferencia

-- Diferencia de dias --
select DATEDIFF(DAY, '2011/08/25','2017/08/25') as DiasDiferencia

-- Diferencia de horas --
select DATEDIFF(HOUR, '2011/08/25 07:00','2017/08/25 12:45') as HorasDiferencia
```

## FUNCION QUE DEVULEVE COMO SALIDA EL NUMERO DE AÑOS QUE HAN TRASCURRIDO ENTRE DOS FECHAS QUE SE RECIBEN COMO PARAMETROS DE ENTRADA

```sql
drop function if exists CalculoNumeroAños
go

create function dbo.CalculoNumeroAños
(
@f_inicial date,
@f_final date
)
returns int
as
	begin
		declare
			@años int
			set @años=DATEDIFF(YEAR, @f_inicial,@f_final)
			return @años
	end

select dbo.CalculoNumeroAños('2008/01/01','2020/05/05') as Fecha
```

## MISMA FUNCIÓN ANTERIOR QUE LA ANTERIOR PERO CON LA HORA DEL SISTEMA

```sql
drop function if exists CalculoFechaSistema
go

create function dbo.CalculoFechaSistema
(
@f_inicial date
)
returns int
as
	begin
		declare
			@años int
			set @años=DATEDIFF(YEAR, @f_inicial,GETDATE())
			return @años
	end

select dbo.CalculoFechaSistema('2008/01/01') as Años

```
