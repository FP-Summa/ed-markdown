
# Incidencia: login devuelve 401
El login contra la API devuelve __401 Unauthorized__ pese a usar credenciales válidas.

La conectividad con el servidor es correcta, así que revisamos la petición.

---
## Síntomas
- El usuario introduce credenciales válidas; la API responde __401__. \
- Conectividad OK (no es un problema de red).

>## Acciones
Endpoint: `POST /api/v1/login`

Cabeceras a revisar: `Content-Type: application/json`

```
curl -i -X POST https://api.ejemplo.com/api/v1/login \
  -H "Content-Type: application/json" \
  -d '{"email":"demo@ejemplo.com","password":"demo123"}'
```

>“No puedo iniciar sesión desde esta mañana.” — cliente

## Conclusión

La causa más probable es un __header ausente__ o un __campo mal escrito__ (p. ej., `email` vs. `username`).
Próxima acción: corregir la request y repetir la prueba (esperamos __200 OK__ y token de sesión).
__Estado:__ incidencia ~~~abierta~~ → __en revisión.__