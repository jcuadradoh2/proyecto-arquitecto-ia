# D-19 · OpenTelemetry + Managed Prometheus / Grafana + CloudWatch / X-Ray

**Estado:** Propuesta (v1.0, 2026-09-25)  
**Sección del documento:** 14

## Contexto
Decisión tomada en el diseño de la arquitectura del Sistema de Banca por Internet de BP (modelo C4). El detalle completo, con el análisis de opciones y las consecuencias, se encuentra en la sección 14 del documento `Arquitectura_Banca_Internet_BP_C4.pdf`.

## Opciones evaluadas
- Datadog / New Relic
- ELK autogestionado

## Decisión
OpenTelemetry + Managed Prometheus / Grafana + CloudWatch / X-Ray.

## Justificaciones
1. Estándar abierto sin bloqueo.
2. Integración nativa y costo.
3. Residencia de datos y control de PII.

## Consecuencias
Ver la sección 14 del documento principal (riesgos asociados en la sección 17).
