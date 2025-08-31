# Stack Tecnológico

Esta carpeta organiza las decisiones y documentación sobre las tecnologías utilizadas en el proyecto.

## Estructura

### Archivos Principales
- **TEMPLATE.md**: Plantilla para documentar el stack completo del proyecto
- **README.md**: Esta guía de uso

### Subcarpetas Especializadas

#### `/backend/`
Tecnologías del lado servidor: frameworks, APIs, servicios, middleware

#### `/frontend/`
Tecnologías del lado cliente: frameworks JS, librerías UI, herramientas de build

#### `/database/`
Sistemas de base de datos, ORMs, schemas, estrategias de datos

#### `/infrastructure/`
DevOps, cloud, contenedores, CI/CD, monitoreo, despliegue

#### `/tools/`
Herramientas de desarrollo, testing, debugging, análisis de código

## Cuándo Usar Cada Estructura

### Proyectos Simples
Usa solo `TEMPLATE.md` en la raíz para documentar todo el stack en un archivo.

### Proyectos Complejos
Utiliza las subcarpetas para organizar por dominio. Cada subcarpeta puede contener:
- Múltiples archivos `.md` por tecnología
- Su propio `TEMPLATE.md` especializado
- Diagramas y documentación técnica

## Flujo de Trabajo

1. **Planificación**: Define tecnologías usando templates
2. **Decisiones**: Documenta el POR QUÉ de cada elección
3. **Evolución**: Actualiza conforme el proyecto evoluciona
4. **ADRs**: Para decisiones importantes, crea ADRs relacionados

## Relación con Otras Secciones

- **ADRs**: Decisiones arquitectónicas importantes del stack
- **Fases**: Cada fase puede requerir tecnologías específicas
- **Arquitectura**: El stack debe alinearse con el diseño arquitectónico

---
*Parte del framework stepwise-planner*