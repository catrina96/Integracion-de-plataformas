# Posibles Clientes

## Definición
Un **posible cliente** es una persona que ha mostrado interés en los productos de Peluditos Pet Chile pero que aún no ha concretado una compra.

## Datos básicos a registrar
- **ID** (generado por el sistema)  
- **Nombre del dueño**  
- **Nombre de la mascota** (opcional)  
- **Canal de origen** (Instagram, WhatsApp, Facebook, TikTok, otro)  
- **Producto de interés**  
- **Mensaje o comentario** (texto libre)  
- **Fecha de contacto**  
- **Estado**: En seguimiento; Convertido en cliente; No concretó compra; Recontactar en fecha X

## Ejemplo de registro (JSON)
```json
{
  "id": "pc-001",
  "nombre": "Carla Pérez",
  "mascota": "Firulais",
  "canal": "Instagram",
  "producto_interes": "Torta cumpleaños 20cm",
  "mensaje": "¿Cuánto cuesta y cuándo la pueden entregar?",
  "fecha_contacto": "2026-10-20",
  "estado": "En seguimiento"
}
