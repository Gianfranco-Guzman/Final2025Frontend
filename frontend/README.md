# Frontend E-commerce (React + TypeScript + Vite)

Este repositorio contiene el frontend de un e-commerce académico/profesional, separado del backend para permitir despliegue y mantenimiento independientes.

## Contexto del proyecto

En este proyecto implementé una aplicación web con enfoque en:

- navegación de tienda (catálogo, categorías y detalle de producto),
- flujo de compra básico,
- vistas administrativas para gestión de datos,
- integración con API REST desplegada externamente.

La aplicación está desplegada en Vercel y consume un backend desplegado en Render.

## Stack utilizado

- **React 18**
- **TypeScript**
- **Vite**
- **React Router DOM**

## Estructura principal

```text
frontend/
├─ src/
│  ├─ api/          # Cliente y tipos para integración con API
│  ├─ components/   # Componentes reutilizables
│  ├─ data/         # Datos y assets de apoyo
│  ├─ layouts/      # Layouts de tienda y admin
│  ├─ pages/        # Pantallas de tienda y panel admin
│  ├─ services/     # Servicios HTTP por recurso
│  ├─ store/        # Estado local (carrito/cuenta/checkout)
│  ├─ styles/       # Estilos globales
│  └─ utils/        # Utilidades
├─ index.html
├─ package.json
└─ vite.config.ts
```

## Variables de entorno

Crear el archivo `.env` dentro de `frontend/`:

```env
VITE_API_URL=https://<tu-backend-render>
```

Para desarrollo local también puede usarse:

```env
VITE_API_URL=http://localhost:8000
```

## Ejecución local

```bash
cd frontend
npm install
npm run dev
```

## Build de producción

```bash
cd frontend
npm run build
npm run preview
```

## Integración con backend

La app consume endpoints REST para categorías, productos, clientes, direcciones, facturas, pedidos, detalle de pedidos y reseñas.

Si necesitás referencia de orden de carga de datos en entorno local, está documentado en `BACKEND_GUIDE.md`.

## Estado actual

- Frontend separado del backend original.
- Deploy activo en Vercel.
- Integración activa con backend y base de datos en Render.

## Notas

Este README describe cómo está implementado actualmente el frontend y cómo ejecutarlo o desplegarlo sin depender de documentación del monorepo original.
