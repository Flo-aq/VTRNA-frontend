# VTRNA: marketplace de moda vintage (frontend)

Frontend de **VTRNA**, una plataforma para comprar y vender ropa vintage con un feed de descubrimiento tipo swipe, ofertas entre usuarios y perfiles de vendedor. Proyecto grupal del curso IIC3143 (Desarrollo de Software, PUC Chile, 2026-1).

## Qué hace

- Registro e inicio de sesión con Auth0, y onboarding por pasos (preferencias de estilo, talla, marcas y metro más cercano)
- Feed de publicaciones con navegación, filtros por tags, likes y guardados
- Ofertas sobre publicaciones, con seguimiento del estado de cada negociación
- Vista de vendedor para crear y editar publicaciones, con carga de múltiples fotos
- Perfiles de usuario con calificación del vendedor, y notificaciones

## Stack

- Next.js 16 (App Router) y React 19, TypeScript
- Tailwind CSS v4, shadcn/ui, Radix UI, Framer Motion
- TanStack React Query, React Hook Form
- Auth0 (`@auth0/nextjs-auth0`)
- MSW (Mock Service Worker) para desarrollar sin backend
- Tests: Vitest/Playwright (unitarios, integración, contrato y e2e). CI y despliegue con GitHub Actions

## Ejecutar localmente

```bash
npm install
npm run dev        # http://localhost:3000
```

La configuración de Auth0 está en [`docs/auth0.md`](docs/auth0.md). Con `NEXT_PUBLIC_ENABLE_MSW=true` la app usa datos simulados y no requiere backend.

## Estructura

```
src/app/            Rutas: feed, ofertas, perfil, notificaciones, onboarding, publicaciones
src/components/     UI: feed, ofertas, perfil, onboarding, vendedor, componentes comunes
src/hooks/          Hooks de datos (feed, interacciones, ofertas, tags, ratings)
src/lib/api/        Cliente de la API
src/lib/msw/        Mocks para desarrollo sin backend
tests/              Tests de contrato, integración y e2e
docs/               Guías de componentes, feed, testing y Auth0
```

## Mi rol

Creé la marca (nombre, logo, paleta de colores y estilo gráfico), diseñé la app, los mockups y los flujos de usuario, y participé en la implementación del frontend junto a otras dos personas.

## Equipo

[@Flo-aq](https://github.com/Flo-aq) (Florencia Aqueveque), Gaspar, Diego y colaboradores. El historial conserva la autoría de cada integrante.

Los mockups de diseño están en [IIC3143-Mockups](https://github.com/Flo-aq/IIC3143-Mockups).
