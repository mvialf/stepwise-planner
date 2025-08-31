# Stack Tecnológico: [Nombre del Proyecto]

**Última actualización:** YYYY-MM-DD  
**Responsable:** [Nombre]  
**Versión:** v1.0

## Resumen Ejecutivo

[Descripción general del stack elegido y la estrategia tecnológica del proyecto]

## Arquitectura General

```
[Diagrama o descripción de alto nivel de la arquitectura]
Frontend ↔ API ↔ Backend ↔ Database
```

## Stack Detallado

### Frontend
| Tecnología | Versión | Propósito | Estado |
|------------|---------|-----------|---------|
| [Framework] | vX.X | Framework principal | ✅ Seleccionado |
| [Librería UI] | vX.X | Componentes UI | ✅ Seleccionado |
| [Build Tool] | vX.X | Build y bundling | 🔄 Evaluando |
| [Testing] | vX.X | Testing unitario | ❌ Por definir |

### Backend
| Tecnología | Versión | Propósito | Estado |
|------------|---------|-----------|---------|
| [Lenguaje] | vX.X | Lenguaje principal | ✅ Seleccionado |
| [Framework] | vX.X | Framework web | ✅ Seleccionado |
| [ORM/DB Client] | vX.X | Acceso a datos | 🔄 Evaluando |
| [Auth] | vX.X | Autenticación | ❌ Por definir |

### Base de Datos
| Tecnología | Versión | Propósito | Estado |
|------------|---------|-----------|---------|
| [Database] | vX.X | Base principal | ✅ Seleccionado |
| [Cache] | vX.X | Sistema de caché | 🔄 Evaluando |
| [Migration] | vX.X | Migraciones | ❌ Por definir |

### Infraestructura
| Tecnología | Versión | Propósito | Estado |
|------------|---------|-----------|---------|
| [Cloud Provider] | - | Hosting | ✅ Seleccionado |
| [Container] | vX.X | Contenedores | 🔄 Evaluando |
| [CI/CD] | vX.X | Despliegue | ❌ Por definir |
| [Monitoring] | vX.X | Monitoreo | ❌ Por definir |

### Herramientas de Desarrollo
| Tecnología | Versión | Propósito | Estado |
|------------|---------|-----------|---------|
| [IDE/Editor] | vX.X | Desarrollo | ✅ Seleccionado |
| [Linter] | vX.X | Code quality | ✅ Seleccionado |
| [Formatter] | vX.X | Code formatting | ✅ Seleccionado |
| [Package Manager] | vX.X | Gestión dependencias | ✅ Seleccionado |

## Decisiones Clave

### [Nombre de la Decisión 1]
- **Problema:** [Qué necesitábamos resolver]
- **Opciones:** [Alternativas consideradas]
- **Decisión:** [Qué elegimos]
- **Razón:** [Por qué lo elegimos]
- **ADR:** [Enlace al ADR si existe]

### [Nombre de la Decisión 2]
- **Problema:** [Qué necesitábamos resolver]
- **Opciones:** [Alternativas consideradas]
- **Decisión:** [Qué elegimos]
- **Razón:** [Por qué lo elegimos]
- **ADR:** [Enlace al ADR si existe]

## Dependencias y Compatibilidad

### Versiones Mínimas
- **Node.js:** vX.X o superior
- **Python:** vX.X o superior
- **Database:** vX.X o superior

### Dependencias Críticas
- [Dependencia crítica 1]: Requerida para [funcionalidad]
- [Dependencia crítica 2]: Requerida para [funcionalidad]

## Configuración y Setup

### Variables de Entorno
```bash
# Database
DB_HOST=localhost
DB_PORT=5432
DB_NAME=proyecto_db

# API
API_PORT=3000
API_SECRET=your-secret-key

# Frontend
REACT_APP_API_URL=http://localhost:3000
```

### Comandos de Setup
```bash
# Backend
npm install
npm run dev

# Frontend
npm install
npm start

# Database
docker-compose up -d
npm run migrate
```

## Convenciones y Estándares

### Estructura de Proyectos
```
proyecto/
├── backend/
│   ├── src/
│   ├── tests/
│   └── package.json
├── frontend/
│   ├── src/
│   ├── public/
│   └── package.json
└── infrastructure/
    ├── docker/
    └── scripts/
```

### Convenciones de Código
- **Naming:** camelCase para variables, PascalCase para componentes
- **Files:** kebab-case para archivos, PascalCase para componentes
- **Commits:** Conventional Commits (feat:, fix:, docs:)
- **Branches:** feature/*, bugfix/*, hotfix/*

## Métricas y Performance

### Targets de Performance
- **Frontend:** First Paint < 1s, Interactive < 3s
- **Backend:** Response time < 200ms (95th percentile)
- **Database:** Query time < 100ms (average)

### Herramientas de Medición
- [Herramienta de frontend performance]
- [Herramienta de backend monitoring]
- [Herramienta de database monitoring]

## Seguridad

### Consideraciones de Seguridad
- **Autenticación:** [JWT/OAuth/etc.]
- **Autorización:** [RBAC/ABAC/etc.]
- **HTTPS:** Requerido en producción
- **Secrets:** Usar variables de entorno
- **Dependencies:** Audit regular con [herramienta]

## Migración y Rollback

### Plan de Migración
- **Fase 1:** [Descripción]
- **Fase 2:** [Descripción]
- **Rollback:** [Estrategia de rollback]

### Backward Compatibility
- **APIs:** Mantener compatibilidad por X versiones
- **Database:** Migraciones reversibles cuando sea posible

## Documentación Técnica

### Referencias
- [Enlace a documentación de Framework 1]
- [Enlace a documentación de Framework 2]
- [Enlace a best practices internas]

### ADRs Relacionados
- [ADR-001: Elección de Framework Frontend](../adr/ADR-001.md)
- [ADR-002: Arquitectura de Base de Datos](../adr/ADR-002.md)

## Roadmap Tecnológico

### Próximas Evaluaciones
- **Q1 2024:** Evaluar actualización de [tecnología]
- **Q2 2024:** Considerar migración a [nueva tecnología]
- **Q3 2024:** Implementar [mejora de infraestructura]

### Deuda Técnica Identificada
- [ ] [Item de deuda técnica 1]
- [ ] [Item de deuda técnica 2]
- [ ] [Item de deuda técnica 3]

---
*Template del framework stepwise-planner*