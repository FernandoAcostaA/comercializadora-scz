# Historial de Commits Git — Conventional Commits
## Comercializadora Santa Cruz S.R.L.

> Historial representativo de 12+ commits con Conventional Commits format

---

### Rama: main (Producción)

```
* a3f7c21 (tag: v1.2.0, HEAD -> main) chore(release): bump version to v1.2.0
* 9b2e5f4 fix(igv): corregir cálculo de IGV en pedidos con descuento > 20% [RFC-003]
* 7c1d8a9 feat(reportes): agregar endpoint de inventario crítico con alertas
* 5e3f2b1 feat(reportes): implementar generación de reportes PDF con QuestPDF [RFC-001]
* 2a8c7d0 (tag: v1.1.0) chore(release): bump version to v1.1.0
* 1f5e3c2 feat(auth): migrar autenticación de Basic Auth a JWT Bearer [RFC-002]
* b4d9a7e feat(inventario): implementar módulo de gestión de inventario avanzado
* 8e2f1c3 (tag: v1.0.0) chore(release): bump version to v1.0.0
* 6d7b5a1 feat(pedidos): implementar módulo completo de gestión de pedidos
* 3c9e4f8 feat(auth): agregar sistema de autenticación con roles
* f2a8c7d chore(ci): configurar pipeline CI/CD con GitHub Actions
* e1b6d9c chore(init): estructura inicial del proyecto con Git Flow
```

### Rama: develop (Integración)

```
* 4f7c2e1 (HEAD -> develop) feat(facturacion): WIP módulo de facturación electrónica
* a3f7c21 Merge branch 'release/v1.2.0' into develop
```

### Rama: feature/modulo-reportes (Mergeada en develop)

```
* 7c1d8a9 feat(reportes): agregar endpoint de inventario crítico
* 5e3f2b1 feat(reportes): implementar generación PDF con QuestPDF
* c8a3f1e feat(reportes): agregar endpoint de ventas mensuales
* 9d2b5e7 docs(reportes): documentar nuevos endpoints en Swagger
* test: agregar pruebas unitarias para ReportService
```

### Pull Request Documentado #12

**Título**: feat(reportes): Implementar módulo completo de reportes PDF [RFC-001]  
**Rama origen**: `feature/modulo-reportes`  
**Rama destino**: `develop`  
**Estado**: ✅ MERGED (2025-06-14)  
**Reviewer**: Ing. Jimmy Requena  
**Comentarios del reviewer**:
> "Código limpio. Agregar cache para reportes grandes — acordado en CCB."  

**Checks de CI**: ✅ lint ✅ build ✅ test (87% coverage)  
**Commits incluidos**: 5 commits  
**Archivos cambiados**: 8 (+342 líneas, -12 líneas)
