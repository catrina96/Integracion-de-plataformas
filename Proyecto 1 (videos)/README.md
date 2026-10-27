
---

### Proyecto-1 README de servicios `/Proyecto-1/README.md`

```markdown
# Servicios Java propuestos (Proyecto-1)

## Resumen
Lista inicial de endpoints REST para gestionar posibles clientes y oportunidades comerciales. Implementar al menos un servicio de prueba que responda con un mensaje JSON.

## Endpoints propuestos

### PosibleClienteService
- **POST /api/posibles-clientes**  
  - **Propósito:** Registrar un posible cliente.  
  - **Entrada (JSON):** `nombre`, `mascota`, `canal`, `producto_interes`, `mensaje`, `fecha_contacto`  
  - **Salida (JSON):** `id`, `mensaje` (confirmación)

- **GET /api/posibles-clientes/{id}**  
  - **Propósito:** Obtener datos de un posible cliente.  
  - **Salida (JSON):** objeto con los campos del registro

### OportunidadService
- **POST /api/oportunidades**  
  - **Propósito:** Crear una oportunidad comercial.  
  - **Entrada (JSON):** `tipo`, `fecha_objetivo`, `clientes_objetivo`, `accion_sugerida`  
  - **Salida (JSON):** `id`, `mensaje` (confirmación)

- **GET /api/oportunidades/{id}**  
  - **Propósito:** Consultar una oportunidad.  
  - **Salida (JSON):** objeto con los campos de la oportunidad

## Servicio de prueba mínimo (requisito de la entrega)
Implementar un endpoint simple:
- **GET /api/ping**  
  - **Respuesta:** `{ "message": "Servicio de prueba ejecutado correctamente" }`

## Notas técnicas
- Se propone usar Spring Boot para el prototipo o algun otro lenguaje.  
- Documentar en el código los contratos de entrada/salida (ej. OpenAPI/Swagger si es posible).  
- Registrar ejemplos de payload en la documentación del repositorio.
