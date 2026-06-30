# RFC-002: Migración de Autenticación Basic Auth → JWT Bearer

**Estado**: ✅ APROBADO  
**Prioridad**: 🔴 Crítica  
**Solicitante**: Área de Seguridad / Ing. David Serrudo  
**Fecha**: 2025-03-01  
**CCB Meeting**: 2025-03-05  
**Release objetivo**: v1.1.0

---

## Descripción

La autenticación Basic Auth actual envía credenciales en cada request. Se requiere migrar a JWT para mejorar seguridad, permitir sesiones stateless y preparar el sistema para integración con aplicaciones móviles.

## Impacto Técnico

- Modificación de middleware de autenticación
- Nuevo endpoint `POST /api/auth/refresh-token`
- Cambio en todos los clientes que consumen la API
- Migración BD: Tabla `RefreshTokens`
- Estimación: 3 días de desarrollo + 1 día de pruebas

## Riesgos

| Riesgo | Mitigación |
|--------|-----------|
| Breaking change para clientes existentes | Periodo de transición 30 días con ambos métodos activos |
| Seguridad de refresh tokens | Almacenamiento hasheado + rotación automática |

## Decisión CCB

**APROBADO** — 2025-03-05  
Votación: 3 a favor / 0 en contra  
Condición: Mantener Basic Auth en deprecado durante v1.1.0, eliminar en v1.2.0  

**Implementado en commit**: `d8e2b45`  
**Incluido en**: v1.1.0
