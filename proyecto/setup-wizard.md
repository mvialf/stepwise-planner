# Setup Wizard - Generación de Fases Dinámicas

Este documento guía el proceso de inicialización de un nuevo proyecto con generación automática de fases.

## Flujo de Inicialización

### 1. Análisis Inicial del Proyecto

**Información básica requerida:**
- **Tipo de aplicación**: Web, API, Mobile, CLI, Desktop, Biblioteca, etc.
- **Funcionalidad principal**: ¿Qué problema resuelve?
- **Usuarios objetivo**: ¿Quién lo va a usar?

### 2. Detección Tecnológica

**Preguntas de contexto:**
- ¿Tienes preferencias de tecnología? (React, Node.js, Python, etc.)
- ¿Hay restricciones técnicas? (bases de datos, APIs existentes)
- ¿Qué nivel de experiencia tienes con estas tecnologías?

### 3. Análisis de Complejidad

**Factores de complejidad:**
- **Autenticación**: ¿Necesita login/usuarios?
- **Datos**: ¿Qué tan complejos son los datos?
- **Integraciones**: ¿APIs externas, pagos, emails?
- **Tiempo**: ¿Timeline aproximado?

### 4. Generación de Fases

**Algoritmo de decisión:**
```
Si es_aplicacion_simple():
    fases = 2-3 fases básicas
Si es_aplicacion_media():
    fases = 4-5 fases estructuradas
Si es_aplicacion_compleja():
    fases = 6+ fases granulares
```

## Templates de Preguntas por Tipo

### 📱 Aplicación Mobile
```
1. ¿React Native, Flutter, o nativo?
2. ¿Necesita funcionar offline?
3. ¿Integraciones con cámara/GPS/notificaciones?
4. ¿Store deployment desde el inicio?
```

### 🌐 API REST
```
1. ¿Qué framework prefieres? (Express, FastAPI, Spring Boot)
2. ¿Base de datos relacional o NoSQL?
3. ¿Autenticación JWT, OAuth, o simple?
4. ¿Documentación con Swagger/OpenAPI?
```

### 💻 Aplicación Web
```
1. ¿SPA o server-side rendering?
2. ¿Framework JS preferido? (React, Vue, Angular)
3. ¿CMS o aplicación personalizada?
4. ¿Dashboard admin incluido?
```

### 🛠️ Herramienta CLI
```
1. ¿Lenguaje preferido? (Python, Go, Rust, Node.js)
2. ¿Configuración via archivos o argumentos?
3. ¿Subcomandos complejos o simple?
4. ¿Distribución via package manager?
```

## Patrones de Fases por Tipo

### Pattern: API REST Básica
```
fase-01: Setup y modelos básicos
fase-02: CRUD endpoints principales  
fase-03: Autenticación y validación
fase-04: Testing y documentación
```

### Pattern: Web App Compleja
```
fase-01: Setup frontend y componentes base
fase-02: Páginas principales y navegación
fase-03: Integración backend y estado
fase-04: Funcionalidades avanzadas
fase-05: Optimización y deployment
```

### Pattern: Mobile App
```
fase-01: Setup del proyecto y navegación
fase-02: Pantallas principales y UI
fase-03: Lógica de negocio y datos
fase-04: Integraciones nativas
fase-05: Testing y store preparation
```

## Heurísticas de Granularidad

### Criterios para División de Fases

**Dividir fase si:**
- Más de 15 tareas en una fase
- Múltiples tecnologías mezcladas
- Dependencias complejas internas
- Cambio significativo de skillset requerido

**Fusionar fases si:**
- Menos de 5 tareas por fase
- Dependencias demasiado acopladas
- Similar nivel de complejidad
- Mismo dominio técnico

## Personalización por Experiencia

### Usuario Principiante
- Fases más granulares (6-8 fases)
- Más documentación por tarea
- Dependencias explícitas
- Tutoriales incluidos

### Usuario Intermedio
- Fases balanceadas (4-6 fases)
- Documentación esencial
- Referencias a mejores prácticas
- Opciones de arquitectura

### Usuario Avanzado  
- Fases condensadas (3-4 fases)
- Documentación mínima
- Enfoque en decisiones arquitectónicas
- Flexibilidad en implementación

## Flujo Conversacional de Ejemplo

```
Usuario: "Quiero crear una tienda online con React"

Claude: "Entiendo que quieres crear un e-commerce con React. 
Para generar las fases apropiadas necesito clarificar:

📋 Funcionalidades: ¿Carrito, pagos, inventario, usuarios?
🛠️ Backend: ¿API existente, necesitas crear backend, o JAMstack?  
💰 Pagos: ¿Stripe, PayPal, o solo mock por ahora?
📱 Responsive: ¿Solo desktop o mobile también?
⏱️ Timeline: ¿Cuánto tiempo tienes disponible?"

[Basándose en las respuestas...]

Claude: "Perfecto. Basándome en tus respuestas, propongo 4 fases:

fase-01: Setup React, routing y componentes base
fase-02: Catálogo de productos y carrito de compras  
fase-03: Sistema de usuarios y checkout
fase-04: Integración de pagos y deployment

¿Te parece adecuada esta división?"
```

## Archivos Generados Automáticamente

Para cada fase se genera:
- `README.md` con contexto específico del proyecto
- `objetivos.md` con metas concretas y medibles
- `tareas.md` con breakdown técnico detallado
- `entregables.md` con criterios de aceptación
- `dependencias.md` si aplica
- `riesgos.md` con mitigaciones específicas
- `notas.md` para seguimiento de progreso

---
*Setup Wizard para generación dinámica de fases*  
*Framework stepwise-planner + Claude Code*