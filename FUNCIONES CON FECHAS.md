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
