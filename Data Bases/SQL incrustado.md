---
tags:
  - Notes
  - RDB
---
Instrucciones SQL que pueden estar entremezcladas con las instrucciones del lenguaje de programación de una aplicación [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p89

# Sintaxis
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

## WHENEVER
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
# Cursores
## Operaciones que involucran cursores
Debido a que generalmente los lenguajes de programación no cuentan con mecanismos para la recuperación de filas a nivel de conjunto (muchas filas a la vez), los `cursores` sirven como un puente entre el `lenguaje de programación` y `SQL` para recuperar las filas una a la vez.

### Sintaxis
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

- Se tiene que declarar `X CURSOR` para asignarle el conjunto a recuperar
- Para declarar el `FETCH` tiene que estar entre `OPEN/CLOSE <nombre del cursor>`
- `FETCH` es el que ayuda a recuperar una por una las filas del conjunto
- El cursor avanza en la `fila[i]` del conjunto activo y el valor correspondiente es asignado a la `variableAnfitrión[i]` especificada en la clausula `INTO`

```SQL
EXEC SQL <UPDATE/DELETE> V
	...
	WHERE CURRENT OF X;
```
- CURRENT permite realizar las operaciones `UPDATE` y `DELETE` en la fila actual en la que se encuentre el cursor
	- Esto no aplica cuando la vista esta restringida
## Operaciones que no involucran cursores
- SELECT /*individual*/
- INSERT
- UPDATE
- DELETE

# SQL dinámico
>Serie de propiedades del [[SQL incrustado]] que están destinadas a apoyar la construcción de aplicaciones generales, en línea y posiblemente interactivas
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p96

# Sintaxis
```SQL
DCL SQLFUENTE CHAR VARYING(6500);

SQLFUENTE = 'DELETE FROM VP WHERE CANT < 300';
EXEC SQL PREPARE SQLPREPARADO FROM :SQLFUENTE;
EXEC SQL EXECUTE SQLPREPARADO;

```

- `SQLFUENTE` : Variable `PL/I`, almacena la instrucción SQL
- `SQLPREPARADO` : Variable `SQL`, almacena de manera compilada la instrucción de `SQLFUENTE`
- `PREPARE` : Compila la instrucción de `SQLFUENTE`
- `EXECUTE` : Ejecuta `SQLPREPARADO`
