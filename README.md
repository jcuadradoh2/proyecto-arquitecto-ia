# Arquitectura de Solución – Sistema de Banca por Internet BP (Modelo C4)

Ejercicio práctico de arquitectura de soluciones: diseño de la plataforma de banca por internet
de la entidad financiera **BP** (canal web y canal móvil), documentado con el **modelo C4**
(contexto, contenedores y componentes), complementado con diagramas de secuencia, un diagrama de
despliegue en **AWS** y un registro de decisiones de arquitectura (ADR) en el que cada decisión
incluye las opciones evaluadas y al menos dos justificaciones teóricas.

## 📄 Entregable principal

**[Arquitectura_Banca_Internet_BP_C4.pdf](./Arquitectura_Banca_Internet_BP_C4.pdf)** – documento completo (59 páginas):

1. Resumen ejecutivo
2. Alcance, supuestos y requerimientos (funcionales y no funcionales)
3. Principios y estilo de arquitectura
4. Vista de contexto (C4 – Nivel 1)
5. Vista de contenedores (C4 – Nivel 2), con vistas de detalle síncrona y asíncrona
6. Vista de componentes (C4 – Nivel 3): transferencias e integración, autenticación, onboarding, auditoría y clientes frecuentes
7. Front-end: Web SPA (Angular) y App Móvil (Flutter) – opciones evaluadas
8. Autenticación y autorización con OAuth 2.0 / OIDC (Authorization Code + PKCE, FAPI 2.0, PAR, DPoP, BFF)
9. Onboarding digital con reconocimiento facial (Amazon Rekognition / Textract y alternativas)
10. Acceso a datos e integración con el Core, el CRM y la red interbancaria
11. Notificación de movimientos por dos sistemas
12. Infraestructura en AWS: alta disponibilidad, DR, latencia y auto-healing
13. Seguridad y cumplimiento normativo
14. Monitoreo, observabilidad y excelencia operativa
15. Gestión de costos (FinOps)
16. Registro de decisiones de arquitectura (D-01 a D-20)
17. Riesgos y hoja de ruta · 18. Conclusiones · Anexos (glosario, referencias, inventario de diagramas)

> Los diagramas están incluidos en el PDF en alta resolución (use el zoom del visor) y también
> se entregan por separado en `docs/diagramas/` en formato PNG y SVG.

## 🗂️ Estructura del repositorio

```
.
├── README.md
├── Arquitectura_Banca_Internet_BP_C4.pdf     # Documento completo
└── docs/
    ├── diagramas/                            # Diagramas como código (PlantUML + C4) y renders
    │   ├── 01_contexto.puml            (.png / .svg)
    │   ├── 02_contenedores.puml
    │   ├── 03_contenedores_sincrono.puml
    │   ├── 04_contenedores_asincrono.puml
    │   ├── 05_componentes_transferencias.puml
    │   ├── 06_componentes_autenticacion.puml
    │   ├── 06b_componentes_onboarding.puml
    │   ├── 07_componentes_auditoria.puml
    │   ├── 08_componentes_clientes_frecuentes.puml
    │   ├── 09_secuencia_login_movil.puml
    │   ├── 10_secuencia_login_spa.puml
    │   ├── 11_secuencia_onboarding.puml
    │   ├── 12_secuencia_transferencia.puml
    │   ├── 13_despliegue_aws.puml
    │   ├── 14_observabilidad.puml
    │   └── _seq_style.iuml                   # Estilo compartido de los diagramas de secuencia
    └── adr/                                  # Un archivo por decisión de arquitectura (D-01 … D-20)
```

## 🖼️ Diagramas C4

