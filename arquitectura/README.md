# Arquitectura del Sistema

Esta carpeta organiza la documentación arquitectónica del proyecto, desde diseño de alto nivel hasta decisiones técnicas específicas.

## Estructura

### Archivos Principales
- **TEMPLATE.md**: Plantilla para documentar la visión arquitectónica completa
- **README.md**: Esta guía de uso

### Subcarpetas Especializadas

#### `/system-design/`
Diseño de alto nivel del sistema: diagramas de arquitectura, componentes principales, interacciones entre servicios

#### `/patterns/`
Patrones arquitectónicos utilizados: MVC, microservicios, event-driven, CQRS, etc.

#### `/security/`
Arquitectura de seguridad: autenticación, autorización, encriptación, threat model

#### `/data-flow/`
Flujo de datos en el sistema: diagramas de secuencia, mapeo de datos, integraciones

## Cuándo Usar Cada Estructura

### Proyectos Simples
Usa solo `TEMPLATE.md` en la raíz para documentar toda la arquitectura en un archivo.

### Proyectos Complejos
Utiliza las subcarpetas para organizar por dominio arquitectónico:
- **system-design/**: Para diagramas C4, vistas arquitectónicas
- **patterns/**: Para documentar patrones específicos implementados
- **security/**: Para arquitectura de seguridad y compliance
- **data-flow/**: Para modelado de datos y flujos de información

## Tipos de Documentación

### Diagramas Recomendados
- **C4 Model**: Context, Containers, Components, Code
- **Sequence Diagrams**: Flujos de interacción
- **Entity Relationship**: Modelo de datos
- **Network Diagrams**: Topología de red
- **Deployment Diagrams**: Arquitectura de despliegue

### Vistas Arquitectónicas
- **Vista Lógica**: Estructura del software
- **Vista de Desarrollo**: Organización del código
- **Vista de Procesos**: Comportamiento en runtime
- **Vista Física**: Mapeo a hardware
- **Vista de Escenarios**: Casos de uso críticos

## Herramientas Recomendadas

### Diagramas
- **Mermaid**: Para diagramas en markdown
- **Draw.io/Lucidchart**: Para diagramas complejos
- **PlantUML**: Para diagramas como código
- **Figma/Sketch**: Para diseño de UI/UX

### Documentación
- **ADRs**: Para decisiones arquitectónicas importantes
- **C4 Model**: Para documentación arquitectónica estructurada
- **Swagger/OpenAPI**: Para documentación de APIs

## Flujo de Trabajo

1. **Análisis**: Define requisitos y restricciones
2. **Diseño**: Crea vistas arquitectónicas principales
3. **Validación**: Revisa con stakeholders técnicos
4. **Documentación**: Actualiza templates y diagramas
5. **ADRs**: Documenta decisiones importantes
6. **Evolución**: Actualiza conforme el sistema evoluciona

## Relación con Otras Secciones

- **Stack Tecnológico**: La arquitectura guía las decisiones del stack
- **ADRs**: Las decisiones arquitectónicas se documentan como ADRs
- **Fases**: Cada fase puede introducir cambios arquitectónicos
- **Riesgos**: Los riesgos arquitectónicos se documentan en las fases

## Quality Gates

### Revisiones Arquitectónicas
- **Inicio de proyecto**: Revisión de diseño inicial
- **Cada fase mayor**: Validación de cambios arquitectónicos
- **Pre-producción**: Revisión de readiness arquitectónico
- **Post-mortem**: Análisis de decisiones arquitectónicas

### Criterios de Calidad
- **Escalabilidad**: Sistema soporta crecimiento esperado
- **Mantenibilidad**: Código y arquitectura son mantenibles
- **Seguridad**: Controles de seguridad apropiados
- **Performance**: Cumple con SLAs definidos
- **Reliability**: Sistema es confiable y resiliente

---
*Parte del framework stepwise-planner*