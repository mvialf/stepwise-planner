# Development Tools: [Nombre del Proyecto]

**Última actualización:** YYYY-MM-DD  
**Responsable:** [Tech Lead/Team Lead]

## Resumen de Herramientas

[Descripción del ecosistema de herramientas de desarrollo y su filosofía]

## IDE y Editores

### IDE Principal
| Herramienta | Versión | Propósito | Team Usage |
|-------------|---------|-----------|------------|
| [VS Code/IntelliJ/etc.] | vX.X | IDE principal | 90% |
| [Secondary IDE] | vX.X | Alternativo | 10% |

### Configuración Compartida
```json
// .vscode/settings.json
{
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "typescript.preferences.importModuleSpecifier": "relative"
}
```

### Extensiones Requeridas
- **ESLint:** Code linting
- **Prettier:** Code formatting  
- **GitLens:** Git integration
- **Thunder Client/REST Client:** API testing
- **[Framework-specific]:** [React/Vue/Angular tools]

## Version Control

### Git Configuration
```bash
# Git hooks instalados
pre-commit: lint + format check
pre-push: tests + build check
commit-msg: conventional commit format
```

### Branch Strategy
```
main           # Production branch
├── develop    # Integration branch  
├── feature/*  # Feature branches
├── bugfix/*   # Bug fix branches
├── hotfix/*   # Emergency fixes
└── release/*  # Release branches
```

### Commit Conventions
```bash
# Conventional commits
feat: add user authentication
fix: resolve login redirect issue  
docs: update API documentation
style: format code with prettier
refactor: extract validation logic
test: add unit tests for auth service
chore: update dependencies
```

## Code Quality

### Linting y Formatting
| Herramienta | Versión | Configuración |
|-------------|---------|---------------|
| [ESLint/TSLint] | vX.X | .eslintrc.json |
| [Prettier] | vX.X | .prettierrc |
| [StyleLint] | vX.X | .stylelintrc |

### Code Analysis
```yaml
# SonarQube/CodeClimate config
coverage_threshold: 80%
maintainability_grade: A
reliability_grade: A  
security_grade: A
```

### Pre-commit Hooks
```bash
#!/bin/sh
# pre-commit hook
npm run lint
npm run type-check
npm run test:staged
npm run build
```

## Testing Tools

### Testing Stack
| Herramienta | Versión | Propósito | Coverage |
|-------------|---------|-----------|----------|
| [Jest/Vitest] | vX.X | Unit testing | 80%+ |
| [Cypress/Playwright] | vX.X | E2E testing | Critical flows |
| [Testing Library] | vX.X | Component testing | 70%+ |
| [Storybook] | vX.X | Component showcase | Major components |

### Test Configuration
```javascript
// jest.config.js
module.exports = {
  collectCoverageFrom: [
    'src/**/*.{js,jsx,ts,tsx}',
    '!src/**/*.d.ts',
    '!src/index.tsx'
  ],
  coverageThreshold: {
    global: {
      branches: 75,
      functions: 75,
      lines: 80,
      statements: 80
    }
  }
}
```

## Package Management

### Package Manager
| Herramienta | Versión | Propósito |
|-------------|---------|-----------|
| [npm/yarn/pnpm] | vX.X | Dependencies |
| [Volta/nvm] | vX.X | Node version |

### Dependency Management
```json
// package.json scripts
{
  "scripts": {
    "dev": "next dev",
    "build": "next build", 
    "start": "next start",
    "lint": "eslint . --ext .ts,.tsx",
    "lint:fix": "eslint . --ext .ts,.tsx --fix",
    "type-check": "tsc --noEmit",
    "test": "jest",
    "test:watch": "jest --watch",
    "test:coverage": "jest --coverage"
  }
}
```

### Security Scanning
```bash
# Regular security checks
npm audit
yarn audit
snyk test
```

## Build Tools

### Build System
| Herramienta | Versión | Propósito |
|-------------|---------|-----------|
| [Webpack/Vite/Rollup] | vX.X | Bundling |
| [Babel/SWC] | vX.X | Transpiling |
| [PostCSS] | vX.X | CSS processing |

### Build Configuration
```javascript
// webpack.config.js / vite.config.js
export default {
  build: {
    target: 'es2020',
    sourcemap: true,
    rollupOptions: {
      output: {
        manualChunks: {
          vendor: ['react', 'react-dom'],
          utils: ['lodash', 'date-fns']
        }
      }
    }
  }
}
```

## Debugging Tools

### Browser DevTools
- **React DevTools:** Component inspection
- **Vue DevTools:** Vue-specific debugging
- **Redux DevTools:** State debugging
- **Network tab:** API monitoring
- **Performance tab:** Performance profiling

### Node.js Debugging
```bash
# Debug configurations
node --inspect-brk src/index.js
npm run debug
# VS Code launch configurations
```

### API Testing
| Herramienta | Versión | Propósito |
|-------------|---------|-----------|
| [Postman/Insomnia] | vX.X | API testing |
| [Thunder Client] | vX.X | VS Code integrated |
| [curl/httpie] | - | Command line |

## Documentation Tools

### Documentation Stack
| Herramienta | Versión | Propósito |
|-------------|---------|-----------|
| [Storybook] | vX.X | Component docs |
| [JSDoc/TSDoc] | vX.X | Code documentation |
| [Swagger/OpenAPI] | vX.X | API documentation |
| [Docusaurus/GitBook] | vX.X | Project docs |

