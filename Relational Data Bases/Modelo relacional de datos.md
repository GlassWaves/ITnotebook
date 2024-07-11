---
tags:
  - Notes
  - RDB
---
> Este modelo se ocupa sólo de los aspectos lógicos de los datos
> [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p79

| Aspecto      | Descripción                                                            |
| ------------ | ---------------------------------------------------------------------- |
| Estructura   | Tiene que ver con las relaciones como tales                            |
| Integridad   | Tiene que ver (entre otras cosas) con las claves primeria y externa    |
| Manipulación | Tiene que ver con los operadores (restringir, proyectar, juntar, etc.) |
# Componentes
- Un [[Conjunto abierto]] de [[Escalar|tipos escalares]] (incluyendo en particular el `tipo lógico` o valor `verdadero`)
	- Este punto se refiere al conjunto de tipos de datos que están contenidos en una [[Relación]]
- Un generador de [[Relación#Tipos y relaciones|tipos de relación]] y una interpretación de dichos tipos
	- Este punto se refiere a que existe un mecanismo que define la estructura de las relaciones (sus atributos)
- Herramientas para definir [[Varrels|variables de relación]] de dichos [[Relación#Tipos y relaciones|tipos de relación]] generados
	- Este punto se refiere al almacenamiento y manipulación de las relaciones
- Una operación [[Relación#Tipos y relaciones|asignación relacional]] para asignar valores de relación a las [[Varrels|variables de relación]] mencionadas
	- Este punto se refiere a que puedes cambiar los valores de la relación
- Un conjunto abierto de [[Sistema relacional#Operador relacional|operadores relacionales]] genéricos para derivar valores de relación de oros valores de relación
	- Este punto se refiere a que puedes anidar operadores relacionales gracias a la [[Sistema relacional#Propiedad de cierre|propiedad de cierre]]

Esta información fue obtenida de [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p62