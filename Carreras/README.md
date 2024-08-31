# Carreras

### Carreras **(ED)**

- carrera_id **(PK)**
- nombre 
- tipo_carrera **(FK)**
- fecha
- tiempo
- mejor_tiempo
- altitud
- lugar
- pais **(FK)**
- foto

### tipos_carreras **(EC)**

- tipo_carrera_id **(PK)**
- descripcion 
- distancia **(UQ)**

### paises **(EC)**

- pais_id **(PK)**
- nombre

---
---
ED = Entidad Dato <br>
EC = Entidad Catalogo <br>
EP = Entidad Pivote <br>

PK = Llave Primaria <br>
FK = LLave Foranea <br>
UQ = Campo Unico
---
---

## Relaciones 
---

1. Una **carrera** _pertenece_ a un **tipo de  carrera** (_1 a M_)
1. Una **carrera** se _corre_ en un **pais** (_1 a M_)

---

## Modelo Entidad-Relación del sistema

---

[![entidad relacion](https://i.postimg.cc/zXnQtSHK/entidad-relacion.png)](https://postimg.cc/6ypzTZ0p)


---

## Modelo Relacional de la Base de Datos

---

[![modelo-relacional.png](https://i.postimg.cc/Fs7R0zYM/modelo-relacional.png)](https://postimg.cc/MvJqSWb5)

## Reglas de Negocio

### Carreras

1. Crear el registro de una carrera
1. Leer el registro de una(s) carrera(s) dada una condición en particular
1. Leer todos los registros de la entidad carreras
1. Actualizar los datos de una carrera dada una condición en particular
1. Elimimar los datos de una carrera dada una condición en partucular 

### tipos_carreras

1. Todos los valores del atributo distancia, deberán estar expresados en _km_ y no se podrán repetir
1. Crear el registro de un tipo de carrera
1. Leer el registro de un(os) tipo(s) de carrera(s) dada una condición en particular
1. Leer todos los registros de la entidad tipos carreras
1. Actualizar los datos de un tipo de carrera dada una condición en particular
1. Elimimar los datos de un tipo de carrera dada una condición en partucular 

### paises

1. Crear el registro de un pais
1. Leer el registro de un(os) pais(es) dada una condición en particular
1. Leer todos los registros de la entidad paises
1. Actualizar los datos de un pais dada una condición en particular
1. Elimimar los datos de un pais dada una condición en partucular 