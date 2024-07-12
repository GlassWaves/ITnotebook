---
tags:
  - Notes
  - RDB
---
# Sub lenguajes
- [[Data definition language|DDL]]
- [[Data manipulation Language|DML]]
- [[Data control language|DCL]]
- [[Transaction control language|TCL]]
## Catálogo y esquema
> Un `catálogo de SQL` consiste en los descriptores de esa parte de la base de datos individual, mientras que un `esquema de SQL` consiste en los descriptores de esa parte de la base da tos que pertenece a un usuario individual
> [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p87

# SQL incrustado
Instrucciones SQL que pueden estar entremezcladas con las instrucciones del lenguaje de programación de una aplicación [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p89

## Sintaxis
```SQL
EXEC SQL BEGIN DECLARE SECTION;

	DCL SQLTATE CHAR(5);
	DCL P# CHAR(6);
	DCL PESO FIXED DECIMAL(5,1);
	
EXEC SQL END DECLARE SECTION;

P# = 'P2'

EXEC SQL SELECT P.PESO
		 INTO :PESO
		 FROM P
		 WHERE P.P# = :P#;
IF SQLSTATE = '00000'
THEN ...;
ELSE ...;
```
 - `EXEC SQL` sirve para distinguir las instrucciones `SQL` de las del lenguaje anfitrión
 - Las `variables anfitrión` que serán referenciadas deben estar declaradas entre `BEGIN` y `END DECLARE SECTION` y precedidas por un `DCL`
 -  Las `variables anfitrión` al ser referenciadas debe ser precedidas por `:` (ejemplo `:PESO`)
 - Debe de haber una `variable anfitrión` llamada `SQLSTATE`, que mediante código indicara el estado de ejecución de las instrucciones SQL
	 - `00000` : se ejecutó con éxito
	 - `02000` : se ejecutó pero no se encontraron datos
- Los tipos de datos de las `variables anfitrión` deben ser apropiadas para lo que serán usadas
- Las `variables anfitrión` y las `columnas SQL` pueden tener el mismo nombre

### WHENEVER
Cuando la comprobación no se desea hacer con la variable anfitrión `SQLSTATE` entonces se usa :

```SQL
EXEC SQL WHENEVER <condicion> <acción>;
```

- Valores de `<condicion>`
	- `SQLERROR`
	- `NOT FOUND`
- Valores de `<acción>`
	- `CONTINUE`
		- El programador insertará a mano las instrucciones
	- `GO TO`
		- `IF <condición> GO TO <etiqueta> END IF
## Cursores
### Operaciones que involucran cursores
Debido a que generalmente los lenguajes de programación no cuentan con mecanismos para la recuperación de filas a nivel de conjunto (muchas filas a la vez), los `cursores` sirven como un puente entre el `lenguaje de programación` y `SQL` para recuperar las filas una a la vez

```SQL
EXEC SQL DECLARE X CURSOR FOR
	SELECT V.V#, V.PROVEEDOR, V.STATUS
	FROM V
	WHERE V.CIUDAD = :Y
	ORDER BY V# ASC;

EXEC SQL OPEN X;
	DO 
		EXEC SQLFETCH X INTO :V#, :PROVEEDOR, :STATUS;
		END;
EXEC SQL CLOSE X;
```

- ``
### Operaciones que no involucran cursores
- SELECT /*individual*/
- INSERT
- UPDATE
- DELETE

# Dato interesante
>en el estándar de SQL ¡no existe el termino "base de datos"! La forma exacta en que se denomina al conjunto de datos que describe el catalogo, esta definida en la implementación. Sin embargo, es razonable pensar en dicho conjunto como en una base datos. 
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p87

# Conceptos que no aplica
SQL no aplica ciertos conceptos del [[Modelo relacional de datos]]

- Relación : En su lugar utiliza el concepto `tabla`
- Varrel : En su lugar utiliza el concepto `tabla`
- Encabezado
- Cuerpo
