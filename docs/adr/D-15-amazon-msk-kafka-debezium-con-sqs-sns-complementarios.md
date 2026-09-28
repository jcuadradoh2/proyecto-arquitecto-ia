# D-15 · Amazon MSK (Kafka) + Debezium, con SQS/SNS complementarios

**Estado:** Propuesta (v1.0, 2026-09-25)  
**Sección del documento:** 10

## Contexto
Decisión tomada en el diseño de la arquitectura del Sistema de Banca por Internet de BP (modelo C4). El detalle completo, con el análisis de opciones y las consecuencias, se encuentra en la sección 10 del documento `Arquitectura_Banca_Internet_BP_C4.pdf`.

## Opciones evaluadas
- EventBridge
- solo SQS/SNS

## Decisión
Amazon MSK (Kafka) + Debezium, con SQS/SNS complementarios.

## Justificaciones
1. Durabilidad, orden y replay para auditoría.
2. Ecosistema CDC / outbox y Kafka Streams.
3. SQS para colas simples.

## Consecuencias
Ver la sección 10 del documento principal (riesgos asociados en la sección 17).
