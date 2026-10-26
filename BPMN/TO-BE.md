# Proceso TO-BE: Peluditos Pet Chile

## Objetivo
Automatizar el registro y seguimiento de **posibles clientes** y generar oportunidades comerciales en fechas relevantes, manteniendo intervención humana en la venta.

## Participantes
- **Cliente**  
- **Sistema (BPMN/Flowable)**  
- **Emprendedora**

## Flujo propuesto (alto nivel)
1. **Recepción de consulta** (canales: Instagram, WhatsApp, Facebook, TikTok).  
2. **Registro automático del posible cliente** en el sistema con datos básicos (nombre, mascota, canal, producto de interés, fecha).  
3. **Notificación a la emprendedora** para seguimiento (mensaje o correo).  
4. **Actividad de seguimiento**: la emprendedora contacta al posible cliente y registra resultado:
   - **Convertido en cliente** → registrar venta; solicitar datos adicionales (dirección, fecha de entrega); crear registro de cliente.
   - **No concretó compra** → marcar como descartado o programar recontacto.
5. **Gestión de fechas relevantes**: el sistema mantiene calendario de fechas (cumpleaños, campañas) y genera **oportunidades comerciales** para clientes existentes o posibles clientes con fecha próxima.
6. **External worker** invoca servicios (por ejemplo, envío de notificaciones o creación de recordatorios) cuando el proceso lo requiere.
7. **Cierre**: registrar resultado final y métricas (tasa de conversión, número de oportunidades generadas).

## Elementos BPMN posibles
- **Eventos de inicio**: llegada de consulta; evento programado (fecha relevante).  
- **Tareas de servicio**: registrar posible cliente (invoca LeadService).  
- **Tareas de usuario**: seguimiento por la emprendedora (formulario).  
- **Tareas externas**: external worker para invocar servicios de notificación.  
- **Decisiones**: ¿se concretó la compra? ¿es cliente recurrente?  
- **Eventos intermedios**: temporizadores para campañas y recordatorios.

## Beneficios esperados
- Registro centralizado de posibles clientes.  
- Seguimiento sistemático que aumenta la conversión.  
- No perder oportunidades comerciales por fechas relevantes.  
- Evidencia y métricas para la emprendedora.
