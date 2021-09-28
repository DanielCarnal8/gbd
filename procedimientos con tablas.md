#PROCEDIMIENTOS EN LOS QUE SE USAN TABLAS DE POR MEDIO.

## Primero se realiza la creación de una tabla
```sql
create database Clientes
go

use Clientes
go

create table tabla_clientes
(
Codigo char(4) NULL,
Nombre varchar(50) NULL,
DNI char(8) NULL,
Pais varchar(15) NULL,
Forma_Pago varchar(15) NULL,
Importe int NULL
)
go
```

## A continuación se insertan datos en las tablas
```sql
insert into tabla_clientes(Codigo,Nombre,DNI,Pais,Forma_Pago,Importe)
values
('Mad1','Antonio','01928374','Portugal','PayPal',1200),
('0002','Ana','8765432','España','Transferencia',150320),
('0003','Peter','1357902','EEUU','T_Credito',65230),
('0004','Sara','2468013','EEUU','PayPal',1200),
('0005','Sophy','5310864','Francia','Transferencia',220650),
('0006','Claire','0102030','Francia','PayPal',650950),
('0007','Toni','4030201','Italia','T_Credito',800),
('0008','Maria','1213141','Italia','PayPal',650),
('0009','Clara','21222324','España','Transferencia',220650),
('0010','John','9192939','EEUU','Transferencia',900540)
go
```
![sql](https://user-images.githubusercontent.com/72084639/135062409-271c306a-cbe2-4acd-848c-717e570bdf01.PNG)
