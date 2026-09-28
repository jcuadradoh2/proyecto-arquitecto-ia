# D-03 · REST en el borde, gRPC interno, eventos por Kafka

**Estado:** Propuesta (v1.0, 2026-09-25)  
**Sección del documento:** 5.2

## Contexto
Decisión tomada en el diseño de la arquitectura del Sistema de Banca por Internet de BP (modelo C4). El detalle completo, con el análisis de opciones y las consecuencias, se encuentra en la sección 5.2 del documento `Arquitectura_Banca_Internet_BP_C4.pdf`.

## Opciones evaluadas
- REST en todo
- gRPC + REST
- todo asíncrono

## Decisión
REST en el borde, gRPC interno, eventos por Kafka.

## Justificaciones
1. Eficiencia y contratos tipados.
2. Desacople temporal para auditoría / notificaciones.
3. Simplicidad para consultas síncronas.

## Consecuencias
Ver la sección 5.2 del documento principal (riesgos asociados en la sección 17).
