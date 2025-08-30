# Architecture Decision Records (ADRs)

## ¿Qué es un ADR?

Un Architecture Decision Record documenta una decisión arquitectónica importante junto con su contexto y consecuencias. Captura el **POR QUÉ** detrás de las decisiones técnicas.

## ¿Cuándo crear un ADR?

Crea un ADR cuando tomes decisiones sobre:
- Elección de frameworks o librerías principales
- Patrones arquitectónicos (MVC, microservicios, etc.)
- Estrategias de autenticación/autorización
- Decisiones de base de datos
- Trade-offs técnicos significativos
- Cualquier decisión que afecte la estructura fundamental del proyecto

## Estructura de un ADR

Cada ADR sigue la plantilla en `TEMPLATE.md`:
- **Título**: ADR-XXX: Descripción breve
- **Estado**: Propuesto | Aceptado | Deprecado | Reemplazado
- **Contexto**: El problema o necesidad
- **Decisión**: Lo que se decidió hacer
- **Consecuencias**: Trade-offs, riesgos y beneficios
- **Alternativas**: Otras opciones consideradas

## Proceso

1. **Creación**: Cuando se toma una decisión arquitectónica importante
2. **Numeración**: Secuencial (ADR-001, ADR-002, etc.)
3. **Estado inicial**: "Propuesto"
4. **Aprobación**: Cambiar a "Aceptado" cuando se implemente
5. **Inmutabilidad**: Una vez aceptado, no modificar
6. **Evolución**: Si cambia la decisión, crear nuevo ADR que reemplace al anterior

## Principios

- **Concisos**: 1-2 páginas máximo
- **Inmutables**: No editar después de aceptados
- **Contextuales**: Explicar el "por qué", no solo el "qué"
- **Honestos**: Documentar trade-offs y riesgos
- **Trazables**: Referenciar ADRs relacionados

## Ejemplo de uso

```bash
# Cuando eliges React sobre Vue:
crear: adr/ADR-001-elegir-react-como-framework-frontend.md

# Si después cambias a Vue:
crear: adr/ADR-005-migrar-de-react-a-vue.md
actualizar ADR-001 estado: "Reemplazado por ADR-005"
```