### Documentation Standards
```javascript
/**
 * Calculates user permissions based on role
 * @param {User} user - The user object
 * @param {string} resource - Resource identifier  
 * @returns {Permission[]} Array of permissions
 * @example
 * const permissions = calculatePermissions(user, 'posts')
 */
function calculatePermissions(user, resource) {
  // implementation
}
```

## Performance Tools

### Monitoring y Profiling
| Herramienta | Versión | Propósito |
|-------------|---------|-----------|
| [Lighthouse] | - | Web performance |
| [Web Vitals] | vX.X | Core metrics |
| [Bundle Analyzer] | vX.X | Bundle analysis |
| [Chrome DevTools] | - | Performance profiling |

### Performance Budgets
```json
// performance-budget.json
{
  "budget": [
    {
      "resourceSizes": [
        {"resourceType": "script", "maximumSizeInBytes": 250000},
        {"resourceType": "total", "maximumSizeInBytes": 500000}
      ]
    }
  ]
}
```

## Database Tools

### Database Management
| Herramienta | Versión | Propósito |
|-------------|---------|-----------|
| [TablePlus/DBeaver] | vX.X | GUI client |
| [pgAdmin/phpMyAdmin] | vX.X | Web interface |
| [CLI tools] | - | Command line |

### Migration Tools
```bash
# Database migration commands
npm run migrate:dev
npm run migrate:reset  
npm run migrate:deploy
npm run seed:dev
```

## Collaboration Tools

### Communication
| Herramienta | Propósito | Usage |
|-------------|-----------|-------|
| [Slack/Discord] | Team communication | Daily |
| [Zoom/Meet] | Video meetings | As needed |
| [Linear/Jira] | Project management | Sprint planning |

### Code Review
```yaml
# GitHub/GitLab PR template
## Changes
- [ ] Feature implementation
- [ ] Tests added/updated  
- [ ] Documentation updated
- [ ] No breaking changes

## Checklist
- [ ] Code follows style guide
- [ ] Tests pass
- [ ] No console.log statements
- [ ] Performance impact considered
```

## Environment Management

### Environment Variables
```bash
# .env.example
NODE_ENV=development
DATABASE_URL=postgresql://localhost:5432/myapp
API_KEY=your_api_key_here
REDIS_URL=redis://localhost:6379
```

### Secrets Management
| Herramienta | Propósito |
|-------------|-----------|
| [dotenv] | Local development |
| [Vault/AWS Secrets] | Production secrets |
| [1Password/Bitwarden] | Team secrets |

## Automation Scripts

### Development Scripts
```bash
#!/bin/bash
# scripts/setup.sh
echo "Setting up development environment..."
npm install
cp .env.example .env.local
docker-compose up -d
npm run migrate:dev
npm run seed:dev
echo "Setup complete! Run 'npm run dev' to start."
```

### Useful Aliases
```bash
# .bashrc / .zshrc aliases
alias ll='ls -la'
alias gst='git status'
alias gco='git checkout'
alias gp='git push'
alias gl='git pull'
alias nr='npm run'
alias ys='yarn start'
```

## Health Checks y Monitoring

### Local Development
```bash
# Health check script
#!/bin/bash
echo "Checking development environment..."
node --version
npm --version  
docker --version
psql --version
redis-cli ping
```

### Development Metrics
- **Build time:** < 30 seconds
- **Hot reload:** < 2 seconds
- **Test execution:** < 5 minutes
- **Startup time:** < 10 seconds

## Team Conventions

### Code Standards
```javascript
// Naming conventions
const userName = 'john_doe';     // variables: camelCase
const MAX_RETRY_COUNT = 3;       // constants: UPPER_SNAKE_CASE  
function getUserData() {}        // functions: camelCase
class UserService {}             // classes: PascalCase
```

### File Organization
```
src/
├── components/     # React components
│   ├── common/    # Reusable components
│   └── pages/     # Page-specific components
├── hooks/         # Custom hooks
├── services/      # API calls
├── utils/         # Utility functions
├── types/         # TypeScript types
└── __tests__/     # Test files
```

## Troubleshooting

### Common Issues
```bash
# Clear cache issues
rm -rf node_modules package-lock.json
npm install

# Port conflicts  
lsof -ti:3000 | xargs kill -9

# Git issues
git reset --hard HEAD
git clean -fd

# Docker issues
docker-compose down
docker system prune -f
```

### Debug Commands
```bash
# Node.js debugging
node --inspect-brk=0.0.0.0:9229 app.js

# Network debugging
netstat -tulpn | grep :3000

# Process debugging  
ps aux | grep node
htop
```

## Tool Updates y Maintenance

### Regular Maintenance
```bash
# Weekly tasks
npm audit fix
npm update
brew upgrade (macOS)
docker system prune

# Monthly tasks  
npm outdated
yarn upgrade-interactive
```

### Version Pinning Strategy
- **Major versions:** Pinned (manual updates)
- **Minor versions:** Caret (^X.Y.Z)
- **Patch versions:** Auto-update
- **Security patches:** Immediate update

## ADRs Relacionados

- [ADR-XXX: IDE and Editor Standardization](../../adr/ADR-XXX.md)
- [ADR-XXX: Testing Strategy and Tools](../../adr/ADR-XXX.md)  
- [ADR-XXX: Code Quality Tools Selection](../../adr/ADR-XXX.md)

---
*Template especializado para Development Tools - stepwise-planner*