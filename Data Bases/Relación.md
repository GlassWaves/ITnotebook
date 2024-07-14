---
tags:
  - Notes
  - RDB
  - DB
---
>Conjunto de $n$ [[#Dominio|tipos o dominios]] $Ti(i=1,2...n)$ que no son necesariamente todos distintos, $r$ es una `relación` sobre esos [[#Tipos y relaciones|tipos]] si consta de dos partes : un encabezado y un cuerpo
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p123

# Encabezado
> Conjunto de $n$ `atributos` de la forma $Ai:Ti$, donde los $Ai$ (que deben ser todos distintos) son los `nombres de atributo` de $r$ y los $Ti$; es decir, el `valor de atributo` para el atributo $Ai$ de la tupla $t(i=1,2,...,n)$
> [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p123

El valor de $n$ es el `grado`, $n$ es cualquier entero no negativo

> [!NOTE] Atributos del tipo relación
> Las relaciones pueden tener atributos cuyos valores sean a su vez relaciones

## Definición informal
>Conjunto de parejas `nombre_de_columna : nombre_de_tipo`
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p79

## Ejemplo de encabezado
``` 
{ idProveedor : idProveedor
proveedor : nombre
status : status
ciudad : ciudad }
```
# Cuerpo
>Conjunto de $m$ tuplas $t$, en donde $t$ es a su vez un conjunto de componentes de la forma $Ai:vi$ en la cual $vi$ es un valor de tipo $Ti$, es decir, el `valor de atributo` $Ai$ de la tupla $t(i=1,2,...,n)$
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p123

El valor de $m$ es la `cardinalidad`


> [!NOTE] Las tuplas no son variables
> Cuando un tupla es "actualizada", nos referimos a que el valor de la tupla $t$ es remplazada por otra tupla $t'$ y no a la asignación de valores a la vartupla $t$ (la cual no existe). 
> [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p133

## Definición informal
>Conjunto de filas que se apegan al encabezado
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p79
## Ejemplo de tupla
```
{ idProveedor : idProveedor('V1'),
proveedor : nombre('Smith'),
status : 20
ciudad : 'Londres' }
```
# Estructura
![[img.Relacion.png]]
Diagrama recuperado de [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p111
## Términos y equivalencias

| **Termino relacional formal** | **Equivalente informal**    |
| ----------------------------- | --------------------------- |
| Relación                      | Tabla                       |
| Tupla                         | Fila o registro             |
| Cardinalidad                  | Número de filas             |
| Atributo                      | Columna o campo             |
| Grado                         | Número de columnas          |
| Clave primaria                | Identificador único         |
| Dominio                       | Conjunto de valores válidos |
Tabla recuperada de [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p112

# Dominio
Es un [[Tipo de dato]] definido por el sistema (`INTEGER`, `CHARACTER`, etc.) o por el usuario (`peso`, `cantidad`, etc.)
Basado en [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p112

## Dominio y clase objeto
>la clase objeto, es un tipo de datos -definido por el sistema o por el usuario- de una complejidad interna arbitraria, cuyos valores son manipulables exclusivamente por medio de los operadores definidos para el tipo en cuestión (y cuya representación interna esta, por lo tanto, oculta para el usuario)... En otras palabras, ¡los dominios y las [[Clase objeto|clases objeto]] son lo mismo!
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p123

# Propiedades
- No existen tuplas duplicadas
- Las tuplas están en desorden, de arriba hacia abajo
- Los atributos están en desorden de izquierda a derecha
- Cada tupla contiene exactamente un valor para cada atributo
# Tipos y relaciones
> - Los `tipos` son (conjuntos de) cosas de las que podemos hablar
> - Las `relaciones` son (conjuntos de) cosas que decimos acerca de las cosas de las que podemos hablar
> [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p66

>Los `tipos` son a las `relaciones` lo que los `sustantivos` son a las `oraciones`.
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p66

>Los `tipos` y las `relaciones` son necesarios y suficientes para representar cualquier dato que queramos (esto es, al nivel lógico)
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p79

# Encabezado y cuerpo
> Dada una relación `r` , el encabezado de `r` denota un cierto `predicado` o `función valuada` como `verdadera`
> [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p66

>Cada fila en el cuerpo de `r` denota una cierta `proposición verdadera`, obtenida del `predicado` por medio de la sustitución de ciertos valores de argumento
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p66
## Interpretación semántica
Por ejemplo de la relación `Empleado`:

| idEmpleado | nombre   | idDepartamento | salario |
| ---------- | -------- | -------------- | ------- |
| 1          | Lopez    | 1              | 40000   |
| 2          | Cheng    | 2              | 42000   |
| 3          | Smith    | 4              | 30000   |
| 4          | Vladimir | 4              | 15000   |
### Predicado
El empleado `idEmpleado` se llama `nombre`, trabaja en el departamento `idDepartamento` y gana un salario de `salario`

Parámetros :
- idEmpleado
- nombre
- idDepartamento
- salario

### Proposición verdadera
El empleado `1` se llama `Lopez`, trabaja en el departamento `idDepartamento` y gana un salario de `40000`

# Tabla y relación
>Una `relación` es lo que la definición dice que es (es decir, una clase de objeto mas bien abstracto) y una `tabla` es una imagen concreta (generalmente sobre papel) de dicho objeto abstracto
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p125

