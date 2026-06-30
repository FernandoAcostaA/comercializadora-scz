# Comercializadora Santa Cruz S.R.L. — Sistema de Gestión

[![CI/CD Pipeline](https://github.com/fernandodev/comercializadora-scz/actions/workflows/ci-cd.yml/badge.svg)](https://github.com/fernandodev/comercializadora-scz/actions/workflows/ci-cd.yml)
[![Build Status](https://github.com/fernandodev/comercializadora-scz/actions/workflows/ci-cd.yml/badge.svg?branch=main)](https://github.com/fernandodev/comercializadora-scz/actions)
[![Coverage](https://img.shields.io/badge/coverage-87%25-brightgreen)](https://github.com/fernandodev/comercializadora-scz)
[![Version](https://img.shields.io/badge/version-1.2.0-blue)](CHANGELOG.md)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![SemVer](https://img.shields.io/badge/SemVer-2.0.0-informational)](https://semver.org)

Sistema de gestión de pedidos y comercialización para Comercializadora Santa Cruz S.R.L.

## 📋 Descripción

Sistema web desarrollado con **ASP.NET Core 8** y **SQL Server** para la gestión integral de pedidos, inventario y ventas de la empresa Comercializadora Santa Cruz S.R.L.

## 🏗️ Arquitectura

```
comercializadora-scz/
├── src/
│   ├── api/           # ASP.NET Core 8 Web API
│   ├── config/        # Configuraciones de entorno
│   └── tests/         # Pruebas unitarias e integración
├── docs/
│   ├── rfc/           # Request for Change documentados
│   └── ccb/           # Actas del Configuration Control Board
├── scripts/           # Scripts de automatización
├── .github/
│   ├── workflows/     # GitHub Actions CI/CD
│   └── ISSUE_TEMPLATE/# Plantillas de Issues RFC
└── CHANGELOG.md       # Historial de cambios
```

## 🌿 Git Flow

| Rama | Propósito |
|------|-----------|
| `main` | Producción estable |
| `develop` | Integración de features |
| `feature/*` | Nuevas funcionalidades |
| `release/*` | Preparación de releases |
| `hotfix/*` | Correcciones urgentes |

## 🚀 Quick Start

```bash
git clone https://github.com/fernandodev/comercializadora-scz.git
cd comercializadora-scz
dotnet restore
dotnet run --project src/api
```

## 🔄 CI/CD Pipeline

El pipeline automatizado ejecuta los siguientes jobs en cada push:

1. **lint** — Análisis estático de código
2. **build** — Compilación del proyecto
3. **test** — Ejecución de pruebas + cobertura
4. **deploy** — Despliegue a ambiente staging

## 📦 Releases

Ver [CHANGELOG.md](CHANGELOG.md) para el historial completo de versiones.

- **v1.2.0** — Módulo de reportes y exportación PDF
- **v1.1.0** — Gestión avanzada de inventario
- **v1.0.0** — Release inicial: módulo de pedidos

## 📝 Proceso de Cambios (RFC/CCB)

Ver carpeta [`docs/rfc/`](docs/rfc/) para los formularios de solicitud de cambio y [`docs/ccb/`](docs/ccb/) para las actas de aprobación del CCB.

## 👥 Equipo

- **Fernando** — Desarrollador Principal / Configuration Manager
- **Ing. Jimmy Requena** — Director de Proyecto

## 📄 Licencia

MIT License — ver [LICENSE](LICENSE) para detalles.
