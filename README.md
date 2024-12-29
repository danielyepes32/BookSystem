# Sistema de Reservas - Proyecto Angular y .NET 8

Este proyecto consiste en una aplicación web para gestionar reservas en diferentes espacios. La aplicación está dividida en dos partes: un **backend** desarrollado en **.NET 8** que maneja la lógica de negocio y las interacciones con la base de datos, y un **frontend** desarrollado con **Angular** que proporciona la interfaz de usuario para realizar las reservas.

## Propósito del Proyecto

El sistema de reservas permite a los usuarios seleccionar un espacio, indicar las fechas de inicio y fin de la reserva, y finalmente confirmar la reserva. El sistema también valida que las fechas sean correctas y que no haya conflictos con otras reservas.

### Características:
- Validación de fecha de inicio para garantizar que no sea menor a la hora actual más 30 minutos.
- Verificación de que la fecha de inicio sea anterior a la fecha de fin.
- Interfaz de usuario amigable para crear y gestionar las reservas.
- Backend que maneja la lógica de creación y almacenamiento de reservas.

---

## Backend - .NET 8

El backend está desarrollado utilizando **.NET 8**, un framework moderno para construir aplicaciones escalables y de alto rendimiento. El backend maneja las operaciones relacionadas con la base de datos, la validación de datos y la comunicación con el frontend.

### Propósitos del Backend:

1. **API RESTful**: El backend ofrece una API RESTful para crear, eliminar y obtener las reservas.
2. **Validación**: Valida la información recibida del frontend antes de almacenarla en la base de datos.
3. **Base de Datos**: Utiliza una base de datos relacional (SQL Server, PostgreSQL, MySQL, etc.) para almacenar la información de las reservas, incluyendo el espacio, la fecha de inicio, y la fecha de fin.
4. **Autenticación y Seguridad**: (Opcional) Implementa seguridad básica y autenticación de usuarios con JWT (JSON Web Tokens).

### Endpoints:
- `POST /api/reservations`: Crear una nueva reserva.
- `GET /api/reservations`: Obtener todas las reservas.
- `DELETE /api/reservations/{id}`: Eliminar una reserva.

### Dependencias:
- `Microsoft.AspNetCore.Mvc`: Para crear los controladores y endpoints de la API.
- `Microsoft.EntityFrameworkCore`: Para interactuar con la base de datos mediante Entity Framework.
- `Microsoft.AspNetCore.Authentication.JwtBearer`: (Opcional) Para autenticar las solicitudes con tokens JWT.

### Instrucciones para ejecutar el backend:

1. Clona este repositorio.
2. Navega al directorio del backend y ejecuta los siguientes comandos:
   ```bash
   dotnet restore
   dotnet build
   dotnet run
