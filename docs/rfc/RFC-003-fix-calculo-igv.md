# RFC-003 (Hotfix): Corrección Cálculo IGV con Descuentos

**Estado**: ✅ APROBADO (Emergencia)  
**Prioridad**: 🔴 Crítica (Bug en Producción)  
**Solicitante**: Soporte / Reporte de cliente  
**Fecha**: 2025-06-01  
**CCB Aprobación**: Verbal + Acta ex-post (2025-06-02)  
**Release objetivo**: v1.2.0 / Hotfix inmediato

---

## Descripción del Bug

Los pedidos con descuento mayor al 20% calculan el IGV sobre el precio original en lugar del precio descontado, generando cobros incorrectos.

**Impacto**: 47 pedidos afectados desde 2025-05-10.

## Fix Aplicado

```csharp
// ANTES (incorrecto)
decimal igv = producto.Precio * 0.16m;

// DESPUÉS (correcto)  
decimal precioConDescuento = producto.Precio * (1 - descuento);
decimal igv = precioConDescuento * 0.16m;
```

## Decisión CCB (Emergencia)

**APROBADO** — Aprobación verbal por Gerente de Proyecto  
Acta formal registrada el 2025-06-02  
Hotfix desplegado en: rama `hotfix/fix-igv-descuento`  
**Commit**: `f1c9d33`  
**Incluido en**: v1.2.0
