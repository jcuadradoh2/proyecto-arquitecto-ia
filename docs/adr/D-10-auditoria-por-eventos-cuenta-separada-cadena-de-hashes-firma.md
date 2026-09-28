# D-10 · Auditoría por eventos, cuenta separada, cadena de hashes firmada y WORM

**Estado:** Propuesta (v1.0, 2026-09-25)  
**Sección del documento:** 6.4

## Contexto
Decisión tomada en el diseño de la arquitectura del Sistema de Banca por Internet de BP (modelo C4). El detalle completo, con el análisis de opciones y las consecuencias, se encuentra en la sección 6.4 del documento `Arquitectura_Banca_Internet_BP_C4.pdf`.

## Opciones evaluadas
- Triggers en BD
- logs de aplicación
- QLDB / blockchain

## Decisión
Auditoría por eventos, cuenta separada, cadena de hashes firmada y WORM.

## Justificaciones
1. Completitud y atomicidad (interceptor + outbox + logs de gateway).
2. Integridad verificable y segregación de funciones.
3. Sin impacto en latencia.

## Consecuencias
Ver la sección 6.4 del documento principal (riesgos asociados en la sección 17).
