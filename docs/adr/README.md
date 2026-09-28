# Registro de decisiones de arquitectura (ADR)

| ID | Decisión | Sección del documento |
|---|---|---|
| D-01 | Microservicios en contenedores con orientación a eventos | 3 |
| D-02 | Dos sistemas de notificación: SNS/SES + Twilio/WhatsApp | 4 |
| D-03 | REST en el borde, gRPC interno, eventos por Kafka | 5.2 |
| D-04 | Amazon API Gateway con JWT Authorizer para canales | 5.2 |
| D-05 | Patrón BFF por canal | 5.2 |
| D-06 | Saga orquestada + Outbox + Idempotent Receiver | 6.1 |
| D-07 | Angular para la SPA | 7 |
| D-08 | Flutter para la app móvil | 7 |
| D-09 | Authorization Code + PKCE (FAPI 2.0, PAR, DPoP); SPA vía BFF; móvil con AppAuth | 8 |
| D-10 | Auditoría por eventos, cuenta separada, cadena de hashes firmada y WORM | 6.4 |
| D-11 | Vista materializada por eventos para clientes frecuentes (DynamoDB + Redis) | 6.5 |
| D-12 | Rekognition Face Liveness + CompareFaces + Textract tras adaptador; Facephi / Incode como alternativas | 9 |
| D-13 | Kong + conectores ACL para integración | 10 |
| D-14 | Aurora PostgreSQL + DynamoDB + ElastiCache Redis | 10 |
| D-15 | Amazon MSK (Kafka) + Debezium, con SQS/SNS complementarios | 10 |
| D-16 | AWS como nube pública | 12 |
| D-17 | EKS + Graviton + Karpenter + Istio | 12 |
| D-18 | DR multi-región warm standby (RTO ≤ 30 min, RPO ≤ 1 min) | 12 |
| D-19 | OpenTelemetry + Managed Prometheus / Grafana + CloudWatch / X-Ray | 14 |
| D-20 | Servicios gestionados + compromisos de largo plazo | 15 |
