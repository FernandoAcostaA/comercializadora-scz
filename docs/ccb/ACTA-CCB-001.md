# Acta de Reunión — Configuration Control Board (CCB)
## Reunión N° 001 — 22 de Mayo de 2025

---

**Proyecto**: Sistema de Gestión — Comercializadora Santa Cruz S.R.L.  
**Fecha**: 22 de Mayo de 2025, 14:00 hs  
**Modalidad**: Presencial — Aula UPDS Santa Cruz  
**Duración**: 45 minutos

---

## Asistentes del CCB

| Rol | Nombre | Firma |
|-----|--------|-------|
| Director de Proyecto | Ing. Jimmy Requena | ✓ |
| Configuration Manager | Fernando (estudiante) | ✓ |
| Representante de QA | Ing. David Serrudo | ✓ |

---

## RFCs Revisados en esta Sesión

### RFC-001: Módulo de Reportes PDF

**Análisis técnico presentado por**: Fernando  
**Tiempo de presentación**: 15 minutos  

**Puntos discutidos**:
- Librería `QuestPDF` evaluada vs `iTextSharp` — QuestPDF seleccionada por licencia MIT
- Rendimiento: reportes grandes pueden tardar hasta 8 segundos
- Solución acordada: caché de 1 hora en memoria para reportes de ventas mensual

**Votación**:
| Miembro | Voto | Observación |
|---------|------|-------------|
| Ing. Requena | ✅ Aprobado | Entregar antes del 15 de junio |
| Fernando | ✅ Aprobado | — |
| Ing. Serrudo | ✅ Aprobado | Agregar logging de generación de reportes |

**Resolución**: APROBADO (3/3 votos a favor)  
**Sprint asignado**: Sprint 8  
**Responsable de implementación**: Fernando

---

## Compromisos y Seguimiento

| Acción | Responsable | Fecha límite |
|--------|-------------|-------------|
| Implementar RFC-001 | Fernando | 2025-06-10 |
| Code review del PR | Ing. Requena | 2025-06-12 |
| QA y pruebas | Ing. Serrudo | 2025-06-14 |
| Deploy a staging | Fernando | 2025-06-15 |

---

## Métricas del Proceso de Cambios

| Métrica | Valor |
|---------|-------|
| RFCs recibidos (acumulado) | 1 |
| RFCs aprobados | 1 (100%) |
| RFCs rechazados | 0 |
| Tiempo promedio de aprobación | 2 días |

---

**Próxima reunión CCB**: 05 de Marzo de 2025  
**Secretario**: Fernando  
**Aprobado por**: Ing. Jimmy Requena Llorentty
