# Sistema de Fases Dinámicas

Este directorio contiene las fases del proyecto que se generan dinámicamente basándose en las necesidades específicas de tu proyecto.

## ¿Cómo Funciona?

A diferencia de sistemas tradicionales con fases predefinidas, este framework genera fases **a medida** según tu proyecto:

1. **Describes tu proyecto** → "Quiero crear una API REST para gestión de inventarios"
2. **Claude Code analiza** → Identifica patrones, tecnologías y complejidad
3. **Se generan fases específicas** → Solo las fases que necesitas, con contenido relevante
4. **Trabajas iterativamente** → Cada fase tiene objetivos, tareas y entregables concretos

## Estructura del Directorio

```
fases/
├── README.md          # Esta guía (siempre presente)
├── TEMPLATE/          # Plantillas base para generar nuevas fases
├── roadmap.md         # Vista general del plan de desarrollo
├── generation-rules.md # Reglas para la generación automática
└── [fases generadas] # Se crean dinámicamente según tu proyecto
    ├── fase-01/       # Primera fase de tu proyecto específico
    ├── fase-02/       # Segunda fase, etc.
    └── ...
```

## Estado Actual

**📋 Fases activas:** Ninguna (proyecto sin inicializar)  
**🚀 Para comenzar:** Describe tu proyecto a Claude Code

## Comandos Útiles

### Inicialización
```
"Claude, quiero crear un [tipo de aplicación] que haga [funcionalidad principal]"
"Inicializa un proyecto de [descripción]"
```

### Gestión de Fases
```
"Crea una nueva fase para [objetivo específico]"
"Muestra el estado de todas las fases"
"Actualiza el roadmap con el progreso actual"
"Divide la fase-02 en dos fases más pequeñas"
```

### Seguimiento
```
"¿Cuál es el progreso general del proyecto?"
"¿Qué tareas están bloqueadas?"
"Genera un reporte de estado"
```

## Ventajas del Sistema Dinámico

### ✅ Lo que SÍ obtienes
- **Fases 100% relevantes** a tu proyecto específico
- **Sin documentación genérica** que no aplique
- **Adaptación automática** según tecnologías elegidas
- **Granularidad apropiada** para tu nivel de experiencia
- **Dependencias reales** entre fases

### ❌ Lo que evitas
- Fases predefinidas que no encajan
- Documentación que debes adaptar manualmente
- Pasos innecesarios para tu tipo de proyecto
- Rigidez en el proceso de desarrollo

## Ejemplos de Fases Generadas

### Para una API REST con Node.js
```
fase-01/ → Setup inicial y modelos de datos
fase-02/ → Endpoints básicos y validaciones
fase-03/ → Autenticación y autorización
fase-04/ → Testing y documentación
```

### Para una App Mobile React Native
```
fase-01/ → Configuración del proyecto y navegación
fase-02/ → Pantallas principales y componentes
fase-03/ → Integración con APIs
fase-04/ → Optimización y deployment
```

### Para un Dashboard Web
```
fase-01/ → Setup de frontend y componentes base
fase-02/ → Integración de datos y gráficos
fase-03/ → Funcionalidades de usuario
fase-04/ → Performance y responsividad
```

## Filosofía del Framework

> **"Las herramientas deben adaptarse a tu proyecto, no al revés"**

Este sistema reconoce que cada proyecto es único y merece un plan de desarrollo específico, no un molde genérico.

## Primeros Pasos

1. **Describe tu proyecto** a Claude Code con el máximo detalle posible
2. **Responde las preguntas** que Claude te haga para clarificar aspectos técnicos
3. **Revisa las fases propuestas** y ajusta si es necesario
4. **¡Comienza a desarrollar!** siguiendo el plan generado

---
*Sistema de fases dinámicas • Framework stepwise-planner*  
*Generación inteligente basada en Claude Code*