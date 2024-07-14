---
tags:
  - Notes
  - RDB
  - DB
---
# Sub lenguajes
- [[Data definition language|DDL]]
- [[Data manipulation Language|DML]]
- [[Data control language|DCL]]
- [[Transaction control language|TCL]]
## Catálogo y esquema
> Un `catálogo de SQL` consiste en los descriptores de esa parte de la base de datos individual, mientras que un `esquema de SQL` consiste en los descriptores de esa parte de la base da tos que pertenece a un usuario individual
> [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p87

# SQL + otros lenguajes
- [[SQL incrustado]]
# Dato interesante
>en el estándar de SQL ¡no existe el termino "base de datos"! La forma exacta en que se denomina al conjunto de datos que describe el catalogo, esta definida en la implementación. Sin embargo, es razonable pensar en dicho conjunto como en una base datos. 
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p87

# Conceptos que no aplica
SQL no aplica ciertos conceptos del [[Modelo relacional de datos]]

- Relación
	- Ya que no cumple con las primeras tres [[Relación#Propiedades|propiedades]] de una relación
- Tipos
	- El usuario no puede crear dominios (que no este formados por un solo dominio integrado), no puedes asignar operadores a los mismos