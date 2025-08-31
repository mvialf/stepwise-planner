# Reglas de Generación Dinámica de Fases

Este documento define las heurísticas y reglas que Claude Code utiliza para generar fases específicas según el tipo y complejidad del proyecto.

## Algoritmo de Detección de Complejidad

### Factores de Complejidad

#### 🔍 **Análisis Automático**
```
complejidad_score = 0

# Funcionalidades detectadas
if "autenticación" or "usuarios" or "login": +2
if "pagos" or "stripe" or "paypal": +3  
if "admin" or "dashboard" or "cms": +2
if "real-time" or "websockets" or "chat": +3
if "mobile" or "react-native" or "flutter": +2
if "API" and ("GraphQL" or "REST"): +1
if "base de datos" and ("relacional" or "SQL"): +1
if "microservicios" or "arquitectura distribuida": +4
if "machine learning" or "AI" or "análisis": +3
if "deployment" or "CI/CD" or "Docker": +1

# Integración con servicios externos
if "API externa" or "third-party": +2
if "email" or "notifications": +1
if "file upload" or "storage": +1
```

### Mapeo Complejidad → Número de Fases

```python
def determinar_fases(complejidad_score, experiencia_usuario):
    base_fases = {
        0-3: 2,    # Proyecto simple
        4-7: 4,    # Proyecto medio
        8-12: 5,   # Proyecto complejo
        13+: 6     # Proyecto muy complejo
    }
    
    # Ajuste por experiencia
    if experiencia_usuario == "principiante":
        return base_fases + 1  # Más granular
    elif experiencia_usuario == "avanzado":
        return max(base_fases - 1, 2)  # Más condensado
    
    return base_fases
```

## Patrones de Fases por Tipo de Proyecto

### 📱 **Aplicación Mobile**

#### Simple (2-3 fases)
```
fase-01: Setup y navegación básica
fase-02: Pantallas principales y funcionalidad core
fase-03: Polish y store deployment
```

#### Complejo (4-6 fases)
```
fase-01: Setup del proyecto y arquitectura
fase-02: Componentes UI y navegación
fase-03: Lógica de negocio y estado
fase-04: Integración con APIs/servicios
fase-05: Funcionalidades nativas (cámara, GPS, etc.)
fase-06: Testing, optimización y store deployment
```

### 🌐 **API REST**

#### Simple (2-3 fases)
```
fase-01: Setup y modelos básicos
fase-02: CRUD endpoints principales
fase-03: Documentación y deployment
```

#### Complejo (4-5 fases)
```
fase-01: Arquitectura base y modelos de datos
fase-02: Endpoints CRUD y validaciones
fase-03: Autenticación y autorización
fase-04: Features avanzadas (filtros, paginación, etc.)
fase-05: Testing, optimización y deployment
```

### 💻 **Aplicación Web (SPA)**

#### Simple (3 fases)
```
fase-01: Setup y componentes base
fase-02: Páginas principales y routing
fase-03: Integración de datos y deployment
```

#### Complejo (5-6 fases)
```
fase-01: Arquitectura frontend y setup
fase-02: Sistema de componentes y diseño
fase-03: Estado global y routing avanzado
fase-04: Integración backend y APIs
fase-05: Funcionalidades de usuario (auth, perfil, etc.)
fase-06: Optimización, testing y deployment
```

### 🛠️ **Herramienta CLI**

#### Simple (2-3 fases)
```
fase-01: Core functionality y argumentos básicos
fase-02: Subcomandos y configuración
fase-03: Testing y distribución
```

#### Complejo (4 fases)
```
fase-01: Arquitectura CLI y parsing de argumentos
fase-02: Core commands y business logic
fase-03: Configuración, plugins y extensibilidad
fase-04: Testing, documentación y packaging
```

## Heurísticas de Contenido por Fase

