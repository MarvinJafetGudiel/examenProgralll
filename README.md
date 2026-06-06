# ProductosApi

API REST desarrollada en ASP.NET Core Web API para la gestión de productos utilizando Entity Framework Core, MySQL y Docker.

## Características

* Crear productos
* Obtener todos los productos
* Obtener producto por ID
* Actualizar productos
* Eliminar productos
* Documentación automática con Swagger
* Persistencia de datos en MySQL
* Base de datos ejecutándose en Docker
* Autenticación mediante JWT
* Entity Framework Core con migraciones

## Tecnologías Utilizadas

* ASP.NET Core Web API
* Entity Framework Core
* MySQL 8
* Docker Desktop
* Swagger / OpenAPI
* JWT Authentication
* C#

## Ejecutar la API

```bash
dotnet run
```

La aplicación se ejecutará en:

```text
http://localhost:5215
```

## Swagger

Acceder a la documentación:

```text
http://localhost:5215/swagger
```


`

## Ejemplo de Producto

```json
{
  "nombre": "Laptop Lenovo",
  "descripcion": "Laptop para oficina y estudio",
  "precio": 4500,
  "stock": 10
}
```

## Endpoints Disponibles

| Método | Endpoint            |
| ------ | ------------------- |
| POST   | /api/Auth/login     |
| POST   | /api/Productos      |
| GET    | /api/Productos      |
| GET    | /api/Productos/{id} |
| PUT    | /api/Productos/{id} |
| DELETE | /api/Productos/{id} |

## Evidencias del Proyecto

Para la entrega se incluyen evidencias de:

* Documentación Swagger.
* Contenedor MySQL ejecutándose en Docker Desktop.
* Pruebas CRUD realizadas desde Swagger.
* Uso de autenticación JWT.
* Migraciones aplicadas correctamente en MySQL.

## Autor

Marvin Jafet Gudiel López

Tercera Serie de Programación
