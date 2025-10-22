# Módulo: Usuarios (registro y login)
**Objetivo:** permitir **registro** y **login** con validaciones básicas.
___
## Requisitos (viñetas)
- Registrar <code>email</code> y <code>password</code>.
- Validar formato de **email** y evitar **duplicados**.
## Flujo (numerado con párrafos dentro de ítems)
1. Registro de usuario.
Recoger **email** y **password**, validar formato y guardar <code>password_hash</code> (no se guarda la contraseña en claro).
2. Login.
Comprobar credenciales y devolver **token** si son válidas.
## Checklist (GFM)
- [ ] Definir esquema en BD
- [ ] <code>POST /api/v1/users</code> (registro)
- [ ] <code>POST /api/v1/login</code> (login)
## Esquema de BD (tabla GFM)
|**Campo**    |**Tipo**          |**Requerido**|
|:------------|:----------------:|------------:|
|id           |entero            |sí           |
|email        |**texto**         |sí           |
|password_hash|<code>texto</code>|sí           |
|created_at   |fecha             |no           |
## Definiciones (opcional)
Hash : Función **unidireccional** para almacenar contraseñas de forma segura.\
Token : Credencial **temporal** para acceder a la API tras el login.