| Nivel | Diagrama | Archivo |
|---|---|---|
| Contexto (N1) | Sistema de Banca por Internet BP y su entorno | [PNG](docs/diagramas/01_contexto.png) · [SVG](docs/diagramas/01_contexto.svg) |
| Contenedores (N2) | Vista general | [PNG](docs/diagramas/02_contenedores.png) · [SVG](docs/diagramas/02_contenedores.svg) |
| Contenedores (N2) | Detalle A: flujo síncrono | [PNG](docs/diagramas/03_contenedores_sincrono.png) · [SVG](docs/diagramas/03_contenedores_sincrono.svg) |
| Contenedores (N2) | Detalle B: flujo asíncrono | [PNG](docs/diagramas/04_contenedores_asincrono.png) · [SVG](docs/diagramas/04_contenedores_asincrono.svg) |
| Componentes (N3) | Transferencias y Pagos + capa de integración | [PNG](docs/diagramas/05_componentes_transferencias.png) · [SVG](docs/diagramas/05_componentes_transferencias.svg) |
| Componentes (N3) | Autenticación y autorización | [PNG](docs/diagramas/06_componentes_autenticacion.png) · [SVG](docs/diagramas/06_componentes_autenticacion.svg) |
| Componentes (N3) | Onboarding facial | [PNG](docs/diagramas/06b_componentes_onboarding.png) · [SVG](docs/diagramas/06b_componentes_onboarding.svg) |
| Componentes (N3) | Auditoría | [PNG](docs/diagramas/07_componentes_auditoria.png) · [SVG](docs/diagramas/07_componentes_auditoria.svg) |
| Componentes (N3) | Clientes frecuentes | [PNG](docs/diagramas/08_componentes_clientes_frecuentes.png) · [SVG](docs/diagramas/08_componentes_clientes_frecuentes.svg) |
| Secuencia | Login móvil / Login SPA vía BFF / Onboarding / Transferencia | [09](docs/diagramas/09_secuencia_login_movil.png) · [10](docs/diagramas/10_secuencia_login_spa.png) · [11](docs/diagramas/11_secuencia_onboarding.png) · [12](docs/diagramas/12_secuencia_transferencia.png) |
| Despliegue | Infraestructura AWS (Multi-AZ + DR) | [PNG](docs/diagramas/13_despliegue_aws.png) · [SVG](docs/diagramas/13_despliegue_aws.svg) |
| Operación | Monitoreo, observabilidad y auto-healing | [PNG](docs/diagramas/14_observabilidad.png) · [SVG](docs/diagramas/14_observabilidad.svg) |

### Contexto (C4 – Nivel 1)
![Contexto](docs/diagramas/01_contexto.png)

### Contenedores (C4 – Nivel 2)
![Contenedores](docs/diagramas/02_contenedores.png)

### Despliegue en AWS
![Despliegue AWS](docs/diagramas/13_despliegue_aws.png)

## 🧾 Decisiones de arquitectura (ADR)

- [D-01](docs/adr/D-01-microservicios-en-contenedores-con-orientacion-a-eventos.md) Microservicios en contenedores con orientacion a eventos
- [D-02](docs/adr/D-02-dos-sistemas-de-notificacion-sns-ses-twilio-whatsapp.md) Dos sistemas de notificacion sns ses twilio whatsapp
- [D-03](docs/adr/D-03-rest-en-el-borde-grpc-interno-eventos-por-kafka.md) Rest en el borde grpc interno eventos por kafka
- [D-04](docs/adr/D-04-amazon-api-gateway-con-jwt-authorizer-para-canales.md) Amazon api gateway con jwt authorizer para canales
- [D-05](docs/adr/D-05-patron-bff-por-canal.md) Patron bff por canal
- [D-06](docs/adr/D-06-saga-orquestada-outbox-idempotent-receiver.md) Saga orquestada outbox idempotent receiver
- [D-07](docs/adr/D-07-angular-para-la-spa.md) Angular para la spa
- [D-08](docs/adr/D-08-flutter-para-la-app-movil.md) Flutter para la app movil
- [D-09](docs/adr/D-09-authorization-code-pkce-fapi-2-0-par-dpop-spa-via-bff-movil-.md) Authorization code pkce fapi 2 0 par dpop spa via bff movil 
- [D-10](docs/adr/D-10-auditoria-por-eventos-cuenta-separada-cadena-de-hashes-firma.md) Auditoria por eventos cuenta separada cadena de hashes firma
- [D-11](docs/adr/D-11-vista-materializada-por-eventos-para-clientes-frecuentes-dyn.md) Vista materializada por eventos para clientes frecuentes dyn
- [D-12](docs/adr/D-12-rekognition-face-liveness-comparefaces-textract-tras-adaptad.md) Rekognition face liveness comparefaces textract tras adaptad
- [D-13](docs/adr/D-13-kong-conectores-acl-para-integracion.md) Kong conectores acl para integracion
- [D-14](docs/adr/D-14-aurora-postgresql-dynamodb-elasticache-redis.md) Aurora postgresql dynamodb elasticache redis
- [D-15](docs/adr/D-15-amazon-msk-kafka-debezium-con-sqs-sns-complementarios.md) Amazon msk kafka debezium con sqs sns complementarios
- [D-16](docs/adr/D-16-aws-como-nube-publica.md) Aws como nube publica
- [D-17](docs/adr/D-17-eks-graviton-karpenter-istio.md) Eks graviton karpenter istio
- [D-18](docs/adr/D-18-dr-multi-region-warm-standby-rto-30-min-rpo-1-min.md) Dr multi region warm standby rto 30 min rpo 1 min
- [D-19](docs/adr/D-19-opentelemetry-managed-prometheus-grafana-cloudwatch-x-ray.md) Opentelemetry managed prometheus grafana cloudwatch x ray
- [D-20](docs/adr/D-20-servicios-gestionados-compromisos-de-largo-plazo.md) Servicios gestionados compromisos de largo plazo