### **Fase Inicial** (siempre presente)
```yaml
objetivos:
  - Setup del entorno de desarrollo
  - Arquitectura base del proyecto
  - Configuración inicial de herramientas

tareas_comunes:
  - Configurar entorno de desarrollo
  - Crear estructura de directorios
  - Setup de herramientas (linting, testing, etc.)
  - Configurar control de versiones

riesgos:
  - Problemas de configuración de entorno
  - Incompatibilidades de versiones
```

### **Fases Intermedias** (específicas al proyecto)
```yaml
# Determinadas por funcionalidades detectadas
# Ejemplo para e-commerce:
fase_productos:
  objetivos: [CRUD de productos, catálogo, categorías]
  tareas: [modelos, APIs, UI components]
  riesgos: [performance con muchos productos]

fase_usuarios:
  objetivos: [registro, login, perfiles]
  tareas: [autenticación, autorización, UI]
  riesgos: [seguridad, validación de datos]
```

### **Fase Final** (siempre presente)
```yaml
objetivos:
  - Testing completo del sistema
  - Optimización de performance
  - Deployment y monitoreo

tareas_comunes:
  - Testing end-to-end
  - Optimización de performance
  - Configurar CI/CD
  - Deployment a producción
  - Documentación final

riesgos:
  - Problemas en producción
  - Performance en carga real
```

## Reglas de Dependencias Automáticas

### **Dependencias Técnicas**
```python
dependencias = {
    "autenticación": ["base de datos", "modelos de usuario"],
    "APIs": ["modelos de datos", "validaciones"],
    "frontend": ["backend APIs", "autenticación"],
    "testing": ["funcionalidades core implementadas"],
    "deployment": ["testing completado", "configuración de entorno"]
}
```

### **Dependencias de Dominio**
```python
# E-commerce
if dominio == "ecommerce":
    dependencias.update({
        "carrito": ["productos", "usuarios"],
        "checkout": ["carrito", "pagos", "inventario"],
        "admin": ["productos", "usuarios", "órdenes"]
    })

# SaaS Dashboard  
if dominio == "dashboard":
    dependencias.update({
        "analytics": ["datos de usuario", "métricas"],
        "reportes": ["analytics", "permisos"],
        "billing": ["usuarios", "planes", "pagos"]
    })
```

## Criterios de División/Fusión de Fases

### **Dividir una fase si:**
- Más de 15 tareas en una sola fase
- Múltiples tecnologías/skillsets diferentes
- Dependencias internas complejas
- Estimación > 2-3 semanas para usuario promedio

### **Fusionar fases si:**
- Menos de 5 tareas por fase
- Misma tecnología y contexto
- Dependencias muy acopladas
- Fases demasiado granulares para el usuario

## Personalización por Stack Tecnológico

### **React/Node.js Stack**
```python
if stack.includes("react", "node"):
    fases_especificas = [
        "Setup de monorepo (frontend + backend)",
        "Componentes React y diseño system",
        "APIs Node.js y base de datos",
        "Integración frontend-backend",
        "Testing y deployment fullstack"
    ]
```

### **Python/Django Stack**
```python
if stack.includes("python", "django"):
    fases_especificas = [
        "Proyecto Django y modelos",
        "Views y templates/API serializers", 
        "Autenticación y permisos Django",
        "Frontend integration (si aplica)",
        "Deploy con gunicorn/nginx"
    ]
```

## Validación de Fases Generadas

### **Criterios de Calidad**
- [ ] Cada fase tiene un objetivo claro y medible
- [ ] Las dependencias son técnicamente correctas
- [ ] El número de tareas está balanceado (5-12 por fase)
- [ ] Los riesgos son específicos al contexto del proyecto
- [ ] Los entregables son concretos y verificables

### **Red Flags para Regeneración**
- Fases con contenido genérico ("implementar funcionalidad")
- Dependencias circulares o inconsistentes
- Desequilibrio extremo en número de tareas
- Falta de coherencia técnica entre objetivos

---
*Reglas de generación inteligente • Framework stepwise-planner*  
*Algoritmos de Claude Code para adaptación contextual*