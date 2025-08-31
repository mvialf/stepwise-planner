# Variables para Templates Dinámicos

Este archivo documenta las variables que Claude Code debe sustituir cuando genera fases dinámicamente.

## Variables Globales del Proyecto

### Información Básica
- `{{PROYECTO_NOMBRE}}` - Nombre del proyecto
- `{{PROYECTO_TIPO}}` - Tipo de proyecto (API REST, App Web, Mobile App, CLI Tool, etc.)
- `{{PROYECTO_DESCRIPCION}}` - Descripción breve del propósito del proyecto

### Stack Tecnológico
- `{{TECNOLOGIAS_PRINCIPALES}}` - Stack principal (ej: "React + Node.js + MongoDB")
- `{{FRONTEND_TECH}}` - Tecnologías frontend específicas
- `{{BACKEND_TECH}}` - Tecnologías backend específicas
- `{{DATABASE_TECH}}` - Base de datos elegida
- `{{DEPLOYMENT_TECH}}` - Plataforma de deployment

## Variables Específicas de Fase

### Identificación de Fase
- `{{FASE_NUMERO}}` - Número de la fase (01, 02, 03, etc.)
- `{{FASE_NOMBRE}}` - Nombre descriptivo de la fase
- `{{OBJETIVO_FASE_BREVE}}` - Resumen del objetivo en 1 línea

### Contexto en el Roadmap
- `{{POSICION_EN_ROADMAP}}` - Descripción de dónde encaja esta fase
- `{{DEPENDENCIAS_FASE_ANTERIOR}}` - Qué se necesita de la fase anterior
- `{{HABILITA_FASE_SIGUIENTE}}` - Qué posibilita para la siguiente fase

## Variables de Objetivos

### Objetivo Principal
- `{{OBJETIVO_PRINCIPAL}}` - Descripción completa del objetivo principal

### Objetivos Específicos (Lista)
```
{{#OBJETIVOS_ESPECIFICOS}}
  {{NUMERO}} - Número del objetivo (1, 2, 3...)
  {{NOMBRE}} - Nombre del objetivo específico
  {{DESCRIPCION}} - Descripción detallada
  {{CRITERIO_EXITO}} - Cómo saber que se completó
  {{METRICA}} - Métrica medible si aplica
  {{PRIORIDAD}} - Alta/Media/Baja
  {{TECNOLOGIAS_RELACIONADAS}} - Stack específico para este objetivo
{{/OBJETIVOS_ESPECIFICOS}}
```

### Criterios de Completitud (Lista)
```
{{#CRITERIOS_COMPLETITUD}}
  {{NOMBRE}} - Nombre del criterio
  {{DESCRIPCION}} - Descripción específica del criterio
{{/CRITERIOS_COMPLETITUD}}
```

## Variables de Tareas

### Información General
- `{{TOTAL_TAREAS}}` - Número total de tareas en la fase

### Categorías de Tareas (Lista)
```
{{#CATEGORIAS_TAREAS}}
  {{EMOJI}} - Emoji representativo (🏗️, 💻, 🧪, 📚, etc.)
  {{NOMBRE_CATEGORIA}} - Nombre de la categoría
  {{TAREAS}} - Lista de tareas en esta categoría
{{/CATEGORIAS_TAREAS}}
```

### Tareas Individuales (Lista anidada)
```
{{#TAREAS}}
  {{ID}} - Identificador único (T01, T02, etc.)
  {{NOMBRE}} - Nombre de la tarea
  {{DESCRIPCION}} - Descripción detallada de qué hacer
  {{TECNOLOGIAS_ESPECIFICAS}} - Stack específico para esta tarea
  {{ESFUERZO}} - S/M/L/XL
  {{JUSTIFICACION_ESFUERZO}} - Por qué tiene esa estimación
  {{DEPENDENCIAS}} - Qué debe completarse antes
  {{RECURSOS_UTILES}} - Links, docs, tutoriales relevantes
{{/TAREAS}}
```

## Variables de Testing

- `{{TIPO_TESTING_REQUERIDO}}` - Tipo de testing apropiado para el proyecto
  - Ejemplos: "Unit tests con Jest", "E2E con Cypress", "API tests con Postman"

## Variables de Riesgos

### Riesgos Específicos (Lista)
```
{{#RIESGOS_ESPECIFICOS}}
  {{NOMBRE_RIESGO}} - Nombre del riesgo
  {{DESCRIPCION}} - Descripción del riesgo
  {{PROBABILIDAD}} - Alta/Media/Baja
  {{IMPACTO}} - Alto/Medio/Bajo  
  {{MITIGACION}} - Estrategia específica de mitigación
  {{TECNOLOGIA_RELACIONADA}} - Stack que causa este riesgo
{{/RIESGOS_ESPECIFICOS}}
```

## Variables de Entregables

### Entregables Principales (Lista)
```
{{#ENTREGABLES_PRINCIPALES}}
  {{NOMBRE}} - Nombre del entregable
  {{DESCRIPCION}} - Qué incluye exactamente
  {{CRITERIOS_ACEPTACION}} - Criterios específicos de aceptación
  {{FORMATO}} - Formato del entregable (código, docs, deployment, etc.)
{{/ENTREGABLES_PRINCIPALES}}
```

## Ejemplos de Sustitución

### Para una API REST con Node.js:
```
{{PROYECTO_TIPO}} → "API REST"
{{TECNOLOGIAS_PRINCIPALES}} → "Node.js + Express + MongoDB"
{{TIPO_TESTING_REQUERIDO}} → "Unit tests con Jest y API tests con Supertest"
```

### Para una App Mobile con React Native:
```
{{PROYECTO_TIPO}} → "Aplicación Mobile"
{{TECNOLOGIAS_PRINCIPALES}} → "React Native + Firebase"
{{TIPO_TESTING_REQUERIDO}} → "Component tests con React Native Testing Library"
```

## Notas para Claude Code

### Sustitución Inteligente
- Usa Context7 para obtener información actualizada sobre tecnologías mencionadas
- Genera contenido específico basado en el stack tecnológico
- Adapta el lenguaje técnico al nivel de experiencia detectado
- Incluye recursos y referencias específicas a las tecnologías elegidas

### Validación de Variables
- Verifica que todas las variables tengan valores apropiados
- No uses placeholders genéricos si puedes inferir contenido específico
- Asegúrate de que las tecnologías mencionadas sean consistentes entre archivos

---
*Guía de variables para generación dinámica de contenido*  
*Framework stepwise-planner • Templates adaptativos*