# Backend Stack: [Nombre del Proyecto]

**Última actualización:** YYYY-MM-DD  
**Responsable:** [Nombre del Backend Lead]

## Resumen del Backend

[Descripción de la arquitectura y responsabilidades del backend]

## Stack Principal

### Framework y Runtime
| Tecnología | Versión | Propósito | Estado |
|------------|---------|-----------|---------|
| [Node.js/Python/Go/etc.] | vX.X | Runtime principal | ✅ |
| [Express/FastAPI/Gin/etc.] | vX.X | Framework web | ✅ |
| [TypeScript/etc.] | vX.X | Tipado estático | ✅ |

### Arquitectura y Patrones
- **Patrón arquitectónico:** [MVC/Clean Architecture/Hexagonal]
- **Estructura de capas:** [Controller → Service → Repository]
- **Inyección de dependencias:** [Sí/No - herramienta]
- **Validación:** [Joi/Zod/Pydantic/etc.]

## APIs y Comunicación

### REST API
```yaml
# Estructura de endpoints
/api/v1/
  /auth/          # Autenticación
  /users/         # Gestión de usuarios
  /[recursos]/    # Recursos del dominio
```

### Documentación API
- **Herramienta:** [Swagger/OpenAPI/Postman]
- **Ubicación:** [URL de la documentación]
- **Versionado:** [Estrategia de versionado]

### Middleware Stack
```javascript
// Ejemplo de middleware stack
app.use(cors())
app.use(helmet())
app.use(morgan())
app.use(express.json())
app.use(rateLimiter())
app.use(auth())
```

## Base de Datos

### Conexión y ORM
| Tecnología | Versión | Propósito |
|------------|---------|-----------|
| [Prisma/TypeORM/SQLAlchemy] | vX.X | ORM principal |
| [pg/mysql2/etc.] | vX.X | Driver de BD |

### Estructura de Datos
```sql
-- Ejemplo de schema principal
Users
├── id (UUID/INT)
├── email (UNIQUE)
├── password_hash
├── created_at
└── updated_at
```

### Migraciones
- **Herramienta:** [Prisma/Alembic/etc.]
- **Estrategia:** [Forward-only/Reversible]
- **Entorno:** [Local/Staging/Production workflow]

## Autenticación y Autorización

### Estrategia Auth
- **Método:** [JWT/Sessions/OAuth]
- **Provider:** [Auth0/Firebase/Custom]
- **Refresh tokens:** [Sí/No]
- **SSO:** [Sí/No - provider]

### Autorización
```javascript
// Ejemplo de middleware de autorización
const authorize = (roles) => {
  return (req, res, next) => {
    // Lógica de autorización
  }
}

// Uso
app.get('/admin/*', authorize(['admin']), handler)
```

## Testing

### Estrategia de Testing
| Tipo | Framework | Coverage Target |
|------|-----------|-----------------|
| Unitarios | [Jest/PyTest] | >80% |
| Integración | [Supertest/etc.] | >70% |
| E2E | [Cypress/Playwright] | Críticos |

### Configuración de Tests
```bash
# Scripts de testing
npm run test          # Unitarios
npm run test:integration
npm run test:e2e
npm run test:coverage
```

## Performance y Monitoring

### Métricas Objetivo
- **Response time:** < 200ms (P95)
- **Throughput:** > X requests/second
- **Error rate:** < 1%
- **Uptime:** > 99.9%

### Herramientas
- **APM:** [New Relic/DataDog/Custom]
- **Logging:** [Winston/Pino/etc.]
- **Metrics:** [Prometheus/etc.]

## Seguridad

### Medidas Implementadas
- [ ] **Input validation:** Validación en todos los endpoints
- [ ] **SQL injection:** Uso de ORM/prepared statements
- [ ] **XSS:** Sanitización de inputs
- [ ] **CSRF:** Tokens CSRF donde aplique
- [ ] **Rate limiting:** Límites por IP/usuario
- [ ] **HTTPS only:** Redirección forzada
- [ ] **Headers security:** helmet.js o similar

### Secrets Management
```bash
# Variables de entorno críticas
DB_PASSWORD=
JWT_SECRET=
API_KEYS=
```

## Estructura del Proyecto

```
backend/
├── src/
│   ├── controllers/     # Controladores HTTP
│   ├── services/       # Lógica de negocio
│   ├── repositories/   # Acceso a datos
│   ├── models/         # Modelos de datos
│   ├── middleware/     # Middleware personalizado
│   ├── utils/          # Utilidades
│   └── types/          # Tipos TypeScript
├── tests/
│   ├── unit/
│   ├── integration/
│   └── fixtures/
├── migrations/         # Migraciones de BD
├── seeds/             # Datos de prueba
└── docs/              # Documentación técnica
```

## Dependencias Críticas

### Production
```json
{
  "[framework]": "^X.X.X",
  "[database-client]": "^X.X.X",
  "[validation]": "^X.X.X",
  "[auth]": "^X.X.X"
}
```

### Development
```json
{
  "[testing-framework]": "^X.X.X",
  "[type-definitions]": "^X.X.X",
  "[linting]": "^X.X.X"
}
```

## Configuración por Entorno

### Development
```bash
NODE_ENV=development
DB_HOST=localhost
LOG_LEVEL=debug
CORS_ORIGIN=http://localhost:3000
```

### Production
```bash
NODE_ENV=production
DB_HOST=prod-db-cluster
LOG_LEVEL=info
CORS_ORIGIN=https://yourdomain.com
```

## Deployment y CI/CD

### Build Process
```bash
# Build steps
npm ci
npm run build
npm run test
npm run lint
```

### Deployment Strategy
- **Estrategia:** [Blue-Green/Rolling/Canary]
- **Containerización:** [Docker/Buildpacks]
- **Orchestration:** [Kubernetes/Docker Swarm/None]

## Troubleshooting

### Logs Comunes
```bash
# Ver logs en tiempo real
tail -f logs/app.log

# Buscar errores
grep "ERROR" logs/app.log

# Filtrar por fecha
grep "2024-01-01" logs/app.log
```

### Debugging
- **Local:** [Debugger configuration]
- **Production:** [Logging strategy]
- **Performance:** [Profiling tools]

## ADRs Relacionados

- [ADR-XXX: Elección de Framework Backend](../../adr/ADR-XXX.md)
- [ADR-XXX: Estrategia de Autenticación](../../adr/ADR-XXX.md)
- [ADR-XXX: Arquitectura de Base de Datos](../../adr/ADR-XXX.md)

---
*Template especializado para Backend - stepwise-planner*