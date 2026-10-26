# External Worker (concepto y diseño)

## Qué es
Un **external worker** es un componente que obtiene tareas externas desde Flowable y las ejecuta fuera del motor BPMN, invocando servicios externos (REST/SOAP) y devolviendo resultados para que el proceso continúe.

## Flujo de interacción (conceptual)
1. **Flowable** crea una tarea externa (external task) cuando el proceso alcanza una actividad de servicio externa.  
2. **External worker** consulta el broker de tareas de Flowable (poll) y obtiene la tarea.  
3. Worker invoca el **PosibleClienteService** o **OportunidadService** según la tarea.  
4. Worker procesa la respuesta y completa la tarea en Flowable, aportando variables de proceso si corresponde.

## Ejemplo de uso
- Tarea: `registrar_posible_cliente`  
  - Worker recibe payload con datos del contacto.  
  - Worker hace `POST /api/posibles-clientes`.  
  - Si la respuesta es exitosa, worker completa la tarea y setea variable `registro_ok=true`.

## Requisitos y consideraciones
- Registrar logs y/o evidencias de invocación.  
- Documentar el contrato entre la tarea externa y el servicio (campos esperados).

## Archivo de evidencia
Cuando Flowable esté disponible, incluir:
- Código del worker (Java/Node/Python).  
