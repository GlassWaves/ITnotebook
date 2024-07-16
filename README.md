# ¡Hola!
Este cuaderno registra temas de TI que investigo en mis ratos libres :D

Esta construido con la tecnología de [Obsidian](https://obsidian.md/), la cual utiliza el lenguaje de marcado [markdown](https://es.wikipedia.org/wiki/Markdown), 
sin embargo tiene algunos ligeros cambios en la sintaxis que impiden leer al 100% el documento en markdown simple, por lo que es recomendable que al descargar 
este `vault`, lo leas mediante el editor de `Obsidian` con los correspondientes `plugins` habilitados.

# Tabla de contenido
- <a name ="Estructura"></a>#Estructura
- [Tipos de notas](Estructura)
  - [Notes](Notes)
  - [Sources](Sources)
- [Directorios especiales](Directorios especiales)
  - [Annexes](Annexes)
  - [Templates](Templates)

# Estructura
El cuaderno esta estructurado mediante notas atomicas agrupadas bajo temas genericos (directorio/tag), por ejemplo : 
La nota *Conjunto abierto* pertenece al tema de *Teoria de conjuntos* pero su tema generico es *Matematicas*. 
Esto es para simplificar la jerarquia de los directorios y de las notas en sí.

# Tipos de notas
## Notes
Notas simples cuyo contenido sigue el `principio de atomicidad` el cual a grandes rasgos trata sobre reducir al minimo
posible las tematicas que se desarrollan en una sola nota.

### Propiedades
- `tags` : Son los tags que identifican la tematica de la nota
  - Por default tienen los tags #Notes, #TemaGenerico, sin embargo
    se les puede complementar con algun tag extra
- *`aliases` : A veces las notas tienen aliases (se debe de agregar)
  - Ejemplo; el titulo de la nota es World Wide Web, pero su alias es WWW

## Sources
Estas notas registran las fuentes que son utilizadas en las `Notes`. Las notas deben ser tituladas con la siguiente
estructura :

"src." + "Titulo original de la fuente sin caracteres especiales"

### Propiedades
- `tags` : Son los tags que identifican la tematica de la fuente
  - Por default tienen los tags #Sources, #TemaGenerico, sin embargo
    se les puede complementar con algun tag extra
- `reference` : Archivo, link web, ISBN-13 o DOI de la fuente consultada
- `aliases` : Alias de las fuente
  - Por default se debe de incluir uno al menos, para evitar usar sus iniciales "src."
 
# Directorios especiales
## Annexes
En este directorios se almacenan imagenes, pdf's, hojas de calculo o cualquier archivo (no markdown) que 
se anexen en las notas. El nombre del archivo debe seguir la siguiente estructura :

"Tipo de archivo." + "Nombre de la primera nota en la que es anexado" + "Numero"

`Tipo de archivo`
- img : Imagenes
- pdf : PDF
- exl : Hojas de calculo
- cod : Codigo

`Numero`
- Si una nota tiene mas de un archivo anexado se deben de enumerar los nombre de los anexos

## Templates
Este directorio almacena los templates de las notas. El nombre del template debe seguir 
la siguiente estructura :

"tpl." + "Nombre generico del template"


