---
tags:
  - Notes
  - RDB
---

# Tipos de datos
- CHARACTER `[ VARYING ]` (n)
- BIT `[ VARYING ]` (n)
- NUMERIC (p,q)
- DECIMAL (p,q)
- INTEGER
- SMALLINT
- FLOAT (p)
- DATE
- TIME
- TIMESTAMP
- INTERVAL
# Esquema de información
## Catalogo y esquema
> Un `catalogo de SQL` consiste en los descriptores de esa parte de la base de datos individual, mientras que un `esquema de SQL` consiste en los descriptores de esa parte de la base da tos que pertenece a un usuario individual
> [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p87

# Dato interesante
>en el estándar de SQL ¡no existe el termino "base de datos"! La forma exacta en que se denomina al conjunto de datos que describe el catalogo, esta definida en la implementación. Sin embargo, es razonable pensar en dicho conjunto como en una base datos. 
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p87

# Conceptos que no aplica
SQL no aplica ciertos conceptos del [[Modelo relacional de datos]]

- Relación : En su lugar utiliza el concepto `tabla`
- Varrel : En su lugar utiliza el concepto `tabla`
- Encabezado
- Cuerpo
