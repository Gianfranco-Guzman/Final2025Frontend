# Guía breve de integración con Backend

Este documento resume el flujo de prueba recomendado para cargar datos en la API sin romper dependencias relacionales.

## Servicios y acceso

Backend y base de datos están desplegados en Render. Para validaciones manuales de endpoints, se puede usar Swagger en la URL `/docs` del backend.

## Orden recomendado para crear datos

Para evitar errores por claves foráneas, usar este orden:

1. Categorías
2. Productos
3. Clientes
4. Direcciones
5. Facturas
6. Pedidos
7. Detalles de pedido
8. Reseñas

## Endpoint de verificación

Antes de probar operaciones CRUD, validar estado del servicio en:

- `GET /health_check/`

## Notas operativas

- El frontend toma la URL base desde `VITE_API_URL`.
- Si se cambia el entorno (local, staging o producción), actualizar la variable de entorno correspondiente.
