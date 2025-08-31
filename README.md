# 🚀 Stepwise Planner

> **Framework inteligente de planificación de proyectos de software que genera fases dinámicas basadas en tu contexto específico**

[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](https://github.com/tuusuario/stepwise-planner)
[![Claude Code](https://img.shields.io/badge/powered%20by-Claude%20Code-orange.svg)](https://claude.ai/code)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

## 🎯 ¿Qué Problema Resuelve?

Los frameworks de planificación tradicionales te fuerzan a usar fases predefinidas que rara vez encajan con tu proyecto específico. **Stepwise Planner** genera fases completamente personalizadas según:

- 🔍 **Tu tipo de proyecto**: API, Web App, Mobile, CLI Tool
- ⚡ **Tu stack tecnológico**: React, Node.js, Python, Go, etc.
- 📊 **Tu nivel de complejidad**: Simple, medio, empresarial
- 👨‍💻 **Tu experiencia**: Principiante, intermedio, avanzado

## ✨ Características Principales

### 🧠 **Generación Dinámica de Fases**
No más fases genéricas. Cada fase se crea específicamente para tu proyecto con:
- Objetivos concretos y medibles
- Tareas técnicamente precisas 
- Dependencias reales (no inventadas)
- Riesgos específicos de tu stack

### 🤖 **Integración Nativa con Claude Code**
```bash
"Quiero crear una API REST para inventarios con Node.js y PostgreSQL"

# Claude Code automáticamente:
# ✅ Detecta: API + CRUD + autenticación probable
# ✅ Pregunta lo esencial: ¿JWT o sesiones? ¿Docker desde inicio?
# ✅ Genera 4 fases específicas con contenido 100% relevante
```

### 📋 **Documentación Como Código**
- Todo versionado en Git
- Markdown legible y editable
- Seguimiento de progreso automatizado
- ADRs para decisiones arquitectónicas

## 🚀 Quick Start

### Requisitos
- [Claude Code](https://claude.ai/code) instalado y configurado

### Inicializar tu primer proyecto
```bash
# 1. Clona o descarga este framework
git clone https://github.com/tuusuario/stepwise-planner.git mi-proyecto
cd mi-proyecto

# 2. Inicia Claude Code
claude

# 3. Describe tu proyecto
"Quiero crear una tienda online con React, autenticación y pagos con Stripe"
```

**¡Listo!** Claude Code generará automáticamente las fases específicas para tu e-commerce.

## 🔄 Cómo Funciona

```
📝 Describes tu proyecto
    ↓
🧠 Claude Code analiza contexto
    ↓  
❓ Hace preguntas específicas (solo lo esencial)
    ↓
⚡ Genera fases dinámicas
    ↓
📁 Crea estructura completa de archivos
    ↓
🎯 ¡Empiezas a desarrollar con plan específico!
```

### Ejemplo de Flujo Real

```
Usuario: "API REST para gestión de tareas con FastAPI"

Claude: "Perfecto. Para generar las fases apropiadas:
- ¿Base de datos relacional (PostgreSQL) o NoSQL (MongoDB)?
- ¿Autenticación JWT o simple API keys?
- ¿Necesitas notificaciones por email?"

[30 segundos después...]

✅ fase-01: Setup FastAPI y modelos Pydantic
✅ fase-02: CRUD endpoints con SQLAlchemy  
✅ fase-03: Sistema JWT y middleware de auth
✅ fase-04: Testing con pytest y deployment
```

## 📁 Estructura del Framework

```
stepwise-planner/
├── 📋 fases/                    # Sistema de fases dinámicas
│   ├── README.md               # Guía del sistema dinámico
│   ├── TEMPLATE/               # Templates para generación
│   ├── generation-rules.md     # Heurísticas de IA
│   ├── roadmap.md             # Roadmap actualizable
│   └── [fases generadas]      # Se crean según tu proyecto
│
├── 📄 proyecto/                # Información del proyecto
│   ├── README.md              # Contexto y descripción
│   └── setup-wizard.md        # Flujo de inicialización
│
├── 🏗️ arquitectura/           # Diseño técnico
├── 🛠️ stack-tecnologico/     # Tecnologías elegidas  
├── 💡 futuras-ideas/          # Ideas para próximas fases
├── ❌ ideas-bloqueadas/       # Ideas descartadas (con razones)
├── 📜 adr/                    # Architecture Decision Records
└── 🤖 claude.md              # Configuración de comportamiento
```

## 🎮 Comandos Principales

### Inicialización
```bash
"Claude, quiero crear [descripción del proyecto]"
"Inicializa un proyecto de [tipo] con [tecnologías]"
```

### Gestión de Fases
```bash
"Crea una nueva fase para [objetivo específico]"
"Divide la fase-02 en dos fases más pequeñas" 
"Fusiona fase-03 y fase-04"
"Muestra el progreso actual del proyecto"
```

### Seguimiento
```bash
"Actualiza las métricas del proyecto"
"¿Qué tareas están bloqueadas?"
"Genera reporte de estado completo"
```

## 💼 Ejemplos de Proyectos Generados

### 🌐 **E-commerce con React + Node.js**
```
fase-01: Setup fullstack y componentes base
fase-02: Catálogo de productos y carrito
fase-03: Sistema de usuarios y checkout  
fase-04: Integración Stripe y deployment
fase-05: Admin dashboard y analytics
```

### 📱 **App Mobile con React Native**
```
fase-01: Setup RN y navegación
fase-02: Pantallas principales y UI
fase-03: Estado global y async storage
fase-04: Integración con APIs
fase-05: Features nativas y store deployment
```

### 🔧 **CLI Tool con Go**
```
fase-01: Core CLI y parsing de argumentos
fase-02: Subcomandos principales
fase-03: Configuración y plugins
fase-04: Testing y distribución
```

### 🚀 **Microservicio con Docker + K8s**
```
fase-01: API base y containerización
fase-02: Base de datos y persistencia
fase-03: Observabilidad (logs, métricas, traces)
fase-04: CI/CD y deployment a K8s
fase-05: Scaling y optimización
```

## 🎯 Filosofía: ¿Por Qué Stepwise Planner?

### ❌ **Problema con Métodos Tradicionales**
```
Metodologías rígidas:
├── Fases predefinidas que no encajan
├── Documentación genérica a adaptar
├── Estimaciones poco realistas
└── Overhead innecesario
```

### ✅ **Nuestra Solución: Fases Adaptativas**
```
Generación inteligente:
├── 100% específico a tu proyecto
├── Basado en tu stack real
├── Ajustado a tu experiencia
└── Sin contenido irrelevante
```

### 🧠 **Principios Core**

1. **🎯 Context Over Convention**: Tu proyecto dicta la estructura, no viceversa
2. **⚡ Specific Over Generic**: Contenido técnicamente preciso vs plantillas genéricas
3. **🤖 AI-Assisted Planning**: La IA reduce fricción, no la elimina
4. **📝 Documentation as Code**: Todo versionado, auditable, colaborativo

## 🛠️ Personalización y Extensión

### Modificar Templates
```bash
# Edita los templates base
vi fases/TEMPLATE/objetivos.md
vi fases/TEMPLATE/tareas.md

# Las variables {{NOMBRE}} se sustituyen automáticamente
```

### Agregar Nuevos Patrones
```bash
# Modifica las reglas de generación
vi fases/generation-rules.md

# Agrega patrones para nuevos tipos de proyecto
```

### Comandos Personalizados
```bash
# Crea comandos específicos en .claude/commands/
vi .claude/commands/mi-comando.md
```

## 🤔 FAQ

### **¿Funciona sin Claude Code?**
El framework es útil manualmente, pero la generación dinámica requiere Claude Code.

### **¿Puedo usar otros LLMs?**
Los templates son estándar Markdown. Adaptar a otros LLMs requiere modificar `claude.md`.

### **¿Escala a proyectos grandes?**
Sí. Ajusta automáticamente la granularidad según complejidad detectada.

### **¿Qué pasa si cambio de tecnología?**
Crea un ADR documentando el cambio y regenera las fases afectadas.

### **¿Funciona para equipos?**
Optimizado para desarrollo individual. Para equipos, considera agregar roles y asignaciones.

## 🚧 Limitaciones Conocidas

- Optimizado para proyectos de desarrollo individual
- Requiere Claude Code para funcionalidad completa
- Generación inicial puede requerir varias iteraciones para proyectos muy específicos
- No incluye estimaciones de tiempo (por diseño - cada desarrollador es diferente)

## 🤝 Contribuir

```bash
# 1. Fork del repositorio
# 2. Crea una rama para tu feature
git checkout -b feature/nuevo-patron-proyecto

# 3. Agrega tu patrón a generation-rules.md
# 4. Testea con proyectos reales
# 5. Crea PR con ejemplos de uso
```

### Áreas que Necesitan Contribuciones
- Patrones para nuevos stacks (Rust, Flutter, Vue, etc.)
- Templates específicos por industria
- Integraciones con otras herramientas de desarrollo
- Métricas automáticas de progreso

## 📜 Licencia

MIT License - Úsalo, modifícalo y compártelo libremente.

---

**¿Listo para planificar tu próximo proyecto de forma inteligente?**

```bash
git clone https://github.com/tuusuario/stepwise-planner.git
cd stepwise-planner
claude

# Luego simplemente describe tu proyecto 🚀
```

---
*Hecho con ❤️ para desarrolladores que quieren planificar menos y construir más*