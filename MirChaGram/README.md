# MirChaGram

## Estado de Entidades

### posts **(ED)**

- post_id **(PK)**
- post_date
- plot
- photo
- user **(FK)**

### user

- user_id **(PK)**
- user_date
- user_name
- email **(UQ)**
- password
- phone **(UQ)**
- bio
- web
- avatar
- birthdate
- genre
- country **(FK)**

### comments **(ED | EP)**

- comment_id **(PK)**
- comment_date
- comment
- post_id **(FK)**
- user_id **(FK)**

### hearts **(ED | EP)**

- heart_id **(PK)**
- heart_date
- post_id **(FK)**
- user_id **(FK)**

### follows

- follow_id **(PK)**
- follow_date
- follow_user **(FK)**
- following_user **(FK)**

### countries **(EC)**

- country_id **(PK)**
- country_name


## Relaciones

1. Los **users** publican **posts** (1 - M)
1. Los **users** escriben **comments** (1 - M)
1. Los **posts** tienen **comments** (1 - M)
1. Los **users** otorgan **hearts** (1 - 1)
1. Los **posts** tienen **hearts** (1 - M)
1. Los **users** tienen **follows** (1 - M)
1. Los **users** siguen **follows** (1 - M)
1. Los **users** tienen un **countries** (1 - M)

<!-- ENUM('Hombre', 'Mujer', 'No Binario') -->
<!-- Listado: tipo de dato para evitar crear un catalogo (menos de 5 valores) -->

## Diagramas

### Modelo Relacional de la BD

![Modelo Relacional](ModeloRelacional.png)

## Reglas de Negocio

### posts

1. Crear un posts
1. Leer todos los posts
1. Leer un post en particular
1. Leer los posts de un user
1. Actualizar el plot de un post
1. Eliminar un post

### user

1. Crear un user
1. Leer todos los users
1. Leer un user
1. Validar un user
1. Actualizar datos del user
1. Actualizar password de user
1. Eliminar user

### comments

1. Crear un comment en un post
1. Leer todos los comments de un post
1. Leer un comment de un post
1. Contar el número de commemts de un post
1. Eliminar comment en un post

### hearts

1. Crear hearts de user en un post
1. Contar el número de hearts de un post
1. Eliminar heart de user en un post

### follows 

1. Crear follow de un user
1. Contar el número de followers de un user
1. Contar el número de followings de un user
1. Eliminar follow de un user

### countries

1. Crear country
1. Leer todos los countries
1. Leer un country
1. Actualizar un country
1. Eliminar country