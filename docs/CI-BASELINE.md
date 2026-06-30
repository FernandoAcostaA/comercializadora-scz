# Línea Base de Configuración (Configuration Items Baseline)
## Comercializadora Santa Cruz S.R.L. — v1.2.0

**Documento**: SCM-BASELINE-001  
**Versión**: 1.2.0  
**Fecha**: 2025-06-15  
**Configuration Manager**: Fernando

---

## Categoría 1: Código Fuente (CSC — Computer Software Component)

| ID | Ítem de Configuración | Ruta | Versión | Responsable | Última modificación |
|----|----------------------|------|---------|-------------|---------------------|
| CI-001 | API Principal (ASP.NET Core 8) | `src/api/` | v1.2.0 | Fernando | 2025-06-15 |
| CI-002 | Controlador de Pedidos | `src/api/Controllers/PedidosController.cs` | v1.2.0 | Fernando | 2025-06-10 |
| CI-003 | Controlador de Clientes | `src/api/Controllers/ClientesController.cs` | v1.2.0 | Fernando | 2025-04-05 |
| CI-004 | Controlador de Inventario | `src/api/Controllers/InventarioController.cs` | v1.1.0 | Fernando | 2025-04-08 |
| CI-005 | Controlador de Reportes | `src/api/Controllers/ReportesController.cs` | v1.2.0 | Fernando | 2025-06-14 |
| CI-006 | Servicio de Autenticación JWT | `src/api/Services/AuthService.cs` | v1.1.0 | Fernando | 2025-04-02 |
| CI-007 | Servicio de Reportes PDF | `src/api/Services/ReportService.cs` | v1.2.0 | Fernando | 2025-06-12 |
| CI-008 | Contexto de Base de Datos (EF Core) | `src/api/Data/AppDbContext.cs` | v1.2.0 | Fernando | 2025-06-01 |
| CI-009 | Suite de Pruebas Unitarias | `src/tests/` | v1.2.0 | Fernando | 2025-06-14 |
| CI-010 | Pruebas de Integración | `src/tests/Integration/` | v1.1.0 | Fernando | 2025-04-09 |

## Categoría 2: Configuración y Entorno

| ID | Ítem de Configuración | Ruta | Versión | Responsable |
|----|----------------------|------|---------|-------------|
| CI-011 | Configuración de Producción | `src/config/appsettings.json` | v1.2.0 | Fernando |
| CI-012 | Configuración de Desarrollo | `src/config/appsettings.Development.json` | v1.2.0 | Fernando |
| CI-013 | Configuración de Staging | `src/config/appsettings.Staging.json` | v1.2.0 | Fernando |
| CI-014 | Variables de Entorno (.env.example) | `.env.example` | v1.1.0 | Fernando |
| CI-015 | Dockerfile | `Dockerfile` | v1.2.0 | Fernando |
| CI-016 | Docker Compose (desarrollo) | `docker-compose.yml` | v1.1.0 | Fernando |

## Categoría 3: Scripts y Automatización

| ID | Ítem de Configuración | Ruta | Versión | Responsable |
|----|----------------------|------|---------|-------------|
| CI-017 | Pipeline CI/CD (GitHub Actions) | `.github/workflows/ci-cd.yml` | v1.2.0 | Fernando |
| CI-018 | Script de migración BD (v1.0.0) | `scripts/V1_InitialSchema.sql` | v1.0.0 | Fernando |
| CI-019 | Script de migración BD (v1.1.0) | `scripts/V2_AddInventoryTables.sql` | v1.1.0 | Fernando |
| CI-020 | Script de migración BD (v1.2.0) | `scripts/V3_AddReportCache.sql` | v1.2.0 | Fernando |
| CI-021 | Script de seed de datos | `scripts/seed-data.sql` | v1.0.0 | Fernando |

## Categoría 4: Documentación

| ID | Ítem de Configuración | Ruta | Versión | Responsable |
|----|----------------------|------|---------|-------------|
| CI-022 | README principal | `README.md` | v1.2.0 | Fernando |
| CI-023 | CHANGELOG | `CHANGELOG.md` | v1.2.0 | Fernando |
| CI-024 | Línea Base CI (este doc) | `docs/CI-BASELINE.md` | v1.2.0 | Fernando |
| CI-025 | RFC-001 Módulo Reportes | `docs/rfc/RFC-001-modulo-reportes.md` | v1.0 | Fernando |
| CI-026 | RFC-002 Migración JWT | `docs/rfc/RFC-002-migracion-jwt.md` | v1.0 | Fernando |
| CI-027 | RFC-003 Fix IGV | `docs/rfc/RFC-003-fix-calculo-igv.md` | v1.0 | Fernando |
| CI-028 | Acta CCB N°001 | `docs/ccb/ACTA-CCB-001.md` | v1.0 | Fernando |
| CI-029 | Acta CCB N°002 | `docs/ccb/ACTA-CCB-002.md` | v1.0 | Fernando |
| CI-030 | Plantilla RFC (Issue Template) | `.github/ISSUE_TEMPLATE/rfc-solicitud-cambio.md` | v1.1.0 | Fernando |

## Categoría 5: Diagramas y Modelos

| ID | Ítem de Configuración | Ruta | Versión | Responsable |
|----|----------------------|------|---------|-------------|
| CI-031 | Diagrama de Componentes (UML) | `docs/diagrams/componentes.drawio` | v1.2.0 | Fernando |
| CI-032 | Modelo de Base de Datos (ERD) | `docs/diagrams/erd.drawio` | v1.1.0 | Fernando |
| CI-033 | Diagrama Git Flow | `docs/diagrams/gitflow.png` | v1.0.0 | Fernando |

---

## Trazabilidad RFC → Commit → Release

| RFC | Descripción | Commit | Release |
|-----|-------------|--------|---------|
| RFC-001 | Módulo de Reportes PDF | `a3f7c21` | v1.2.0 |
| RFC-002 | Migración JWT | `d8e2b45` | v1.1.0 |
| RFC-003 | Fix IGV descuentos | `f1c9d33` | v1.2.0 |

---

## Resumen del Inventario

| Categoría | Cantidad de CIs |
|-----------|----------------|
| Código Fuente | 10 |
| Configuración y Entorno | 6 |
| Scripts y Automatización | 5 |
| Documentación | 9 |
| Diagramas y Modelos | 3 |
| **TOTAL** | **33 ítems** |

**Control de cambios**: Toda modificación a un CI requiere RFC aprobado por CCB (excepto hotfixes críticos con aprobación verbal + acta ex-post).
