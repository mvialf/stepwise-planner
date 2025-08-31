# Frontend Stack: [Nombre del Proyecto]

**Última actualización:** YYYY-MM-DD  
**Responsable:** [Nombre del Frontend Lead]

## Resumen del Frontend

[Descripción de la arquitectura frontend y experiencia de usuario objetivo]

## Stack Principal

### Framework y Runtime
| Tecnología | Versión | Propósito | Estado |
|------------|---------|-----------|---------|
| [React/Vue/Angular] | vX.X | Framework principal | ✅ |
| [TypeScript] | vX.X | Tipado estático | ✅ |
| [Node.js] | vX.X | Runtime de desarrollo | ✅ |

### Build Tools y Bundling
| Tecnología | Versión | Propósito | Estado |
|------------|---------|-----------|---------|
| [Vite/Webpack/Parcel] | vX.X | Build tool principal | ✅ |
| [ESLint] | vX.X | Linting | ✅ |
| [Prettier] | vX.X | Code formatting | ✅ |

## UI y Styling

### Sistema de Componentes
- **Librería base:** [Material-UI/Ant Design/Chakra/Custom]
- **Design system:** [Propio/Existente]
- **Storybook:** [Sí/No]

### Estrategia de Styling
```css
/* Enfoque elegido */
Approach: [CSS Modules/Styled Components/Tailwind/SCSS]
```

| Tecnología | Versión | Propósito |
|------------|---------|-----------|
| [Styled-components/Emotion] | vX.X | CSS-in-JS |
| [Tailwind] | vX.X | Utility CSS |
| [PostCSS] | vX.X | CSS processing |

### Responsividad
- **Breakpoints:** [Mobile-first/Desktop-first]
- **Grid system:** [CSS Grid/Flexbox/Framework]
- **Dispositivos objetivo:** [Lista de dispositivos]

## Estado y Data Management

### Gestión de Estado
| Tecnología | Versión | Propósito |
|------------|---------|-----------|
| [Redux/Zustand/Pinia] | vX.X | Estado global |
| [React Query/SWR] | vX.X | Server state |
| [Context API/Vuex] | vX.X | Estado local |

### Arquitectura de Estado
```javascript
// Estructura del estado
{
  user: { ... },
  ui: { ... },
  data: { ... },
  cache: { ... }
}
```

## Comunicación con API

### Cliente HTTP
```javascript
// Configuración del cliente
const apiClient = axios.create({
  baseURL: process.env.REACT_APP_API_URL,
  timeout: 10000,
  headers: {
    'Content-Type': 'application/json'
  }
})
```

### Data Fetching Strategy
- **Librería:** [Axios/Fetch/Apollo Client]
- **Caching:** [React Query/SWR/Apollo Cache]
- **Error handling:** [Global/Component level]
- **Loading states:** [Global/Local]

## Routing y Navegación

### Router Configuration
| Tecnología | Versión | Propósito |
|------------|---------|-----------|
| [React Router/Vue Router] | vX.X | Client-side routing |

```javascript
// Estructura de rutas
/                    // Home
/auth/login         // Autenticación
/dashboard          // Dashboard principal
/[feature]/         // Features específicas
/admin/*            // Rutas admin
```

### Navegación y UX
- **Lazy loading:** [Sí/No - estrategia]
- **Code splitting:** [Por ruta/Por feature]
- **Breadcrumbs:** [Sí/No]
- **Back navigation:** [Historia/Estado]

## Testing

### Estrategia de Testing Frontend
| Tipo | Framework | Coverage Target |
|------|-----------|-----------------|
| Unitarios | [Jest/Vitest] | >80% |
| Componentes | [Testing Library] | >70% |
| E2E | [Cypress/Playwright] | Flujos críticos |
| Visual | [Chromatic/Percy] | Componentes clave |

### Configuración de Tests
```bash
# Scripts de testing
npm run test              # Unitarios
npm run test:components   # Testing de componentes
npm run test:e2e         # End-to-end
npm run test:visual      # Visual regression
```

## Performance

### Métricas Objetivo
- **First Contentful Paint:** < 1.5s
- **Largest Contentful Paint:** < 2.5s
- **Time to Interactive:** < 3s
- **Cumulative Layout Shift:** < 0.1
- **Bundle size:** < 250KB (gzipped)

