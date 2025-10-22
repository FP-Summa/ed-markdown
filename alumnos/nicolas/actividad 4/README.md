# **modelo:Usuarios(registro login)**
**Objetivo**: permitir **registro** y **login** con validaciones básicas.
 
## **Requisitos (viñetas)**
Registrar `email` y `password`.
 
Validar formato de **email** y evitar **duplicados**.
 
## **Flujo (numerado con párrafos dentro de ítems)**
 
1.Registro de usuario.
 
Recoger **email** y **password**, validar formato y guardar `password_hash` (no se guarda la contraseña en claro).
 
2.Login.
 
Comprobar credenciales y devolver **token** si son válidas.
 
## **Checklist (GFM)**
+ [ ] Definir esquema en BD
+ [ ] `POST /api/v1/users` (registro)
+ [ ] `POST /api/v1/login` (login)
 
## **Esquema de BD (tabla GFM)**
| **campo**     | **tipo**   | **requerido** |
|:-----------|:------:|----------:|
| id    | entero |       si |
|   email   | **texto**|       si |
| password_hash|    `texto`|   si |
|created_at | fecha | no |
## **Definiciones (opcional)**
Hash : Función **unidireccional** para almacenar contraseñas de forma segura.
 
Token : Credencial **temporal** para acceder a la API tras el login.