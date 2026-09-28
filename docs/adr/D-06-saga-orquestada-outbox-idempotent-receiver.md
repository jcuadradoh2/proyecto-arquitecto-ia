# D-06 · Saga orquestada + Outbox + Idempotent Receiver

**Estado:** Propuesta (v1.0, 2026-09-25)  
**Sección del documento:** 6.1

## Contexto
Decisión tomada en el diseño de la arquitectura del Sistema de Banca por Internet de BP (modelo C4). El detalle completo, con el análisis de opciones y las consecuencias, se encuentra en la sección 6.1 del documento `Arquitectura_Banca_Internet_BP_C4.pdf`.

## Opciones evaluadas
- 2PC / XA
- saga coreografiada

## Decisión
Saga orquestada + Outbox + Idempotent Receiver.

## Justificaciones
1. 2PC inviable con legado y red.
2. Visibilidad del estado.
3. Publicación confiable y sin duplicados.

## Consecuencias
Ver la sección 6.1 del documento principal (riesgos asociados en la sección 17).