### Optimizaciones
- [ ] **Code splitting:** Por rutas y componentes
- [ ] **Lazy loading:** Imágenes y componentes
- [ ] **Tree shaking:** Eliminación de código muerto
- [ ] **Bundle analysis:** Análisis regular del bundle
- [ ] **Image optimization:** Formatos modernos (WebP, AVIF)
- [ ] **Caching strategy:** Service workers/HTTP caching

## Accesibilidad

### Estándares
- **WCAG Level:** [A/AA/AAA]
- **Testing:** [axe-core/Manual testing]
- **Screen readers:** [Compatibilidad verificada]

### Checklist A11y
- [ ] Semantic HTML
- [ ] Keyboard navigation
- [ ] Focus management
- [ ] Alt text para imágenes
- [ ] Color contrast ratio
- [ ] Screen reader labels

## Estructura del Proyecto

```
frontend/
├── public/
│   ├── index.html
│   └── assets/
├── src/
│   ├── components/      # Componentes reutilizables
│   │   ├── common/     # Componentes base
│   │   └── ui/         # Componentes UI específicos
│   ├── pages/          # Componentes de página
│   ├── hooks/          # Custom hooks
│   ├── services/       # API calls y servicios
│   ├── store/          # Gestión de estado
│   ├── styles/         # Estilos globales
│   ├── types/          # Tipos TypeScript
│   ├── utils/          # Utilidades
│   └── __tests__/      # Tests
├── stories/            # Storybook stories
└── docs/              # Documentación
```

## Configuración por Entorno

### Development
```bash
REACT_APP_ENV=development
REACT_APP_API_URL=http://localhost:3001
REACT_APP_DEBUG=true
REACT_APP_ANALYTICS=false
```

### Production
```bash
REACT_APP_ENV=production
REACT_APP_API_URL=https://api.yourdomain.com
REACT_APP_DEBUG=false
REACT_APP_ANALYTICS=true
```

## Build y Deployment

### Build Configuration
```json
{
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview",
    "lint": "eslint src --ext ts,tsx",
    "type-check": "tsc --noEmit"
  }
}
```

### Static Assets
- **CDN:** [CloudFront/Cloudinary]
- **Images:** [Optimización automática]
- **Fonts:** [Google Fonts/Self-hosted]
- **Icons:** [SVG/Icon fonts]

## Progressive Web App (PWA)

### Características PWA
- [ ] **Service Worker:** Caching strategy
- [ ] **Web App Manifest:** Configurado
- [ ] **Offline support:** Páginas críticas
- [ ] **Install prompt:** Configurado
- [ ] **Push notifications:** [Sí/No]

## Monitoring y Analytics

### Herramientas
- **Analytics:** [Google Analytics/Mixpanel]
- **Error tracking:** [Sentry/Bugsnag]
- **Performance:** [Web Vitals/Lighthouse CI]
- **User feedback:** [Hotjar/FullStory]

### Métricas de Usuario
- **User flows:** [Flujos críticos monitoreados]
- **Conversion rates:** [Métricas de conversión]
- **Error rates:** [Threshold de errores]

## Browser Support

### Targets
```json
{
  "browserslist": [
    "> 1%",
    "last 2 versions",
    "not dead",
    "not ie 11"
  ]
}
```

### Polyfills
- **Core-js:** [Para funcionalidades ES6+]
- **Custom polyfills:** [Lista específica]

## Internacionalización (i18n)

### Strategy
- **Librería:** [react-i18next/vue-i18n]
- **Idiomas:** [Lista de idiomas soportados]
- **Fallback:** [Idioma por defecto]
- **Loading:** [Lazy loading de traducciones]

## Security

### Medidas Frontend
- [ ] **Content Security Policy:** Configurado
- [ ] **XSS Prevention:** Sanitización de inputs
- [ ] **HTTPS only:** Forzado en producción
- [ ] **Sensitive data:** No almacenado en localStorage
- [ ] **Dependencies:** Audit regular con npm audit

## ADRs Relacionados

- [ADR-XXX: Elección de Framework Frontend](../../adr/ADR-XXX.md)
- [ADR-XXX: Estrategia de Estado Global](../../adr/ADR-XXX.md)
- [ADR-XXX: Sistema de Diseño](../../adr/ADR-XXX.md)

---
*Template especializado para Frontend - stepwise-planner*