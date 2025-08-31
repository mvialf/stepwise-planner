# Infrastructure Stack: [Nombre del Proyecto]

**Última actualización:** YYYY-MM-DD  
**Responsable:** [Nombre del DevOps Lead]

## Resumen de Infraestructura

[Descripción de la estrategia de infraestructura, despliegue y operaciones]

## Cloud Strategy

### Proveedor Principal
| Servicio | Proveedor | Propósito | Estado |
|----------|-----------|-----------|---------|
| [AWS/GCP/Azure] | [Provider] | Cloud principal | ✅ |
| [Multi-cloud/Hybrid] | [Strategy] | Estrategia | 🔄 |

### Servicios Core
| Servicio | Tecnología | Propósito | Costo Est. |
|----------|------------|-----------|------------|
| Compute | [EC2/GCE/VM] | Aplicaciones | $XXX/mes |
| Database | [RDS/Cloud SQL] | Base de datos | $XXX/mes |
| Storage | [S3/Cloud Storage] | Archivos estáticos | $XXX/mes |
| CDN | [CloudFront/Cloud CDN] | Distribución global | $XXX/mes |
| Load Balancer | [ALB/Cloud LB] | Balanceeo de carga | $XXX/mes |

## Containerización

### Container Strategy
```dockerfile
# Dockerfile ejemplo
FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN npm ci --only=production
COPY . .
EXPOSE 3000
CMD ["npm", "start"]
```

### Orchestration
| Tecnología | Versión | Propósito | Estado |
|------------|---------|-----------|---------|
| [Docker] | vX.X | Containerización | ✅ |
| [Kubernetes/Docker Swarm] | vX.X | Orquestación | ✅ |
| [Helm] | vX.X | Package manager | 🔄 |

### Registry
- **Container registry:** [Docker Hub/ECR/GCR]
- **Image scanning:** [Habilitado/Herramienta]
- **Image lifecycle:** [Retention policy]

## CI/CD Pipeline

### Pipeline Architecture
```yaml
# Pipeline stages
stages:
  - lint_and_test
  - build_images
  - security_scan
  - deploy_staging
  - integration_tests
  - deploy_production
```

### Herramientas
| Tecnología | Versión | Propósito |
|------------|---------|-----------|
| [GitHub Actions/GitLab CI] | - | CI/CD principal |
| [Jenkins/CircleCI] | vX.X | CI/CD alternativo |
| [ArgoCD/Flux] | vX.X | GitOps |

### Deployment Strategy
- **Estrategia:** [Blue-Green/Rolling/Canary]
- **Rollback time:** < 5 minutos
- **Zero-downtime:** [Sí/No]
- **Feature flags:** [LaunchDarkly/Custom]

## Infrastructure as Code

### IaC Tools
```hcl
# Terraform ejemplo
resource "aws_instance" "web" {
  ami           = "ami-0c55b159cbfafe1d0"
  instance_type = "t3.micro"
  
  tags = {
    Name = "WebServer"
    Environment = var.environment
  }
}
```

### Stack Management
| Tecnología | Versión | Propósito |
|------------|---------|-----------|
| [Terraform/Pulumi] | vX.X | IaC principal |
| [CloudFormation/ARM] | - | IaC nativo |
| [Ansible] | vX.X | Configuration mgmt |

### Version Control
- **Repository:** [Mono-repo/Separate repos]
- **State management:** [Remote backend]
- **Secrets:** [Vault/Cloud secrets]

## Networking

### Network Architecture
```
Internet → CDN → Load Balancer → App Servers
                    ↓
                Database Subnet (Private)
                    ↓
                Cache Subnet (Private)
```

### Security Groups/Firewall
```yaml
# Reglas de red principales
web_tier:
  - port 80/443 from internet
  - port 3000 from load balancer

app_tier:
  - port 3000 from web_tier
  - port 5432 to database_tier

database_tier:
  - port 5432 from app_tier only
```

