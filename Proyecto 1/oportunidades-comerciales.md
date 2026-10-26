
```markdown
# Oportunidades Comerciales

## Definición
Una **oportunidad comercial** es un evento o fecha relevante que justifica contactar a un cliente o posible cliente para fomentar una compra.

## Tipos de oportunidades
- **Cumpleaños de la mascota**  
- **Navidad**  
- **Halloween**  
- **Día del Perro / Día del Gato**  
- **Aniversario del emprendimiento**  
- **Lanzamiento de nuevos productos**  
- **Campañas estacionales**

## Datos a registrar
- **ID oportunidad**  
- **Tipo** (cumpleaños, campaña, lanzamiento)  
- **Fecha objetivo**  
- **Clientes objetivo** (lista de IDs)  
- **Acción sugerida** (ej. enviar oferta, recordatorio)  
- **Estado** (Pendiente, Enviado, Completado)

## Ejemplo de oportunidad (JSON)
```json
{
  "id": "op-001",
  "tipo": "Cumpleaños",
  "fecha_objetivo": "2026-11-15",
  "clientes_objetivo": ["c-001", "c-023"],
  "accion_sugerida": "Enviar oferta 10% descuento para torta de cumpleaños",
  "estado": "Pendiente"
}
