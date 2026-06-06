# Analisis del Proyecto ProductosApi

## a. Decisiones tomadas sobre estructuras de datos y entidades

Para este proyecto decidí crear una entidad llamada `Producto`, ya que el objetivo de la API era almacenar información de productos. Los campos seleccionados fueron:

* Id: identificador único del producto.
* Nombre: nombre del producto.
* Descripcion: descripción o detalle del producto.
* Precio: valor monetario del producto.
* Stock: cantidad disponible en inventario.

Utilicé una tabla llamada `Productos` en MySQL y Entity Framework Core para realizar las operaciones CRUD de manera más sencilla. También utilicé un `DbContext` para gestionar la comunicación entre la aplicación y la base de datos.

La API fue desarrollada siguiendo una arquitectura sencilla basada en controladores

## b. Secuencia de comandos utilizados para generar migraciones

Primero instalé las dependencias necesarias para trabajar con Entity Framework Core y MySQL.

```bash
dotnet add package Microsoft.EntityFrameworkCore.Design --version 9.0.0
dotnet add package Pomelo.EntityFrameworkCore.MySql --version 9.0.0
```

Posteriormente instalé la herramienta de Entity Framework:

```bash
dotnet tool install --global dotnet-ef
```

Luego generé la migración inicial:

```bash
dotnet ef migrations add InitialCreate
```

Finalmente apliqué la migración a la base de datos:

```bash
dotnet ef database update
```

## c. Comandos de Docker utilizados

Para ejecutar MySQL en un contenedor Docker utilicé los siguientes comandos:

```bash
docker compose up -d
```

Para verificar que el contenedor estuviera funcionando:

```bash
docker ps
```

Y para detener el contenedor cuando fuera necesario:

```bash
docker compose down
```

## d. Partes desarrolladas manualmente y con apoyo de IA

La mayor parte de la configuración del entorno fue realizada manualmente por mí. Esto incluyó:

* Creación del proyecto ASP.NET Web API.
* Configuración de Docker Desktop.
* Ejecución de comandos en la terminal.
* Configuración de MySQL en Docker.
* Creación y aplicación de migraciones.
* Pruebas de los endpoints mediante Swagger.
* Verificación de los datos almacenados en MySQL.

Utilicé apoyo de inteligencia artificial principalmente para resolver errores de configuración que surgieron durante el desarrollo, especialmente relacionados con las versiones de Entity Framework, la configuración de JWT para autenticación y algunos ajustes de Swagger.

También utilicé la IA como apoyo para comprender mejor ciertos conceptos y para documentar de forma más clara las decisiones tomadas en el proyecto, pero la implementación, pruebas y ejecución final del sistema fueron realizadas por mí.
