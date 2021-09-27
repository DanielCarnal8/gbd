#FUNCIONES CON BBDD

## PARA EL USO DE FUNCIONES HACE FALTA ESTAR DENTRO DE UNA BASE DE DATOS O CREAR UNA. EN MI CASO CREO UNA BASE DE DATOS QUE SE LLAMA FUNCIONES

```sql
IF OBJECT_ID('tbl_kunde', N'U') is not null
	drop table tbl_kunde;
GO
create table tbl_kunde (
  id_kunde int not null primary key,
  fi_moral_nr int,
  name varchar(25) not null,
  vorname varchar not null,
  wohnort varchar
);
GO
```




