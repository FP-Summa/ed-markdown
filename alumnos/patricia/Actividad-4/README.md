# Módulo: Usuarios (registro y login)
__Objetivo:__ permitir __registro__ y __login__ con validaciones básicas.

## Requisitos (viñetas)
- Registrar `email` y `password`.

- Validar formato de __email__ y evitar __duplicados__.

## Flujo (numerado con párrafos dentro de ítems)
1. Registro de usuario.

    Recoger __email__ y __password__, validar formato y guardar `password_hash` (no se guarda la contraseña en claro).

2. Login.

    Comprobar credenciales y devolver __token__ si son válidas.

## Checklist (GFM)
- [ ] Definir esquema en BD
- [ ] `POST /api/v1/users` (registro)
- [ ] `POST /api/v1/login` (login)
## Esquema de BD (tabla GFM)
|Campo  |	Tipo |	Requerido |
|:-----:|:------:|:----------:|
|id	|entero	|sí |
|email	| __texto__	| sí |
|password_hash	| `texto` |	sí |
|created_at	|fecha |	no |


## Definiciones (opcional)
Hash : Función __unidireccional__ para almacenar contraseñas de forma segura.

Token : Credencial __temporal__ para acceder a la API tras el login.