Índice completo con la sección del documento en [docs/adr/README.md](docs/adr/README.md).

## 🔧 Regenerar los diagramas

Requisitos: Java 17+ y Graphviz. Los diagramas usan la librería estándar de PlantUML
(`<C4/…>` y `<awslib/…>`), por lo que no necesitan dependencias adicionales.

```bash
# Descargar PlantUML (una sola vez)
curl -L -o plantuml.jar https://github.com/plantuml/plantuml/releases/latest/download/plantuml.jar

# Renderizar todos los diagramas a PNG y SVG
java -DPLANTUML_LIMIT_SIZE=16384 -jar plantuml.jar -tpng docs/diagramas/*.puml
java -DPLANTUML_LIMIT_SIZE=16384 -jar plantuml.jar -tsvg docs/diagramas/*.puml
```

## 🧭 Resumen de la arquitectura

- **Nube:** AWS (us-east-1 primaria, us-east-2 DR warm standby; RTO ≤ 30 min, RPO ≤ 1 min), Multi-AZ activo-activo,
  conectividad privada con el data center de BP (Direct Connect + VPN).
- **Estilo:** microservicios en Amazon EKS (Istio, Karpenter, Graviton) orientados a eventos (Amazon MSK / Kafka),
  BFF por canal, API Gateway de canales (Amazon API Gateway) y API Gateway de integración (Kong) con conectores ACL.
- **Patrones:** Saga, Transactional Outbox, Idempotent Receiver, Circuit Breaker, Bulkhead, BFF, API Composition,
  CQRS / Materialized View, Cache-Aside, Decorator, Strategy, Observer, Chain of Responsibility, Anti-Corruption Layer, Token Handler.
- **Front-end:** Web SPA en Angular; App Móvil multiplataforma en Flutter (alternativas evaluadas: React / Vue; React Native / nativo / KMP).
- **Autenticación:** OAuth 2.0 / OIDC sobre el IdP existente con Authorization Code + PKCE (FAPI 2.0, PAR, DPoP),
  MFA con passkeys FIDO2, step-up para transacciones; SPA vía BFF (sin tokens en el navegador), móvil con AppAuth.
- **Onboarding:** Amazon Textract + Amazon Rekognition Face Liveness / CompareFaces tras un adaptador intercambiable
  (Facephi / Incode como alternativas), Registro Civil, listas AML/PEP, alta en Core / CRM y enrolamiento SCIM + FIDO2.
- **Auditoría:** eventos por outbox → Kafka → servicio en cuenta AWS separada, cadena de hashes firmada (KMS),
  Aurora append-only, S3 Object Lock (WORM) y OpenSearch.
- **Notificaciones:** Amazon SNS / SES + Twilio / WhatsApp Business (dos sistemas, con contingencia y evidencia de entrega).
- **Seguridad y cumplimiento:** Zero Trust, LOPDP (Ecuador), normativa de la Superintendencia de Bancos, AML, PCI DSS 4.0,
  ISO 27001, NIST CSF 2.0 / SP 800-63B, OWASP ASVS / MASVS, FAPI 2.0.
- **Operación:** OpenTelemetry + Managed Prometheus / Grafana + CloudWatch / X-Ray, SLOs y error budgets,
  auto-healing, runbooks automatizados, ingeniería de caos, IaC (Terraform) y GitOps; FinOps (≈ USD 14–16 k/mes).

## 📝 Notas

- Jurisdicción de referencia: Ecuador (el diseño indica equivalentes regionales e internacionales).
- Los nombres de productos y proveedores se usan solo con fines de diseño; no implican relación comercial.
- Versión 1.0 · 25 de septiembre de 2026.
