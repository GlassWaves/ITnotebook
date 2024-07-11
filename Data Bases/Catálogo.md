---
tags:
  - Notes
  - RDB
---
>Conjunto de [[Varrels]] del sistema que contienen descriptores de los diversos elementos que son de interés para el sistema
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p79

# Descriptores
>Información detallada respecto de los distintos objetos que son de interés para el propio sistema
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p70

## Ejemplos
- Varrels 
- indices
- Usuarios
- Restricciones de integridad
- Restricciones de seguridad

# Ejemplo

A continuación se muestran los descriptores de la `TABLA` y `COLUMNA`, los metadatos que registra son de `DEPTO` y `EMP` 

| NOMTABLA | CONTCOL | CONTFILA | ..... |
| -------- | ------- | -------- | ----- |
| DEPTO    | 3       | 3        | ..... |
| EMP      | 4       | 4        | ..... |

| NOMTABLA | CONTCOL     | ..... |
| -------- | ----------- | ----- |
| DEPTO    | DEPTO#      | ..... |
| DEPTO    | NOMDEPTO    | ..... |
| DEPTO    | PRESUPUESTO |       |
| EMP      | EMP#        |       |
| EMP      | NOMEMP      |       |
| EMP      | DEPTO#      |       |
| EMP      | SALARIO     |       |
