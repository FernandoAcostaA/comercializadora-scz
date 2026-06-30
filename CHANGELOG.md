# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [Unreleased]

### Added
- Módulo de facturación electrónica (en desarrollo)
- Integración con API de Impuestos Nacionales Bolivia

---

## [1.2.0] - 2025-06-15

### Added
- **Módulo de Reportes**: Generación de reportes en PDF y Excel
- **Dashboard Ejecutivo**: Panel con KPIs de ventas en tiempo real
- **Exportación de datos**: Exportación a CSV/XLSX de pedidos e inventario
- **Notificaciones por email**: Alertas automáticas al cambiar estado de pedidos
- `GET /api/reportes/ventas-mensual` — Endpoint de reporte mensual
- `GET /api/reportes/inventario-critico` — Alerta de stock mínimo
- Configuración de ambiente staging en `.env.staging`

### Changed
- **Mejorado**: Tiempo de respuesta del endpoint de pedidos reducido en 40%
- **Actualizado**: Dependencia `Microsoft.EntityFrameworkCore` de 8.0.1 → 8.0.6
- **Refactorizado**: Servicio de notificaciones con patrón Observer

### Fixed
- **fix**: Error de cálculo de IGV en pedidos con descuento > 20%
- **fix**: Timeout en consultas de inventario con más de 10,000 registros
- **fix**: Validación incorrecta de RUC en formulario de clientes

### Security
- Actualización de `System.Text.Json` por vulnerabilidad CVE-2024-38095

---

## [1.1.0] - 2025-04-10

### Added
- **Módulo de Inventario Avanzado**: Control de stock con alertas automáticas
- **Gestión de Proveedores**: CRUD completo de proveedores con evaluación
- **API de Categorías**: Categorización jerárquica de productos
- `POST /api/inventario/ajuste-stock` — Ajuste manual de inventario
- `GET /api/proveedores/{id}/evaluacion` — Evaluación de proveedor
- Soporte para múltiples almacenes (sucursales)
- Migración de base de datos `V3_AddInventoryTables.sql`

### Changed
- **Mejorado**: Módulo de pedidos con soporte de pedidos parciales
- **Actualizado**: Esquema de base de datos con índices optimizados
- **Cambiado**: Autenticación de Basic Auth → JWT Bearer tokens
- Campos `Pedido.FechaActualizacion` ahora se actualiza automáticamente

### Fixed
- **fix**: Duplicación de pedidos al recargar página de confirmación
- **fix**: Error 500 en búsqueda de productos con caracteres especiales (ñ, á)
- **fix**: Cálculo incorrecto de totales con múltiples impuestos

### Deprecated
- Endpoint `GET /api/productos/lista` — usar `GET /api/productos` con paginación

---

## [1.0.0] - 2025-02-20

### Added
- **Módulo de Pedidos**: Creación, edición, cancelación y seguimiento de pedidos
- **Gestión de Clientes**: Registro y administración de clientes con historial
- **Catálogo de Productos**: CRUD de productos con precios y descripción
- **Autenticación**: Sistema de login con roles (Admin, Vendedor, Repartidor)
- **API REST**: Endpoints iniciales del sistema
  - `POST /api/auth/login` — Autenticación
  - `GET /api/pedidos` — Listado paginado
  - `POST /api/pedidos` — Crear pedido
  - `PUT /api/pedidos/{id}` — Actualizar pedido
  - `GET /api/clientes` — Listado de clientes
  - `GET /api/productos` — Catálogo de productos
- Configuración inicial de SQL Server con migraciones EF Core
- Dockerfile para containerización
- Pipeline CI/CD básico en GitHub Actions

### Infrastructure
- Repositorio inicializado con estructura Git Flow
- Configuración de ramas protegidas (`main`, `develop`)
- Plantillas de Issues RFC y Bug Report
- Configuración de `.editorconfig` y `.gitignore`

---

## Links de Comparación

[Unreleased]: https://github.com/fernandodev/comercializadora-scz/compare/v1.2.0...HEAD
[1.2.0]: https://github.com/fernandodev/comercializadora-scz/compare/v1.1.0...v1.2.0
[1.1.0]: https://github.com/fernandodev/comercializadora-scz/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/fernandodev/comercializadora-scz/releases/tag/v1.0.0