### DNS y SSL
- **DNS provider:** [Route53/CloudFlare]
- **SSL certificates:** [Let's Encrypt/ACM]
- **Certificate management:** [Auto-renewal]

## Monitoring y Observability

### Monitoring Stack
| Tecnología | Versión | Propósito |
|------------|---------|-----------|
| [Prometheus] | vX.X | Metrics collection |
| [Grafana] | vX.X | Dashboards |
| [ELK/EFK Stack] | vX.X | Logging |
| [Jaeger/Zipkin] | vX.X | Distributed tracing |

### Key Metrics
```yaml
# SLIs principales
availability: 99.9%
response_time_p95: < 500ms
error_rate: < 1%
throughput: > 1000 req/sec
```

### Alerting
- **Alert manager:** [PagerDuty/OpsGenie]
- **Escalation:** [On-call schedule]
- **Notification channels:** [Slack/Email/SMS]

## Security

### Security Measures
- [ ] **Network segmentation:** VPC/Subnets configurados
- [ ] **WAF:** Web Application Firewall activo
- [ ] **DDoS protection:** [CloudFlare/AWS Shield]
- [ ] **Intrusion detection:** [IDS/IPS configurado]
- [ ] **Vulnerability scanning:** [Automated scanning]
- [ ] **Secrets rotation:** [Automated rotation]

### Compliance
- **Standards:** [SOC2/ISO27001/PCI-DSS]
- **Auditing:** [CloudTrail/Audit logs]
- **Data encryption:** [At rest and in transit]
- **Backup encryption:** [Encrypted backups]

## Disaster Recovery

### DR Strategy
```yaml
# RTO/RPO targets
RTO: 4 hours      # Recovery Time Objective
RPO: 1 hour       # Recovery Point Objective
```

### Backup Strategy
- **Application data:** [Daily automated]
- **Database:** [Continuous WAL + daily full]
- **Infrastructure:** [IaC templates in git]
- **Secrets:** [Encrypted backup]

### DR Testing
```bash
# DR testing schedule
Monthly: Backup restoration test
Quarterly: Full DR drill
Annually: Multi-region failover test
```

## Cost Optimization

### Cost Monitoring
| Servicio | Costo Actual | Costo Target | Optimización |
|----------|--------------|--------------|--------------|
| Compute | $XXX/mes | $XXX/mes | Right-sizing |
| Storage | $XXX/mes | $XXX/mes | Lifecycle policies |
| Network | $XXX/mes | $XXX/mes | CDN optimization |

### Optimization Strategies
- [ ] **Reserved instances:** [Para cargas predecibles]
- [ ] **Spot instances:** [Para cargas no críticas]
- [ ] **Auto-scaling:** [Horizontal/Vertical]
- [ ] **Storage tiering:** [Hot/Warm/Cold storage]
- [ ] **CDN optimization:** [Cache policies]

## Environments

### Development
```yaml
# Configuración desarrollo
instances: 1x small
database: shared development DB
monitoring: basic
backup: none
ssl: self-signed
```

### Staging
```yaml
# Configuración staging  
instances: 2x medium
database: dedicated staging DB
monitoring: full metrics
backup: daily
ssl: valid certificate
```

### Production
```yaml
# Configuración producción
instances: 3+ large (auto-scaling)
database: HA cluster
monitoring: full observability
backup: continuous + daily
ssl: enterprise certificate
```

## Scaling Strategy

### Horizontal Scaling
```yaml
# Auto-scaling configuration
min_instances: 2
max_instances: 20
scale_up_threshold: 70% CPU
scale_down_threshold: 30% CPU
```

### Database Scaling
- **Read replicas:** [Automated deployment]
- **Connection pooling:** [PgBouncer/Connection pools]
- **Caching layer:** [Redis cluster]
- **CDN caching:** [Static + dynamic content]

## Performance Tuning

### Application Level
- **Connection pooling:** [Optimized pool sizes]
- **Caching:** [Multi-level caching strategy]
- **Asset optimization:** [Compression, minification]
- **Database queries:** [Query optimization]

### Infrastructure Level
- **Instance sizing:** [CPU/Memory optimization]
- **Network optimization:** [Placement groups]
- **Storage optimization:** [SSD/NVMe selection]
- **CDN configuration:** [Global distribution]

## Troubleshooting

### Common Issues Playbook
```bash
# High CPU
kubectl top nodes
kubectl top pods

# Memory issues
free -h
docker stats

# Network issues
netstat -tulpn
ss -tulpn

# Disk space
df -h
du -sh /*
```

### Emergency Procedures
- **Service outage:** [Step-by-step recovery]
- **Data corruption:** [Recovery procedures]
- **Security incident:** [Incident response]
- **Performance degradation:** [Investigation steps]

## Tools y Scripts

### Automation Scripts
```bash
#!/bin/bash
# Deploy script ejemplo
./scripts/deploy.sh staging
./scripts/health-check.sh
./scripts/rollback.sh # if needed
```

### Useful Commands
```bash
# Kubernetes
kubectl get pods -A
kubectl describe pod <pod-name>
kubectl logs -f <pod-name>

# Docker
docker ps
docker logs <container-id>
docker exec -it <container-id> /bin/bash
```

## Documentation Links

### Runbooks
- [Service Deployment Guide](./runbooks/deployment.md)
- [Incident Response Guide](./runbooks/incidents.md)  
- [Backup/Recovery Guide](./runbooks/backup-recovery.md)
- [Security Incident Response](./runbooks/security.md)

### Architecture Diagrams
- [Network Architecture](./diagrams/network.md)
- [Deployment Pipeline](./diagrams/ci-cd.md)
- [Monitoring Architecture](./diagrams/monitoring.md)

## ADRs Relacionados

- [ADR-XXX: Cloud Provider Selection](../../adr/ADR-XXX.md)
- [ADR-XXX: Container Orchestration Strategy](../../adr/ADR-XXX.md)
- [ADR-XXX: CI/CD Pipeline Architecture](../../adr/ADR-XXX.md)

---
*Template especializado para Infrastructure - stepwise-planner*